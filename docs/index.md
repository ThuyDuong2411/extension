#Extension

"Extension" là một web page nhỏ tùy chỉnh trải nghiệm trình duyệt web. Chungs cho phép người dùng điều chỉnh chức năng và hành vi của Chrome theo nhu cầu hoạc sở thích cá nhân. Chúng được xây dụng dựa trên công nghệ HTML, CSS và Javascript.

Một extension phải thực hiện một `a single purpose` được định nghĩa một cách dễ hiểu. Một extension có thể bao gồm nhiều thành phần và một loạt các function, miễn là mọi thứ đều đóng góp cho mục đích chung.

Giao diện người dùng nên đơn giản hóa và cố định. Chúng có thể là một biểu tượng đơn giản, chẳng hạn như `Google Mail Checker extension` như hình.

<p align= "center"><img src="/images/gmail-small.png"></p>

Các tệp extension được nén thành `.crx` cho người dùng tải xuống và cài đặt. Điều này có nghĩa extension không phụ thuộc vào nội dung trang web, không giống như các ứng dụng web thông thường.

Extension được phân phối thông qua `Chrome Developer Dashboard` và được triển khai trên `Chrome Web Store`. 

#Hello Extensions

Thực hiện ví dụ Hello Extension đơn giản. Đầu tiên tạo một thư mục mới để lưu trữ các tệp của extension.

Tiếp theo, thêm file `manifest.json` chứa các dòng code sau:

```
 {
    "name": "Hello Extensions",
    "description" : "Base Level Extension",
    "version": "1.0",
    "manifest_version": 2
  }
```

Mọi extension đều yêu cầu một `manifest`, mặc dù hầu hết các extension sẽ không làm được điều gì chỉ với `manifest`. Để bắt đầu nhanh, extension này có tệp và biểu tượng bật lên được khai báo trong trường `browser_action`:

```
{
    "name": "Hello Extensions",
    "description" : "Base Level Extension",
    "version": "1.0",
    "manifest_version": 2,
    "browser_action": {
      "default_popup": "hello.html",
      "default_icon": "hello_extensions.png"
    }
  }
```

Sau đó, tạo file hello.html: 

```
  <html>
    <body>
      <h1>Hello Extensions</h1>
    </body>
  </html>
```
Bây giờ extension sẽ hiển thị hello.html khi biểu tượng được click. Bước tiếp theo bao gồm một `command` trong `manifest.json` cho phép phím tắt (Bước này không cần thiết):

```
 {
    "commands": {
      "_execute_browser_action": {
        "suggested_key": {
          "default": "Ctrl+Shift+F",
          "mac": "MacCtrl+Shift+F"
        },
        "description": "Opens hello.html"
      }
    }
  
  }
```

Bước cuối cùng trong việc cài đặt extension trên máy local:

- Chuyển hướng đến `chrome://extensions` trên trình duyệt của bạn.

- Bật chế độ `Developer Mode`.
 
- Click `Load Unpacked` và chọn thư mục chứa extension của bạn.

Bây giờ bạn có thể sử dụng extension trên cửa sổ bật lên cửa mình bằng cách click vào biểu tượng hoặc nhấn tổ hợp phím `Ctrl+Shift+F`.
