## How long did you spend on the coding test?

I spent approximately 2 hours on the coding test. Most of the time was spent setting up the project, structuring the components, and ensuring smooth functionality for task management. Debugging and refining the user experience also took a fair amount of time, especially when working with localStorage and implementing search and filtering features.

## What was the most useful feature that was added to the latest version of your chosen language? Please include a snippet of code that shows how you've used it.
One of the most useful features in the latest versions of JavaScript (ES2020+) is optional chaining (?.). It allows us to safely access deeply nested object properties without having to check each level manually, preventing runtime errors.

Here's an example of how I used it in the task management application:

```javascript
const task = {
  title: "Complete project",
  details: {
    dueDate: "2025-02-20",
  },
};

const taskTitle = task?.title ?? "Untitled Task";
const taskDueDate = task?.details?.dueDate ?? "No due date";

console.log(taskTitle);
console.log(taskDueDate); 
```

In this case, if task or task.details is null or undefined, the optional chaining operator (?.) ensures that accessing .title or .dueDate doesn't throw an error. Instead, the fallback values "Untitled Task" and "No due date" are used.

## How would you track down a performance issue in production? Have you ever had to do this?


To track down a performance issue in production, I would follow these steps:
Use Browser DevTools: Open Chrome DevTools (or similar) to check performance profiling, identify slow components, and inspect network requests.Monitor Console Logs & Errors: Check if there are any warnings or errors that could indicate bottlenecks.
Yes, I have had to debug performance issues before. One instance was when an inefficient state update in React caused excessive re-renders. Optimizing component rendering with useMemo and useCallback helped improve performance significantly.

## If you had more time, what additional features or improvements would you consider adding to the task management application?

If I had more time, I would add the following enhancements:
Drag & Drop Task Reordering: Allow users to rearrange tasks dynamically using a library like React DnD.
Recurring Tasks: Support for tasks that repeat daily, weekly, or monthly.
These improvements would make the application more powerful, user-friendly, and scalable.