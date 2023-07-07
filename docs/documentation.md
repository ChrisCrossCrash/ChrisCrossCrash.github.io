---
layout: page
title: Documentation
---

Documentation is essential in development projects, serving as a roadmap for both current and future developers. It provides an understanding of the project's structure and functionality, captures the rationale behind key decisions, and offers solutions to common issues. Ultimately, good documentation ensures continuity, enabling any developer to contribute effectively and ensuring the project's long-term success.

It is also important to recognize the evolving nature of documentation within a project. Documentation should be updated as the project changes, and should be reviewed periodically to ensure that it is still accurate and up-to-date. This is especially important for documentation that is intended for end users, such as a user manual or help guide.

In general, the following types of documentation should be written:

1. **`README.md`**: Every project should have a README file that provides an overview of the project, including its purpose, structure, and usage.
2. **`CONTRIBUTING.md`**: Projects should provide documentation for contributors, including instructions for setting up the development environment, running tests, and submitting pull requests.
3. **`CHANGELOG.md`**: Projects should maintain a changelog that lists all changes made to the project, including new features, bug fixes, and breaking changes.
4. **API Documentation**: If a project includes an API, it should provide detailed documentation for each endpoint, including the HTTP method, URL, required parameters, and example responses. A useful tool for this is [Swagger](https://swagger.io/docs/), which can automatically generate API documentation from code annotations.
5. **Developer Documentation**: For small projects, the `README.md` file might be sufficient for developer documentation. However, for larger projects, it might be useful to create a separate documentation website that provides more detailed information. Here are some examples of what this documentation might include:
   - **Getting Started Tutorial**:
6. **User Documentation**: Some projects might require documentation for end users, such as a user manual or help guide. It might be useful to create a documentation website for this purpose.
7. **Code Annotations**: Code should be annotated with comments that explain its purpose and functionality. IDEs like VS Code or PyCharm can read these comments and display them as tooltips or documentation popups.
8. **Code Comments**: Code should be commented to explain its purpose and functionality. This is especially important for complex or tricky code.
9. **Tests**: Tests can be considered a form of documentation, as they provide examples of how the code should be used and what the expected behavior is.

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