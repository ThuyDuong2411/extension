#Tổng quan

Extension được nén bằng các gói HTML, CSS, Javascript, images và các tệp khác được sử dụng trên nền tảng web, tùy chỉnh trải nghiệm duyệt web của Google Chrome. Các extension được xây dựng bằng công nghệ web và có thể sử dụng các API mà trình duyệt cung cấp cho web mở.

Chrome extension có thể được config để chỉ hoạt động trên một số trang nhất định thông qua param Page Actions, hoặc thiết lập code chạy nền sử dụng Background Pages hay thậm chí thay đổi thành phần của trang web đã được load hiện tại sử dụng Content Scripts.

#Các thành phần chính

##Extension UIs

Mỗi extension có thể có một browser action hoặc page action:

- Browser action: khi extension liên quan hầu hết đến các trang.

- Page action: khi extension có tác dụng trên những trang nhất định.

Những extensions có thể trình diễn theo những cách khác như: thêm context menu, cung cấp một option page, hoặc sử dụng content script để thay đổi hiển thị trên web page,...Các bạn có thể biết một số ví dụ về extension UI:

<p align= "center"><img src="images/exUI.png"></p>

##Extension Files

