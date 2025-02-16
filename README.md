# Silent Failure in AsyncStorage with Large JSON Objects

This repository demonstrates a subtle bug in React Native's AsyncStorage when dealing with large JSON objects.  The issue is that AsyncStorage does not explicitly throw an error when storing data exceeding its capacity; instead, it fails silently.

The `bug.js` file showcases how this can lead to unpredictable application behavior. The `bugSolution.js` file offers a solution using a more robust method for handling large data persistence in React Native.

This is a common issue that often requires a significant amount of debugging time to identify.

**To reproduce the bug:** Run `bug.js` and attempt to store a large JSON object. Observe that there is no error message thrown, yet the data isn't saved.

**Solution:** The `bugSolution.js` demonstrates a solution that uses a more suitable approach for managing large datasets, such as Realm or a remote database. This prevents the silent failure that might occur with AsyncStorage.