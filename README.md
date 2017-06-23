# practical-js


>数字转为千分位，两位小数
``` javascript
function format (num) {
    return (num.toFixed(2) + '').replace(/\d{1,3}(?=(\d{3})+(\.\d*)?$)/g, '$&,');
}
```
