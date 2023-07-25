# React context

## What is React context?
- Context provides a way to pass data through the component tree without having to pass props down manually at every level.
- In a typical React application, data is passed top-down (parent to child) via props, but such usage can be cumbersome for certain types of props (e.g. locale preference, UI theme) that are required by many components within an application.

## When to use React context?
- Context is designed to share data that can be considered “global” for a tree of React components, such as the current authenticated user, theme, or preferred language.
- Context is primarily used when some data needs to be accessible by many components at different nesting levels.
- Apply it sparingly because it makes component reuse more difficult.

## How to use React context?
- Create a context object by calling React.createContext().
- Create a provider component by calling Context.Provider.
- Create a consumer component by calling Context.Consumer.
- The context object contains a Provider component that allows consuming components to subscribe to context changes.
- The Provider component accepts a value prop to be passed to consuming components that are descendants of this Provider.
- One Provider can be connected to many consumers. Providers can be nested to override values deeper within the tree.
- All consumers that are descendants of a Provider will re-render whenever the Provider’s value prop changes.

## Example
```js
// Create a context object
const ThemeContext = React.createContext('light');

// Create a provider component
let App = () => {
  return (
    <ThemeContext.Provider value="dark">
      <Toolbar />
    </ThemeContext.Provider>
  );
};

// Create a consumer component
let Toolbar = () => {
  return (
    <div>
      <ThemedButton />
    </div>
  );
};

let ThemedButton = () => {
  return (
    <ThemeContext.Consumer>
      {theme => <Button theme={theme} />}
    </ThemeContext.Consumer>
  );
};

let Button = ({ theme }) => {
  return (
    <button style={{ background: theme }}>
      I am styled by theme context!
    </button>
  );
};
```

## How to update context from a nested component?
- In order to update the context from a nested component, we can pass a function down through the context to allow consumers to update the context.
- The context provider should pass down a state (or updater function) and the consumer should pass down an event handler.
- The event handler should call the updater function from the context provider.
- The updater function should update the state and re-render the context provider.
- The context provider should pass down the updated state to the consumer.

## Example
```js
// Create a context object
const ThemeContext = React.createContext({
  theme: 'light',
  toggleTheme: () => {},
});

// Create a provider component

let App = () => {
  const [theme, setTheme] = React.useState('light');

  const toggleTheme = () => {
    setTheme(theme => (theme === 'light' ? 'dark' : 'light'));
  };

  return (
    <ThemeContext.Provider value={{ theme, toggleTheme }}>
      <Toolbar />
    </ThemeContext.Provider>
  );
};

// Create a consumer component

let Toolbar = () => {
  return (
    <div>
      <ThemedButton />
    </div>
  );
};

let ThemedButton = () => {
  return (
    <ThemeContext.Consumer>
      {({ theme, toggleTheme }) => (
        <Button theme={theme} onClick={toggleTheme} />
      )}
    </ThemeContext.Consumer>
  );
};

let Button = ({ theme, onClick }) => {
  return (
    <button style={{ background: theme }} onClick={onClick}>
      I am styled by theme context!
    </button>
  );
};
```

## How to use multiple contexts?
- To use multiple contexts, we can create multiple context objects.
- We can create a context object for each piece of data that needs to be shared.
- We can create a provider component for each context object.
- We can create a consumer component for each context object.
- We can nest the provider components and the consumer components to share multiple pieces of data.

## Example
```js
// Create a context object
const ThemeContext = React.createContext('light');
const LanguageContext = React.createContext('en');

// Create a provider component
let App = () => {
  return (
    <ThemeContext.Provider value="dark">
      <LanguageContext.Provider value="fr">
        <Toolbar />
      </LanguageContext.Provider>
    </ThemeContext.Provider>
  );
};

// Create a consumer component
let Toolbar = () => {
  return (
    <div>
      <ThemedButton />
    </div>
  );
};

let ThemedButton = () => {
  return (
    <ThemeContext.Consumer>
      {theme => (
        <LanguageContext.Consumer>
          {language => <Button theme={theme} language={language} />}
        </LanguageContext.Consumer>
      )}
    </ThemeContext.Consumer>
  );
};

let Button = ({ theme, language }) => {
  return (
    <button style={{ background: theme }}>
      I am styled by theme context!
      I am translated by language context!
    </button>
  );
};
```

## How to use context with hooks?
- We can use the useContext hook to consume a context object.
- The useContext hook accepts a context object and returns the current context value for that context.
- The useContext hook is equivalent to the Context.Consumer component.
- The useContext hook is equivalent to the Context.Provider component.