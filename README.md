[![](https://img.shields.io/badge/NACG_CJanGe-HttpAttack-yellow)](http://github.com/NACG-Mohr/CJan-Ge)
<h1 align="center">HttpAttack</h1>
基于JavaScript ，利用HTTP触发事件扫描用户HTTP请求，并建黑白名单来进行溯源。找到攻击者，解决网站被攻击后还不知道是怎么死的尴尬局面。使用 `Javascript` 实现前端防御 `http劫持` 及防御 `XSS攻击`，并且对可疑攻击进行上报。

## Usage

引入 `httphijack1.0.0.js` 。

```HTML
<script type="text/javascript" src='./httphijack1.0.0.js'></script>

<script>
        window.httphijack.init();
</script>   
```
## Features：

- 所有内联 on* 事件执行的代码
- a标签 href 属性 `javascript:` 内嵌的代码
- 静态脚本、`iframe` 等恶意内容
- 动态添加的脚本文件、`iframe` 等恶意内容
- `document-write`添加的内容
- 页面被 `iframe` 嵌套劫持 

## Tips:

建立自己的域名白名单、关键字黑名单、上报系统及接收后端。

防御 `XSS` 及 `http劫持`，更多的还是得依靠升级 `https` 和 `CSP/CSP2(内容安全策略)` 等非 `JavaScript` 技术，高明的攻击者可以绕过任何 `JavaScript` 防护。

> 组件未在生产环境使用，使用了很多 HTML5 才支持的 API，仅供学习交流。