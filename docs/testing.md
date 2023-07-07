---
layout: page
title: Testing
---

Testing is a vital part of the development process, acting as a safety net that ensures the code performs as expected. It verifies the functionality of new features, confirms the resolution of bugs, and safeguards against regressions. By highlighting issues early, testing saves time and effort in the long run, and contributes to the delivery of a reliable, high-quality product. Ultimately, comprehensive testing gives developers the confidence to innovate and iterate, knowing that any potential impact on existing functionality will be detected.

In general, tests are required for all new code that is not experimental or extremely trivial. A good approach might be to use TDD (Test Driven Development) to write tests before writing code. This is a good way to ensure that tests are written for all code.

Here are some examples of when tests should be written:

1. **New Features**: Whenever a new feature is added, tests should be written to verify that the feature works as expected and doesn't break existing functionality. This includes both unit tests (to test individual components in isolation) and integration tests (to test how components interact).
2. **Bug Fixes**: When a bug is fixed, a test should be written to reproduce the bug and confirm that it has been fixed. This helps prevent regression, where a bug that was previously fixed reappears in a later version.
3. **Refactoring**: When code is refactored, tests should be run to ensure that the behavior of the code hasn't changed, even if its structure or appearance has.
4. **Performance Improvements**: If you're making changes to improve performance, tests should be written to verify that the changes actually improve performance and don't introduce new bugs.
5. **Critical Path**: Any code that lies on the "critical path" (i.e., code that is crucial for the basic functionality of your application) should be thoroughly tested.
6. **Complex Code**: Code that is particularly complex or tricky should have tests, even if it's not on the critical path. This can help catch bugs that might be missed otherwise.
7. **Before Deployment**: Before deploying any code, a full suite of tests should be run to catch any last-minute issues.

However, there are some cases where testing is not practical or necessary:

1. **Trivial Code**: If the code is extremely simple and straightforward, it might not need dedicated tests. For example, a getter or setter method that simply returns or sets a value might not need a test.
2. **Experimental Code**: If you're just experimenting with a feature or trying out a new idea, you might not need to write tests right away. However, if the experiment becomes a permanent part of your codebase, tests should be added.
3. **Third-Party Code**: If you're using a third-party library or framework, you generally don't need to test that code. You can assume that the third-party code has its own tests. However, you should still write tests for your own code that uses the third-party code.
4. **Temporary Code**: If you're writing code that you know will be removed in the near future, it might not be worth the effort to write tests for it.
5. **UI and Visuals**: While it's possible to write tests for user interfaces and visuals, it can often be difficult and time-consuming. In many cases, manual testing or user testing might be more effective for these aspects.
