# Công nghệ và kiến trúc

Trang này mô tả công nghệ của Shoukaku ở mức tổng quan công khai. Tài liệu cố ý không công bố thông tin xác thực, endpoint riêng tư, chi tiết truy cập mạng nội bộ, bí mật production hoặc quy trình vận hành được bảo vệ.

## Ứng dụng cốt lõi

| Công nghệ | Vai trò trong Shoukaku |
|---|---|
| TypeScript | Ngôn ngữ ứng dụng chính và bề mặt phát triển an toàn kiểu |
| Node.js 22 | Runtime JavaScript cho backend bot |
| Discord.js v14 | Gateway Discord, interaction, lệnh, quyền và tích hợp thoại |
| PostgreSQL | Lưu trữ lâu dài cho tính năng, kiểm duyệt và dữ liệu âm nhạc người dùng |
| Redis | Cache dùng chung, cooldown, trạng thái tạm thời, ánh xạ phương tiện và phối hợp đa tiến trình |
| Knex | Công cụ migration và truy vấn cơ sở dữ liệu |

## Đăng ký lệnh

Lệnh được nạp qua manifest danh mục và module export rõ ràng. Quy trình triển khai Discord thực hiện ghi đè toàn bộ danh sách lệnh ứng dụng.

Danh mục công khai đầy đủ nằm trong [COMMANDS.md](COMMANDS.md):

- lệnh hoạt động được export bởi registry hiện tại;
- lệnh bị giới hạn được đăng ký nhưng kiểm soát truy cập;
- lệnh bị vô hiệu hóa có thể còn trong mã hoặc kiểm thử nhưng không được registry chính thức export.

Thay đổi mã nguồn không xóa lệnh Discord đã triển khai trước đó cho đến khi registry hiện tại được triển khai thành công.

## Âm nhạc

| Công nghệ | Vai trò trong Shoukaku |
|---|---|
| Lavalink | Phát âm thanh và xử lý nguồn được phê duyệt |
| Shoukaku / lavalink-client | Kết nối Lavalink và quản lý player phía ứng dụng |
| PostgreSQL | Tùy chọn người dùng, mục yêu thích và lịch sử nghe |
| Redis | Hàng đợi hoạt động, phiên, cache và phối hợp shard |

Bề mặt `/music` hiện tại gồm phát nhạc, chỉnh sửa hàng đợi, tua, tùy chọn dùng cho hệ thống phát, mục yêu thích trong mô hình dữ liệu backend, lịch sử và autoplay.

Tính sẵn sàng phụ thuộc node và nguồn được cấu hình. Dịch vụ chính thức không được cố ý dùng thông tin xác thực do người dùng cung cấp hoặc biện pháp kỹ thuật để vượt giới hạn riêng tư, trả phí, thuê bao, độ tuổi, khu vực hoặc DRM. Backend có thể dùng thông tin xác thực API hoặc dịch vụ do Người vận hành kiểm soát cho tích hợp được phê duyệt khi được phép.

## Xử lý phương tiện

| Công nghệ | Vai trò trong Shoukaku |
|---|---|
| Cobalt | Thành phần nội bộ để lấy và xử lý phương tiện |
| yt-dlp | Thành phần trích xuất theo nhà cung cấp chỉ dùng trong quy trình được phê duyệt |
| Dịch vụ proxy phương tiện | Chuẩn bị và phân phối preview phương tiện công khai tạm thời có kiểm soát |
| Redis media store | Định danh phương tiện ổn định và ánh xạ nguồn YouTube ngắn hạn |
| Cloudflare R2 | Phân phối đối tượng công khai tạm thời cho preview được tạo, khi bật |

Bản triển khai chính thức bật `/download` qua `DOWNLOAD_COMMAND_ENABLED`. `/download` chỉ dành cho phương tiện công khai được hỗ trợ mà người dùng sở hữu, được phép sử dụng hoặc được pháp luật áp dụng cho phép sử dụng. Quy trình `/media` hỗ trợ sửa embed mạng xã hội được chọn, URL ảnh hoặc GIF công khai trực tiếp và preview phương tiện công khai được hỗ trợ. Người dùng không được gửi thông tin xác thực tài khoản, liên kết riêng tư, nội dung trả phí, bị giới hạn hoặc được bảo vệ bằng DRM.

Một số máy chủ ảnh bên thứ ba có thể chứa nội dung trưởng thành. Dịch vụ chính thức không đăng ký lệnh chuyên biệt về nội dung người lớn, nhưng quản trị viên và người dùng vẫn chịu trách nhiệm về kênh phù hợp và quy định Discord.

### Thời gian tồn tại phương tiện hiện tại

| Dữ liệu phương tiện | Mặc định hoặc giới hạn hiện tại |
|---|---|
| Tệp nguồn tải xuống dùng trong xử lý | Tuổi tối đa 1.800 giây theo mặc định |
| Đối tượng preview R2 công khai tạm thời, khi bật | Mục tiêu lưu 86.400 giây |
| Ánh xạ phương tiện YouTube ổn định trong Redis | TTL có thể gia hạn 604.800 giây theo mặc định |
| Tuổi tuyệt đối của ánh xạ Redis | Giới hạn 2.592.000 giây từ khi tạo theo mặc định |
| Cache URL upstream trực tiếp | 300 giây theo mặc định |
| Ủy quyền URL phương tiện đã ký | Tối đa 86.400 giây |

Khoảng bảy đến 30 ngày của Redis áp dụng cho metadata ánh xạ như URL nguồn chuẩn hóa, ID video và định dạng, metadata representation, timestamp và giá trị kiểm tra toàn vẹn. Nó không có nghĩa tệp nguồn tải xuống được giữ 30 ngày.

Người vận hành có thể thay đổi cấu hình, nhưng Chính sách Quyền riêng tư công khai phải được cập nhật khi thay đổi ảnh hưởng đáng kể đến thời gian lưu dữ liệu người dùng.

## Tích hợp bên ngoài

Shoukaku có thể tích hợp với dịch vụ dùng cho:

- thông tin anime;
- nội dung Reddit;
- nội dung Pixiv;
- thông tin Steam;
- tìm kiếm Wikipedia;
- đề xuất hỗ trợ bởi Spotify khi được cấu hình;
- nguồn âm nhạc, phương tiện, hình ảnh và embed công khai được phê duyệt.

Tích hợp chuyên biệt về nội dung người lớn không được đăng ký trên Dịch vụ chính thức. Mỗi tích hợp được bật chịu sự điều chỉnh của tính sẵn sàng, điều khoản, rate limit, chính sách quyền riêng tư và quy tắc nội dung của bên thứ ba.

## Triển khai và hạ tầng

| Công nghệ | Vai trò trong Shoukaku |
|---|---|
| Docker và Docker Compose | Triển khai ứng dụng và dịch vụ có thể tái tạo |
| Linux / Ubuntu | Môi trường host kiểu production chính |
| Công cụ Cloudflare | Hỗ trợ mạng và tuyến công khai tùy chọn |
| Nginx hoặc thành phần proxy | Định tuyến có kiểm soát cho dịch vụ công khai hoặc nội bộ được chọn |

Kiến trúc production chính xác có thể thay đổi và không được mô tả đầy đủ trong tài liệu công khai này.

## Độ tin cậy, nhật ký và quan sát

| Công nghệ | Vai trò trong Shoukaku |
|---|---|
| Prometheus | Thu thập metrics |
| Grafana | Dashboard vận hành |
| Alertmanager | Định tuyến cảnh báo |
| Sentry | Báo lỗi và chẩn đoán tùy chọn |
| Ghi nhật ký có cấu trúc | Gỡ lỗi, độ tin cậy, bảo mật và điều tra lạm dụng |

Triển khai Docker dùng file log container quay vòng có giới hạn cho dịch vụ cốt lõi. Nhà cung cấp quan sát bên ngoài tùy chọn có thể áp dụng thời gian lưu riêng theo tài khoản. Người dùng công khai không được truy cập dashboard, thông tin xác thực hoặc chẩn đoán chi tiết được bảo vệ.

## Chất lượng phát triển

| Công nghệ | Vai trò trong Shoukaku |
|---|---|
| Jest | Kiểm thử tự động |
| ESLint | Kiểm tra chất lượng mã tĩnh |
| Prettier | Định dạng nhất quán |
| Kiểm tra TypeScript strict | An toàn kiểu và hàng rào kiến trúc |

## Luồng yêu cầu mức cao

```text
Người dùng Discord
    |
    v
Interaction hoặc sự kiện Discord
    |
    v
Lệnh / handler Shoukaku
    |
    +--> PostgreSQL cho cấu hình, kiểm duyệt và dữ liệu âm nhạc lâu dài
    +--> Redis cho trạng thái tạm thời dùng chung và ánh xạ phương tiện
    +--> Lavalink cho nguồn âm nhạc được phê duyệt
    +--> Dịch vụ phương tiện cho xử lý tạm thời được phê duyệt
    +--> API bên thứ ba cho thông tin công khai được yêu cầu
    |
    v
Phản hồi được trả qua Discord
```

## Ranh giới công khai và riêng tư

Cả kho tài liệu và backend đều được công khai để xem. Việc công khai mã nguồn không cho phép công bố dữ liệu production hoặc bí mật và không tự động tạo giấy phép nguồn mở.

Nội dung công khai có thể mô tả:

- danh mục lệnh hướng người dùng và lệnh bị vô hiệu hóa;
- công nghệ mức cao;
- hành vi tính năng chung;
- chính sách quyền riêng tư, điều khoản, sở hữu trí tuệ và bảo mật;
- thông tin hỗ trợ và trạng thái;
- mã triển khai đã có trong kho backend công khai.

Các nội dung sau phải giữ riêng tư:

- token, mật khẩu, API key, cookie và thông tin xác thực;
- cấu hình production riêng tư và endpoint chưa công bố;
- xác thực và chi tiết truy cập dashboard được bảo vệ;
- nội dung cơ sở dữ liệu, bản sao lưu, nhật ký riêng tư và dữ liệu cá nhân;
- ngưỡng chống lạm dụng có thể giúp vượt kiểm soát;
- chi tiết sự cố hoặc lỗ hổng tạo rủi ro đang hoạt động.

## Liên kết kho

- Tài liệu công khai: https://github.com/alG-N/ShoukakuDocs
- Mã backend công khai để xem: https://github.com/alG-N/ShoukakuBot

Việc sử dụng và phân phối lại tuân theo giấy phép hoặc thông báo bản quyền của từng kho.
