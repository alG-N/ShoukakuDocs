# Tài liệu Shoukaku Bot

**Ngôn ngữ:** [EN](../EN/README.md) | **VI**

Shoukaku là bot Discord đa chức năng, tập trung vào âm nhạc, kiểm duyệt, tiện ích và một số tích hợp bên thứ ba được chọn lọc.

> **Kho này là trung tâm tài liệu công khai của Shoukaku.**
> Mã nguồn backend cũng được công khai trong một kho riêng, nhưng thông tin xác thực, cấu hình riêng tư, dữ liệu production, quyền truy cập giám sát được bảo vệ và bí mật nội bộ không bao giờ được công bố.

## Liên kết nhanh

- [Mời Shoukaku](https://discord.com/oauth2/authorize?client_id=1472185156809920615&permissions=8&integration_type=0&scope=bot+applications.commands)
- [Máy chủ hỗ trợ](https://discord.gg/qGwKsqH62k)
- [Trạng thái Dịch vụ](https://altergolden.dev)
- [Danh mục lệnh đầy đủ](COMMANDS.md)
- [Chính sách Quyền riêng tư](PP_VI.md)
- [Điều khoản Dịch vụ](TOS_VI.md)
- [Chính sách Bản quyền và Sở hữu trí tuệ](IP_POLICY.md)
- [Chính sách Bảo mật](SECURITY.md)
- [Câu hỏi thường gặp](FAQ.md)
- [Tài liệu tiếng Anh](../EN/README.md)

## Bối cảnh dự án

Shoukaku là dự án phần mềm cá nhân độc lập được tạo ra để áp dụng kinh nghiệm của Người vận hành về TypeScript, ứng dụng Discord, dịch vụ phân tán, hệ thống kiểm duyệt và hạ tầng phương tiện.

Tên Shoukaku được sử dụng như một tham chiếu lịch sử. Shoukaku không liên kết, được chứng thực hoặc tài trợ bởi Discord, C2 Praparat, Kadokawa, DMM.com, Kantai Collection, bên duy trì các gói phần mềm có tên tương tự hoặc nền tảng bên thứ ba được tích hợp với Dịch vụ.

## Shoukaku có thể làm gì

| Lĩnh vực | Tính năng chính |
|---|---|
| Âm nhạc | Phát nhạc, hàng đợi, tua, tùy chọn, mục yêu thích, lịch sử, autoplay, lặp, trộn và điều khiển kênh thoại |
| Kiểm duyệt | Cảnh cáo, vụ việc, mute, kick, ban, tự động kiểm duyệt, chống raid và bảo vệ máy chủ |
| Tiện ích | AFK, avatar, thông tin vai trò, người dùng, máy chủ, báo cáo và công cụ chung |
| Tích hợp | Anime, Reddit, Pixiv, Steam, Wikipedia, tải xuống và preview phương tiện công khai được hỗ trợ cùng các dịch vụ được phê duyệt khác |
| Giải trí | Lệnh vui và hoạt động cộng đồng |

[Danh mục lệnh đầy đủ](COMMANDS.md) liệt kê các phần triển khai đang hoạt động, bị giới hạn và đã bị vô hiệu hóa. Bản triển khai chính thức bật `/download` qua `DOWNLOAD_COMMAND_ENABLED`. Các lệnh chuyên biệt về nội dung người lớn (`/nhentai` và `/rule34`) cùng `/snipe` vẫn bị vô hiệu hóa.

## Tài liệu

| Tài liệu | Mục đích |
|---|---|
| [Danh mục lệnh đầy đủ](COMMANDS.md) | Danh sách đầy đủ các lệnh đang hoạt động, bị giới hạn và bị vô hiệu hóa |
| [Công nghệ](TECHNOLOGY.md) | Công cụ, dịch vụ, lưu trữ, thời gian lưu và kiến trúc ở mức tổng quan |
| [Câu hỏi thường gặp](FAQ.md) | Hướng dẫn cài đặt, sử dụng, tính sẵn sàng, quyền riêng tư, kho mã và hỗ trợ |
| [Chính sách Quyền riêng tư](PP_VI.md) | Dữ liệu Dịch vụ chính thức xử lý và cách dữ liệu được quản lý |
| [Điều khoản Dịch vụ](TOS_VI.md) | Quy tắc và điều kiện sử dụng Dịch vụ chính thức |
| [Chính sách Bản quyền và Sở hữu trí tuệ](IP_POLICY.md) | Khiếu nại bản quyền, gỡ bỏ, phản hồi và vi phạm lặp lại |
| [Chính sách Bảo mật](SECURITY.md) | Quy trình báo cáo lỗ hổng riêng tư |
| [Đóng góp](CONTRIBUTING.md) | Quy tắc đóng góp tài liệu |
| [Giấy phép](LICENSE) | Tình trạng bản quyền và quyền sử dụng kho này |

Bản tiếng Anh và tiếng Việt của tài liệu pháp lý được xây dựng để thể hiện cùng quy tắc. Nếu khác biệt hoặc điểm không rõ ảnh hưởng đến người dùng tại Việt Nam, cách giải thích bắt buộc theo pháp luật và quyền bảo vệ bắt buộc của người tiêu dùng hoặc chủ thể dữ liệu được ưu tiên.

## Quan hệ giữa các kho

Shoukaku được chia thành hai kho công khai với mục đích khác nhau:

| Kho | Mục đích |
|---|---|
| [`alG-N/ShoukakuDocs`](https://github.com/alG-N/ShoukakuDocs) | Tài liệu công khai cùng Chính sách Quyền riêng tư và Điều khoản Dịch vụ chính thức |
| [`alG-N/ShoukakuBot`](https://github.com/alG-N/ShoukakuBot) | Backend, kiểm thử, tài nguyên triển khai và tài liệu dành cho bên duy trì |

Việc công khai mã nguồn không tự động cấp giấy phép nguồn mở. Việc sử dụng mã và tài liệu tuân theo giấy phép hoặc thông báo bản quyền của kho tương ứng.

Không kho nào được chứa thông tin xác thực đang hoạt động, cấu hình riêng tư, dữ liệu cá nhân production, bản xuất cơ sở dữ liệu, nhật ký riêng tư, quyền truy cập dashboard được bảo vệ hoặc bí mật.

## Tổng quan công nghệ

Shoukaku chủ yếu được xây dựng bằng TypeScript và Node.js. Hệ thống được lưu trữ sử dụng Discord.js, PostgreSQL, Redis, Lavalink, Docker, các thành phần xử lý phương tiện được chọn và công cụ quan sát tùy chọn.

Xem [TECHNOLOGY.md](TECHNOLOGY.md) để biết chi tiết ở mức tổng quan mà không công bố thông tin xác thực hoặc quyền truy cập production được bảo vệ.

## Tính sẵn sàng và thay đổi

Shoukaku đang được phát triển tích cực. Lệnh, tích hợp, hạn mức và tính sẵn sàng có thể thay đổi theo Discord, API bên thứ ba, pháp luật và yêu cầu dự án.

Để kiểm tra hành vi hiện tại:

1. Dùng `/help` trong Discord.
2. Kiểm tra [máy chủ hỗ trợ](https://discord.gg/qGwKsqH62k).
3. Kiểm tra [trang trạng thái](https://altergolden.dev).
4. Dùng [COMMANDS.md](COMMANDS.md) khi cần xem cả phần triển khai đã bị vô hiệu hóa.

## Quyền riêng tư, an toàn và báo cáo

- Shoukaku không bán dữ liệu cá nhân.
- Dịch vụ chính thức có thể xử lý định danh Discord, cấu hình máy chủ, hồ sơ kiểm duyệt, dữ liệu nhập vào lệnh, tùy chọn âm nhạc, mục yêu thích, lịch sử nghe, dữ liệu phương tiện tạm thời, metadata ánh xạ phương tiện, tín hiệu bảo mật và nhật ký kỹ thuật như mô tả trong [Chính sách Quyền riêng tư](PP_VI.md).
- `/download` chỉ dành cho phương tiện công khai được hỗ trợ mà người dùng sở hữu, được phép sử dụng hoặc được pháp luật áp dụng cho phép sử dụng. Tệp nguồn cục bộ mặc định có tuổi tối đa 1.800 giây; đối tượng R2 công khai tạm thời, khi bật, hướng tới tối đa 86.400 giây.
- Lệnh chuyên biệt về nội dung người lớn và việc thu thập tin nhắn đã xóa vẫn bị tắt trong Dịch vụ chính thức.
- Khiếu nại bản quyền phải tuân theo [IP_POLICY.md](IP_POLICY.md).
- Lỗ hổng bảo mật phải được báo cáo theo [SECURITY.md](SECURITY.md).
- Thông báo quyền riêng tư, pháp lý, bản quyền và bảo mật có thể gửi đến **whittylord@gmail.com**.

Không công bố lỗ hổng, token, thông tin xác thực, dữ liệu cá nhân, nội dung có bản quyền hoặc hướng dẫn khai thác trong issue công khai.

## Quyền Discord

Liên kết mời chính thức yêu cầu quyền **Administrator** của Discord. Đây là quyền truy cập rộng: chỉ mời Shoukaku vào máy chủ bạn sở hữu hoặc được ủy quyền rõ ràng để quản trị, đồng thời rà soát quyền được yêu cầu trước khi xác nhận cài đặt.

## Đóng góp tài liệu

Các chỉnh sửa và cải thiện tài liệu công khai được chào đón theo [CONTRIBUTING.md](CONTRIBUTING.md). Nội dung đóng góp chỉ được chứa thông tin phù hợp để công khai và không được gồm bí mật, dữ liệu riêng tư hoặc quyền truy cập hạ tầng được bảo vệ.

## Quyền và nhãn hiệu

Kho này được cung cấp theo [LICENSE](LICENSE). Tên, nhãn hiệu, API, phần mềm và nội dung bên thứ ba thuộc về chủ sở hữu tương ứng. Không ngụ ý quan hệ liên kết hoặc chứng thực.
