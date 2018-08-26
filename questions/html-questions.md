# HTML Questions:

* What does a `doctype` do?
始终将<！DOCTYPE>声明添加到HTML文档中，以便浏览器知道所期望的文档类型。
<！DOCTYPE>声明不是HTML标记; 它是Web浏览器关于页面编写的HTML版本的指令。
在HTML 4.01中，<！DOCTYPE>声明引用DTD，因为HTML 4.01基于SGML。DTD指定标记语言的规则，以便浏览器正确呈现内容。
HTML5不基于SGML，因此不需要引用DTD。

* How do you serve a page with content in multiple languages?
通过更改langhtml元素的属性。

* What kind of things must you be wary of when design or developing for multilingual sites?
根据不同受众的位置正确定位内容，并允许用户轻松更改其国家/语言。

* What are `data-` attributes good for?
将数据存储在HTML中以进行DOM解析或其他跟踪信息的方法。

* Consider HTML5 as an open web platform. What are the building blocks of HTML5?
<article>
<aside>
<audio>
<canvas>
<figcaption>
<figure>
<footer>
<header>
<hgroup>
<output>
<section>
<video>

* Describe the difference between a `cookie`, `sessionStorage` and `localStorage`.
cookie：
最大大小为4093字节
可以设置到期日期
每次请求都会发送
sessionStorage的：
最大大小为2.5MBs +取决于浏览器
存储在浏览器中，不会随每个请求一起发送
如果使用sessionStorage关闭选项卡，打开新选项卡或退出浏览器 - 您将丢失该特定的sessionStorage数据。
localStorage的：
最大大小为2.5MBs +取决于浏览器
存储在浏览器中，不会随每个请求一起发送
如果浏览器/标签关闭，它将持续存在。

* Describe the difference between `<script>`, `<script async>` and `<script defer>`.
常规<script>标记将阻止页面的呈现，并且在脚本完成之前页面将不会继续加载。
<script async>将以异步方式运行脚本，这意味着它不会阻止呈现，但会在脚本可用时立即运行。这通常用于CDN文件或其他此类文件，这些文件不会更改页面结构。
<script defer> 在页面完成解析之后和onload事件之前，将推迟脚本运行。

* Why is it generally a good idea to position CSS `<link>`s between `<head></head>` and JS `<script>`s just before `</body>`? Do you know any exceptions?
您通常将<link>标记放在两者之间<head>以防止Flash of Unstyled Content，这样可以在解析页面的其余部分时为用户提供一些内容。
由于Javascript默认阻止渲染，并且DOM和CSSOM构造也可以延迟，因此通常最好将脚本保留在页面底部。
例外情况是您异步获取脚本，或者至少将它们推迟到页面末尾。
  
* What is progressive rendering?


* Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute.
* Have you used different HTML templating languages before?
