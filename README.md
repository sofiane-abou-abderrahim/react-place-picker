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
