---
title: React Form Note
date: 2019-09-11 00:12:29
tags: React
---

## Forms

#### Controlled Components
In React, **this.state** or **state of component** is the ***single source of truth***, which takes all mutable state, and only can be changed by using **setState()** function.

**Controlled Components** stands for that react component not only render a form but also controls what happend when user input.
```javascript
    <input type='text' value={this.state.formValue} onChange={this.change}/>
```
the Value are displied as the value from state, and when user is inputting, **change()** runs to update **this.state**, meamwhile **value** will be updated as well. 
```javascript
    chnage(event){
        this.setState({
            this.state.formValue: event.target.value
        })
    }
```


### Different Types of Form Tag

#### The textarea Tag
