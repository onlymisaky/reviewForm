checkbox、radio、select复习

[效果查看](https://onlymisaky.github.io/reviewForm/)
[原生版Code](https://github.com/onlymisaky/reviewForm/blob/master/index.html)
[jQuery版本Code](https://github.com/onlymisaky/reviewForm/blob/master/jQuery.html)
[angular版本Code](https://github.com/onlymisaky/reviewForm/blob/master/angular.html)
[angular不完美版本Code](https://github.com/onlymisaky/reviewForm/blob/master/angular2.html)



其实我是想写成博客的，但是我发现。。。。。。。。。。。




## 前言
用`angular`已经快半年了，基本上都是在写`component`或者用别人写好的`component`，最近在写一个需要用到`checkbox`、`radio`、`select`这些表单的组件，发现对这些表单在`angular`中的运用还不是很熟练，或者说是理解不到位，所以就单独拿出来练习一下。
## checkbox
### 基础
`checkbox`用`ng-model`绑定时，默认绑定的值是`Boolean`类型的。

![image](http://i4.buimg.com/1949/a9431167786724e2.png)

我们也可以用`ng-true-value`,`ng-false-value`为其指定选中时绑定的值，*注意 `ng-true-value`中的值如果需要显示字符串的话必须使用单引号*
```html
<body ng-app="app" ng-controller="Ctrl as ctrl">
    <input type="checkbox" 
           ng-model="ctrl.checked" 
           ng-true-value="'选中'"
           ng-false-value="'取消选中'"       
           ng-change="ctrl.changeCheckbox()">checkbox
</body>
```
```javascript
angular
    .module("app", [])
    .controller("Ctrl", function () {
        var vm = this;
        vm.changeCheckbox = function () {
            console.log(vm.checked);
        }
    });
```
![image](http://i4.buimg.com/1949/a4f4aa5b4b011b3b.png)
### 进阶
在实际开发中，我们常常会用到多个`checkbox`，这个时候就需要知道选中的哪些选项，还有全选反选这些操作。除了`angular.html`中所提供的方法，我们也可以使用`ng-true-value`








好吧，我不适合写作。。。
