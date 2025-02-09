# React Native FlatList Performance Issue

This repository demonstrates a common performance issue encountered when using the `FlatList` component in React Native with large datasets and complex item rendering. The problem is characterized by intermittent crashes, freezes, and significant performance degradation, especially on lower-end devices.

## Bug Description

The bug is reproduced when a `FlatList` is populated with a significant number of items, each requiring intensive rendering. This leads to dropped frames and noticeable lag. In some cases, the app may even crash.

## Solution

The provided solution explores techniques to mitigate this performance bottleneck.  These include optimization strategies for rendering individual items, improving data fetching, using `React.memo` to prevent unnecessary re-renders and implementing `windowSize` and `maxToRenderPerBatch` for better batch rendering in the `FlatList`.  The optimized `FlatList` ensures smoother performance even with a large number of items.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` or `yarn install`.
3. Run the app using `npx react-native run-android` or `npx react-native run-ios`.
4. Observe the performance of the `FlatList` with a large dataset.