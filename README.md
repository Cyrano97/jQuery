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
