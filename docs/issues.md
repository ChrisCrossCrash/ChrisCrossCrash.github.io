---
layout: page
title: Issues
---

> “Always start with an issue” says Job, VP of Product here at GitLab. Before you begin anything else, summarize your ideas in an issue and share it. It’s such a simple rule, but the impact is huge.

*From the GitLab blog article [Always start with an issue](https://about.gitlab.com/blog/2016/03/03/start-with-an-issue/) by Heather McNamee*

Starting with an issue is a fundamental practice in development projects. Issues provide a space to summarize and discuss ideas before any work begins. This approach promotes clear communication, helps in planning, and ensures that every task has a defined purpose. By creating an issue first, we can outline the task at hand, discuss potential approaches, and track progress in a structured manner. In short, issues are a crucial tool for managing work in a project, keeping everything organized and everyone on the same page.

## Writing Issues

When writing an issue, it is important to provide as much information as possible. This helps ensure that the issue is understood by everyone, and that the task can be completed successfully. Here are some guidelines for writing issues:

- **Use a descriptive title**: The title should be short and to the point, but should also provide enough information to understand the issue at a glance. It should clearly state the issue that needs to be addressed. Always consider whether the title is sufficient to identify the issue in a list of other issues.
- **Provide context**: The issue should provide enough context to understand the problem and its purpose. This includes the rationale behind the issue, as well as any relevant background information, such as screenshots or logs. It should also describe the environment in which the issue occurs, such as the operating system, browser, or device. The more context that is provided, the easier it will be to reproduce and understand the issue.
- **Clearly state the problem**: The issue should clearly state the problem that needs to be addressed. This includes the expected behavior, the actual behavior, and any other relevant details.
- **Describe the solution or next steps**: It's not enough to simply state the problem. The issue should also describe the solution, or if the solution is not known, the next steps that need to be taken. This helps ensure that the issue is actionable, and that the task can be completed successfully. It might be useful to include a checklist of steps that need to be completed.
- **State the desirable outcome**: The issue should state the desirable outcome. This helps ensure that everyone is on the same page.

## Prioritizing Issues

As mentioned previously, I use a variation of [the MoSCoW method](https://draft.io/example/moscow-method) to prioritize issues. Each issue should be labeled with one of the following categories:
- **Must do**: Critical issues that must urgently be addressed. This includes bugs that cause the application to crash or break, as well as any other issues that prevent the application from functioning properly.
- **Should do**: Important issues that should be addressed soon. This includes bugs that cause the application to behave unexpectedly, as well as any other issues that affect the user experience.
- **Could do**: Issues that are not critical or important, but would be nice to have. This includes minor bugs that don't affect the user experience, as well as any other issues that are not urgent.
- **Back burner**: Issues that are not critical or important, and can be put off indefinitely. This includes minor bugs that don't affect the user experience, as well as any other issues that are not urgent.

GitLab has a feature called [Issue Boards](https://docs.gitlab.com/ee/user/project/issue_board.html) where issues are organized to columns based on their labels. I use this feature to display the MoSCoW categories in a column view. The issues can be dragged-and-dropped between columns to adjust their priority. [Labels can also be prioritized](https://docs.gitlab.com/ee/user/project/labels.html#set-label-priority) so that they can be sorted by priority in places other than the Issue Board page.

GitHub as a similar feature to GitLab's Issue Boards called [Project Boards](https://docs.github.com/en/github/managing-your-work-on-github/about-project-boards).
