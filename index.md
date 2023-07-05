---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---

Welcome to my personal documentation website.

## Prioritization

I use the [MoSCoW method](https://draft.io/example/moscow-method) to prioritize work, which categorizes tasks as **Must do**, **Should do**, **Could do**, or **Won't do**. I find it useful to label issues with these categories, and use the GitLab issue board to display the categories in a column view.

## Testing

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

## Documentation

Documentation is essential in development projects, serving as a roadmap for both current and future developers. It provides an understanding of the project's structure and functionality, captures the rationale behind key decisions, and offers solutions to common issues. Ultimately, good documentation ensures continuity, enabling any developer to contribute effectively and ensuring the project's long-term success.

It is also important to recognize the evolving nature of documentation within a project. Documentation should be updated as the project changes, and should be reviewed periodically to ensure that it is still accurate and up-to-date. This is especially important for documentation that is intended for end users, such as a user manual or help guide.

In general, the following types of documentation should be written:

1. **`README.md`**: Every project should have a README file that provides an overview of the project, including its purpose, structure, and usage.
2. **`CONTRIBUTING.md`**: Projects should provide documentation for contributors, including instructions for setting up the development environment, running tests, and submitting pull requests.
3. **`CHANGELOG.md`**: Projects should maintain a changelog that lists all changes made to the project, including new features, bug fixes, and breaking changes.
5. **API Documentation**: If a project includes an API, it should provide detailed documentation for each endpoint, including the HTTP method, URL, required parameters, and example responses. A useful tool for this is Swagger, which can automatically generate API documentation from code annotations.
4. **Developer Documentation**: For small projects, the `README.md` file might be sufficient for developer documentation. However, for larger projects, it might be useful to create a separate documentation website that provides more detailed information. Here are some examples of what this documentation might include:
   - **Getting Started Tutorial**:
5. **User Documentation**: Some projects might require documentation for end users, such as a user manual or help guide. It might be useful to create a documentation website for this purpose.
6. **Code Annotations**: Code should be annotated with comments that explain its purpose and functionality. IDEs like VS Code or PyCharm can read these comments and display them as tooltips or documentation popups.
7. **Code Comments**: Code should be commented to explain its purpose and functionality. This is especially important for complex or tricky code.
8. **Tests**: Tests can be considered a form of documentation, as they provide examples of how the code should be used and what the expected behavior is.

### Commenting Best Practices

- **Use comments to explain why, not what**: Comments should explain the purpose and rationale behind the code, not what the code does. The code itself should be self-explanatory, so comments should only be used to provide additional context.
- **Keep comments concise**: Comments should be short and to the point. If a comment is too long, it can be just as hard to understand as the code it's trying to explain.
- **Update comments as code changes**: Comments should always reflect the current state of the code. If you update the code, make sure to update any associated comments as well.
- **Avoid commenting out code**: Instead of commenting out code that's no longer needed, remove it. If you need to refer back to it, you can always find it in the version control history.
- **Wrap long comments**: If a comment is too long to fit on one line, wrap it at the same indentation level as the surrounding code. This makes it easier to read and understand.
- **Use TODO comments**: These special comments make it easy to find code that needs to be updated or fixed. These comments are especially useful for issues that cannot be fixed immediately, but need to be addressed in the future. However, if used too often, they can become overwhelming and lose their effectiveness.

### Code Annotation Best Practices

Code annotations are special comments that provide additional information about the code. IDEs like VS Code or PyCharm can read these comments and display them as tooltips or documentation popups. This makes it easy to understand the code without having to look at the source code itself.

Here is an example of a short-form JSDoc comment:

```ts
/** Return the sum of two numbers. */
function add(a: number, b: number): number {
  return a + b
}
```

Using the short form is ideal for a simple function such as this, since the types are explicit and the function is self-explanatory. However, for more complex functions, it might be better to use the long form:

```ts
/**
 * Return a string containing a greeting with the user's name and the current time.
 * 
 * @param name The user's name.
 * @param time The current time.
 * @returns A string containing a greeting with the user's name and the current time.
 */
function greet(name: string, time: Date): string {
  const greeting = `Hello, ${name}!`
  const timeString = time.toLocaleTimeString()
  return `${greeting} It is currently ${timeString}.`
} 
```

Code annotations are not limited to functions. They can also be used for variables, classes, and other types of code. For example, here is a variable with a JSDoc comment:

```ts
/** The number of milliseconds in a second. */
const MS_PER_SECOND = 1000
```

Code annotations even work across files. This is especially useful when documenting exports that get used throughout a codebase.

For these reasons, it is recommended to use code annotations for everything except the most trivial code. They make it easy to understand the code without having to look at the source code itself.

### Documentation Style

- Documentation should always be written in [Markdown](https://www.markdownguide.org/) format.
- Documentation should always be stored in a `docs` folder at the root of the project (with the exception of `README.md`, `CONTRIBUTING.md`, and `CHANGELOG.md`, which belong at the project root).
- Headings should have a strict hierarchy, with only one `h1` or single `#` heading per page.
- Headings should be written in [Title Case](https://en.wikipedia.org/wiki/Title_case), with all of the words capitalized, except for minor words.
- HTML tags should be used sparingly, and only when Markdown is insufficient.
- Images should be stored in a `docs/images` folder. Prefer JPEG over PNG to reduce file size.

## Filing Issues

TODO

## Version Control

TODO

### Semantic Versioning

TODO

### Branching

TODO

### Commit Messages

TODO

## Code Style

TODO

### Naming Conventions

TODO

### Formatting

TODO

### Linting

TODO

## Security

TODO

### Security Audits

TODO

### Vulnerability Scanning

TODO

## Developer Tools

TODO
