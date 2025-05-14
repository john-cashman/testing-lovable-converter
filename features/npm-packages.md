---
title: 'Using npm packages'
description: 'Learn how to leverage npm packages to extend your Lovable applications with advanced features'
icon: 'box'
---

While Lovable is powerful on its own, enabling users to build sophisticated web applications, you can leverage npm packages for more advanced and extended features. These packages help you build even more complex and feature-rich applications with ease.

## Using npm packages for advanced features

Let's say you'd like to create a tool that enables you to arrange your tasks in different Kanban boards, similar to many popular project management tools. You can prompt Lovable to build this tool from scratch, but it might be slower and more challenging to achieve the desired functionality.

Instead, you can use npm packages to simplify and speed up the process. For example, the [@hello-pangea/dnd](https://www.npmjs.com/package/@hello-pangea/dnd) package provides robust drag-and-drop functionality. By using this package, you can easily create a Kanban board where users can add new cards, move them within columns, and reorder them.

This prompt directs Lovable to integrate the package into your project, making it easier to achieve the desired functionality. Depending on other requirements, your result might look somewhat like this.

## Quality and responsibility

It's important to note that while npm packages can significantly enhance your projects, Lovable cannot guarantee the quality or reliability of these third-party packages.

The functionality and performance of npm packages are the responsibility of the end user, and it's essential to thoroughly test and validate them within your application.

### Increasing your chances of success

Here are a few strategies to help you evaluate the legitimacy and quality of npm packages before integrating them into your projects.

* **Number of downloads** - Check the number of downloads on the package's npm page. A high number of downloads typically indicates that the package is widely used and trusted by the community.

* **Maintenance status and latest updates** - Look at the package's repository to see if it is actively maintained. Frequent commits, recent updates, and responsiveness to issues are good indicators of an actively maintained package. Ensure the package has recent updates. A package that is regularly updated is more likely to be compatible with the latest versions of dependencies and security practices.

* **Reviews and community feedback** - A lot of npm packages are hosted on GitHub or similar code repositories. Read through reviews, discussions, and feedback from other developers on those locations, too. Additionally, specific developer forums can provide insights into the package's reliability and any potential issues.