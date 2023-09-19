# aikill

## 官网地址

[React Router](https://reactrouter.com/en/6.16.0/route/action)
[React](https://zh-hans.react.dev/)
[mobx](https://mobx.js.org/README.html)
[AI](https://chat.sixciv.com/?inviter=93800#/chat/1647251)

## react-router-dom v6 传参

[react-router-dom@6 的三种传参方式](https://juejin.cn/post/7104185670712688653)

### state 传参（当前使用）

```js
// 原页面
import { useNavigate } from "react-router-dom";

const navigate = useNavigate();
const goHome = () => {
  navigate("/home", { state: { id: 123 } });
};

// 跳转页
import { useLocation } from "react-router-dom";

const location: any = useLocation();
const back = () => {
  console.log(location.state.id); //打印结果为123
};
```
