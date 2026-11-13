# Trùm Săn Sale

Website responsive tiếng Việt, có landing page và bản xem trước khu vực thành viên.

## Xem thử

Mở `index.html` trong trình duyệt. Tạo một tài khoản demo bằng email và mật khẩu (ít nhất 6 ký tự). Tài khoản và nhiệm vụ demo lưu trong `localStorage` của trình duyệt.

## Đưa lên InfinityFree

1. Tạo website/domain trong InfinityFree.
2. Tải nội dung thư mục này lên `htdocs` bằng File Manager hoặc FTP. Trang chính là `index.html`, không cần build hay PHP.
3. Để đăng nhập hoạt động thật, tạo Firebase project, bật Authentication > Email/Password và tạo Firestore Database.
4. Dán Firebase Web config vào `FIREBASE_CONFIG` trong `index.html`.
5. Cấu hình Authorized domains trong Firebase Authentication với domain website.

## Trạng thái chức năng

- Bản hiện tại là prototype front-end: dữ liệu demo nằm trên trình duyệt hiện tại, chưa đồng bộ giữa người dùng/thiết bị.
- Firebase Auth (đăng ký, đăng nhập, gửi email đặt lại mật khẩu) được khởi tạo khi có cấu hình.
- Nhiệm vụ, gửi bằng chứng, mã đơn không trùng, trạng thái đơn, mã vận đơn, hồ sơ và yêu cầu rút tiền hiện là mô phỏng local. Ảnh tải lên mới chỉ lưu tên file trong demo, chưa upload ảnh.
- Chưa có trang quản trị hoặc backend xử lý duyệt nhiệm vụ, đối soát, cộng tiền, tạo/chỉnh nhiệm vụ và hoàn tất chuyển khoản. Không dùng số dư demo hoặc localStorage để chi tiền thật.
- Các con số thành viên/tỷ lệ duyệt trên landing page là số minh họa, cần thay bằng số liệu thật trước khi xuất bản.

## Cần có trước khi vận hành thật

Ứng dụng cần backend có xác thực và phân quyền admin ở phía máy chủ, Firestore Security Rules chặt chẽ, Storage Rules cho ảnh, transaction chống trùng mã đơn toàn hệ thống và chống cộng tiền/rút tiền lặp. Không nhúng khóa Admin SDK hay bí mật máy chủ vào HTML. InfinityFree chỉ phục vụ file tĩnh ở gói hosting cơ bản; nên dùng Firebase (Auth/Firestore/Storage/Functions hoặc backend riêng) cho dữ liệu và tác vụ tin cậy.

## GitHub

Thư mục này sẵn sàng để đưa lên repository GitHub. Cần repository đích (URL) và quyền GitHub được kết nối để xuất bản lên tài khoản của bạn.
