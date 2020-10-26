## Other Questions
<br/>

1. What Is Git SSH Key?
> - Let github knows we authorize the specific computer has permission to push code by gening and setting ssh key, one computer only need to authorize for one time.
> - Related Reference : [Git 版本控制筆記 - 使用 github 及 ssh 金鑰設定](https://blog.jaycetyle.com/2018/02/github-ssh/)

<br/>

2. What Is The Difference Between Git SSH And HTTPS?
> - SSH : When you want to push/pull code that you **DON'T** need to enter the id and password due to set up the SSH key already.
> - HTTPS : When you want to push/pull code that you need to enter the id and password.
> - Related Reference : [設定 Github SSH 金鑰 feat. Github SSH、HTTPS 的差異](https://ithelp.ithome.com.tw/articles/10205988)
<br/>

 3. What Is The Semantic Version?

| 3 | 2 | 6 | 
|---|---|---|
| Major | Minor | Patch  |

> - The semantic version is `consist of Major, Minor and Patch`.
> - **Add Major** : it means add new function and it **IS NOT** downward compatibility, mahor number add one, minor and patch number change to 0.
> - **Add Minor** : it means add new function and it **IS** downward compatibility, minor number add one, patch number change to 0.
> - **Add Patch** : it means fixs the simple bugs, patch number add one.
> - Related Reference : [SemVer - 語意化版本規範](https://www.eebreakdown.com/2016/09/semver.html)

<br/>

 4. What Is CSRF?
<p align="center">
  <img src="img/csrf.png" alt="csrf" title="csrf">
</p>

> - Cross-Site Request Forgery (CSRF) is an attack that forces an end user to execute unwanted actions on a web application in which they’re currently authenticated.
> - If you login website A then visit a dangerous website B, and click the btn on website B, send a request to website A however website A's session or cookie doesn't expired, website A will accept the request from user then execute it.
> - Related Reference : [讓我們來談談 CSRF](https://blog.techbridge.cc/2017/02/25/csrf-introduction/), [常見攻擊：CSRF](https://yakimhsu.com/project/project_w12_Info_Security-CSRF.html)
<br/>

5. What Is CORS? (ref:4)

> -  `A request from the orgin domain is different from the target domain` which violate the same-origin policy, for the security, usually fobidden cross domain access to prevent CSRF.
> - `Cross Origin Resource Sharing` is a mechanism that allows : Get data from other domain outside our own domain. To be requested from another domain outside our own domain. There are three way to implement - Form Submit, JSONP and W3C - CORS

```
<? php
 
// Cross-Origin Resource Sharing Header
header('Access-Control-Allow-Origin: *');
header('Access-Control-Allow-Methods: GET, POST, PUT, DELETE, OPTIONS');
header('Access-Control-Allow-Headers: Origin, X-Requested-With, Content-Type, Accept');
 
?>
```

> - Related Reference : [什麼是CORS？](https://sibevin.github.io/posts/2017-06-05-101518-note-cors), [什麼是CORS](https://ithelp.ithome.com.tw/articles/10204004)
<br/>

6. What Is XSS?
> - Cross-Site Scripting (XSS) attack website through the website vulnerability by script.
> - Related Reference : [常見攻擊：XSS、SQL Injection
SQL Injection](https://yakimhsu.com/project/project_w12_Info_Security-XSS_SQL.html)
<br/>

7. What Is Cloud Computing?
> - The cloud(internet) computing is a way of `managing IT resources that replaces local machines and private data centers with virtual infrastructure`, including servers, storage, databases, networking, software, analytics. Users access virtual compute, network, and storage resources made available online by a remote provider. 
> - These resources can be provisioned instantly, which is particularly useful for companies that need to scale their infrastructure up or down quickly in response to fluctuating demand.
> - Related Reference : [徹底了解 Cloud Computing](https://www.ithome.com.tw/article/93006)
<br/>
