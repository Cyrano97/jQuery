# jQuery
some notes about jQuery


###2、内容选择过滤器
***:contain(text)*** 选择含有文本内容为“text”的元素,返回的是一个集合元素
```jQuery
$("div:contains('我')")选择含有文本“我”的<div>元素
```

***：has（selector）*** 选取含有选择器所匹配的元素的元素,返回的是一个集合元素
```jQuery
$("div:has(p)")选取含有<p>元素的div元素
```
***:empty*** 选取不包含子元素或者文本的空元素，返回一个集合元素
```jQuery
$("div:empty")选择不包含（包括文本元素）的<div>空元素
```

***：parent*** 选取含有子元素或者文本的元素，返回一个集合元素
```jQuery
$("div:parent")选取拥有子元素（包含文本元素）的<div>元素
```


js获取当前url地址中文参数
```JavaScript 
//首先获取到当前页面的地址栏信息
var url = window.location.href;
console.log(url);

var obj = {};
var reg = /\?/;
if(url.match(reg)) {
    //判断传入参数，以问号截取，问号后是参数
    var chars = url.split('?')[1];

    //再截&号
    var arr = chars.split('&');

    //获得截取后的数组为键值对字符串
    for (var i = 0; i < arr.length; i++) {

        //保守一点确定看是否为 name=value形式
        var num = arr[i].indexOf("=");

        if (num > 0) {
            //拼接字符串
            var name = arr[i].substring(0, num);
            var value = arr[i].substr(num + 1);

            //拼接对象，并转码
            obj[decodeURIComponent(name)] = decodeURIComponent(value);
        }
    }
}
console.log(obj);
```
