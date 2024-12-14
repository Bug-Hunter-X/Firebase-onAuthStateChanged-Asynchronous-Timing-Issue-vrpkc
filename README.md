# Firebase onAuthStateChanged Asynchronous Timing Bug

This repository demonstrates a common asynchronous timing issue with Firebase's `onAuthStateChanged` listener.  The bug involves a delay between authentication changes (sign-in/sign-out) and the listener triggering, potentially leading to unexpected behavior in your application.

The `authBug.js` file shows the problematic code, where we attempt to access user data before the authentication state is updated. `authSolution.js` presents a solution using Promises or async/await to ensure data access occurs only after state changes are reflected.