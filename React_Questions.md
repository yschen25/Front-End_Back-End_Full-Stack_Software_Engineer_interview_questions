## React Questions
<br/>

1. What Is React.js ?
> - React is a front-end JavaScript library developed by Facebook, now Instagram, Netflix, Whatsapp, Uber, Dropbox, IMDB and Reddit, etc. also use React.js 
> - It follows the component based approach which helps in building reusable UI components.
> - Build a huge website which includes complicated events and status change instead of buliding a simple web.<br /><br/>

1.2 What Is The Strength And Weakness Of React.js ?

> - **Strength** : 
> - Virtual DOM : Only repaint the changes by comparing the original DOM and virtual DOM, reduces manipulating DOM and enhance the website rendering performance.</br>
> - Components : Everythings in React is components, components enhence the readability and reausability, make website developing more effectively and time-saving.</br>
> - SEO : More friendly to SEO.
> - Server-side rendering.
> - Uni-directional data flow or data binding.
<br/>

> - **Weakness** : 
> - React is just a library, not a full-blown framework.
> - Coding gets complex as it uses inline templating and JSX.
<br/><br/>

1.3 How To Solve It ?

<br/><br/>

2. What Is The Differences Between Vue.js, Angular.js and React.js ?
<br/><br/>

3. What Is Function Components(Stateless Component) And Class Components (Stateful Components) ?
<br/><br/>

3.1 What Is Strength And Weakness Of Function Components And Class Components?

> - **Function Components** : 
> - **Strength** 
> - Easy to develop, read and test
> - Better performance

> - **Weakness** 

<br/>

> - **Class Components** : 
> - **Strength** 

> - **Weakness** 

<br/><br/>

3.2 What Is The Difference Between Function Components And Class Components ?
<br/><br/>

3.3 When Use Function Components And Class Components ?

> - **Function Components** : 
> - Don't need to use lifecycle
> - Don't need to use state
> - Create reusable components
<br/>

> - **Class Components** :
> - Need to use lifecycle
> - Need to use state
> - Have to receive data form user
> - Create interactive objects

<br/><br/>

4. What Is Props ?
> - Props is the shorthand for Properties in React. They are read-only components which must be kept pure i.e. immutable. They are always passed down from the parent to the child components throughout the application. A child component can never send a prop back to the parent component. This help in maintaining the unidirectional data flow and are generally used to render the dynamically generated data.
<br/><br/>

4.1 What Is Strength And Weakness Of Props ?
<br/><br/>

4.2 What Is PropTypes And DefaultProps ?
> - A typechecking tool to make sure the data is valid, propTypes is only checked in development mode.
> - You can define default values for props by assigning defaultProps.
<br/><br/>

5. What Is State ?
<br/><br/>

5.1 When Use State ?
<br/><br/>

5.2 How To Change State ?
> - State of a component can be updated using this.setState().
<br/><br/>

5.3 What Is The Difference Between Props And Status ?

|  Conditions | State | Props |
|---|---|---|
| Receive initial value from parent component | Yes | Yes |
| Parent component can change value | No | Yes |
| Set default values inside component | Yes | Yes |
| Changes inside component | Yes | No |
| Set initial value for child components | Yes | Yes |
| Changes inside child components | No | Yes |
<br/><br/>

6. When Should We Bind The Function?
> - Related Reference : [進入Component的事件處理篇](https://ithelp.ithome.com.tw/articles/10200941)
<br/><br/>

7. Explain The Life Cycle Of React.js (componentdidmount)
<br/><br/>

8. Axios
<br/><br/>

9. Flux
> - Flux is an architectural pattern which enforces the uni-directional data flow. It controls derived data and enables communication between multiple components using a central Store which has authority for all data. Any update in data throughout the application must occur here only. Flux provides stability to the application and reduces run-time errors.
<br/><br/>

10. Redux
> - It is a predictable state container for JavaScript applications and is used for the entire applications state management.
<br/><br/>

10.1 What Are The Three Principles That Redux Follows?
> - Single source of truth: The state of the entire application is stored in an object/ state tree within a single store. The single state tree makes it easier to keep track of changes over time and debug or inspect the application.
 > - State is read-only: The only way to change the state is to trigger an action. An action is a plain JS object describing the change. Just like state is the minimal representation of data, the action is the minimal representation of the change to that data. 
 > - Changes are made with pure functions: In order to specify how the state tree is transformed by actions, you need pure functions. Pure functions are those whose return value depends solely on the values of their arguments.
<br/><br/>

10.2 List Down The Components Of Redux.

> - Action – It’s an object that describes what happened.
> - Reducer –  It is a place to determine how the state will change.
> - Store – State/ Object tree of the entire application is saved in the Store.
> - View – Simply displays the data provided by the Store.
<br/><br/>

10.3 Show How The Data Flows Through Redux ?
<br/><br/>

10.4 What Are The advantages of Redux?

> - Predictability of outcome – Since there is always one source of truth, i.e. the store, there is no confusion about how to sync the current state with actions and other parts of the application.
> - Maintainability – The code becomes easier to maintain with a predictable outcome and strict structure.
> - Server-side rendering – You just need to pass the store created on the server, to the client side. This is very useful for initial render and provides a better user experience as it optimizes the application performance.
> - Developer tools – From actions to state changes, developers can track everything going on in the application in real time.
Community and ecosystem – Redux has a huge community behind it which makes it even more captivating to use. A large community of talented individuals contribute to the betterment of the library and develop various applications with it.
> - Ease of testing – Redux’s code is mostly functions which are small, pure and isolated. This makes the code testable and independent.
> - Organization – Redux is precise about how code should be organized, this makes the code more consistent and easier when a team works with it.

10.5 What is Redux Different From Flux?

<br/><br/>

11. Styled Component
<br/><br/>

12. Jest
<br/><br/>

12.1 Enzyme
<br/><br/>

12.2 React-testing-library
<br/><br/>

13. Refs
> - Refs is the short hand for References in React. It is an attribute which helps to store a reference to a particular React element or component, which will be returned by the components render configuration function. It is used to return references to a particular element or component returned by render(). They come in handy when we need DOM measurements or to add methods to the components.
<br/><br/>

14. How To Use Arrow Function In The Class Components?
> - Related Reference : [React | 那個在 Class Component 中的 Arrow function ](https://medium.com/enjoy-life-enjoy-coding/react-%E9%82%A3%E5%80%8B%E5%9C%A8-class-component-%E4%B8%AD%E7%9A%84-arrow-function-%E7%AE%AD%E9%A0%AD%E5%87%BD%E5%BC%8F-b5fa02db94a1)
<br/><br/>

15. Explain What Is Hook And How To Use It (State Hook, Effect Hook, Customized Hook) ?
> - Related Reference : [使用 State Hook](https://zh-hant.reactjs.org/docs/hooks-state.html), [Hook 概觀](https://zh-hant.reactjs.org/docs/hooks-overview.html), [React | 為了與 Hooks 相遇 - Function Components 升級記](https://medium.com/enjoy-life-enjoy-coding/react-%E7%82%BA%E4%BA%86%E8%88%87-hooks-%E7%9B%B8%E9%81%87-function-components-%E5%8D%87%E7%B4%9A%E8%A8%98-86869d869a45)
<br/><br/>

16. What Are Higher Order Components(HOC) ?
<br/><br/>

17. What are Pure Components ? 
<br/><br/>

https://www.edureka.co/blog/interview-questions/react-interview-questions/
