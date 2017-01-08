## html

+ 不要结束自结束元素，即编写 <br> ，而不是<br />。

  ```html
  <area>, <base>, <br>, <col>, <command>, <embed>, <hr>, <img>, <input>, <keygen>, <link>, <meta>, <param>, <source>, <track>, <wbr>,
  ```

  ​

+ 忽略样式表和脚本的类型属性。

  ```html
  不推荐:
  <link rel="stylesheet" href="css/style.css" type="text/css">
  ```

  ```html
  推荐：
  <link rel="stylesheet" href="css/style.css">
  ```

+ 在引用属性值时，使用双引号

  + ```html
    不推荐：
    <a href='login/' class='btn btn-secondary'>Login</a>
    推荐：
    <a href="login/" class="btn btn-secondary">Login</a>
    ```



## CSS

+ 在使用字体简写属性时，请注意，如果未注明字体的大小`font-size` 和系列 `font-family`，浏览器会忽略整个字体声明。

+ ```css
  去掉0值后面的单位。
  不推荐：
  margin: 0em;
  padding: 0px;
  推荐：
  margin: 0;
  padding: 0;

  ```

+ ```css
  CSS 引号
  Use double quotation marks for attribute selectors or property values. Do not use quotation marks in
  URI values (url()).
  属性选择符和属性值均需使用双引号，链接值（ url()）中不可使用双引号。
  不推荐：
  @import url("css/links.css");
  html {
  font-family: 'Open Sans', arial, sans-serif;
  }
  推荐：
  @import url(css/links.css);
  html {
  font-family: "Open Sans", arial, sans-serif;
  ```

+ meta viewport

  + ```css
    <meta name="viewport" content="width=device-with,initial-scale=1">
    ```

+ link

  ```css
  <link rel="stylesheet" media="screen and (min-width:500px)" href="over500.css">
  ```

+ calc

  ```css
  width: cal((100% - 10px) / 2)
  ```