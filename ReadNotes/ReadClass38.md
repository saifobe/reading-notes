# React

## React-Lists&Keys
- Lists are a common way to display a collection of similar data.
- React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.
- When you run a loop to create elements, you should assign a key to each element.
- Keys help React identify which items have changed, are added, or are removed.
- Keys should be given to the elements inside the array to give the elements a stable identity.
- Keys used within arrays should be unique among their siblings. However they don’t need to be globally unique. 
- Keys serve as a hint to React but they don’t get passed to your components. If you need the same value in your component, pass it explicitly as a prop with a different name.
- You can pass an array into the JSX using curly braces {}.
- You can build collections of elements and include them in JSX using curly braces {}.
- Each list item needs a unique key.

Example:
```js
const numbers = [1, 2, 3, 4, 5];
const listItems = numbers.map((number) =>
  <li>{number}</li>
);
```
- In the example above, the map() method is called on the numbers array.
- The map() method creates a new array populated with the results of calling a provided function on every element in the calling array.
- For each item in the array, a <li> element is returned.
- Finally, the returned array of elements is assigned to listItems.


- A good rule of thumb is that elements inside the map() call need keys.
- Keys used within arrays should be unique among their siblings. However they don’t need to be globally unique.
- Keys serve as a hint to React but they don’t get passed to your components. If you need the same value in your component, pass it explicitly as a prop with a different name.
- Keys do not need to be globally unique; they only need to be unique between components and their siblings.

Example:
```js
const todoItems = todos.map((todo) =>
  <li key={todo.id}>
    {todo.text}
  </li>
);
```
-In the example above, the todo.id is used as the list item’s key.
- When you don’t have stable IDs for rendered items, you may use the item index as a key as a last resort.
- We don’t recommend using indexes for keys if the order of items may change. This can negatively impact performance and may cause issues with component state.
- If you extract list items as a separate component, you should keep the key on the <ListItem /> elements in the array rather than on the <li> element in the ListItem itself.

Example:
```js
function ListItem(props) {
  // Correct! There is no need to specify the key here:
  return <li>{props.value}</li>;
}

function NumberList(props) {
  const numbers = props.numbers;
  const listItems = numbers.map((number) =>
    // Correct! Key should be specified inside the array.
    <ListItem key={number.toString()}
              value={number} />

  );
  return (
    <ul>
      {listItems}
    </ul>
  );
}
```

## React-Forms
- HTML form elements work a little bit differently from other DOM elements in React, because form elements naturally keep some internal state.
- In HTML, form elements such as <input>, <textarea>, and <select> typically maintain their own state and update it based on user input.
- In React, mutable state is typically kept in the state property of components, and only updated with setState().
- We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input.
- An input form element whose value is controlled by React in this way is called a “controlled component”.

Example:
```js
class NameForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {value: ''};
  }
```
- In the example above, we used the JavaScript class syntax to define a React component called NameForm.


## React-Lifting State 
- Often, several components need to reflect the same changing data. We recommend lifting the shared state up to their closest common ancestor.
- There should be a single “source of truth” for any data that changes in a React application.
- Usually, the state is first added to the component that needs it for rendering. Then, if other components also need it, you can lift it up to their closest common ancestor.
- Instead of trying to sync the state between different components, you should rely on the top-down data flow.
- Lifting state involves writing more “boilerplate” code than two-way binding approaches, but as a benefit, it takes less work to find and isolate bugs.
- Since any state “lives” in some component and that component alone can change it, the surface area for bugs is greatly reduced. Additionally, you can implement any custom logic to reject or transform user input.
- If something can be derived from either props or state, it probably shouldn’t be in the state. For example, instead of storing both celsiusValue and fahrenheitValue, we store just the last edited temperature and its scale.

Example:
```js
function BoilingVerdict(props) {
  if (props.celsius >= 100) {
    return <p>The water would boil.</p>;
  }
  return <p>The water would not boil.</p>;
}
```
- In the example above, we create a BoilingVerdict component that accepts the celsius temperature as a prop, and prints whether it is enough to boil the water.
- We will store the current temperature in the Calculator component’s state, and pass it to the BoilingVerdict.
- We can now change the Calculator to render the BoilingVerdict instead of the temperature itself.

Example:
```js
class Calculator extends React.Component {
  constructor(props) {
    super(props);
    this.handleChange = this.handleChange.bind(this);
    this.state = {temperature: ''};
  }

  handleChange(e) {
    this.setState({temperature: e.target.value});
  }

  render() {
    const temperature = this.state.temperature;
    return (
      <fieldset>
        <legend>Enter temperature in Celsius:</legend>
        <input
          value={temperature}
          onChange={this.handleChange} />
        <BoilingVerdict
          celsius={parseFloat(temperature)} />
      </fieldset>
    );
  }
}
```