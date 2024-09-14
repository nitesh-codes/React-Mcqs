# React MCQ Questions

## Question 1
What is the purpose of the `React.memo()` function and how does it work under the hood?

- **A)** It is used to memoize values across renders and is equivalent to `useMemo`.
- **B)** It prevents unnecessary re-renders of functional components by memoizing the result of the component’s function based on its props.
- **C)** It is used to memoize asynchronous calls to APIs to avoid making duplicate requests in concurrent rendering.
- **D)** It wraps class-based components for performance optimization by memoizing the class instance.

**Answer: B**

---

## Question 3
What happens if you forget to include a dependency in the dependency array of a `useEffect` hook?

- **A)** The effect will never run.
- **B)** The effect will run once and never again, regardless of changes.
- **C)** The effect will run on every re-render.
- **D)** The effect will run only when the component mounts.

**Answer: C**

---

## Question 4
What will happen if you update a state value inside `useEffect` without providing a dependency array?

- **A)** The `useEffect` will run only once after the initial render.
- **B)** The `useEffect` will enter an infinite loop as the state update will trigger a re-render, causing the effect to run again.
- **C)** The component will not re-render even after the state change.
- **D)** React will throw an error, preventing the state update.

**Answer: B**

---

## Question 5
Which of the following is the main benefit of using `React.lazy()` and `Suspense`?

- **A)** They allow you to create lazy state updates.
- **B)** They enable dynamic imports and lazy loading of components.
- **C)** They help memoize components to prevent unnecessary re-renders.
- **D)** They simplify state management in functional components.

**Answer: B**

---

## Question 6
Which of the following best describes the behavior of the `useRef` hook?

- **A)** It allows you to store a mutable reference that persists across renders without causing re-renders when updated.
- **B)** It triggers a re-render every time the referenced value changes.
- **C)** It is used to create a reference to DOM elements, but only in class components.
- **D)** It is primarily used to manage side effects in functional components.

**Answer: A**

---

## Question 7
Why is Babel used in JavaScript development?

- **A)** To manage application state and handle side effects in React applications.
- **B)** To minify JavaScript code for better performance and faster load times.
- **C)** To bundle multiple JavaScript files into a single file to improve load times.
- **D)** To JavaScript code into a backward-compatible version.

**Answer: D**


---

## Question 8
What is the key difference between Context API and Redux in React for state management?

- **A)** Context API is a state management library, while Redux is built-in to React for managing global states.
- **B)** Redux uses a single store and strict actions/reducers to update state, while Context API provides a simpler mechanism to pass data across components without props.
- **C)** Context API supports asynchronous updates natively, while Redux requires middleware like thunk or saga.
- **D)** Context API can manage more complex global states than Redux, making it a better choice for large-scale applications.

**Answer: B**

## Question 9
In React Native, how does the `FlatList` component optimize rendering compared to a standard list or map function?

- **A)** `FlatList` renders all items at once but caches them for faster scrolling.
- **B)** `FlatList` renders only visible items and dynamically loads more items as the user scrolls, using a "windowing" technique.
- **C)** `FlatList` renders only the first item and batches the rest in a background thread.
- **D)** `FlatList` uses pagination to load a fixed number of items at a time, pre-fetching the next batch when the user scrolls.

**Answer: B**

---

## Question 10
Which of the following statements is true regarding React Native’s `StyleSheet.create()` function?

- **A)** `StyleSheet.create()` is only a utility for organizing styles but does not improve performance.
- **B)** `StyleSheet.create()` ensures that styles are created once and are frozen.
- **C)** `StyleSheet.create()` allows for dynamic style recalculations on every render, which helps optimize styling for different states.
- **D)** `StyleSheet.create()` is deprecated in newer versions of React Native.

**Answer: B**

---

## Question 11
In React Native, which hook or component is responsible for managing app lifecycle events such as moving to the background or resuming in the foreground?

- **A)** `useEffect`
- **B)** `AppState`
- **C)** `useFocusEffect`
- **D)** `useCallback`

**Answer: B**

---

## Question 12
Which of the following is not a part of the React Native Library?

- **A)** Async Storage
- **B)** ActivityIndicator
- **C)** Stylesheet
- **D)** Pressable

**Answer: A**

---

## Question 13
What will be the output of this code in the console when the button is clicked multiple times?

```jsx
function App() {
  const [count, setCount] = useState(0);

  const handleClick = () => {
    setCount(count + 1);
    setCount(count + 1);
    setCount(count + 1);
  };

  return <button onClick={handleClick}>Click me</button>;
}
```
- **A)** The count will increment by 1 each time the button is clicked.
- **B)** The count will increment by 3 each time the button is clicked.
- **C)** The count will increment by 2 each time the button is clicked.
- **D)** The count will not change.

**Answer: A**

## Question 14
What will be the output of the following code when the button is clicked?

```jsx
function App() {
  const [items, setItems] = useState(["A", "B"]);

  const addItem = () => {
    setItems([...items, "C"]);
  };

  return (
    <div>
      <button onClick={addItem}>Add Item</button>
      <List items={items} />
    </div>
  );
}

const List = React.memo(({ items }) => {
  console.log("List rendered");
  return (
    <ul>
      {items.map((item, index) => (
        <li key={index}>{item}</li>
      ))}
    </ul>
  );
});

```
- **A)** "List rendered" is logged only when new items are added to the list.
- **B)** "List rendered" is logged only the first time the button is clicked.
- **C)** "List rendered" is logged each time the button is clicked.
- **D)** "List rendered" is logged when the items array reference changes.

**Answer: C**
