```
# import react,react-dom
# 定义组件
# 绑定及渲染
ReactDOM.reader(e(组件名), 'dom元素')

# 可选的jsx
```

工具链

## 元素和组件

### jsx

jsx: 编译后转成普通的javascript函数调用 

``` 
React.createElement() 
#  返回对象的简化结构
{
    type: "",
    props: {
        className: "",
        children: "",
    },
}
```

嵌入表达式
属性：camelCase定义属性的名称

### 元素

组件 -> react 元素 --(react-dom)--> dom
```
ReactDOM.render(react-element, dom-element)
```
react元素是不可变变量，只能创建全新的元素再传入到ReactDOM.render

### 组件 & Props

组件：类似函数，接受参数 props，返回 react 元素

组合组件：
提取组件：

**组件的props是不可更改**

### state & 生命周期 


state 更新:
```
setState( (state, props) => {
    // new state
})
```

### 数据流动：向下单向流动

###  事件处理


命名采用小驼峰 camelCase

必须显式的使用 preventDefault来阻止默认行为
e 是一个合成事件( SyntheticEvent )
this 的处理：可以使用箭头函数


```
<button onClick={activateLasers}>
  Activate Lasers
</button>
```
### 表单

受控组件