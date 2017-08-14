# practical-js

>数字转为千分位，两位小数
``` javascript
function format (num) {
    return (num.toFixed(2) + '').replace(/\d{1,3}(?=(\d{3})+(\.\d*)?$)/g, '$&,');
}
```

>GetQueryString
``` typescript
class Utilities {
    /**
     * 根据 查询参数,找到对应的值
     * @param name
     */
    static GetQueryString(name) {
        var reg = new RegExp('(^|&)' + name + '=([^&]*)(&|$)', 'i');
        var r = window.location.search.substr(1).match(reg);
        if (r != null) {
            return decodeURI(r[2]);
        }
        return null;
    }
}
```

>转化为数字的简单方式
``` javascript
// + statement
+ '123'  // ==> 123
+ 'ABC'  // ==> NaN
+ new Date() // ==> 431231231231(毫秒数)
// 思考下面例子
'foo' + + 'bar' // ==> 'fooNaN'
```             
