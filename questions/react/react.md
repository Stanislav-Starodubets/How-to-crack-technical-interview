# React Interview Questions & Answers

### Table of Contents

| No.  | Questions                                                                                           | Priority |
|------|-----------------------------------------------------------------------------------------------------|----------|
|      | **Core React**                                                                                      |          |
| 1    | What is React?                                                                                      | HIGH     |
|      | A JavaScript library for building user interfaces. React is a tool for building UI components                                                                                             |          |
| 2    | What are the major features of React?                                                               | HIGH     |
|      | -Virtual DOM. This characteristic of React helps to speed up the app development process and offers flexibility.<br/> -JavaScript XML or JSX.<br/> -React Native.<br/> -One-Way Data Binding.<br/> -Declarative UI.<br/> -Component Based Architecture.<br/> -Short Learning Curve.<br/> -Enables Building Rich UI.                                                                                              |          |
| 3    | What is JSX?                                                                                        | HIGH     |
|      | JSX is a JavaScript Extension Syntax used in React to easily write HTML and JavaScript together                                                                                              |          |
| 3.1  | Is it possible to use react without JSX?                                                            | HIGH     |
|      | React doesn’t require using JSX                                                                                              |          |
| 4    | What is the difference between Element and Component?                                               | HIGH     |
|      | `React Element:` It is the basic building block in a react application, it is an object representation of a virtual DOM node. React Element contains both type and property. It may contain other Elements in its props. React Element does not have any methods, making it light and faster to render than components. <br/> `React Component:` It is independent and reusable. It returns the virtual DOM of the element. One may or may not pass any parameter while creating a component. A component can be further described into functional components and class components. <br/><br/>`React Element:`<br/> - An element is always gets returned by a component.	<br/> - The element does not have any methods.	<br/> - A React element is an object representation of a DOM node.	<br/> - Elements are immutable i,e once created cannot be changed.	<br/> - An element can be created using React.createElement( ) with type property.	<br/> - We cannot use React Hooks with elements as elements are immutable.	<br/> - Elements are light, stateless and hence it is faster.	<br/><br/> `React Component:`<br/> - A component can be functional or a class that optionally takes input and returns an element.<br/> - Each component has its life cycle methods.<br/> - A component encapsulates a DOM tree.<br/> - The state in a component is mutable.<br/> - A component can be declared in different ways like it can be an element class with render() method or can be defined as a function.<br/> - React hooks can be used with only functional components<br/> - It is comparatively slower than elements.<br/>                                                                                          |          |
| 5    | How to create components in React?                                                                  | HIGH     |
|      | When creating a React component, the component's name MUST start with an upper case letter.  A class component must include the extends React.Component statement. This statement creates an inheritance to React.Component, and gives your component access to React.Component's functions.  The component also requires a render() method, this method returns HTML. A Function component also returns HTML, and behaves much the same way as a Class component, but Function components can be written using much less code, are easier to understand                                                                                         |          |
| 6    | When to use a Class Component over a Function Component?                                            | LOW      |
| 7    | What are Pure Components?                                                                           | MEDIUM   |
| 7.1  | If Pure Component is better from the optimization point of view, why don't we use it by default?(#) | MEDIUM   |
| 8    | What is state in React?                                                                             | HIGH     |
|      | State is a plain JavaScript object used by React to represent an information about the component’s current situation.It’s managed in the component                                                                                              |          |
| 9    | What are props in React?                                                                            | HIGH     |
|      | Props stand for "Properties." They are read-only components. It is an object which stores the value of attributes of a tag and work similar to the HTML attributes. It gives a way to pass data from one component to other components. It is similar to function arguments. Props are passed to the component in the same way as arguments passed in a function.                                                                                              |          |
| 10   | What is the difference between state and props?                                                     | HIGH     |
|      | `PROPS`: <br/> - The Data is passed from one component to another. <br/> - It is Immutable (cannot be modified).	<br/> - Props can be used with state and functional components.	<br/> - Props are read-only.	<br/> `STATE`<br/> - The Data is passed within the component only.<br/> - It is Mutable (can be modified).<br/> -  State can be used only with the state components/class component (Before 16.0).<br/> -  State is both read and write.                                                                                         |          |
| 11   | Why should we not update the state directly?                                                        | HIGH     |
|      | React, keeps a track record of all its virtual DOM. Whenever a change happens, all the components are rendered and this new virtual DOM is then compared with the old virtual DOM. Only the differences found are then reflected in the original DOM.So, it’s obvious from the statement that if we mutate the state directly, it will change the reference of the state in the previous virtual DOM as well.                                                                                              |          |
| 11.1 | Is the state updated synchronously?                                                                 | HIGH     |
|      | after React 18 all setStates are executed asynchronously in batches.                                                                                              |          |
| 12   | What is the purpose of callback function as an argument of setState()?                              | MEDIUM   |
|      | The setState function takes an optional callback parameter that can be used to make updates after the state is changed. This function will get called once the state has been updated, and the callback will receive the updated value of the state.                                                                                              |          |
| 13   | What is the difference between HTML and React event handling?                                       | LOW      |
| 14   | How to bind methods or event handlers in JSX callbacks?                                             | HIGH     |
|      | - Binding Event Handler in Render Method: We can bind the handler when it is called in the render method using bind() method. <br/> - Binding Event Handler using Arrow Function: This is pretty much the same approach as above, however, in this approach we are binding the event handler implicitly. This approach is the best if you want to pass parameters to your event. <br/> - Binding Event Handler in the Constructor: In this approach, we are going to bind the event handler inside the constructor. This is also the approach that is mentioned in ReactJS documentation. This has performance benefits as the events aren’t binding every time the method is called<br/> - Binding Event Handler using Arrow Function as a Class Property: This is probably the best way to bind the events and still pass in parameters to the event handlers easily.                                                                                           |          |
| 15   | How to pass a parameter to an event handler or callback?                                            | HIGH     |
|      | - You can use an arrow function to wrap around an event handler and pass parameters <br/> `<button onClick={() => this.handleClick(id)} />`<br/> - This is an equivalent to calling .bind: `<button onClick={this.handleClick.bind(this, id)} />`<br/> - you can also pass arguments to a function which is defined as arrow function `<button onClick={this.handleClick(id)} />;`<br/>`handleClick = (id) => () => {`<br/>`  `&nbsp;&nbsp;&nbsp;&nbsp;`console.log('Hello, your ticket number is', id);`<br/>`};`                                                                                            |          |
| 16   | What are synthetic events in React?                                                                 | HIGH     |
|      | synthetic event - is a cross-browser object. It is made with a wrapper around the actual event of the browser.  The react event handling system is known as Synthetic Events. The synthetic event is a cross-browser wrapper of the browser's native event. Handling events with react have some syntactic differences from handling events on DOM. These are: React events are named as camelCase instead of lowercase. The synthetic events are different from, and do not map directly to, the browser's native events. synthetic event,                                                                                             |          |
| 17   | What are inline conditional expressions?                                                            | MEDIUM   |
| 18   | What is "key" prop and what is the benefit of using it in arrays of elements?                       | HIGH     |
|      | A key is a special string attribute you should include when creating arrays of elements. Key prop helps React identify which items have changed, are added, or are removed.                                                                                              |          |
| 19   | What is the use of refs?                                                                            | HIGH     |
|      | Refs are a function provided by React to access the DOM element and the React element that you might have created on your own. They are used in cases where we want to change the value of a child component, without making use of props and all.                                                                                              |          |
| 20   | How to create refs?                                                                                 | HIGH     |
|      | You can create a ref by calling React. createRef() and attaching a React element to it using the ref attribute on the element. We can “refer” to the node of the ref created in the render method with access to the current attribute of the ref.                                                                                              |          |
| 20.1 | Difference between "createRef" and "useRef"(#)                                                      | MEDIUM   |
|      | useRef: The useRef is a hook that uses the same ref throughout. It saves its value between re-renders in a functional component and doesn't create a new instance of the ref for every re-render. It persists the existing ref between re-renders. createRef: The createRef is a function that creates a new ref every time.                                                                                              |          |
| 21   | What are forward refs?                                                                              | MEDIUM   |
| 22   | React.memo VS useMemo                                                                               | HIGH     |
|      | `React.memo` is for when you find an existing component that is expensive to render, and you don't have the option to optimize it internally. Just wrap it and let React do an extra check. `React.useMemo` is for internally optimizing a component by saving the return value of an expensive function call.                                                                                              |          |
| 23   | How do you memoize a component?                                                                     | HIGH     |
|      | Since React v16.6.0, we have a React.memo. It provides a higher order component which memoizes component unless the props change. To use it, simply wrap the component using React.memo before you use it.                                                                                              |          |
| 24   | What is Virtual DOM?                                                                                | HIGH     |
|      | Virtual DOM in React is a “virtual” representation of the actual DOM. It is nothing but an object created to replicate the actual DOM. Unlike the actual DOM, the virtual DOM is cheap to create because it doesn’t write to the screen. It is only available as a strategy to prevent a redraw of unnecessary page elements during re-render.                                                                                              |          |
| 25   | How Virtual DOM works?                                                                              | HIGH     |
|      | In summary, here’s what happens when you try to update the DOM in React:<br/><br/>The entire virtual DOM gets updated.:<br/> - The virtual DOM gets compared to what it looked like before you updated it. React figures out which objects have changed.:<br/> - The changed objects, and the changed objects only, get updated on the real DOM.:<br/> - Changes on the real DOM cause the screen to change.                                                                                              |          |
| 26   | What is the difference between Shadow DOM and Virtual DOM?                                          | HIGH     |
|      | In short, the shadow DOM is a browser technology whose main objective is to provide encapsulation when creating elements. On the other hand, the virtual DOM is managed by JavaScript libraries—e.g., React—and it's mostly a strategy to optimize performance.                                                                                              |          |
| 27   | What is React Fiber?                                                                                | HIGH     |
|      | React Fiber is a concept of ReactJS that is used to render a system faster and smoother. React Fiber: A fiber in a react is just a plain JavaScript object with some properties. The current react reconciler, the fiber reconciler is named after this object and is the default reconciler since react version 16. React fiber is a complete rewrite of react that fixes a few long-standing issues and offers incredible and offers opportunities heading into the future.                                                                                               |          |
| 28   | What is the main goal of React Fiber?                                                               | HIGH     |
|      | Fiber focuses on animations and responsiveness. It has the ability to split work into chunks and prioritize tasks. We can pause work and come back to it later. We can also reuse previously completed work or maybe abort it if it is not needed. As opposed to the old React reconciler, it is asynchronous.                                                                                              |          |
| 29   | What are controlled components?                                                                     | MEDIUM   |
| 30   | What are uncontrolled components?                                                                   | MEDIUM   |
| 30.1 | Controlled Uncontrolled VS Uncontrolled inputs.                                                     | MEDIUM   |
| 31   | What is the difference between createElement and cloneElement?                                      | LOW      |
| 32   | What is Lifting State Up in React?                                                                  | HIGH     |
|      | sharing state is accomplished by moving it up to the closest common ancestor of the components that need it. This is called “lifting state up”.                                                                                              |          |
| 33   | What are the different phases of component lifecycle?                                               | HIGH     |
|      | Lifecycle methods: In ReactJS, the development of each component involves the use of different lifecycle methods. All the lifecycle methods used to create such components, together constitute the component’s lifecycle. They are defined as a series of functions invoked in various stages of a component. Each phase of the lifecycle components includes some specific lifecycle methods related to that particular phase. There are primarily 4 phases involved in the lifecycle of a reactive component, as follows.<br/><br/> - Initializing<br/> - Mounting<br/> - Updating<br/> - Unmounting                                                                                              |          |
| 34   | What are the lifecycle methods of React?                                                            | HIGH     |
|      | `Mounting lifecycle methods`<br/>constructor()<br/>static getDerivedStateFromProps()<br/>render()<br/>componentDidMount()<br/>`Updating lifecycle methods`<br/>static getDerivedStateFromProps()<br/>shouldComponentUpdate()<br/>render()<br/>getSnapshotBeforeUpdate()<br/>componentDidUpdate()<br/>`Unmounting lifecycle method`<br/>componentWillUnmount<br/>`Error handling lifecycle methods`<br/>static getDerivedStateFromError()<br/>componentDidCatch()                                                                                              |          |
| 35   | What are Higher-Order components?                                                                   | HIGH     |
|      | A higher-order component (HOC) is an advanced element for reusing logic in React components. Components take one or more components as arguments, and return a new upgraded component. Sounds familiar, right? They are similar to higher-order functions, which take some functions as an argument and produce a new function.                                                                                              |          |
| 36   | How to fetch data with React Hooks?                                                                 | HIGH     |
|      |  - useEffect makes fetching data easier<br/> - Always provide a cleanup function to useEffect, to avoid running on every render.<br/> - useEffect can't be async, use an async function inside useEffect                                                                                              |          |
| 37   | What is context?                                                                                    | HIGH     |
|      | Context lets you “broadcast” such data, and changes to it, to all components below. React Context is a method to pass props from parent to child component(s), by storing the props in a store(similar in Redux) and using these props from the store by child component(s) without actually passing them manually at each level of the component tree.                                                                                             |          |
| 38   | What is children prop?                                                                              | HIGH     |
|      | children is a special prop, automatically passed to every component, that can be used to render the content included between the opening and closing tags when invoking a component.                                                                                               |          |
| 39   | What is prop drilling?                                                                              | MEDIUM   |
|      | Prop drilling is a situation where data is passed from one component through multiple interdependent components until you get to the component where the data is needed                                                                                              |          |
| 40   | What is the purpose of using super constructor with props argument?                                 | LOW      |
|      | Super() function calls the constructor of the parent class. Using super constructor with props arguments basically allows accessing this. props in a Constructor function.                                                                                              |          |
| 41   | What is reconciliation?                                                                             | HIGH     |
|      | The mechanism to diff one tree with another to determine which parts need to be changed and then update the original DOM with it is called Reconciliation.                                                                                              |          |
| 42   | How do you conditionally render components?                                                         | HIGH     |
|      |  - 1. Using an if…else Statement <br/> - 2. Using a switch Statement<br/> - Using Element Variables<br/> - 4. Using Ternary Operators<br/> - 5. Using Logical && (Short Circuit Evaluation)<br/> - 6. Using Immediately Invoked Function Expressions (IIFEs)<br/> - 7. Using Enhanced JSX Libraries                                                                                              |          |
| 43   | What are error boundaries in React v16                                                              | HIGH     |
|      | Error boundaries are React components that catch JavaScript errors anywhere in their child component tree, log those errors, and display a fallback UI instead of the component tree that crashed.                                                                                              |          |
| 44   | What are hooks?                                                                                     | HIGH     |
|      | Hooks are JavaScript functions that manage the state's behaviour and side effects by isolating them from a component.                                                                                              |          |
| 44.1 | React hooks rules                                                                                   | HIGH     |
|      | - Only Call Hooks at the Top Level<br/> -  Don’t call Hooks inside loops, conditions, or nested functions. <br/> - Only Call Hooks from React Functions <br/> - Don’t call Hooks from regular JavaScript functions.-                                                                                               |          |
| 45   | Why React uses className over class attribute?                                                      | LOW      |
| 46   | What are fragments?                                                                                 | HIGH     |
|      | A common pattern in React is for a component to return multiple elements. Fragments let you group a list of children without adding extra nodes to the DOM.                                                                                              |          |
| 47   | Why fragments are better than container divs?                                                       | HIGH     |
|      | Fragments let you group a list of children without adding extra nodes to the DOM.                                                                                              |          |
| 48   | What are portals in React?                                                                          | MEDIUM   |
| 49   | What are stateless components?                                                                      | MEDIUM   |
| 50   | What are stateful components?                                                                       | MEDIUM   |
|      | **React Redux**                                                                                     | HIGH     |
|      | answer                                                                                              |          |
| 51   | What is Flux?                                                                                       | HIGH     |
|      | answer                                                                                              |          |
| 52   | What is Redux?                                                                                      | HIGH     |
|      | answer                                                                                              |          |
| 52.1 | What hooks does Redux have                                                                          | HIGH     |
|      | answer                                                                                              |          |
| 53   | What are the core principles of Redux?                                                              | HIGH     |
|      | answer                                                                                              |          |
| 54   | What are the downsides of Redux compared to Flux?                                                   | HIGH     |
|      | answer                                                                                              |          |
| 56   | What is the difference between mapStateToProps() and mapDispatchToProps()?                          | LOW      |
| 57   | Can I dispatch an action in reducer?                                                                | HIGH     |
|      | answer                                                                                              |          |
| 58   | How to access Redux store outside a component?                                                      | HIGH     |
|      | answer                                                                                              |          |
| 59   | What are the drawbacks of MVW pattern                                                               | MEDIUM   |
| 60   | Are there any similarities between Redux and RxJS?                                                  | MEDIUM   |
| 61   | How to dispatch an action on load?                                                                  | MEDIUM   |
| 62   | How to use `connect` from React Redux?                                                              | MEDIUM   |
| 63   | How to reset state in Redux?                                                                        | MEDIUM   |
| 64   | Whats the purpose of at symbol in the redux connect decorator?                                      | LOW      |
| 65   | What is the difference between React context and React Redux?                                       | HIGH     |
|      | answer                                                                                              |          |
| 66   | Why are Redux state functions called reducers?                                                      | MEDIUM   |
| 67   | How to make AJAX request in Redux?                                                                  | MEDIUM   |
| 68   | Should I keep all component's state in Redux store?                                                 | HIGH     |
|      | answer                                                                                              |          |
| 69   | What is the proper way to access Redux store?                                                       | HIGH     |
|      | answer                                                                                              |          |
| 70   | What is the difference between component and container in React Redux?                              | MEDIUM   |
| 71   | What is the purpose of the constants in Redux?                                                      | HIGH     |
|      | answer                                                                                              |          |
| 72   | What are the different ways to write mapDispatchToProps()?                                          | MEDIUM   |
| 73   | What is the use of the ownProps parameter in mapStateToProps() and mapDispatchToProps()?            | MEDIUM   |
| 74   | How to structure Redux top level directories?                                                       | MEDIUM   |
| 75   | What is redux-saga?                                                                                 | LOW      |
| 76   | What is the mental model of redux-saga?                                                             | LOW      |
| 77   | What are the differences between call and put in redux-saga                                         | LOW      |
| 78   | What is Redux Thunk?                                                                                | MEDIUM   |
| 79   | What are the differences between redux-saga and redux-thunk                                         | LOW      |
| 80   | What is Redux DevTools?                                                                             | LOW      |
| 81   | What are the features of Redux DevTools?                                                            | LOW      |
| 82   | What are Redux selectors and Why to use them?                                                       | LOW      |
| 83   | What is Redux Form?                                                                                 | LOW      |
| 84   | What are the main features of Redux Form?                                                           | LOW      |
| 85   | How to add multiple middlewares to Redux?                                                           | LOW      |
| 86   | How to set initial state in Redux?                                                                  | MEDIUM   |
| 87   | How Relay is different from Redux?                                                                  | LOW      |
| 88   | What is an action in Redux?                                                                         | HIGH     |
|      | answer                                                                                              |          |
|      | **React Router**                                                                                    |          |
| 89   | What is React Router?                                                                               | HIGH     |
|      | answer                                                                                              |          |
| 90   | Why do we need to React Router?                                                                     | HIGH     |
|      | answer                                                                                              |          |
| 91   | What are the main benefits of using React Router?                                                   | HIGH     |
|      | answer                                                                                              |          |
| 92   | How is React routing different from conventional routing?                                           | HIGH     |
|      | answer                                                                                              |          |
| 93   | How React Router is different from history library?                                                 | MEDIUM   |
| 94   | What is the purpose of push and replace methods of history?                                         | MEDIUM   |
| 95   | How do you implement React routing?                                                                 | HIGH     |
|      | answer                                                                                              |          |
| 96   | What is the purpose of Outlet component?                                                            | HIGH     |
|      | answer                                                                                              |          |
| 97   | What is nested routing?                                                                             | HIGH     |
|      | answer                                                                                              |          |
| 98   | How to do nested routing?                                                                           | HIGH     |
|      | answer                                                                                              |          |
| 99   | How to suspense routing with route splitting?                                                       | LOW      |
| 100  | How to do redirect?                                                                                 | MEDIUM   |
| 101  | How to navigate backward and forward?                                                               | LOW      |
| 102  | How to create a protected (private) route?                                                          | HIGH     |
|      | answer                                                                                              |          |
| 103  | What are some ways that you can share data among routes in React Router?                            | LOW      |
| 104  | What are the differences between types of routing: Hash, Browser, Memory?                           | HIGH     |
|      | answer                                                                                              |          |
| 105  | How to get search params?                                                                           | MEDIUM   |
| 106  | How to implement default or NotFound page?                                                          | HIGH     |
|      | answer                                                                                              |          |
| 107  | What are the differences between v5 and v6?                                                         | MEDIUM   |
| 108  | Have you ever upgraded the major version of router? If yes, what issues you faced?                  | LOW      |

# WORKING IN PROGRESS...
![img.png](img.png)
