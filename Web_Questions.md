## Web Questions
<br/>

:white_check_mark: 1. What Is The Difference Between Session, Cookie, Sessionstorage and Localstorage?

<table>
    <tr>
        <th>Type</th>
        <th>session</th>
        <th>cookie</th>
        <th>sessionStorage</th>
        <th>localStorage</th>
    </tr>
    <tr>
        <td>Storage location</td>
        <td>Server-side</td>
        <td>Client-side</td>
        <td>Client-side</td>
        <td>Client-side</td>
    </tr>
    <tr>
        <td>Maximum data size</td>
        <td>1024KB</td>
        <td>4K for one cookie, max 20 cookies for a website</td>
        <td>5M</td>
        <td>5M</td>
    </tr>
    <tr>
        <td>Expired Time</td>
        <td>If user doesn’t active for a long time which over expire time, the server-side will delete the session to
            save the space
        </td>
        <td><li>user can set expiration time for each cookies.</li> <li>It will expire after closing browser if it set on client-side
        </li></td>
        <td>The data clear automatically when the browser is closed</td>
        <td>The data <b>WILL NOT</b> be deleted when the browser is closed until user clear through JavaScript, browser cache /
            locally stored data
        </td>
    </tr>
    <tr>
        <td>Scope</td>
        <td>No</td>
        <td>Changes made are saved and available for all same-origin page</td>
        <td>Changes made are saved and available for the current page</td>
        <td>Changes made are saved and available for all same-origin page</td>
    </tr>
    <tr>
        <td>Security</td>
        <td>High</td>
        <td>Low</td>
        <td>Low</td>
        <td>Low</td>
    </tr>
    <tr>
        <td>Usability</td>
        <td>Easily to use</td>
        <td>The api is difficult to use</td>
        <td colspan="2">Has method setItem, getItem, removeItem, clear that easily to use</td>
    </tr>
    <tr>
        <td>HTTP Request</td>
        <td></td>
        <td>The data is sent back to the server for every HTTP request which cause performance problems</td>
        <td colspan="2">The data is <b>NOT</b> sent back to the server for every HTTP request</td>
    </tr>
    <tr>
        <td>Application</td>
        <td>Login</td>
        <td>Login, shopping cart, game scores</td>
        <td>Form</td>
        <td>Shopping cart</td>
    </tr>
</table>
<br/>

:white_check_mark: 2. How To Speed Up The Website?

> - Reduce the HTTP request : use sprite images, combine files...etc. <br/>
> - Use CDN. <br/>
> - Reduce redirects. <br/>
> - Delete unused code : remove spaces, commas, and other unnecessary characters. <br/>
> - Minify files : use gzip for file compression, to reduce the size of your CSS, HTML, and JavaScript files.
> - Defer lag file loading : ensure that the rest of your content can load without a delay. <br/>
> - Use asynchronous loading : the browser could continue loading other elements on the page at the same time. <br/>

> - Related Reference : [20 Ways to Speed Up Your Website](https://www.crazyegg.com/blog/speed-up-your-website/), [讓你的網頁加載時間降低到1s 內](https://www.jianshu.com/p/d857c3ff78d6)
<br/>

:white_check_mark: 3. Explain The Meaning Of HTTP Status Code 200, 400, 403, 404, 500, 502. 

> ① 200 : Request success. <br/>
> ② 400 : Syntax error -> The reason usually is programming error. <br/>
> ③ 403 : Not allow to visit. <br/>
> ④ 404 : Page not found. <br/>
> ⑤ 500 : Server error -> There are lots of possibilities : .htaccess document setting error, database setting error...etc <br/>
> ⑥ 502 : Bad gateway -> Wait and reload or find mis.
<br/>

:white_check_mark: 4. What Is NPM?

> - NPM is short for Node Package Manager, it is an online library for download open-source javaScript projects,
we can manage packages via NPM.
<br/>

:white_check_mark: 4.1 Why Use NPM?
> - For example if we want to use jQuery, we used to download jQuery or include jQuery CDN url, but how about we need to use a lots of packages? NPM is a tool to solve this time-consuming things.

> - Related Reference : [從零開始: 使用NPM套件](https://medium.com/html-test/從零開始-使用npm套件-317beefdf182)
<br/><br/>

:white_check_mark: 5. What Is Webpack?

> - There are lots of prepressors and frameworks, We may need to compile ES6, SCSS, webpack can help us compile preprocessors to the code which browser can understand then bundle it, we can also use webpack to minify or optimize code...etc., which makes work efficiently.

> - Related Reference : [什麼是Webpack?](https://medium.com/i-am-mike/什麼是webpack-你需要webpack嗎-2d8f9658241d), [關於 Webpack](https://neighborhood999.github.io/webpack-tutorial-gitbook/Part1/), [Webpack 初學者教學課程](https://neighborhood999.github.io/webpack-tutorial-gitbook/Part1/)
<br/><br/>

:white_check_mark: 6. What Is Graceful Degradation And Progressive Enhancement?

> - **Graceful Degradation** : Building the website so it provides a good level of user experience in **modern browsers first**, then fix the problem for other browsers 

> - **Progressive Enhancement** : Building the website to keep all functions work properly for **all the browsers**, then optimize the website to support the newer browser, let the basic functionality will work on older systems.

> - Use progressive enhancement will cost more time and manpower in the begging, but easily to maintain. Use graceful degradation can make website online quickly. Choose which to use it depends on the requirements.

> - Related Reference : [認識優雅降級與漸進增強](http://augus-blog.logdown.com/posts/143403-graceful-degradation-and-progressive-enhancement)
<br/><br/>

7. How The Browser Renders A Web Page? 

<br/>

8. What Is SPA?

> - SPA is short for single page application. 
One SPA is one web application, what it needs will loaded (HTML, CSS, JS) in one time request, to manipulate DOM don't need to refresh browser just JavaScript.
<br/>

> - Related Reference : [跟著小明一起搞懂技術名詞：MVC、SPA 與 SSR](https://medium.com/@hulitw/introduction-mvc-spa-and-ssr-545c941669e9)
<br/><br/>

8.1 What Is SPA's Strength And Weakness?

8.2 How To Solve The Problem?

> - Related Reference : [淺談SPA、SEO與SSR](https://juejin.im/entry/5bbbf852f265da0aea699497)

<br/>

:white_check_mark: 9. What Is PWA?

> - PWA is short of Progressive Web App, the purpose is to keep adventage of website and native app to make sure the user have best experience.
<br/>

:white_check_mark: 10. What Is Webview?

> -  Webview is hybrid(Native + Web) app or in-app browser, open a website in native app.
> - Related Reference : [Native, Hybrid, Web App, Cross App](https://medium.com/@milkmidi/native-hybrid-web-app-cross-app%E5%93%AA%E4%B8%80%E5%80%8B%E6%98%AF%E9%96%8B%E7%99%BCapp%E6%9C%80%E4%BD%B3%E6%96%B9%E6%A1%88%E5%91%A2-381e5529e47), [用 Line、FB 手機 APP 開啟網頁對前端工程師的困擾﹍JS 辨識內建瀏覽器(webview)的方法](https://www.wfublog.com/2018/06/mobile-detect-webview-fb-line-in-app.html)
<br/>

:white_check_mark: 11. What Is Gateway, API Gateway and API?

> - Gateway : a interface to receive and handle the request.
> - API Gateway : a service that makes it easy for developers to publish, maintain, monitor, secure, and operate APIs. 
> - API : a Application Programming Interface to let user manipulate to achieve what they want.
> - Related Reference : [Amazon API Gateway](https://aws.amazon.com/tw/api-gateway/features/), [什麼是 Amazon API Gateway？](https://docs.aws.amazon.com/zh_tw/apigateway/latest/developerguide/welcome.html)
<br/>

:white_check_mark: 12. What Is Rest API? 

> - Rest API also call Restful API, it's a  and isn't mandatory to use it. The purpose is make api easily to maintain and develop. 

```
https://localhost:8080/myweb/getDogs --> GET /rest/api/dogs get dogs 
https://localhost:8080/myweb/addDogs --> POST /rest/api/dogs add dog
https://localhost:8080/myweb/updateDogs/:dog_id --> PUT /rest/api/dogs/:dog_id modify a dog
https://localhost:8080/myweb/deleteDogs/:dog_id --> DELETE /rest/api/dogs/:dog_id delete a dog
```

> - Related Reference : [REST與RESTful](https://www.twblogs.net/a/5d404cf0bd9eee517423039c), [休息(REST)式架構](https://progressbar.tw/posts/53), [API 是什麼? RESTful API 又是什麼?](https://medium.com/itsems-frontend/api-%E6%98%AF%E4%BB%80%E9%BA%BC-restful-api-%E5%8F%88%E6%98%AF%E4%BB%80%E9%BA%BC-a001a85ab638), [RESTful Web API 設計指南](https://www.footmark.info/programming-language/design/restful-webapi-design-guide/), [簡明RESTful API設計要點](https://tw.twincl.com/programming/*641y)
<br/>

:white_check_mark: 12.1 What Is Strength And Weakness?

> - Strength : simple and uniform Interface, cachable
> - Weakness : need to create multiple requests to get complex data 
<br/>

:white_check_mark: 12.2 How To Solve The problem 11?

> - GraphQL allow using one entry point to get all data, doesn’t like restful api which needs to call multiple times to get enough data. And what your get is what you search, it also can reduce the requests.

```
Serach：

{
    user(uid:1) {
        uid
        name
    }
}
```

```
Get：

{
  "data": {
    "user": {
      "uid": "1",
      "name": "xxx"
    }
  }
}
```
> - Related Reference : [GraphQL和RESTful的比較](https://segmentfault.com/a/1190000012878342)
<br/>

:white_check_mark: 13. What Is Token?

> - Token likes a passport, after user enter the id and password, sever-side will generate a token for this user,
then the user will have permission to view or manipulate corresponding informations. There are a lots of way to generate token, such use Mac, sessionId, etc.

> - Related Reference : [Token令牌入門學習](https://codertw.com/%E7%A8%8B%E5%BC%8F%E8%AA%9E%E8%A8%80/35304/#outline__1_0_1), [簡單理解token機制](http://www.woshipm.com/pd/877760.html)

<br/>

:white_check_mark: 14. What Is Web Accessibility?

> - To ensure everyone includes disables can use the website's function working normally.
> - Use semantic element, properly tag, provide equivalent alternatives to image, audio and video, don't just use color to pass the information, consider about keyboard-only user.

> - Related Reference : [我們都應該了解的無障礙網頁概念](https://designtongue.me/website-accessibility/)
<br/>
