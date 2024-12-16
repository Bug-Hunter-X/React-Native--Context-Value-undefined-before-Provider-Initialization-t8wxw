# React Native: Context Value undefined before Provider Initialization

This repository demonstrates a common React Native bug where a component attempts to access context values before the context provider has a chance to populate them. This leads to the context value being `undefined`, causing unexpected behavior or application crashes.

## Problem

The `MyComponent` attempts to access the value from `MyContext` before the provider has finished rendering and providing the values. This results in the `contextValue` being `undefined`.

## Solution

The provided solution demonstrates how to use `useContext` safely and handle cases where the context value is initially `undefined`. This is done by checking for the `undefined` value using the optional chaining operator (`?.`) or by using a conditional rendering to prevent the component from rendering until the context is ready.

## How to reproduce the bug

1. Clone this repository.
2. Navigate to the project directory in your terminal.
3. Run `npm install`.
4. Run `npx react-native run-android` or `npx react-native run-ios`.
5. Observe the initial render. The component will initially display an error, or potentially crash, due to accessing an undefined context value.