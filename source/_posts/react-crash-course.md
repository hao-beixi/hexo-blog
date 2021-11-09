---
title: react crash course
date: 2021-10-29 13:29:34
tags:
---
https://www.youtube.com/watch?v=w7ejDZ8SWv8

# React Crash Course
Learn React by building a hands on project

## What Is React?
React is a library for building user interfaces

React runs on the client as a SPA (Single Page App), but can be used to build full stack apps by communicating with a server/API (eg. MERN stack)

React is often referred to as a front-end "framework" because it is capable and directly comparable to a framework such as Angular or Vue
## Why Would You Use React?
- Structure the "view" layer of your application
- Reusable components with their own state
- JSX - Dynamic markup
- Interactive UIs with Virtual DOM
- Performance & Testing
- Very popular in the industry
## What should you know first?
you should have a good handle on JavaScript.
I would not suggest jumping into React without learning JavaScript first

- data types, variables, functions, loops, etc
- promises & asynchronous programming
- array methods like forEach() & map()
- Fetch API & making HTTP requests
## UI components
when using React, think of your UI as a bunch of separate components
## Components: Functions vs. Classes
```
export const Header = () => {
    return {
        <div>
            <h1>My Header</h1>
        </div>
    }
}
```
```
export default class Header extends React.Component {
    render() {
        return (
            <div>
                <h1>My Header</h1>
            </div>
        )
    }
}
```
Components render/return JSX (JavaScript Syntax Extension)
Components can also takes in "props"
<Header title="My Title">
## Working With State
Components can have "state" which is an object that determines how a component renders and behaves

"App"  or "global" state refers to state that is available to the entire UI, not just a single component.

Prior to React 16.8, we had to use class based components to use state.
Now we can use functional components with hooks