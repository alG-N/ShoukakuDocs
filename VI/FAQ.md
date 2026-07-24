# Câu hỏi thường gặp

## Làm thế nào để mời Shoukaku?

Dùng liên kết mời chính thức theo nguyên tắc quyền tối thiểu:

https://discord.com/oauth2/authorize?client_id=1472185156809920615&permissions=0&integration_type=0&scope=bot+applications.commands

Liên kết không chọn trước quyền Discord nào. Quản trị viên chỉ nên cấp quyền cần thiết cho tính năng họ sử dụng.

## Làm thế nào để xem các lệnh khả dụng?

Chạy `/help` trong Discord để xem các lệnh đang hoạt động và hiển thị theo quyền cùng ngữ cảnh kênh hiện tại.

[Danh mục lệnh đầy đủ](COMMANDS.md) cũng liệt kê lệnh bị giới hạn và phần triển khai đã bị vô hiệu hóa. Lệnh bị vô hiệu hóa có thể vẫn xuất hiện trong mã nguồn, kiểm thử, ảnh chụp cũ hoặc đăng ký Discord lịch sử nhưng không sử dụng được trên Dịch vụ chính thức.

## Tại sao một lệnh bị thiếu hoặc không khả dụng?

Tính năng có thể không khả dụng vì:

- bị tắt để rà soát pháp lý, quyền riêng tư, bản quyền, an toàn hoặc chính sách nền tảng;
- chỉ dành cho chủ bot, máy chủ hỗ trợ, quản trị viên hoặc quyền cụ thể;
- bị tắt hoặc giới hạn trong máy chủ;
- người dùng hoặc Bot thiếu quyền Discord;
- vai trò Bot thấp hơn vai trò mục tiêu;
- nhà cung cấp âm nhạc, phương tiện hoặc bên thứ ba không khả dụng;
- yêu cầu bị cooldown, rate limit, quy tắc an toàn hoặc giới hạn kích thước;
- lệnh đã thay đổi trong quá trình phát triển.

Dịch vụ chính thức hiện không đăng ký `/nhentai`, `/rule34`, `/download` hoặc `/snipe`.

## Tại sao lệnh cũ đã bị tắt vẫn có thể xuất hiện trong Discord?

Lệnh ứng dụng Discord chỉ được xóa sau khi backend hiện tại ghi đè thành công toàn bộ registry lệnh. Xóa export trong mã nguồn không tự động xóa lệnh đã triển khai trước đó.

Lệnh cũ còn hiển thị không đồng nghĩa backend hiện tại vẫn hỗ trợ chức năng đó. Người vận hành cần triển khai lại registry hiện tại.

## Tại sao Shoukaku offline?

Shoukaku có thể đang khởi động lại, bảo trì, gặp sự cố lưu trữ hoặc chờ dịch vụ bên thứ ba.

Kiểm tra:

- Trạng thái: https://altergolden.dev
- Hỗ trợ: https://discord.gg/qGwKsqH62k

## Tại sao Shoukaku không kiểm duyệt được một thành viên?

Thứ bậc vai trò Discord áp dụng cho bot. Shoukaku thường không thể kiểm duyệt:

- chủ sở hữu máy chủ;
- thành viên có vai trò cao nhất bằng hoặc cao hơn vai trò cao nhất của Bot;
- thành viên được bảo vệ bởi quyền hoặc vai trò do tích hợp quản lý.

Người chạy lệnh cũng phải có quyền phù hợp.

## Có những điều khiển âm nhạc nào?

`/music` bao gồm phát, hàng đợi, tạm dừng, dừng, bỏ qua, âm lượng, lặp, trộn, xóa, di chuyển, xóa hàng đợi, tua, lịch sử và autoplay. Tùy chọn chính xác được hiển thị qua `/help command:music` và trong [COMMANDS.md](COMMANDS.md).

## Tại sao phát nhạc thất bại?

Nguyên nhân thường gặp:

- người dùng hoặc Bot không ở trong kênh thoại có thể sử dụng;
- Bot thiếu quyền Connect hoặc Speak;
- nguồn không được hỗ trợ, không khả dụng, riêng tư, trả phí, chỉ dành cho thuê bao, giới hạn độ tuổi, giới hạn khu vực hoặc được bảo vệ bằng DRM;
- Lavalink hoặc nhà cung cấp nguồn tạm thời không khả dụng;
- URL đã thay đổi hoặc hết hạn.

Không gửi mật khẩu, cookie, access token hoặc liên kết riêng tư. Hãy thử nguồn công khai được phê duyệt khác và kiểm tra máy chủ hỗ trợ.

## Shoukaku có lưu thông tin âm nhạc không?

Backend chính thức có thể lưu tùy chọn âm nhạc, mục yêu thích và lịch sử nghe trong PostgreSQL. Hiện tại mục yêu thích giới hạn 200 mục gần nhất mỗi người dùng và lịch sử nghe giới hạn 100 mục gần nhất.

Người dùng có thể xóa lịch sử nghe qua giao diện âm nhạc được hỗ trợ. Yêu cầu truy cập, sửa hoặc xóa khác có thể gửi qua kênh quyền riêng tư. Xem [Chính sách Quyền riêng tư](PP_VI.md).

## Shoukaku có thể tải phương tiện không?

Lệnh công khai `/download` hiện bị vô hiệu hóa.

Lệnh `/media` còn lại có thể sửa embed mạng xã hội, hiển thị ảnh hoặc GIF trực tiếp và chuẩn bị preview phương tiện công khai được hỗ trợ. Không được dùng để truy cập nội dung riêng tư, trả phí, bị giới hạn, giới hạn độ tuổi hoặc được bảo vệ bằng DRM.

## Thông tin liên quan đến phương tiện có thể tồn tại bao lâu?

Các thành phần có thời gian khác nhau:

- tệp nguồn tạm thời mặc định có tuổi tối đa 1.800 giây;
- đối tượng công khai tạm thời, khi được bật, hướng tới tối đa 86.400 giây;
- metadata ánh xạ phương tiện YouTube ổn định trong Redis mặc định có TTL có thể gia hạn bảy ngày và giới hạn tuyệt đối 30 ngày từ khi tạo.

Khoảng thời gian Redis dài hơn áp dụng cho metadata và ánh xạ nguồn, không có nghĩa tệp nguồn tải xuống được giữ 30 ngày. Xem [Chính sách Quyền riêng tư](PP_VI.md).

## `/media` có thể hiển thị nội dung người lớn không?

Shoukaku không cung cấp lệnh chuyên biệt về nội dung người lớn trên Dịch vụ chính thức. Tuy nhiên, một số máy chủ ảnh bên thứ ba có thể chứa nội dung trưởng thành.

Người dùng và quản trị viên không được dùng `/media` để cho người chưa thành niên tiếp xúc với nội dung người lớn, né giới hạn kênh hoặc vi phạm quy định Discord. Người vận hành có thể chặn nhà cung cấp hoặc yêu cầu khi cần.

## Shoukaku có lưu tin nhắn của tôi không?

Shoukaku không lưu mọi tin nhắn như một kho chat chung. Dịch vụ chính thức hiện tắt thu thập `/snipe`. Tính năng kiểm duyệt, tự động kiểm duyệt, chống lạm dụng và báo cáo được bật có thể xử lý nội dung tin nhắn giới hạn khi cần cho tính năng được yêu cầu.

Xem [Chính sách Quyền riêng tư](PP_VI.md).

## Làm thế nào để yêu cầu truy cập, sửa hoặc xóa dữ liệu?

Gửi email đến **whittylord@gmail.com** kèm:

- ID người dùng Discord;
- ID máy chủ Discord liên quan, nếu có;
- dữ liệu hoặc tính năng liên quan;
- yêu cầu cần thực hiện.

Có thể cần xác minh để tránh tiết lộ hoặc xóa trái phép. Máy chủ hỗ trợ có thể tiếp nhận hỗ trợ ban đầu, nhưng yêu cầu quyền riêng tư và pháp lý nên hoàn tất qua email.

## Lệnh NSFW có khả dụng không?

Không. `/nhentai` và `/rule34` không được đăng ký trên Dịch vụ chính thức. Chúng chỉ còn trong danh mục đầy đủ để giải thích tham chiếu triển khai lịch sử.

## Shoukaku có phải nguồn mở không?

Cả kho tài liệu và backend đều được công khai để xem:

- Tài liệu: https://github.com/alG-N/ShoukakuDocs
- Backend: https://github.com/alG-N/ShoukakuBot

Việc công khai không tự động biến dự án thành nguồn mở. Các kho là source-visible và tuân theo giấy phép hoặc thông báo bản quyền tương ứng. Không được tự suy diễn quyền sao chép, phân phối lại, sửa đổi hoặc vận hành mã ngoài phạm vi giấy phép cho phép rõ ràng.

## Tôi có thể đóng góp không?

Các chỉnh sửa và cải thiện tài liệu công khai được chào đón theo [CONTRIBUTING.md](CONTRIBUTING.md). Không đưa thông tin xác thực, chi tiết production, nhật ký riêng tư, quyền truy cập dashboard nội bộ, dữ liệu cá nhân hoặc bí mật vào issue hay pull request công khai.

Đóng góp backend tuân theo quy tắc và tình trạng giấy phép của kho backend.

## Báo cáo lạm dụng, vi phạm bản quyền hoặc vấn đề bảo mật như thế nào?

- Lạm dụng và hỗ trợ: https://discord.gg/qGwKsqH62k
- Thông báo quyền riêng tư, pháp lý, bản quyền và bảo mật: **whittylord@gmail.com**
- Quy trình bản quyền: [IP_POLICY.md](IP_POLICY.md)
- Quy trình lỗ hổng: [SECURITY.md](SECURITY.md)

Không đăng token, dữ liệu cá nhân, nội dung có bản quyền, chi tiết khai thác hoặc lỗ hổng đang hoạt động trong issue công khai.
