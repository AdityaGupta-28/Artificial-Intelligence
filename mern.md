## Mern 
MERN is a full-stack JavaScript technology stack used to build web applications.

It consists of four technologies:
1. MongoDB: NoSQL database used to store application data in document format.
2. Express.js: Backend framework for Node.js used to build APIs and handle HTTP requests.
3. React.js: Frontend JavaScript library used to build interactive user interfaces.
4. Node.js: JavaScript runtime used to execute JavaScript on the server.

### Topic 2: REST API
1. What is an API?
An API (Application Programming Interface) allows two software applications to communicate with each other.

For example, in your e-Governance chatbot, the React frontend communicates with the Node.js backend through APIs to retrieve government scheme information.

2. What is a REST API?
A REST API is an API that follows REST (Representational State Transfer) architectural principles. It uses HTTP methods to perform operations on resources.


### Topic 3: Middleware in Express.js
1. What is middleware?
Middleware is a function in Express.js that executes during the request-response cycle. It has access to the request object (req), response object (res), and the next() function.

It is commonly used for:
- Authentication and authorization.
- Logging requests.
- Validating input.
- Handling errors.
- Parsing JSON request bodies.

### 4. Types of middleware
1. Application-level middleware
2. Router-level middleware
3. Built-in middleware
4. Third-party middleware
5. Error-handling middleware

### Topic 4: Authentication and Authorization in MERN

1. What is authentication?
Authentication is the process of verifying the identity of a user.

2. What is authorization?
Authorization determines what an authenticated user is allowed to access or perform.

3. What is JWT?
JWT (JSON Web Token) is a compact token format used to securely transfer information between parties.
It is commonly used for user authentication in web applications.


4. Structure of JWT
A JWT contains three parts:
Header.Payload.Signature
- Header: Contains token type and signing algorithm.
- Payload: Contains claims such as user ID and role.
- Signature: Verifies token integrity and authenticity.
Important: JWT payloads are encoded, not encrypted by default. Never store passwords or sensitive secrets inside them.


###         $$######      React  ##################
3. What are Props?
Props (properties) are used to pass data from a parent component to a child component.
Important: Props are read-only inside the receiving component.




1. What is React.js?
React is an open-source JavaScript library developed by Meta for building interactive and dynamic user interfaces.
It follows a component-based architecture, where an application is divided into smaller, reusable components.


Important features:
- Component-based: UI is divided into independent, reusable components.
- Declarative: We describe what the UI should look like, and React manages the updates.
- Virtual DOM: React uses an in-memory representation of the UI to determine necessary DOM changes.
- One-way data flow: Data generally flows from parent components to child components through props.
- Hooks: Allow functional components to use state and other React features.

What is SPA?
A Single Page Application loads a single HTML page and dynamically updates its content without reloading the entire page for every navigation.

2. What is JSX?
JSX stands for JavaScript XML. It is a syntax extension for JavaScript that allows us to write HTML-like code inside JavaScript.
React uses JSX to describe how the UI should appear.

3. What are Components in React?
Components are independent and reusable building blocks of a React application.
They help divide a large user interface into smaller, manageable parts.

There are two commonly discussed types:
1. Functional Components
JavaScript functions that return React elements. They can use Hooks to manage state and other React features.

2. Class Components
ES6 classes that extend React.Component and use a render() method to return UI.


4. What are Props?
It is read only data Props (properties) are used to pass data from a parent component to a child component.
They make components reusable because the same component can display different information depending on the props received.

5. What is State in React?
State is data managed within a component that can change over time.

When state changes, React schedules a re-render so the UI can display the updated data.
React provides the useState Hook to manage state in functional components.

What are React Hooks?
Hooks are special React functions that allow functional components to use features such as state, context, references and effects.


A. useState- useState is a Hook used to add and manage state in functional components.

B. useEffect lets us run code when a component renders or when specific state or props change.

#### Dependency array:
Syntax          	        When the effect runs
No dependency array	        After every committed render
[]	                        After initial mount
[count]	                    After mount and when count changes
Generally used with useEffect


C. useContext-  useContext allows components to access shared data without passing props manually through multiple intermediate components.



9. What is Virtual DOM?
The Virtual DOM is a lightweight JavaScript representation of the UI.
React uses it to determine which changes need to be applied to the browser's actual DOM.

How it works:
1. React renders the component and creates a UI representation.
2. When props or state change, React renders the updated component.
3. React compares the new result with the previous one through reconciliation.
4. React commits the necessary changes to the actual DOM.
Example: If a counter changes from 5 to 6, React determines that the displayed counter value needs updating rather than requiring you to manually rebuild the entire page.


10. What is Reconciliation?
Reconciliation is the process React uses to compare the previous and new rendered UI trees to determine what changes are needed.
React uses this process to update the UI efficiently.


12. Component Communication
React supports different ways for components to communicate.

Parent to Child: Through props.

Child to Parent: Through callback functions passed from parent to child.

Sibling to Sibling: Through shared state in their common parent or Context API.


What is Prop Drilling?
Prop drilling means passing data through multiple intermediate components just to reach a deeply nested child component.

Solution: Context API or state management libraries such as Redux.

What is Context API?
Context API is a React feature that allows components to share data without manually passing props through every intermediate component.




##### NODE JS 
What is Callback Hell?

Callback Hell occurs when multiple nested callbacks make code difficult to read, maintain and debug.
It can often be avoided using Promises and async/await.

What are Promises?
A Promise is a JavaScript object representing the eventual completion or failure of an asynchronous operation.

It has three states:
1. Pending – Operation is still in progress.
2. Fulfilled – Operation completed successfully.
3. Rejected – Operation failed.

What is Express.js?
Express.js is a lightweight and flexible web application framework built on top of Node.js. It simplifies backend development by providing features for routing, middleware, handling HTTP requests and creating REST APIs.

