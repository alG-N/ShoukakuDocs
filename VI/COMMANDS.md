# Danh mục lệnh

Trang này cung cấp danh mục công khai về bề mặt lệnh hướng tới người dùng của Shoukaku, bao gồm lệnh đang hoạt động, bị giới hạn và bị vô hiệu hóa.

> Dùng `/help` trong Discord để xem tên lệnh, tùy chọn, quyền và tính sẵn sàng đang hoạt động mới nhất. Tài liệu này cũng ghi lại các lệnh đã bị vô hiệu hóa để giải thích đúng mã nguồn lịch sử, ảnh chụp cũ hoặc đăng ký lệnh Discord cũ.

## Ý nghĩa trạng thái

| Trạng thái | Ý nghĩa |
|---|---|
| **Hoạt động** | Được backend hiện tại đăng ký và dành cho sử dụng thông thường, tùy quyền và cấu hình |
| **Bị giới hạn** | Được đăng ký nhưng chỉ dành cho chủ bot, máy chủ hỗ trợ, quản trị viên, kênh cụ thể hoặc quy tắc truy cập khác |
| **Vô hiệu hóa** | Chỉ còn dưới dạng lịch sử hoặc mã triển khai và không được Dịch vụ chính thức đăng ký |

## Lệnh chung và tiện ích

| Lệnh | Mục đích | Trạng thái |
|---|---|---|
| `/afk` | Quản lý trạng thái AFK | Hoạt động |
| `/avatar` | Hiển thị avatar của người dùng | Hoạt động |
| `/display` | Hiển thị thông tin người dùng hoặc hồ sơ được hỗ trợ | Hoạt động |
| `/help` | Duyệt registry lệnh hiện tại và cách dùng chính xác | Hoạt động |
| `/invite` | Hiển thị liên kết mời bot chính thức, có yêu cầu quyền Administrator | Hoạt động |
| `/ping` | Kiểm tra khả năng phản hồi của bot | Hoạt động |
| `/report` | Gửi báo cáo qua kênh máy chủ hoặc dự án đã cấu hình | Hoạt động |
| `/roleinfo` | Hiển thị thông tin vai trò Discord | Hoạt động |
| `/serverinfo` | Hiển thị thông tin máy chủ hiện tại | Hoạt động |

## Kiểm duyệt và an toàn máy chủ

Các lệnh kiểm duyệt yêu cầu quyền Discord phù hợp và có thể bị ảnh hưởng bởi thứ bậc vai trò hoặc cấu hình máy chủ.

| Lệnh | Mục đích | Trạng thái |
|---|---|---|
| `/automod` | Cấu hình hoặc quản lý tự động kiểm duyệt | Bị giới hạn |
| `/ban` | Cấm thành viên khi được phép | Bị giới hạn |
| `/case` | Xem vụ việc kiểm duyệt | Bị giới hạn |
| `/clearwarns` | Xóa hồ sơ cảnh cáo được hỗ trợ | Bị giới hạn |
| `/delete` | Xóa tin nhắn được hỗ trợ | Bị giới hạn |
| `/delwarn` | Xóa một hồ sơ cảnh cáo | Bị giới hạn |
| `/kick` | Kick thành viên khi được phép | Bị giới hạn |
| `/lockdown` | Hạn chế hoạt động kênh hoặc máy chủ khi có sự cố | Bị giới hạn |
| `/mute` | Tạm thời hạn chế thành viên khi được phép | Bị giới hạn |
| `/raid` | Truy cập công cụ chống raid hoặc ứng phó raid | Bị giới hạn |
| `/setting` | Cấu hình thiết lập máy chủ được hỗ trợ | Bị giới hạn |
| `/slowmode` | Cấu hình slowmode của kênh | Bị giới hạn |
| `/warn` | Tạo hồ sơ cảnh cáo | Bị giới hạn |
| `/warnings` | Xem hồ sơ cảnh cáo | Bị giới hạn |

Quản trị viên máy chủ chịu trách nhiệm rà soát hành động kiểm duyệt, cấu hình quyền, thông báo cho thành viên khi cần và tuân thủ quy định Discord cùng pháp luật áp dụng.

## Âm nhạc

Shoukaku cung cấp tính năng âm nhạc qua `/music` và các subcommand.

| Subcommand | Mục đích | Trạng thái |
|---|---|---|
| `play` | Tìm hoặc phát bài hát hay playlist từ nguồn được phê duyệt | Hoạt động |
| `stop` | Dừng phát và xóa hàng đợi hiện tại | Hoạt động |
| `skip` | Bỏ qua bài hiện tại | Hoạt động |
| `pause` | Tạm dừng hoặc tiếp tục phát | Hoạt động |
| `queue` | Xem hàng đợi hiện tại | Hoạt động |
| `nowplaying` | Xem bài đang phát | Hoạt động |
| `volume` | Điều chỉnh âm lượng | Hoạt động |
| `loop` | Cấu hình lặp bài hoặc hàng đợi | Hoạt động |
| `shuffle` | Bật hoặc tắt trộn hàng đợi | Hoạt động |
| `remove` | Xóa một bài khỏi hàng đợi | Hoạt động |
| `move` | Di chuyển bài trong hàng đợi | Hoạt động |
| `clear` | Xóa bài đang chờ nhưng giữ bài hiện tại | Hoạt động |
| `seek` | Tua đến một vị trí trong bài hiện tại | Hoạt động |
| `history` | Xem lịch sử nghe được hỗ trợ | Hoạt động |
| `autoplay` | Cấu hình autoplay | Hoạt động |

Không được dùng âm nhạc để truy cập nội dung riêng tư, trả phí, chỉ dành cho thuê bao, giới hạn độ tuổi, giới hạn khu vực hoặc được bảo vệ bằng DRM; cũng không được vi phạm điều khoản nguồn hoặc quyền của chủ sở hữu.

## Dịch vụ bên thứ ba được phê duyệt

| Lệnh | Mục đích | Trạng thái |
|---|---|---|
| `/anime` | Tìm thông tin anime từ nguồn được hỗ trợ | Hoạt động |
| `/download` | Chuẩn bị và gửi preview của phương tiện công khai được hỗ trợ | Hoạt động |
| `/media` | Sửa embed mạng xã hội, hiển thị ảnh hoặc GIF trực tiếp và chuẩn bị preview phương tiện công khai được hỗ trợ | Hoạt động |
| `/pixiv` | Lấy thông tin hoặc phương tiện Pixiv được hỗ trợ | Hoạt động |
| `/reddit` | Lấy nội dung Reddit được hỗ trợ | Hoạt động |
| `/steam` | Lấy thông tin Steam được hỗ trợ | Hoạt động |
| `/wikipedia` | Tìm kiếm Wikipedia | Hoạt động |

Các lệnh bên thứ ba phụ thuộc API bên ngoài và có thể bị gián đoạn, giới hạn hoặc gỡ bỏ. Bản triển khai chính thức bật `/download` qua `DOWNLOAD_COMMAND_ENABLED`. Người dùng chỉ được gửi phương tiện công khai được hỗ trợ mà mình sở hữu, được phép sử dụng hoặc được pháp luật áp dụng cho phép sử dụng. Người dùng không được cung cấp mật khẩu tài khoản, cookie phiên, access token hoặc URL tới nội dung riêng tư, trả phí, bị giới hạn hay được bảo vệ bằng DRM.

Tệp nguồn tải xuống dùng để xử lý mặc định có tuổi cục bộ tối đa 1.800 giây. Đối tượng R2 công khai tạm thời, khi bật, hướng tới tối đa 86.400 giây.

Một số máy chủ ảnh bên thứ ba có thể chứa nội dung người lớn dù Shoukaku không cung cấp lệnh chuyên biệt về nội dung đó. Người dùng và quản trị viên không được dùng `/media` để cho người chưa thành niên tiếp xúc với nội dung người lớn, né giới hạn kênh hoặc vi phạm quy định Discord. Người vận hành có thể chặn nguồn hoặc yêu cầu khi cần vì an toàn, pháp luật, chính sách nền tảng hoặc bản quyền.

## Giải trí

| Lệnh | Mục đích | Trạng thái |
|---|---|---|
| `/deathbattle` | Chạy tương tác giải trí được hỗ trợ | Hoạt động |
| `/say` | Gửi văn bản do bot định dạng khi được phép | Hoạt động |

## Vận hành dành cho chủ bot

| Lệnh | Mục đích | Trạng thái |
|---|---|---|
| `/botcheck` | Xem chẩn đoán vận hành chỉ dành cho chủ bot | Bị giới hạn |

Lệnh dành cho chủ bot được triển khai riêng tới máy chủ hỗ trợ đã cấu hình và không dành cho người dùng thông thường.

## Phần triển khai lệnh đã bị vô hiệu hóa

Các lệnh sau được giữ trong danh mục đầy đủ vì file triển khai, kiểm thử, cấu trúc cơ sở dữ liệu hoặc ảnh chụp cũ có thể vẫn nhắc tới chúng. Chúng không được export bởi registry hiện tại và không được cung cấp trong Dịch vụ chính thức.

| Lệnh | Mục đích lịch sử | Trạng thái |
|---|---|---|
| `/snipe` | Hiển thị tin nhắn đã xóa gần đây được thu thập cho máy chủ | Vô hiệu hóa |
| `/nhentai` | Tìm hoặc lấy nội dung doujin hướng người lớn | Vô hiệu hóa |
| `/rule34` | Tìm hoặc lấy hình ảnh hướng người lớn | Vô hiệu hóa |

Việc giữ mã triển khai không kích hoạt lệnh. Lệnh Discord cũ chỉ biến mất sau khi registry ứng dụng chính thức được ghi đè thành công bằng bản triển khai hiện tại.

## Quyền và lỗi

Lệnh có thể thất bại khi:

- người dùng hoặc Bot thiếu quyền Discord cần thiết;
- vai trò Bot thấp hơn vai trò của thành viên mục tiêu;
- tính năng bị tắt trong máy chủ hoặc Dịch vụ chính thức;
- dịch vụ bên thứ ba không khả dụng;
- người dùng bị giới hạn tần suất;
- URL, truy vấn hoặc nội dung không được hỗ trợ hoặc bị giới hạn;
- kiểm soát pháp lý, an toàn, bản quyền, quyền riêng tư hoặc nền tảng chặn yêu cầu.

Để được hỗ trợ, dùng `/help` hoặc truy cập máy chủ hỗ trợ chính thức:

https://discord.gg/qGwKsqH62k
