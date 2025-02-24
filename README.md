# React 18/19 useEffect Event Listener Memory Leak

This repository demonstrates a common mistake in using useEffect hooks in React 18 and 19 that can lead to memory leaks.  Specifically, this example shows how attaching event listeners without the proper dependency array leads to the listener being re-added on every render, causing memory issues.

The `bug.js` file contains the problematic code, while `bugSolution.js` provides the corrected version.

## How to reproduce the bug:

1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the console (if you've added logging) or use memory profiling tools to detect the memory leak.

## Solution:

The solution involves correctly managing the dependencies within useEffect to prevent the event listener from being added repeatedly. This is explained in detail in `bugSolution.js`.