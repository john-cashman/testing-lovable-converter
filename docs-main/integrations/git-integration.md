---
title: "GitHub Integration"
description: "Learn how to connect and sync your projects with GitHub repositories"
icon: "github"
---

![Github Lovable integration](/images/github-lovable.png)

## What is GitHub

Integrating GitHub into your Lovable project ensures you have full version control, collaboration tools, and code portability throughout your app's lifecycle. 

### **TL;DR:**

- **Git** is a version control system that tracks changes in your code.
- **GitHub** is the industry-standard platform for hosting Git repositories and tracking code changes, which makes it essential for both solo builders and teams using Lovable.
- By linking your project to GitHub, every change in your Lovable app is backed up in a Git repository in real time. This means you get a complete history of your code, the ability to collaborate with developers in familiar workflows, and the freedom to host or deploy your app outside of Lovable if needed.
- **GitHub integration** brings transparency, safety, and flexibility to your Lovable development process.

## Key Benefits of GitHub Integration:

Lovable backs every project with a Git repository, making it easy for developers to push commits directly to GitHub. This means:

- **Version History & Backup:** All your code is tracked with Git, so you can review changes or roll back to any previous state. Every commit is saved to GitHub, providing an external backup of your project​
- **Team Collaboration:** Your code lives on GitHub where others (developers, contributors) can easily view it, comment, and contribute via pull requests​. Non-technical team members can also see the code history for transparency.
- **Real-Time Sync:** Lovable automatically syncs with your GitHub repo. If you push code to GitHub, Lovable pulls it in almost immediately​. If you edit code in Lovable, it pushes those changes to GitHub. You’ll always have the latest code in both places without manual copying.
- **Workflow Integration:** Use GitHub’s tools (branches, pull requests, issues, CI/CD, etc.) alongside Lovable​. For example, you can run tests or deploy your app via GitHub Actions when code is merged, all while continuing to use Lovable’s editor and AI to develop features.
- **Deployment Flexibility:** Connecting to GitHub gives you the option to host your app on your own infrastructure or platform of choice. You’re not locked into Lovable’s hosting – you can export the code and deploy it anywhere​. (Lovable will still sync changes with GitHub, so you can continue editing in Lovable even if you host the app elsewhere.)

## Connecting Lovable to Your GitHub Account (Setup Guide)

To start using GitHub with Lovable, you need to connect your GitHub account and create a repository for your project. Here’s how to set it up:

  
  
  </Step>
  
  
</Steps>

## How Syncing Works (Lovable ↔ GitHub)

Once your project is connected to GitHub, Lovable ensures that code changes stay in sync between the Lovable editor and your GitHub repository. The integration is **bidirectional**, but it follows some specific rules and behaviors:

- **Default Branch Sync Only:** Lovable currently tracks **only the default branch** of your GitHub repository​. This is typically the `main` branch (or `master`, depending on your repo). If you push commits to other branches on GitHub, those changes will **not** appear in your Lovable project until they are merged into the default branch​. For example, if you’re working on a `feature/login` branch, Lovable won’t show those updates in the editor until you merge `feature/login` into `main` on GitHub. Similarly, Lovable will only push its changes to the default branch. Keep this in mind when using multiple branches. (See the FAQ on switching default branch if you need to change which branch Lovable syncs.)
- **Real-Time Updates from GitHub:** When you commit and push code to the default branch on GitHub, those commits will show up in Lovable almost automatically​. Lovable’s integration listens for changes – whenever you push to GitHub, Lovable pulls the latest commit into the project. You don’t need to manually refresh or import anything; the editor will reflect the new code typically within a few seconds of the push​. This allows developers to work in their own environment and see the results in Lovable instantly.
- **Pushing Changes from Lovable:** If you make changes in Lovable (for example, editing code via Lovable’s Dev Mode or having the AI generate new code), those changes are also saved to the Git repository backing your project. Lovable will push these commits to GitHub automatically, updating the repository. In practice, you can treat Lovable as another git client – when the AI or you modify code in the Lovable editor, it’s as if you committed and pushed to GitHub. For instance, adding a new page or editing a file in Lovable will result in a commit (with the changes) appearing in the GitHub repo’s commit history. This ensures both Lovable and GitHub always have the same latest code.
- **No Manual Pull/Push Needed:** The sync is continuous. You do not have to manually “pull” updates into Lovable or “push” updates to GitHub – Lovable handles it. Pushing code to GitHub triggers Lovable to fetch the changes, and editing in Lovable triggers a push to GitHub behind the scenes​. Your focus can be on building, not on syncing. If you ever suspect a change didn’t sync, a quick refresh of the Lovable editor or checking the GitHub repo can confirm the latest state (but in general it’s automatic).
- **Conflict Handling:** Because both Lovable and GitHub can change the code, there’s a chance of a git conflict if changes happen on the same file at the same time. In practice this is rare, but if a conflict does occur, you would resolve it just like any Git conflict. For example, you might need to go to the GitHub repo and manually merge or fix conflicting changes, then commit. Lovable will then pull the resolved code. To avoid conflicts, it’s best to coordinate who is editing or use branches for larger changes (merging to main when ready).

In summary, the GitHub integration means your Lovable project’s code and the GitHub repository are effectively one and the same source, mirrored in real time. You can confidently switch between the Lovable editor and other development tools knowing both will stay updated​

## Importing an Existing GitHub Repository into Lovable

What if you already have a codebase on GitHub and want to use Lovable with it? Currently, **Lovable does not yet support directly importing or linking to an existing external GitHub repo as a new project**​. In other words, you can’t point Lovable at an existing repository and have it pull in all that code automatically (as of now). However, there are ways to bring your existing code into Lovable:

- **Manual Import via a New Repo:** One workaround is to create a new Lovable project and connect it to GitHub (following the setup steps above), which gives you an empty repository (or a repository with the starter code from Lovable). Then, you can **manually add your existing code to that repository**. For example, you could clone the new GitHub repo to your local machine, copy in the files from your old project, commit and push. Once you push your existing code into the repo’s default branch, Lovable will sync those files and you’ll see them in the Lovable editor. This effectively migrates your code into a Lovable project.
- **Copy-Paste Smaller Snippets:** If your project is small, you might also start a Lovable project and copy code pieces (like individual files or functions) into Lovable via the editor or the AI (for instance, by pasting code into Lovable’s code editor or prompting the AI with your code). This is less ideal for large projects but can work for minor modules.
- **[Planned Import Feature:](https://feedback.lovable.dev/p/have-the-possibility-to-import-an-existing-github-project)** The Lovable team is aware that direct repo import is a desired feature, and it’s something under consideration for future updates​. Keep an eye on Lovable’s roadmap or announcements for any feature that allows importing an existing repo more directly.

## Developing with GitHub and Lovable in Parallel

Once connected, you can build and edit your application using GitHub (or your local development environment) and Lovable simultaneously. This is great for developers who want to use their own tools or for teams where some members prefer coding by hand. Here are some ways to work effectively with the integration:

- **Viewing the Repository:** In the Lovable editor, you’ll have an option to view the GitHub repository (often via a **“View on GitHub”** link or button)​. Clicking this will take you straight to the repository page on GitHub. From there, you can browse the code, open files, and even edit directly on GitHub if needed.
- **Using Local IDE or Codespaces:** You can clone the GitHub repository to your local machine and open it in your favorite IDE (like VS Code, WebStorm, etc.), or use GitHub Codespaces (a cloud IDE on GitHub) for development​. This means you can write and modify code outside of Lovable’s interface.

  
- **Normal GitHub Workflows:** You can leverage all of GitHub’s collaboration features on your project’s repo: create **branches** for new features, open **pull requests** to review code before merging, file **issues** and use project boards to track tasks, etc.​. Lovable doesn’t interfere with these; it simply watches the default branch for actual code changes. For instance, you might do all your work for a new feature on a `feature` branch, push it to GitHub, get it reviewed via a pull request, and then merge it to `main`. Once merged, Lovable will pull in those changes so the running app updates. This way, teams can enforce code reviews and use GitHub’s project management, while still benefiting from Lovable’s rapid development capabilities.
- **Combining AI and Manual Coding:** You can continue to use Lovable’s AI assistant to generate code or new components, and then inspect or fine-tune that code via GitHub. The integration allows a hybrid workflow: for example, a non-technical founder might use Lovable to scaffold a feature with AI, and a developer can then clean up or optimize that code in the GitHub repo. Both sets of changes merge seamlessly.

  
- **Remember:** even while doing heavy development through GitHub, you can always go back to the Lovable editor to use the visual tools or AI chat for assistance. The codebase is the same, so any changes you made by hand will be present in Lovable. This integration makes Lovable a part of your toolchain rather than an isolated environment.

## Documenting Changes and Rolling Back

Working with GitHub encourages good software development practices like documenting changes and managing versions. Here are some tips on managing your code changes and reverting when necessary:

- **Use Meaningful Commit Messages:** Whenever you commit changes (especially when committing via a local IDE or GitHub’s interface), write a clear commit message describing _what_ you changed and _why_. For example, `"Fix signup form validation bug"` is much more useful than `"update code"`. Good commit messages help team members (and your future self) understand the history of the project. They serve as documentation for the evolution of your app. If Lovable’s AI made a lot of changes in one go, consider breaking them into logical commits with messages for each major change, if you’re doing it manually. If commits are being generated automatically, you can always squash or edit them later on GitHub for clarity.
- **Track Versions in Lovable:** Lovable provides a version history in the editor (similar to Google Docs revision history) that keeps track of changes made through the platform. You can access the version history panel to see previous states of your project and even restore an earlier version with one click​. This is effectively a “rollback” feature built on top of Git – if something goes wrong after an AI-generated change or an edit, you can revert to a known good state. It’s a quick way for non-developers to undo mistakes without using GitHub directly.
- **Rolling Back with Git or Lovable (Reverts):** Since your project is under Git, you can perform rollbacks by reverting commits on GitHub as well. For example, if a certain commit introduced an issue, you (or a developer) can click “Revert” on GitHub for that commit, or use `git revert` locally and push. This will create a new commit that undoes the changes of the bad commit. Lovable will sync this revert commit and your project will go back to the previous behavior. Always test your app after a revert to ensure the issue is resolved and no other functionality is affected.
- **Use Branches for Big Changes:** A good strategy to reduce the need for rollbacks is to use feature branches for major changes. You might develop a big feature on a separate branch and only merge it to the main branch (which Lovable uses) after it’s fully tested. This way, your main branch (and the live app in Lovable) stays stable, and you only introduce changes when they are ready. If something on the feature branch isn’t working, it doesn’t affect your production code in Lovable until merged.
- **Documentation of Changes:** If you are collaborating with others or handing off the project, consider maintaining a brief **changelog** or using GitHub’s release notes. While commit messages are the primary log, summarizing changes in human-readable form (e.g., “Implemented user authentication, updated UI for profile page, fixed payment bug”) can be helpful for non-technical stakeholders to follow progress. You can do this in a Markdown file in the repo or in GitHub Releases.
- **Lovable’s Rollback Feature:** Lovable automatically backs up your project, so if you made a mistake, you can use the built-in rollback in the Lovable interface to undo accidental changes​. This is essentially using Git version control under the hood. It ensures that even non-technical users have a safety net – you don’t have to be a Git expert to restore a previous version of your app. However, for complex version management (like maintaining multiple versions or doing partial rollbacks), you will likely use GitHub’s tools.

By diligently documenting your changes and taking advantage of GitHub’s and Lovable’s versioning features, you can move fast with confidence. If a published update causes issues, you have clear records of what changed and multiple ways to revert or fix forward. This significantly de-risks the development process.

## Troubleshooting & FAQ (GitHub Sync)

Below are some common questions and issues that users encounter with the GitHub integration, along with guidance on how to resolve them. Click on a question to view the answer.

  
  
  
    Do note that if you do host the app yourself outside of Lovable, you’ll need to manage environment variables, secrets, database connections, and other config in your new environment just as you would for any app. The Lovable integration with services like Supabase or Stripe will still be in your code – those continue to work as long as the appropriate config is in place on the new host.
  </Accordion>
</AccordionGroup>

By following this guide and utilizing GitHub with Lovable, you’ll combine the speed of AI-assisted development with the reliability and control of traditional software practices. This integration is designed to be approachable for non-technical users (you get a safe backup and easy way to hand off code) while providing all the power that developers expect in a modern toolchain. 

Happy coding!