# Bug-Solving Guide for FE Developers:

---

### Identify the root of the bug.

-   Start by collecting all relevant information about the bug, this includes:
    -   the description of the bug
    -   the steps to reproduce it
    -   any error messages or warnings.

-   Check the site

-   Check if all of the APIs are having success response in Network tab.

-   Check if a recent PR broke it. We can use [git-bisect](https://git-scm.com/docs/git-bisect) for that.

-   When an issue affects just one or 2 users, check if the user has an ad-blocker installed.

### Debug and replicate the bug.

-   Follow the steps provided to reproduce the bug if any.

-   Use debugging tools available in the browser or React developer tools to inspect the application's state, props, and component hierarchy. Use breakpoints to pause execution and analyze the code flow.

-   Carefully read any error messages or warnings displayed in the browser's console. They often provide valuable information about the cause and location of the bug.

### Fix the bug.

-   Take the time to understand the overall system and the codebase. This understanding helps identify the bug's source and accelerates the bug-fixing process.

-   When a specific user encounters an issue, consider it as a subtle bug embedded in the system or an opportunity to identify such bugs. Avoid getting fixated on why it's occurring only for one user and approach it with a problem-solving mindset.

-   **Don't hesitate to ask for help or clarification**, it's important to seek help or clarification to address issues quickly and efficiently.

-   Ask for more information from the person that reported the bug if the issue is not clear enough. *Investigating a malfunction that you don't understand will lead you nowhere.*

-   If you suspect an issue is related to a specific component, isolate it and test its expected behaviors in an isolated environment like [codesandbox](https://codesandbox.io/).

-   When making changes that affect user data, keep the pull requests small. Consider the possible side effects and thoroughly investigate to ensure you don't introduce subtle errors.

-   If the bug impacted the user experience, state in your comment that you need an urgent review and QA for your PR.

-   If the bug impacted the user experience, involve QA to verify the resolution and ensure the bug no longer occurs in different environments or scenarios.

