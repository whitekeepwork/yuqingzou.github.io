---
title: Note for React (1)
date: 2019-07-31 23:11:16
tags: React 
---

## JSX
#### When specifiying the react element type
1. React must be in scope
Always remeber to import react and required component
``` javascript
    import React from 'react'
    import Customerone from './Customerone'
```
As long as we want to use JSX, the **React** library must be imported

2. Using Dot Notation for JSX Type
If in a module file, mutiple React components are exported, we can use **Modulename.ComponentName** to choose the one component.
``` javascript
    return(<Modulename.ComponentName />)
```

3. User-Defined Component Must Be Capitalized
Any element type that starts with lowercase letter refers to a **built-in component**. Everytime naming components with a capital letter, both for function based and class based component
```javascript
    // user definded component should be capitalized
    function App (){}

    class App extends React.Component{}
    export default App
```

4. Choosing the Type at Runtime
Gneral expression can not be used as React element type. if you want it, need as it to a capitalized variable first. (used when render a differne t component basd on a prop)
```javascript
    //wrong way
    function Story(props) {
    // Wrong! JSX type can't be an expression.
    return <components[props.storyType] story={props.story} />;
    }

    //right way
    function Story(props) {
    // Correct! JSX type can be a capitalized variable.
        const SpecificStory = components[props.storyType];
    return <SpecificStory story={props.story} />;
        }
    }
```
reference link [here][https://reactjs.org/docs/jsx-in-depth.html]
 