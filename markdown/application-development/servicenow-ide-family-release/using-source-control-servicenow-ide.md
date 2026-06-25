---
title: Using source control in the ServiceNow IDE
description: Use Git commands and other source control features in the ServiceNow IDE to manage changes to an application across a development team.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-ide-family-release/using-source-control-servicenow-ide.html
release: australia
product: ServiceNow IDE \(Family Release\)
classification: servicenow-ide-family-release
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [The following Git commands are supported]
breadcrumb: [Integrate source control, ServiceNow IDE, Building applications in source code, Building pro-code applications, Developing your application, Building applications]
---

# Using source control in the ServiceNow IDE

Use Git commands and other source control features in the ServiceNow IDE to manage changes to an application across a development team.

Role required: admin

## Git commands

After initializing a local Git repository in the ServiceNow IDE, you can perform several Git commands from the Source Control view \(\[Omitted image "servicenow-ide-source-control-icon.png"\] Alt text: Source Control\) or command palette, including but not limited to the following commands.

<table><thead><tr><th>

Command

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Checkout to \(\[Omitted image "servicenow-ide-more-actions-icon.png"\] Alt text: More actions &gt; **Checkout to...**\) Command palette: **Git: Checkout to...**

</td><td>

Check out another branch from the repository. Select the branch from the list or create a branch and push it to the remote repository.Only one branch per repository can be checked out at a time on an instance\(or developer sandbox\).

</td></tr><tr><td>

Clone \(\[Omitted image "servicenow-ide-more-actions-icon.png"\] Alt text: More actions &gt; **Clone**\) Command palette: **Git: Clone**

</td><td>

Clone a remote repository to add an application to your workspace.For more information, see [Clone a Git repository with the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/clone-git-repository-servicenow-ide.md).

</td></tr><tr><td>

Commit \(\[Omitted image "servicenow-ide-commit-icon.png"\] Alt text: Commit\) Command palette: **Git: Commit**

</td><td>

Commit your staged changes to the local repository. Enter a commit message to describe your changes.

</td></tr><tr><td>

Create branch \(\[Omitted image "servicenow-ide-more-actions-icon.png"\] Alt text: More actions &gt; **Branch** &gt; **Create branch...**\)Command palette: **Git: Create branch...**

</td><td>

Add a branch to a repository and check it out.

</td></tr><tr><td>

Discard \(\[Omitted image "servicenow-ide-discard-icon.png"\] Alt text: Discard Changes\)Command palette: **Git: Discard Changes**

</td><td>

Discard changes to undo modifications to an application.

</td></tr><tr><td>

Fetch \(\[Omitted image "servicenow-ide-more-actions-icon.png"\] Alt text: More actions &gt; **Fetch**\)Command palette: **Git: Fetch**

</td><td>

Fetch to sync commits and branches from the remote repository into the local repository.

</td></tr><tr><td>

Pull \(\[Omitted image "servicenow-ide-more-actions-icon.png"\] Alt text: More actions &gt; **Pull**\)Command palette: **Git: Pull**

</td><td>

Pull to merge the latest changes from the remote repository into the local repository.

</td></tr><tr><td>

Push \(\[Omitted image "servicenow-ide-more-actions-icon.png"\] Alt text: More actions &gt; **Push**\)Command palette: **Git: Push**

</td><td>

Push your committed changes to the remote repository.

</td></tr><tr><td>

Stage \(\[Omitted image "servicenow-ide-stage-icon.png"\] Alt text: Stage Changes\) Command palette: **Git: Stage Changes**

</td><td>

Stage the changes in your working directory that you want to commit. When you stage changes, files move from the Changes list to the Staged Changes list.

</td></tr><tr><td>

Stash \(\[Omitted image "servicenow-ide-more-actions-icon.png"\] Alt text: More actions &gt; **Stash**\)Command palette: **Git: Stash**, **Git: Pop**, **Git: Drop**, **Git: List**, **Git: Apply**, **Git: Clear**

</td><td>

Stash all uncommitted changes to save them in your working directory locally and come back to them later.The pop, drop, list, apply, and clear subcommands are supported when stashing. Select **Stash** &gt; **Apply** to reapply your changes in your working directory.

</td></tr></tbody>
</table>## Merge conflicts

If there’s a conflict between local and remote changes in a file, the file is listed under Merge conflicts in the Source Control view \(\[Omitted image "servicenow-ide-source-control-icon.png"\] Alt text: Source Control\). You can review conflicts in the editor and resolve them by accepting the current or incoming change, both, or manually editing the file.

## Commit history

The commit history for a branch is listed in the Commits section of the Source Control view \(\[Omitted image "servicenow-ide-source-control-icon.png"\] Alt text: Source Control\) and includes details about the commits. To see the commit history for a file, navigate to the File Explorer view \(\[Omitted image "servicenow-ide-file-explorer-icon.png"\] Alt text: File Explorer\), select the file, and expand the Timeline section. When you select a commit, a Diff editor comparing the changes opens.

## Repository changes

To update the remote repository an application is connected to, you can use the `Git: Update remote origin` command from the command palette and enter a different remote repository URL.

**Parent Topic:**[Integrating source control with the ServiceNow IDE](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/servicenow-ide-family-release/integrating-source-control-servicenow-ide.md)

**Related topics**  


[Connect to a Git provider using basic authentication with the ServiceNow IDE]()

[Connect to a Git provider using OAuth 2.0 with the ServiceNow IDE]()

[Configure a MID Server to use source control with the ServiceNow IDE]()

[Initialize a Git repository with the ServiceNow IDE]()

