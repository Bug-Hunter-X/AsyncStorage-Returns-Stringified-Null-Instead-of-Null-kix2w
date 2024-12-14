# AsyncStorage Returns Stringified Null Instead of Null in React Native

This repository demonstrates a common, yet subtle bug in React Native's AsyncStorage. When retrieving a value that doesn't exist, AsyncStorage returns '"null"' instead of `null`, which can lead to unexpected behavior if not handled correctly.

## Problem

The core issue lies in the type checking.  A strict equality check (`===`) against `null` will fail because '"null"' is a string, not `null`.

## Solution

The solution involves checking for both `null` and the stringified version of `null`.

## Setup

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run the project using a React Native emulator or device.

## License

MIT