# Javascript编码规范

[1 代码风格](#user-content-1-代码风格)

　　[1.1 结构](#user-content-11-结构)

　　　　[1.1.1 缩进](#user-content-111-缩进)

[2 变量方法命名规范](#user-content-2-变量方法命名规范)

## 1 代码风格
### 1.1 结构

#### 1.1.1 缩进

#### [强制] 使用 `4` 个空格做为一个缩进层级，不允许使用 `2` 个空格 或 `tab` 字符。

##### [强制] `switch` 下的 `case` 和 `default` 必须增加一个缩进层级。

示例：

```javascript
// good
switch (variable) {

    case '1':
        // do...
        break;

    case '2':
        // do...
        break;

    default:
        // do...

}

// bad
switch (variable) {

case '1':
    // do...
    break;

case '2':
    // do...
    break;

default:
    // do...

}
```

## 2 变量方法命名规范

| 数据类型 | 数据类型中文名 | 前缀  | 说明 |
| -------- | -------- | --- | --- |
| Array | 数组 | a |--|
| Bool | 布尔值 | b |--|
| Float | 浮点数 | l |--|
| Function | 函数,方法 |--|--|
| Int | 整型 | n |--|
| Object | 对象 | o |--|
| Regular Expression | 正则 | r |--|
| String | 字符串 | s |--|
| JQuery Object | JQuery对象 | $ |--|
| Class | 类 |--|等同于function|

