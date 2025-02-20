# React useEffect Infinite Loop Bug
This repository demonstrates a common React bug involving the `useEffect` hook and missing dependencies. The bug causes an infinite loop because the effect runs on every render, causing an update that triggers another render, and so on.

## Bug Description
The `useEffect` hook is used to perform side effects after a component renders.  However, if the dependency array is omitted or incorrectly defined, it can lead to unexpected behavior. In this case, it creates an infinite loop that crashes the browser.

## Bug Solution
The solution is to correctly specify the dependency array of the `useEffect` hook.  Including the `count` variable in the dependency array ensures that the effect only runs when the value of `count` changes.