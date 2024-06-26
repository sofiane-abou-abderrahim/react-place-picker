# Dealing with Side Effects

## Keeping the UI Synchronized

- Understanding Side Effects & useEffect()
- Effects & Dependencies
- When NOT to use useEffect()

# Steps

## 0. Starting Project

1. run `npm install`
2. run `npm run dev`
3. create a `README.md` file

## 1. What's a "Side Effect"? A Thorough Example

1. get the user's current location in `App.jsx`
2. use the `sortPlacesByDistance` function imported from `loc.js`

## 2. A Potential Problem with Side Effects: An Infinite Loop

1. add a `availablePlaces`state to manage the available places in `App.jsx`

## 3. Using useEffect for Handling (Some) Side Effects

1. import `useEffect` from React in `App.jsx`
2. execute the `useEffect` hook inside the `App.jsx` component

## 4. Not All Side Effects Need useEffect

1. store the entire list of selected places in the browser storage with help of `localStorage` browser function in `App.jsx`

## 5. useEffect Not Needed: Another Example

1. delete items from local storage in `App.jsx`
2. fetch the items when the app starts
3. use `useEffect` to show that it is a redondant usage of `useEffect`
4. use `storedPlaces` to initialize the `pickedPlaces` state instead of `useEffect`

## 6. Preparing Another Use-Case For useEffect

1. use another alternative to open & close the modal in `Modal.jsx` & `App.jsx`

## 7. Using useEffect for Syncing With Browser APIs

1. try to open the modal in `Modal.jsx` without `useEffect()`
2. use `useEffect()` to synchronize the `open` prop to the `showModal()` & `close()` DOM APIs

## 8. Understanding Effect Dependencies

1. add the `open` prop as one of the `useEffect` dependencies in `Modal.jsx`

## 9. Fixing a Small Bug

1. listen to the modal being closed by adding the built-in `onClose` prop to the `<dialog>`
2. In `App.jsx`, set the `handleStopRemovePlace` function as a value for the `onClose` prop on the `<Modal>` component

## 10. Preparing Another Problem That Can Be Fixed with useEffect

1. set a timer in `DeleteConfirmation.jsx`
2. try to conditionally render `<DeleteConfirmation>` component in `App.jsx`
3. or conditionally render the `{children}` prop in `Modal.jsx`

## 11. Introducing useEffect's Cleanup Function

1. use `useEffect` in `DeleteConfirmation.jsx` to stop the timer when the `<DeleteConfirmation>` component disappears
2. return a cleanup function inside the Effect function

## 12. The Problem with Object & Function Dependencies

1. add the `onConfirm` prop as a dependency of the `useEffect` function in `DeleteConfirmation.jsx`

## 13. The useCallback Hook

1. wrap the `handleRemovePlace` function with the`useCallback`hook in`App.jsx` to prevent it from recreating again

## 14. useEffect's Cleanup Function: Another Example

1. add a progress bar in `DeleteConfirmation.jsx`
2. add a `useState` hook to manage the progress bar remaining time
3. add a `setInterval` function to update this state
4. return a cleanup function to stop the interval

## 15. Optimizing State Updates

1. outsource the progress indicator & the related state logic & the useEffect hook into a seperate component for better performance
2. create a `ProgressBar.jsx` component
