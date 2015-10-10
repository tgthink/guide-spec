# Javascript编码规范

[1 代码风格](#user-content-1-代码风格)

　　[1.1 结构](#user-content-11-结构)

　　　　[1.1.1 缩进](#user-content-111-缩进)

　　　　[1.1.2 空格](#user-content-112-空格)

　　[1.2 命名](#user-content-12-命名)

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

#### 1.1.2 空格

##### [强制] 二元运算符两侧、三元运算符'?:'前后必须有一个空格，一元运算符与操作对象之间不允许有空格。

示例：

```javascript
// good
var a = !arr.length;
a++;
a = b + c;
z = x ? 1 : 2;

// bad
z = x?1:2;

```

##### [强制] 用作代码块起始的左花括号 `{` 前必须有一个空格。

示例：

```javascript
// good
if (condition) {
}

while (condition) {
}

function funcName() {
}

// bad
if (condition){
}

while (condition){
}

function funcName(){
}
```

##### [强制] `if / else / for / while / do / switch / case / try / catch / finally / with / return / typeof / function` 关键字后，必须有一个空格,`else / while / catch / finally`关键字前必须有空格。

示例：

```javascript
// good
if (condition) {
} else if (condition) {
} else {
}

while (condition) {
}

(function () {
})();

// bad
if(condition) {
}

while(condition) {
}

(function() {
})();
```

##### [强制] 在对象创建时，属性中的 `:` 之后必须有空格，`:` 之前不允许有空格。

示例：

```javascript
// good
var obj = {
    a: 1,
    b: 2,
    c: 3
};

// bad
var obj = {
    a : 1,
    b:2,
    c :3
};
```

##### [强制] 函数声明、具名函数表达式、函数调用中，函数名和 `(` 之间不允许有空格。

示例：

```javascript
// good
function funcName() {
}

var funcName = function funcName() {
};

funcName();

// bad
function funcName () {
}

var funcName = function funcName () {
};

funcName ();
```

##### [强制] `,` 和 `;` 前不允许有空格。

示例：

```javascript
// good
callFunc(a, b);

// bad
callFunc(a , b) ;
```

##### [强制] 在函数调用、函数声明、括号表达式、属性访问、`if / for / while / switch / catch` 等语句中，`()` 和 `[]` 内紧贴括号部分不允许有空格。

示例：

```javascript
// good

callFunc(param1, param2, param3);

save(this.list[this.indexes[i]]);

needIncream && (variable += increament);

if (num > list.length) {
}

while (len--) {
}


// bad

callFunc( param1, param2, param3 );

save( this.list[ this.indexes[ i ] ] );

needIncreament && ( variable += increament );

if ( num > list.length ) {
}

while ( len-- ) {
}
```

##### [强制] 单行声明的数组与对象，如果包含元素，`{}` 和 `[]` 内紧贴括号部分不允许包含空格。

解释：

声明包含元素的数组与对象，只有当内部元素的形式较为简单时，才允许写在一行。元素复杂的情况，还是应该换行书写。


示例：

```javascript
// good
var arr1 = [];
var arr2 = [1, 2, 3];
var obj1 = {};
var obj2 = {name: 'obj'};
var obj3 = {
    name: 'obj',
    age: 20,
    sex: 1
};

// bad
var arr1 = [ ];
var arr2 = [ 1, 2, 3 ];
var obj1 = { };
var obj2 = { name: 'obj' };
var obj3 = {name: 'obj', age: 20, sex: 1};
```

##### [强制] 行尾不得有多余的空格。

### 1.2 命名

##### [强制] `变量` 使用 `Camel命名法`。

示例：

```javascript
var loadingModules = {};
```

##### [强制] `常量` 使用 `全部字母大写，单词间下划线分隔` 的命名方式。

示例：

```javascript
var HTML_ENTITY = {};
```

##### [强制] `函数` 使用 `Camel命名法`。

示例：

```javascript
function stringFormat(source) {
}
```

##### [强制] 函数的 `参数` 使用 `Camel命名法`。

示例：

```javascript
function echo(hello) {
}
```


##### [强制] `类` 使用 `Pascal命名法`。

示例：

```javascript
function TextNode(options) {
}
```

##### [强制] 类的 `方法 / 属性` 使用 `Camel命名法`。

示例：

```javascript
function TextNode(value,engine) {
    this.value = value;
    this.engine = engine;
}

TextNode.prototype.clone = function () {
    return this;
};
```

##### [强制] `枚举变量` 使用 `Pascal命名法`，`枚举的属性` 使用 `全部字母大写，单词间下划线分隔` 的命名方式。

示例：

```javascript
var TargetState = {
    READING: 1,
    READED: 2,
    APPLIED: 3,
    READY: 4
};
```

##### [强制] `命名空间` 使用 `Camel命名法`。

示例：

```javascript
equipments.heavyWeapons = {};
```

##### [强制] 由多个单词组成的缩写词，在命名中，根据当前命名法和出现的位置，所有字母的大小写与首字母的大小写保持一致。

示例：

```javascript
function XMLParser() {
}

function insertHTML(element, html) {
}

var oHttpRequest = new HTTPRequest();
```

##### [强制] `类名` 使用 `名词`。

示例：

```javascript
function Engine(options) {
}
```

##### [建议] `函数名` 使用 `动宾短语`。

示例：

```javascript
function getStyle(element) {
}
```

##### [建议] `boolean` 类型的变量使用 `is` 或 `has` 开头。

示例：

```javascript
var isReady = false;
var hasMoreCommands = false;
```

##### [建议] `Promise对象` 用 `动宾短语的进行时` 表达。

示例：

```javascript
var oLoadingData = ajax.get('url');
oLoadingData.then(callback);
```

