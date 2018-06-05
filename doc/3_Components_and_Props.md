* [1.Functional and Class Components](#functional-and-class-components)
* [2.Rendering a Component](#rendering-a-component)
* [3.Composing Components](#composing-components)



` Component là 1 thứ tuyệt vời để xây dựng giao diện 
trước khi component của react ra đời các trang html được viết tất cả trong 1 file và được phân tách theo cách người tạo chương trình tự định nghĩa và phân chia
`
Compoment cho phép chia giao diện thành các phần nhỏ có thể reuses, và có thể xử lý độc lập 
=> chia nhỏ cái to và trị từng vấn đề nhỏ
Component giống funtion trong js => có đầu vào(props) và đầu ra (jsx <react element> => mô tả cho brower hiển thị ntn)

# Functional and Class Components
*  tạo components đơn giản
```
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
* Chi cho 1 param là props (properties) => lamda function
es6 
```
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```
# Rendering a Component
`khi mà các thuộc tính của 1 jsx được truyền như 1 object thì đó là props`
```javascript
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}

const element = <Welcome name="Sara" />;
ReactDOM.render(
  element,
  document.getElementById('root')
);
```
* ReactDOM.render() gọi components với đầu vào là obj 
* components return element 
* ReactDOM.render() update để khớp vs DOM (react element jsx) đã được khai báo => render 
` lưu ý là compoment cần viết hoa để react ko nhầm lẫn vs DOM HTML 

# Composing Components
` components có thể gọi tới các components khác => chia nhỏ hết cỡ để tái sử dụng ???

### My Multi Word Header
