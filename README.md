# Tahoma di Asino
Lưu trữ phông Tahoma tạm thời cho dự án `Vietnamese writing problems: Chữ giùn cảitạo` của `Zì Zùn` aka. `An Hoàng Trung Tướng`
##### Mã CSS gốc
```css
@font-face {
  font-family: "Tahoma di Asino";
  src: url("link.eot"); /* IE9 Compat Modes */
  src: url("link.eot?#iefix") format("embedded-opentype"), /* IE6-IE8 */
       url("link.woff2") format("woff2"), /* Super Modern Browsers */
       url("link.woff") format("woff"), /* Pretty Modern Browsers */
       url("link.ttf")  format("truetype"), /* Safari, Android, iOS */
       url("link.svg#svgFontName") format("svg"); /* Legacy iOS */
}
* {
	font-family: Tahoma di Asino !important;
}
```
##### Mã Javascript gốc
```javascript
var fontLink = prompt("Nhập link phông (WOFF) mới.\nCancel để chọn mặc định từ GitHub.", "xxx");
if (fontLink === "") {
    fontLink = "xxx";
}
var css = "@font-face {font-family: \"Tahoma di Asino\";src: url(\"" + fontLink + "\") format(\"woff\");}* {font-family: Tahoma di Asino !important;}",
    head = document.head || document.getElementsByTagName("head")[0],
    style = document.createElement("style");
style.type = 'text/css';
if (style.styleSheet){
    style.styleSheet.cssText = css;
} else {
    style.appendChild(document.createTextNode(css));
}
head.appendChild(style);
```

## Hướng dẫn sử dụng mã Javascript để thay đổi phông trên mọi website trần gian
Hiện tại có 2 cách.
### 1. Bookmarklet (không tự động)
Sử dụng đoạn mã sau (copy):
```javascript
javascript:var fontLink=prompt("Nhập link phông (WOFF) mới.\nCancel để chọn mặc định từ GitHub.","https://raw.githubusercontent.com/AsOrticami/TahomaDiAsino/master/fonts/Tahoma.woff");if(fontLink==""){fontLink="https://raw.githubusercontent.com/AsOrticami/TahomaDiAsino/master/fonts/Tahoma.woff";}
var css="@font-face {font-family: \"Tahoma di Asino\";src: url(\""+fontLink+"\") format(\"woff\");}* {font-family: Tahoma di Asino !important;}",head=document.head||document.getElementsByTagName("head")[0],style=document.createElement("style");style.type='text/css';if(style.styleSheet){style.styleSheet.cssText=css;}else{style.appendChild(document.createTextNode(css));}
head.appendChild(style);
```
Trên thanh `Bookmark` của Chrome hoặc Firefox, chuột phải và tạo trang mới (Add page...) với URL là đoạn mã ở trên (paste).

Sau đó Lưu lại (Save). Đây chính là một `Bookmarklet`.

![alt tag](https://c7.staticflickr.com/6/5741/30471857006_9028a612d6_b.jpg)

Mở một lá cải Giùn bất kỳ. Nhấn vào `Bookmarklet` vừa tạo và hưởng thụ thành quả.

![alt tag](https://c7.staticflickr.com/6/5738/29877876094_f021eac6c2_b.jpg)
### 2. Tampermonkey (tự động)
[Tampermonkey](https://chrome.google.com/webstore/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo) hiện chỉ sử dụng được trên Chrome, add-on tương tự trên Firefox có tên [Greasemonkey](https://addons.mozilla.org/en-US/firefox/addon/greasemonkey/).
Mời cài đặt

Sử dụng đoạn mã sau (copy):
```javascript
// ==UserScript==
// @name         TalaScript
// @namespace    http://tampermonkey.net/
// @version      0.1
// @description  try to take over the world!
// @author       You
// @include      http://*
// @include      https://*
// @grant        none
// ==/UserScript==

(function() {
   var css = "@font-face {font-family: \"Tahoma di Asino\";src: url(\"https://raw.githubusercontent.com/AsOrticami/TahomaDiAsino/master/fonts/Tahoma.woff\") format(\"woff\");}* {font-family: Tahoma di Asino !important;}",
		 head = document.head || document.getElementsByTagName("head")[0],
		 style = document.createElement("style");
		 style.type = 'text/css';
    if (style.styleSheet){
         style.styleSheet.cssText = css;
    } else {
         style.appendChild(document.createTextNode(css));
    }
    head.appendChild(style);
})();
```
Trên Chrome, click chuột vào icon của `Tampermonkey`, chọn thêm một script mới (Add new script...)

Thay thế bằng đoạn mã ở trên, sau đó lưu lại (icon Save). Tiếp tục hưởng thụ thành quả khi mở một trang lá cải Giùn bất kỳ.

![alt tag](https://c7.staticflickr.com/6/5751/30210777150_24c87889e4_b.jpg)

Chi bộ lưu ý, đoạn mã `// @include http://*/*` hoặc `//@match  http://*/*` giúp cài đặt các website sẽ được áp dụng, ở đây là toàn bộ các trang http.

Nếu chỉ muốn sử dụng tại Faceboook, hãy chuyển sang `// @include https://facebook.com/*` và xóa các dòng `@include` còn lại.

##Quán Bựa - An Hoàng Trung Tướng
 
 [Vietnamese writing problems: Chữ giùn cảitạo](http://an-hoang-trung-tuong-2014.blogspot.com/2016/07/vietnamese-writing-problems-chu-giun.html)
 
 [Comics: vietnamese new writing concept #4](http://an-hoang-trung-tuong-2014.blogspot.com/2016/09/comics-vietnamese-new-writing-concept-4.html)
#####Liu í
Tác giả không có bất cứ thông đồng, quan hệ nào với An Hoàng Trung Tướng hay bù đụi của gã.
