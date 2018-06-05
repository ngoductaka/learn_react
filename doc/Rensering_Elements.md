` Brower dùng DOM element ( document object model) để định nghĩa các thành phần, đơn vị để tạo trang web )
React DOM dùng các object là đơn vị để tạo trang web `
# rendering an element into DOM
mỗi app tạo bởi react đều có 1 div có id là root. các phần tử con trong nó được quản lý bởi react 
` các phần tử muốn ghép vào 1 app có sẵn cần cô lập root ?? là như lào?? `
để tạo 1 phần tử con trong root:
```
const element = <h1>Hello, world</h1>;
ReactDOM.render(element, document.getElementById('root'));
```
# update render elements
* earch element is immutable nghĩa là cố định các thuộc tính và con ..... nó có thể thay đổi trang thái các thuộc tính của nó và thuộc tính của các con
nhưng không thay đổi cấu trúc khi hiển thị ... như các hình trong video nó đại diện cho giao diện trong 1 thời điểm
* THe only way to update the UI í creace new element 
=> why call one time in app ??? =. componentDidMount willMount
# react only update what is Necessary 
 react element is immutable it is reason React DOM so sánh the element và con liền trước của nó, để tìm sự khác biệt và từ đó 
 update những thứ cần thiết cho => nhanh ??
# 





