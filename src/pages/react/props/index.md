---
title: Props
---
### What are the props?
Props (short for properties) are the data passed into the component. They are immutable (read-only).

For example lets define some props that have some data about a person and pass it to a component:  
```javascript
const props = {
    name: "john",
    age: 33,
    country: "Canada"
};

const Test = (props) => {
  return(
    <div
        name={props.name}
        age={props.age}
        country={props.country}>
        Content Here
        <ul>
          <li>name={props.name}</li>
          <li>age={props.age}</li>
          <li>country={props.country}</li>
        </ul>
    </div>
  );
};

ReactDOM.render(
    <div>
        <Test {...props}/>
        <hr/>
        <Test 
            name={props.name}
            age={props.age}
            country={props.country}
        />
    </div>
    , mountNode
);
```
Here we define props, pass them as inputs into a component and then render (or display) the component with its props.
