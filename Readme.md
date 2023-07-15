# Assignment 8 - React

Q.1 What is React and its pros and cons?

Ans.1 React is a popular JavaScript library for building user interfaces. It allows developers to create reusable UI components and efficiently update the user interface when the underlying data changes. React follows a component-based architecture, where the UI is divided into small, self-contained components that manage their own state and can be composed to build complex user interfaces.

Pros of React:

1. **Component-Based Development**: React promotes a modular approach to building UIs, where the UI is divided into reusable components. This leads to better code organization, reusability, and maintainability.

2. **Virtual DOM**: React uses a virtual representation of the DOM, which is an in-memory representation of the UI. This allows React to efficiently update only the necessary parts of the UI when the data changes, resulting in better performance.

3. **One-Way Data Flow**: React follows a unidirectional data flow, where data flows from parent components to child components. This makes it easier to understand and debug the data flow in the application.

4. **Rich Ecosystem**: React has a large and active community, which has resulted in a rich ecosystem of libraries, tools, and resources. There are many third-party libraries available for common functionalities, making it easier to build complex applications.

5. **React Native**: React can be used to build not only web applications but also mobile applications using React Native. This allows developers to write code once and deploy it on multiple platforms, saving time and effort.

Cons of React:

1. **Steep Learning Curve**: React has a learning curve, especially for developers who are new to JavaScript frameworks or the concept of component-based development. Understanding the React ecosystem and best practices may take some time.

2. **Complexity**: As applications grow in size and complexity, managing state and data flow in React can become more challenging. Developers need to carefully design the component hierarchy and manage state to avoid performance and maintenance issues.

3. **Tooling Dependencies**: React development often requires additional tooling, such as build tools (Webpack, Babel), which may introduce complexity to the development setup and configuration.

4. **Lack of Opinionated Structure**: React is a library, not a full-fledged framework, which means it doesn't provide a predefined structure or conventions for organizing code. Developers need to make architectural decisions and choose additional libraries or patterns to build a complete application.

Overall, React provides a powerful and flexible way to build user interfaces, but it requires some initial learning and may introduce complexity as the application grows. However, the benefits of code reusability, performance optimizations, and a vibrant community make React a popular choice for many web developers.

---

Q.2 What do you understand by Virtual Dom?

Ans.2 The Virtual DOM (Document Object Model) is a concept used in the React library to optimize the updating process of the user interface. It is a lightweight copy or representation of the actual DOM tree that is present in the browser.

In React, when the state or data of a component changes, the Virtual DOM is updated rather than directly manipulating the actual DOM. The Virtual DOM is a tree-like structure that reflects the current state of the user interface. It consists of React elements, which are plain JavaScript objects representing the UI components.

When a change occurs in the application's data, React creates a new Virtual DOM by comparing it with the previous Virtual DOM. This process is known as reconciliation. React analyzes the differences between the previous and new Virtual DOM trees and determines the minimal number of changes required to update the actual DOM. This approach is more efficient than directly manipulating the entire DOM tree.

Once the minimal set of changes is identified, React applies these changes to the actual DOM, updating only the necessary parts of the UI. This process is known as DOM diffing and helps to improve the performance and efficiency of the application.

The Virtual DOM serves as an abstraction layer between the developer and the actual DOM, allowing React to optimize the rendering process by minimizing unnecessary updates. By utilizing the Virtual DOM, React can efficiently update the UI, provide a smooth user experience, and avoid unnecessary re-renders.

Overall, the Virtual DOM is a key concept in React that contributes to its performance optimizations and efficient rendering capabilities.

---

Q.3 Difference between Virtual Dom vs Real Dom?

Ans.3 The main difference between the Virtual DOM and the Real DOM (Document Object Model) lies in how they are structured and updated.

1. Structure:

   - Virtual DOM: The Virtual DOM is a lightweight copy or representation of the actual DOM. It is a tree-like structure consisting of plain JavaScript objects that reflect the current state of the UI components.
   - Real DOM: The Real DOM is the actual tree-like structure that represents the HTML elements on a web page. It is created by the browser and directly interacts with the underlying web technologies.

2. Updating Process:

   - Virtual DOM: When a change occurs in the application's data, React creates a new Virtual DOM by comparing it with the previous Virtual DOM. It analyzes the differences between the previous and new Virtual DOM trees and determines the minimal number of changes required to update the actual DOM. Once the changes are identified, React applies them to the Real DOM, updating only the necessary parts of the UI.
   - Real DOM: Any change made to the Real DOM directly affects the underlying web technologies. If a change is made to a single element, the browser recalculates the layout and repaints the entire web page, which can be an expensive operation. Modifying the Real DOM directly for every change can result in slower rendering and performance issues.

3. Performance:

   - Virtual DOM: The Virtual DOM allows React to optimize the rendering process by minimizing unnecessary updates. It performs diffing, which means it compares the previous and new Virtual DOM trees to identify the minimal set of changes needed. This approach significantly reduces the number of operations required to update the Real DOM, resulting in improved performance.
   - Real DOM: Modifying the Real DOM directly can be inefficient and time-consuming, especially when dealing with complex and frequently changing UIs. The browser needs to recalculate the layout and repaint the entire page even for small changes, which can impact performance, especially in large-scale applications.

4. Developer Experience:
   - Virtual DOM: The Virtual DOM provides a more developer-friendly experience by abstracting away the complexities of directly manipulating the Real DOM. Developers can work with the Virtual DOM, which is a more lightweight and efficient representation, allowing for easier development and debugging.
   - Real DOM: Manipulating the Real DOM requires more low-level operations and can be error-prone. It involves directly accessing and modifying elements, attributes, and styles, which can be challenging, especially in large applications.

In summary, the Virtual DOM acts as a lightweight and optimized representation of the Real DOM, allowing for efficient updates and better performance. It simplifies the development process and provides a smoother user experience.

---

Q.4 What are components in react? Types of component in react?

Ans.4 In React, components are the building blocks of the user interface. They are reusable and self-contained pieces of code that encapsulate a specific functionality or user interface element. Components allow developers to break down the UI into smaller, modular parts, making the code more manageable and reusable.

Types of components in React include:

1. Functional Components: Also known as Stateless Components, functional components are JavaScript functions that return JSX (JavaScript XML) to describe the UI. They are simpler, easier to write, and recommended for most use cases.

2. Class Components: Class components are JavaScript classes that extend the `React.Component` class. They have more features and capabilities than functional components, including the ability to have state and lifecycle methods.

3. Higher-Order Components (HOC): Higher-order components are functions that take a component as input and return an enhanced component with additional functionality. They enable code reuse and allow for cross-cutting concerns to be added to multiple components.

4. Functional Hooks-based Components: With the introduction of React Hooks, functional components can now manage state and lifecycle using built-in hooks like useState, useEffect, and more. Hooks-based components offer a simpler and more concise way to write components.

These different types of components provide flexibility and options for structuring and organizing React applications. The choice of component type depends on the specific requirements and complexity of the application.

---

Q.5 Difference between class & function based component?

Ans.5 The main difference between class-based and function-based components in React is the syntax and the features they offer.

Class-based components:

- Written as JavaScript classes that extend the `React.Component` class.
- Use the `render()` method to return JSX (JavaScript XML) to describe the UI.
- Have access to lifecycle methods such as `componentDidMount`, `componentDidUpdate`, etc., which allow for managing component state and performing side effects.
- Can have local component state using the `this.state` property.
- Can define custom methods within the class.
- Use the `this` keyword to access props and state.

Function-based components:

- Written as JavaScript functions.
- Use the function's return value to return JSX to describe the UI.
- Introduced with the introduction of React Hooks and the `useState` hook, which allows for managing component state within functional components.
- Can use other hooks such as `useEffect`, `useContext`, etc., to manage lifecycle and state in a functional way.
- Can be simpler and more concise compared to class-based components.
- Typically, do not have local component state, but can use the `useState` hook to create local state.
- Cannot define custom methods directly within the function, but can use JavaScript functions or helper functions as needed.

In summary, class-based components provide access to lifecycle methods, have local state, and offer more traditional object-oriented programming syntax. Function-based components, on the other hand, are simpler, more lightweight, and rely on hooks for managing state and lifecycle. With the introduction of React Hooks, function-based components have gained popularity and are now the recommended approach for most use cases.

---

Q.6 Explain react component life cycle ?

Ans. React component lifecycle refers to the various stages or phases that a React component goes through during its existence. Each stage provides hooks or methods that allow you to perform specific actions or implement certain behavior at different points in the component's lifecycle.

The React component lifecycle can be divided into three main phases:

1. Mounting:

   - `constructor`: Called when a component is being initialized.
   - `render`: Responsible for rendering the component's JSX markup.
   - `componentDidMount`: Invoked after the component is rendered and inserted into the DOM. Used for initialization, data fetching, or setting up event listeners.

2. Updating:

   - `componentDidUpdate`: Called after the component's updates are flushed to the DOM. Used for handling state or prop changes and performing side effects.
   - `shouldComponentUpdate`: Determines whether the component should re-render or not based on changes in state or props.
   - `render`: Re-renders the component with updated state or props.

3. Unmounting:
   - `componentWillUnmount`: Invoked before a component is removed from the DOM. Used for cleanup tasks such as removing event listeners or cancelling timers.

In addition to these main phases, React provides other lifecycle methods that allow for more fine-grained control and customization, such as `componentDidCatch`, which handles errors within the component, and `getDerivedStateFromProps`, which updates the component's state based on changes in props.

It's important to note that with the introduction of React Hooks, the class-based component lifecycle methods are being gradually phased out in favor of the `useEffect` hook and other hooks provided by React. Hooks provide a more concise and flexible way to handle state, side effects, and lifecycle behavior in function-based components.

---

Q.7 Explain Prop Drilling in React & Ways to avoid it?

Ans.7 Prop drilling refers to the process of passing props from a parent component down through multiple levels of child components that do not actually need those props. It can lead to complex and messy code, as props have to be passed through intermediary components that have no use for them.

Ways to avoid prop drilling in React include:

1. Context API: Use the Context API to create a context at a higher level in the component tree and provide the necessary data to the components that need it. This way, you can access the data directly without the need to pass it through every intermediate component.

2. React Redux: Implement Redux, a state management library, to manage the state of your application globally. Redux provides a centralized store where components can access the required data without prop drilling.

3. React Query: Utilize React Query, a data fetching library, to handle remote data fetching and caching. React Query manages the data globally and provides hooks to access the data without the need for prop drilling.

These approaches help in avoiding prop drilling and make the code cleaner, more maintainable, and less prone to errors.

---

Q.8 Create a Counter Web App using React

- Develop a web application using React that functions as a counter.
- Include two buttons in the UI:
  1. "Increment" button:
     - On clicking this button, the counter value should be incremented by one.
  2. "Decrement" button:
     - On clicking this button, the counter value should be decremented by one.
- Implement the counter logic using React's state management.
- Ensure that the counter value is displayed in the UI and updates in real-time when incremented or decremented.
- Use appropriate React components and hooks to manage the counter state and handle button click events.

Ans. 8 [Source Code Link](https://github.com/yashPundhir/Counter_App_Assignment)

---

**Q.9** Develop a **GitHub User Finder** web application using **React** The application should allow users to enter a **GitHub username** and display relevant information about the user, including their avatar and name. The design of the application should follow the layout provided in the image below.

- Use Github Api to get User Data “https://api.github.com/users”

Ans.9 [Source Code Link](https://github.com/yashPundhir/GitHub_User_Finder)

---

**Q.10** Develop a simple website using React, fetch and display products from the "https://fakestoreapi.com/products" API. The website should have the following features:

- Fetch product data from the "https://fakestoreapi.com/products" API.
- Display the products in a user-friendly UI.
- Show **Three products** in a single row for optimal visibility and layout.
- Use **React** to achieve the desired layout and functionality.
- Ensure that the UI is visually appealing and responsive.
- Implement error handling to handle any issues with API requests.
- Test the website thoroughly to ensure proper functionality and performance.
- Provide clear and concise documentation to guide users on how to interact with the website and understand its features.

**Note**: Refer to the provided image or design specification for the desired layout and styling of the product display in a single row.

Ans.10 [Source Code Link](https://github.com/yashPundhir/E-Comm_Landing_Page)

---
