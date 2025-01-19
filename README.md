# Expo CLI Linking Error: Vague Dependency Conflict

This repository demonstrates a bug encountered while using the Expo CLI to build a React Native application. The issue involves a vague dependency conflict between `react-native-gesture-handler` and `react-native-reanimated`, preventing the successful linking and build process.

## Problem Description

During the Expo build process, an error occurred indicating a dependency conflict. The error message lacked specifics, making troubleshooting difficult.  Standard solutions such as `expo prebuild` and `expo install` did not resolve the problem.

## Solution

The issue was resolved by explicitly specifying the versions of `react-native-gesture-handler` and `react-native-reanimated` in the `package.json` file, ensuring compatibility between these libraries.  This involved carefully checking the versions of those dependencies and updating them to compatible versions as mentioned in each package's documentation. In some cases, manually removing and reinstalling the packages may be required.

## Reproduction Steps

1. Clone this repository.
2. Navigate to the project directory: `cd expo-linking-error`
3. Install the dependencies: `npm install` or `yarn install`
4. Attempt to build the app using the Expo CLI (e.g., `expo build:ios` or `expo build:android`).
5. Observe the vague dependency conflict error.
6. Apply the solution from `bugSolution.js`.
7. Rebuild the app and verify that the error is resolved.
