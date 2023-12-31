# New version React

---

## Install

Using **[npx create-react-app my-app]**, install create-react-app
Using **[npm start]** to run the code.

## Edit

1. index.js: The index.js file is the entry point to your React application. It primarily serves the following purposes.

```
1.1 Calling ReactDOM.render(): Renders React elements to the real DOM via the React DOM library's ReactDOM.render() function.

1.2 Render the <App /> component (a feature of App.js discussed below) inside a DOM element with an id of 'root' in index.html

1.3 Typically, this file imports the necessary components and libraries, and performs initialization tasks.
```

2. App.js: The App.js file is primarily used as the root component of an application

```
2.1 Define and export React components. They are typically written as class or functional components.

2.2 It primarily combines and organizes other components to create the layout and structure of the overall app. Within this file, other components are called and combined to create the UI.

2.3 Used in conjunction with React Router or another state management library, it can be responsible for things like routing configuration or state management for your app.
```

- Index.js is the entry point for rendering and launching your app, while App.js is responsible for defining and organizing the main components of your application. Both play an important role in a React application, and work together to make up the entire app.

## Deployment

An application run with **[npm start]** is a development application. It is good for development, but it is not suitable for use in a real service because it is large and contains such as unnecessary messages.

If so, can you create an efficient application for your service?

In the terminal, type **[npm run build]** to start the build command.

The **[npm run build]** command is typically used before deploying a React application. When you run it, it creates a set of static files that are optimized for the production environment.

**Key features:**

- Generate optimized builds: optimize and bundle source code to reduce size and improve performance. This is done by minimizing CSS, JavaScript, and image files and generating them in the build directory.

- Static file generation: During development with tools like **create-react-app**, there may be unused files or code. **[npm run build]** removes these unnecessary pieces and bundles the necessary files together.

- Apply environment settings: There are settings required for production that are different from development. For example, Source Maps are usually disabled in production builds.

- Generate deliverables: When the build is complete, a series of static files are generated. These files can be deployed to a web server to host your application, or uploaded to a CDN to make them accessible to users.

The output generated by the **[npm run build]** command is usually stored in the _build_ or _dist_ directory, which makes your app available for deployment. These built files are not the source code, but rather the version that will be delivered to end users, which is smaller in size and optimized for better performance.

**[npx serve -s build]**

The **[npx serve -s build]** command runs a simple local web server that serves the production-built files of your project. This allows you to test the production build of the application you're developing locally. After building that project, running this command will allow you to preview the application locally.

---

# Component

```
React is a technology for creating custom tags.
```

Do you agree with that?

In a way, yes, but the statement might need a bit of clarification. React is a JavaScript library primarily used for building user interfaces, specifically for web applications. It allows developers to create reusable UI components, which can indeed be thought of as custom tags in a sense.

These components can encapsulate various functionalities and represent specific parts of the UI. When you use React, you essentially create your own custom HTML elements or tags by defining these components. For example, you might create a Header, Button, or Card component, and then use them in your code as if they were HTML tags.

So, while React itself doesn't directly create HTML tags, it provides a way to build custom components that can be used similarly to HTML tags within your application, thereby allowing you to create your own reusable, custom elements to structure your UI.

**Simple webpage code for example**

```JavaScript
<div className="App">
    <header className="App-header">
        <h1>
            <a href="/">WEB</a>
        </h1>
    </header>
    <nav>
        <ol>
            <li>
                <a href="/read/1">HTML</a>
            </li>
            <li>
                <a href="/read/2">CSS</a>
            </li>
            <li>
                <a href="/read31">JavaScript</a>
            </li>
        </ol>
    </nav>
    <article>
        <h2>Welcom</h2>
        Hello, WEB
    </article>
</div>
```

This code has some HTML tags for organizing web pages. As you can see, it is not too long because it is simple code for example. By the wat, what if there are thousond of code lines for complicate web page? what about we need more pages? If so, the code will become more complex and unreadable.

_What do we need to do?_

> Create a custom tag, also known as **component**.

In React, a component is a fundamental building block used to create user interfaces. Components are reusable and self-contained pieces of code that encapsulate a part of the UI's functionality and appearance.

1. Functional Components: These are JavaScript functions that accept properties (props) as arguments and return React elements that describe the UI. They are typically used for simpler components.

2. Class Components: These are ES6 classes that extend the React.Component class. They include a render() method that returns the UI description. Class components have additional features like local state and lifecycle methods.

Components allow developers to create a modular and reusable UI. They can be composed together to form more complex UI structures. Each component can manage its own state (in the case of class components) or receive data through props to render UI based on that data.

```JavaScript
function Header() {
	return (
		<header className="App-header">
			<h1>
				<a href="/">WEB</a>
			</h1>
		</header>
	);
}
    ...

function App() {
	return (
			<Header></Header>
    ...
```
