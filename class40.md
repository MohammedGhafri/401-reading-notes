# React 3

 1. Installation

You can install React Router from the public npm registry with either npm or yarn.  `npm install react-router-dom`

2. React - Styling FAQ


- Can I use inline styles?
Yes, 

- Are inline styles bad?
CSS classes are generally better for performance than inline styles.

- What is CSS-in-JS?

“CSS-in-JS” refers to a pattern where CSS is composed using JavaScript instead of defined in external files.

Note that this functionality is not a part of React, but provided by third-party libraries. React does not have an opinion about how styles are defined; if in doubt, a good starting point is to define your styles in a separate *.css file as usual and refer to them using className.

Can I do animations in React?
React can be used to power animations. 


3. NextJs

o build a complete web application with React from scratch, there are many important details you need to consider:

- Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
- You need to do production optimizations such as code splitting.
- You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side rendering or client-side rendering.
- You might have to write some server-side code to connect your React app to your data store.

- A framework can solve these problems. But such a framework must have the right level of abstraction — otherwise it won’t be very useful. It also needs to have great "Developer Experience", ensuring you and your team have an amazing experience while writing code.



- Next.js: The React Framework
Enter Next.js, the React Framework. Next.js provides a solution to all of the above problems. But more importantly, it puts you and your team in the pit of success when building React applications.

Next.js has the best-in-class "Developer Experience" and many built-in features; a sample of them are:

* An intuitive page-based routing system (with support for dynamic routes)
* Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
* Automatic code splitting for faster page loads
* Client-side routing with optimized prefetching
* Built-in CSS and Sass support, and support for any CSS-in-JS library
* Development environment with Fast Refresh support
* API routes to build API endpoints with Serverless Functions
* Fully extendable
Next.js is used in tens of thousands of production-facing websites and web applications, including many of the world's largest brands.



[For more information](https://reactrouter.com/web/guides/quick-start)
[For more information](https://reactjs.org/docs/faq-styling.html)
[For more information](https://nextjs.org/learn/basics/create-nextjs-app)
