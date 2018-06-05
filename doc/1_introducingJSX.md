[1. JSX là gì ? javascript syntax extension? . Cú pháp mở rộng???](#what-is-jSX)
# What Is JSX
* HTML là 1 ngôn ngữ đánh dấu diêu văn bản. file html là kiểu file text có cấu trúc, sử dụng ngôn ngữ đánh dấu. cùng js,css giúp Brower đọc, để hiển thị trang web.
* JSX là cú pháp mở rộng của js nó mô tả có thể mô tả cách trang web hiển thị, và đầy đủ chức năng của giao giao diên ứng dụng:
(how events are handled, how the state changes over time, and how the data is prepared for display.) => cách event đc xử lý, thay đổi trong thái theo thời gian, chuẩn bị dữ liệu hiển thị 
# 2. Why use JSX
* chia trang web thành cách thành phần một cách tường minh. giúp sử dụng lại, cấu trúc trang đơn giản 
=> break big ploblem to the small and handle it
sử
# 3. cách dùng
* Có thể nhận biểu thức bên trong jsx bằng : curly braces {}
biểu thức : luôn trã về 1 giá trị! => phép tính, phép gán , lời gọi hàm .....
* jsx cũng là 1 biêủ thức. đồng nghĩa với việc nó có thể gán, có thể return có thể truyền vào như 1 param .....
# 4. Sử dụng các thuộc tính HTML với JSX
* lưu ý 
  * `là  dùng curly braces and quotes in the same attribute`
  * ` sử dung camelCase property naming instead ò HTML attribute names` class => className tabindex => tabIndex
# 5. Specifying Children with JSX 
* nếu tag rỗng => ko có con , ko có giá trị ....thì đóng luôn
# 6. JSX prevents Injection Attacks
* chế độ mặc định React DOM sẽ chuyển ký tự đặc biệt về bộ ký tự chuẩn của HTML trước khi render 
=> không bao  giờ bị inject 
# 7. JSX represent Object 
``` javascript
// jsx
const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
);
// babel  convert 
const element = React.createElement(
  'h1',
  {className: 'greeting'},
  'Hello, world!'
);
// essentially it creates an object like this:
// Note: this structure is simplified
const element = {
  type: 'h1',
  props: {
    className: 'greeting',
    children: 'Hello, world!'
  }
};
```
this object is `"react elements" ` this descriptions of what you want to see in screen => nói cho react biết là nó cần hiển thị gì 


