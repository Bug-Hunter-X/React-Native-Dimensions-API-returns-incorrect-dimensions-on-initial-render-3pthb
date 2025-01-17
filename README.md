# React Native Dimensions API Inconsistency

This repository demonstrates a common issue encountered when using the `Dimensions` API in React Native to retrieve screen dimensions. The problem arises when attempting to access these dimensions before the layout is fully calculated, resulting in incorrect values and potentially misaligned UI elements.

## Problem Description

The provided `bug.js` file showcases a simple component that utilizes `Dimensions.get('window')` to determine the screen width and height. Due to the asynchronous nature of layout calculations in React Native, accessing these values immediately upon component mount might yield inaccurate results.

## Solution

The `bugSolution.js` file presents a solution using the `useEffect` hook and `onLayout` event listener. This approach ensures that the dimensions are fetched only after the component has been laid out correctly. 

## How to Reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install the necessary dependencies.
4. Run `npx react-native run-android` (or `npx react-native run-ios`) to start the app.
5. Observe the initial rendering and note any inconsistencies in the positioning of elements.

## License

MIT