## React Questions
<br/>

1. What Is React.js ?
> - React is a front-end JavaScript library for building user interfaces which developed by Facebook, now Instagram, Netflix, Whatsapp, Uber, Dropbox, IMDB and Reddit, etc. also use React.js 
> - Build a huge website which includes complicated events and status change instead of buliding a simple web.<br /><br/>
> - Related Reference : [What is React?](https://www.simplilearn.com/what-is-react-article)
<br/>

1.2 What Is Features Of React.js ?
> - Only the View of MVC.
> - JSX.
> - Virtual DOM.
> - Uni-directional data flow.
> - Components based.
<br/>

1.3 What Is Strength And Weakness Of React.js ?
> - **Strength** : 
> - Ensures faster rendering with virtual DOM, which compares the components’ previous states and updates only the items in the Real DOM that were changed, instead of updating all of the components again. 
> - It follows the component based approach which helps in building reusable UI components.
> - Uni-directional data flow make it becomes easier to debug errors and know where a problem occurs in an application at the moment in question. And even small changes made to the child structures will not affect their parents, that makes code stable.
> - SEO friendly, React can run on the server, rendering and returning the virtual DOM to the browser as a regular webpage.
> - Can be used for the development of both web and mobile apps
> - Server-side rendering accelerates loads of starting page because users do not need to wait for JavaScript loadings before viewing web sites.
> - Useful developer toolset.
> - Strong community support.
<br/>

> - **Weakness** : 
> - React focus on view, lacking of route, ajax, async promise, etc.
> - Coding gets complex as it uses inline templating and JSX.

<br/>

❗ 2. What Is The Differences Between Vue.js, Angular.js and React.js ?

| TOPIC | React | Vue | Angular |
|---|---|---|---|
| Architecture | Only the View of MVC |  | Complete MVC |
| Rendering | Server-side rendering |  | Client-side rendering |
| DOM | virtual DOM | virtual DOM | Uses real DOM |
| Data Binding | One-way data binding |  | Two-way data binding |
| Author | Facebook | Former google employee | Google |
| When Use | | |  |

> - Related Reference : [Angular vs React vs Vue](https://levelup.gitconnected.com/angular-vs-react-vs-vue-which-is-the-best-choice-for-2020-81f577697c7e)

<br/>

3. What Is JSX ?
> - JSX stands for JavaScript XML.
> - JSX is not JavaScript nor HTML, is an XML/HTML like extension to JavaScript.
> - JSX as a syntax sugar for calling React.createElement().
> - Instead of putting JavaScript into HTML, JSX allows us to put HTML into JavaScript, then Babel will transform these expressions into actual JavaScript code. 
> - Examples : <br/>
 (1) Return one element https://jsfiddle.net/yschen25/29xrnmtw/ <br/>
 (2) Self-closing tags https://jsfiddle.net/yschen25/8g0w7thy/ <br/>
 (3) Comments https://jsfiddle.net/yschen25/c9uwgox1/ <br/>
 (4) Js in JSX https://jsfiddle.net/yschen25/knrg7ydm/ <br/>
 (5) Ternary operator https://jsfiddle.net/yschen25/L9o6ymcg/ <br/>
 (6) CamelCase https://jsfiddle.net/yschen25/x2n3oc8y/11/ <br/>
<br/><br/>

3.1 Why Can’t Browsers Read JSX?
> - Browsers can only read JavaScript objects but JSX in not a regular JavaScript object. Thus to enable a browser to read JSX, first, we need to transform JSX file into a JavaScript object using JSX transformers like Babel and then pass it to the browser.
<br/><br/>

4. What Is Virtual DOM ?

<p align="center">
<img src="img/virtual_DOM2.jpg" alt="virtual DOM" title="virtual DOM" width="70%">
<img src="img/virtual_DOM1.png" alt="virtual DOM" title="virtual DOM" width="55%">
</p>

> - If a developer uses JSX to manipulate and update its DOM, React JS creates something called a Virtual DOM. The Virtual DOM is a copy of the site’s DOM, and React JS uses this copy to see what parts of the actual DOM need to change when an event happens.

> - If you’re not using React JS (and JSX), your website will use HTML to update its DOM. This works fine for simple, static websites, but for dynamic websites that involve heavy user interaction it can become a problem, since the entire DOM needs to reload every time the user clicks a feature calling for a page refresh.

<br/>

5. What Is Functional Components(Stateless Component) And Class Components (Stateful Components) ?

> - **Functional Components** :
> - These components have no state of their own and only contain a render method, so they are also called stateless components. They may derive data from other components as props (properties).
> - Example : https://jsfiddle.net/yschen25/dmacrpjq/
<br/>

> - **Class Components** :
> - These components can hold and manage their state and have a separate render method for returning JSX on the screen. They are also called stateful components, as they can have a state.
> - Constructor is optional, add the constructor when you need to use state or binfd function. In this example, this.props works fine even without constructor, Example : https://jsfiddle.net/yschen25/2jcgbom0/
> - Related Reference : [有無加上constructor的差異](https://github.com/kdchang/reactjs101/issues/28)
<br/><br/>


5.2 What Is The Difference Between Functional Components And Class Components ?

|  Functional Components | Class Components |
|---|---|
| Calculates the internal state of the components | Stores info about component’s state change in memory |
| Do not have the authority to change state | Have authority to change state |
| Contains no knowledge of past, current and possible future state changes | Contains the knowledge of past, current and possible future changes in state |
| They receive the props from the Stateful components and treat them as callback functions | Stateless components notify them about the requirement of the state change, then they send down the props to them |

<br/>

5.3 When Use Functional Components And Class Components ?

> - **Functional Components** : 
> - Don't need to use lifecycle
> - Don't need to use state
> - Create reusable components
> - Only render UI
<br/>

> - **Class Components** :
> - Need to use lifecycle
> - Need to use state
> - Have to receive data form user
> - Create interactive objects
> - Render after change state

<br/>

6. What Is Props ?
> - Props is the shorthand for Properties. props data is read-only, which means that data coming from the parent should not be changed by child components.
> - They are always passed down from the parent to the child components in a uni-directional flow, a child component can never send a prop back to the parent component.
> - Props form the parent to the child components will cause child components re-render.
> - When your applications have a massive quantity of nested components it will may causes props hell (wrapper hell).
> - Examples : <br/>
    (1) Pass props via Functional Component (notice : use props.data) https://jsfiddle.net/yschen25/0e5udb1x/ <br/>
    (2) Pass props via Class Component (notice : use this.props.data) https://jsfiddle.net/yschen25/3vhqL8bn/
<br/><br/>

6.1 When Use Props ?
> - To pass data & event handlers down to your child components.
<br/><br/>

6.2 What Is PropTypes And DefaultProps ?
> - PropTypes : A typechecking tool to make sure the data is valid, propTypes is only checked in development mode, Example : https://jsfiddle.net/yschen25/oahjbq81/.
> - DefaultProps : You can define default values for props by assigning defaultProps, Example : https://jsfiddle.net/yschen25/763g8Lqv/.
<br/><br/>

6.3 How To Solve Props Hell (Wrapper Hell) ?
> - Redux.
> - Functional components + hook. 

<br/>

7. What Is State ?
> - The state is a data structure that starts with a default value when a Component mounts.
> - A component’s state can change over time; whenever it changes, the component re-renders. The change in state can happen as a response to user action or system-generated events, and these changes determine the behavior of the component and how it will render.  
> - Example : https://jsfiddle.net/yschen25/wc1qapz2/14/
<br/>

7.1 When Use State ?
> - To store the data your current page needs in your controller-view.
<br/><br/>

7.2 How To Change State ?
> - State of a component can be updated using this.setState().
> - setState is asynchronous.
> - Example : https://jsfiddle.net/yschen25/a2cmdb04/
<br/><br/>

7.3 What Is The Difference Between Props And Status ?

|  Conditions | State | Props |
|---|---|---|
| | Internal | External |
| | Mutable | Immutable |
| | Can be modified using setState() method | Can't not be modified |
| | Starts with a default value which is generally updated by event handlers | Passed as attributes from parent component to child component |
| (ref:8)| Can only be used with Class Components | Can be used with both Class as well as Functional Components |

<br/>

8. When And Why Should We Bind The Function ?
```
Example : Using class function (bind is required in constructor)

constructor(props) {
    		super(props);
      this.state = {count : 0};
      this.addCount = this.addCount.bind(this);
}

addCount() {
  this.setState({
      count : this.state.count + 1
  });
}
```
> - When you define a component using an ES6 class, a common pattern is for an event handler to be a method on the class. In JavaScript, class methods are not bound by default. If you forget to bind this.someEventHandler and pass it to onChange, this will be undefined when the function is actually called.
> - This is a way of saving the current value of this, which is in scope during the call to the constructor, so that it can be used later when the function is called.
> - Bind creates a new function that will force the this inside the function to be the parameter passed to bind().
> - When you need to access props, state or other members on the class, then you would need to bind it.
> - There are another way to handel ```this``` : Bind in Render (ref : 8.1), Arrow Function (ref : 8.2)
> - Related Reference : [why do you need to bind a function in a constructor
](https://stackoverflow.com/questions/38334062/why-do-you-need-to-bind-a-function-in-a-constructor), [Why and when do we need to bind functions and eventHandlers in React?](https://stackoverflow.com/questions/41113798/why-and-when-do-we-need-to-bind-functions-and-eventhandlers-in-react), [What is the use of the JavaScript 'bind' method?](https://stackoverflow.com/questions/2236747/what-is-the-use-of-the-javascript-bind-method), [進入Component的事件處理篇](https://ithelp.ithome.com.tw/articles/10200941), [React Binding Patterns: 5 Approaches for Handling `this`](https://www.freecodecamp.org/news/react-binding-patterns-5-approaches-for-handling-this-92c651b5af56/?source=post_page---------------------------)
<br/><br/>

8.1 Why Should We Bind The Function In Render ?

```
Example : Using bind in render (bind in required)

addCount() {
  this.setState({
      count : this.state.count + 1
  });
};
  
  render() {
    		return(
        		<div>
        		  <button onClick={this.addCount.bind(this)}>Click Me!</button>
              <h1>{this.state.count}</h1>
        		</div>
        )
    }
```
<br/>


8.2 Why We Don't Need Bind Arrow Function ?

```
Example : Using arrow function (No bind in required)

addCount = () => {
  this.setState({
     count : this.state.count + 1
  });
```
> - Arrow function does not have the following in its context : this, arguments, super and new.target. So when you reference this inside an arrow function it treat this as any other variable and look for its declaration in its scope first and it can not find it so it search the upper scope which is the this referring to the react component class which what is required so we do not need to bind the this to the class.
> - Related Reference : [Why we don't need to bind the arrow function in React?](https://stackoverflow.com/questions/52979915/why-we-dont-need-to-bind-the-arrow-function-in-react)
<br/><br/>


❗ 9. Explain The Life Cycle Of React.js (componentdidmount)
<br/><br/>

❗ 10. Axios
<br/><br/>

❗ 11. Flux
> - Flux is an architectural pattern which enforces the uni-directional data flow. It controls derived data and enables communication between multiple components using a central Store which has authority for all data. Any update in data throughout the application must occur here only. Flux provides stability to the application and reduces run-time errors.
<br/><br/>

❗ 12. Redux
> - It is a predictable state container for JavaScript applications and is used for the entire applications state management.
> - Related Reference : [Redex 核心概念筆記](https://note.pcwu.net/2017/03/04/redux-intro/), [Redux 入門](https://www.twblogs.net/a/5bb2a4c02b71770e645e017b)
<br/><br/>

❗ 12.1 What Are The Three Principles That Redux Follows?
> - Single source of truth: The state of the entire application is stored in an object/ state tree within a single store. The single state tree makes it easier to keep track of changes over time and debug or inspect the application.
 > - State is read-only: The only way to change the state is to trigger an action. An action is a plain JS object describing the change. Just like state is the minimal representation of data, the action is the minimal representation of the change to that data. 
 > - Changes are made with pure functions: In order to specify how the state tree is transformed by actions, you need pure functions. Pure functions are those whose return value depends solely on the values of their arguments.
<br/><br/>

❗ 12.2 List Down The Components Of Redux.

> - Action – It’s an object that describes what happened.
> - Reducer –  It is a place to determine how the state will change.
> - Store – State/ Object tree of the entire application is saved in the Store.
<br/><br/>

❗ 12.3 Show How The Data Flows Through Redux ?
<p align="center">
<img src="img/redux_data_flow.png" alt="redux_data_flow" title="redux_data_flow" width="70%">
</p>
<br/><br/>

❗ 12.4 What Are The advantages of Redux?

> - Predictability of outcome – Since there is always one source of truth, i.e. the store, there is no confusion about how to sync the current state with actions and other parts of the application.
> - Maintainability – The code becomes easier to maintain with a predictable outcome and strict structure.
> - Server-side rendering – You just need to pass the store created on the server, to the client side. This is very useful for initial render and provides a better user experience as it optimizes the application performance.
> - Developer tools – From actions to state changes, developers can track everything going on in the application in real time.
Community and ecosystem – Redux has a huge community behind it which makes it even more captivating to use. A large community of talented individuals contribute to the betterment of the library and develop various applications with it.
> - Ease of testing – Redux’s code is mostly functions which are small, pure and isolated. This makes the code testable and independent.
> - Organization – Redux is precise about how code should be organized, this makes the code more consistent and easier when a team works with it.

❗ 12.5 What is Redux Different From Flux?

| Flux | Redux |
|---|---|
| The Store contains state and change logic	| Store and change logic are separate |
| There are multiple stores | There is only one store |
| All the stores are disconnected and flat | Single store with hierarchical reducers |
| Has singleton dispatcher | No concept of dispatcher |
| React components subscribe to the store | Container components utilize connect |
| State is mutable | State is immutable |
<br/><br/>

13. What Is Styled Component ?
> - Styled Components is a CSS-in-JS library that enables you to create React components with a given style very easily.
> - It also allows you to use React.js props that we can pass to components in styled-components to create dynamic styling for our app.
> - Related Reference : [Styled-component](https://ithelp.ithome.com.tw/articles/10215800)
<br/><br/>

14. What Is Jest?
> - A delightful JavaScript Testing Framework which acts as a test runner, assertion library, and mocking library.

<br/>

14.1 What Is Enzyme?
> - Enzyme adds some great additional utility methods for rendering a component (or multiple components), finding elements, and interacting with elements.
> - Not support function components + hook so far.
> - Related Reference : [Jest | 經過測試，讓你的組件安全有把關 shallow render 篇 - feat.React, Enzyme](https://medium.com/enjoy-life-enjoy-coding/jest-%E7%B6%93%E9%81%8E%E6%B8%AC%E8%A9%A6-%E8%AE%93%E4%BD%A0%E7%9A%84%E7%B5%84%E4%BB%B6%E5%AE%89%E5%85%A8%E6%9C%89%E6%8A%8A%E9%97%9C-shallow-render-%E7%AF%87-feat-react-enzyme-be5ebbdf54a1)
<br/><br/>

14.2 Jest And Enzyme.
> - Both Jest and Enzyme are specifically designed to test React applications, Jest can be used with any other Javascript app but Enzyme only works with React.
> - Jest can be used without Enzyme to render components and test with snapshots, Enzyme simply adds additional functionality.
> - Enzyme can be used without Jest, however Enzyme must be paired with another test runner if Jest is not used.
> - Related Reference : [Testing React with Jest and Enzyme](https://medium.com/codeclan/testing-react-with-jest-and-enzyme-20505fec4675)
<br/><br/>

14.3 React-testing-library
> - React Testing Library is not an alternative to Jest, because they need each other and every one of them has a clear task, but it's a alternative to Enzyme.
> - Install @testing-library/react-hooks to test hooks.
<br/><br/>

❗ 15. Refs
> - Refs is the short hand for References in React. It is an attribute which helps to store a reference to a particular React element or component, which will be returned by the components render configuration function. It is used to return references to a particular element or component returned by render(). They come in handy when we need DOM measurements or to add methods to the components.
<br/><br/>

16. How To Use Arrow Function In The Class Components? (ref : 8)
> - Install @babel/plugin-proposal-class-properties then we can use arrow function and don't need to bind this.
> - Related Reference : [React | 那個在 Class Component 中的 Arrow function ](https://medium.com/enjoy-life-enjoy-coding/react-%E9%82%A3%E5%80%8B%E5%9C%A8-class-component-%E4%B8%AD%E7%9A%84-arrow-function-%E7%AE%AD%E9%A0%AD%E5%87%BD%E5%BC%8F-b5fa02db94a1)
<br/><br/>

❗ 17. Explain What Is Hook And How To Use It (State Hook, Effect Hook, Customized Hook) ?
> - Related Reference : [使用 State Hook](https://zh-hant.reactjs.org/docs/hooks-state.html), [Hook 概觀](https://zh-hant.reactjs.org/docs/hooks-overview.html), [React | 為了與 Hooks 相遇 - Function Components 升級記](https://medium.com/enjoy-life-enjoy-coding/react-%E7%82%BA%E4%BA%86%E8%88%87-hooks-%E7%9B%B8%E9%81%87-function-components-%E5%8D%87%E7%B4%9A%E8%A8%98-86869d869a45), [React 16.7 的 Hooks 為何讓人眼睛一亮](https://blog.yoctol.com/react-16-7-%E7%9A%84-hooks-%E7%82%BA%E4%BD%95%E8%AE%93%E4%BA%BA%E7%9C%BC%E7%9D%9B%E4%B8%80%E4%BA%AE-17796bd4e63d)
<br/><br/>

❗ 18. What Are Higher Order Components(HOC) ?
<br/><br/>

❗ 19. What are Pure Components ? 
<br/><br/>

20. What Is The Difference Between React And React Native ?
> - ReactJS is a JavaScript library, supporting both front-end web and being run on a server, for building user interfaces and web applications. It follows the concept of reusable components.
> - React Native is a mobile framework that makes use of JavaScript engine available on the host, allowing you to build mobile applications for different platforms (iOS, Android, and Windows Mobile) in JavaScript that allows you to use ReactJS to build reusable components and communicate with native components.
> - Both are open-sourced by Facebook follow the JSX syntax extension to JavaScript. Which compiles to React.createElement calls under the hood.
<br/><br/>

21. Uncontrolled Components And Controlled Components
<br/><br/>

22. Why Do I Need Keys In React Lists ?
> - Keys help React identify which items have changed, are added, or are removed.
> - React recommends that you do not use indexes as keys, since it could impact performance negatively and could lead to some unstable component behaviour.
> - React does not automatically pass they key like a prop. If you wanted to use the key for some computation, you would need to pass it as another prop, like the example below.
```
const content = posts.map((post) =>
  <Post
    key={post.id}
    id={post.id}
    title={post.title} />
);
```
> - Related Reference : [Why do I need Keys in React Lists?
](https://medium.com/@adhithiravi/why-do-i-need-keys-in-react-lists-dbb522188bbb), [List key 的使用](https://note.pcwu.net/2017/03/23/react-array-key/)
<br/><br/>

22.1 What are some exceptions where it is safe to use index as key?
> - If your list is static (no additions/re-ordering/removal to the list).
> - The list will never be re-ordered.
> - The list will not be filtered (adding/removing items from the list).
> - There are no ids for the items in the list.
<br/><br/>



https://www.edureka.co/blog/interview-questions/react-interview-questions/
