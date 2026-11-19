---
title: Project explorer
description: The Project Explorer is the primary file management panel in Lux Lab. It provides a hierarchical view of your project's files and folders, and is the starting point for navigating, creating, and organizing your work.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/application-development/project-explorer.html
release: zurich
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 4
keywords: [Project explorer, Panel location, Opening and switching projects, Creating files and folders, File tree navigation, Explorer panel context menu, File and folder context menu, Inline run and preview icons, File status markers, Filtering and searching files, Moving, copying, and selecting files]
breadcrumb: [Exploring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Project explorer

The Project Explorer is the primary file management panel in Lux Lab. It provides a hierarchical view of your project's files and folders, and is the starting point for navigating, creating, and organizing your work.

## Panel location

The Project Explorer occupies the left sidebar when the **Explorer** icon, the top icon in the Activity Bar, is active. It shows the full directory tree rooted at your current project folder.

## Opening and switching projects

You open and switch projects from the title bar drop-down list. Selecting the project name in the title bar reveals the project picker, which has the options in the following table.

|Option|Description|
|------|-----------|
|**Recent**|Recently opened projects and workspaces. Select any project to switch to it.|
|**Open Folder…**|Option to open an existing project folder from disk|
|**New Project**|Option to create a Lux project from a template|
|**New Workspace**|Option to create a multi-root workspace|

For the steps to open an existing project folder, see [Open a project folder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/open-a-project-folder.md).

## Creating files and folders

You create files and folders directly in the tree. When you hover over any folder, Lux Lab reveals its action icons, including **New File**.

For the steps to add a file, see [Create a file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-a-file.md). For the steps to add a subfolder, see [Create a folder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/application-development/create-a-folder.md).

## File tree navigation

The following table lists the keys for moving through the file tree.

|Action|Method|
|------|------|
|Expand folder or open file|→ arrow or select the chevron|
|Collapse folder|← arrow|
|Open file or toggle folder|Enter|
|Quick peek preview|Space \(press Esc to close\)|
|Move focus up or down|↑ / ↓|
|Delete focused item|Del|
|Reveal active file in tree|Cmd+Shift+E|
|Jump to a file by name|Cmd+P \(Quick Open\)|

## Explorer keyboard shortcuts

The following table lists the Explorer keyboard shortcuts for macOS and Windows.

|Action|macOS|Windows|
|------|-----|-------|
|New file in folder|Cmd+N|Ctrl+N|
|New folder|Cmd+Shift+N|Ctrl+Shift+N|
|Rename|F2|F2|
|Duplicate file|Cmd+D|Ctrl+D|
|Select all|Cmd+A|Ctrl+A|
|Copy absolute path|Cmd+Shift+C|Ctrl+Shift+C|
|Copy relative path|Cmd+Shift+Option+C|Ctrl+Shift+Alt+C|
|Reveal active file in tree|Cmd+Shift+E|Ctrl+Shift+E|
|Focus explorer search|Cmd+Shift+F|Ctrl+Shift+F|
|Toggle dotfiles|Cmd+Shift+.|Ctrl+Shift+.|
|Undo last file operation|Cmd+Z|Ctrl+Z|

## Explorer panel context menu

Right-clicking the Explorer panel background, rather than a file, shows the panel-level actions in the following table.

|Action|Description|
|------|-----------|
|**Add Folder to Workspace**|Adds another project folder to the current workspace|
|**Expand All**|Expands all folders in the tree|
|**Collapse All**|Collapses all folders in the tree|
|**Show Dotfiles**|Toggles visibility of dotfiles such as `.env` and `.gitignore`|
|**Open Focused Root in Terminal**|Opens a terminal session at the project root|
|**Reveal Focused Root in Finder**|Opens the project root in Finder \(macOS\)|

## File and folder context menu

Right-clicking a file or folder reveals the actions in the following table.

|Action|Description|
|------|-----------|
|**New File**|Creates a new file inside the selected folder|
|**New Folder**|Creates a new subfolder|
|**Add Page…**|Scaffolds a new Lux page inside the project|
|**Add Extension Target…**|Adds a new extension target to the project|
|**Add Glide View Page…**|Scaffolds a new Glide View page|
|**Copy**|Copies the file or folder|
|**Cut**|Cuts the file or folder|
|**Duplicate**|Creates a copy of the file in the same location|
|**Copy Path**|Copies the absolute path to the clipboard|
|**Copy Relative Path**|Copies the path relative to the project root|
|**Reveal in Finder**|Opens the file location in Finder \(macOS\)|
|**Open in Terminal**|Opens a terminal session rooted at this folder|
|**Rename**|Renames the file or folder inline|
|**Delete**|Deletes the file or folder|

**Note:** **Add Page…**, **Add Extension Target…**, and **Add Glide View Page…** are unique to Lux Lab and scaffold the corresponding Lux application artifacts directly into your project.

## Inline run and preview icons

For files that support it, Lux Lab shows the action icons in the following table when you hover over the file in the Explorer tree.

|File type|Icon|Action|
|---------|----|------|
|Page file, for example `page.js`|View icon \(eye\)|Opens the page in the Preview panel|
|Server script|Play icon \(▶\)|Runs the server script|

These icons also appear on the parent folder of the file.

## File status markers

The Explorer reflects Git status using the color and badge markers in the following table.

|Color or marker|Meaning|
|---------------|-------|
|Green text|New file \(untracked or newly added\)|
|Yellow or amber text|Modified file|
|Gray text|Ignored by `.gitignore`|
|Badge with count|Folder contains N changed files|

## Filtering and searching files

Press Cmd+Shift+F while the Explorer panel is focused to filter the file tree by name. Enter a partial file or folder name, and the tree filters in real time. Press Escape to clear the filter.

## Moving, copying, and selecting files

-   Move: Drag a file onto a destination folder to move it.
-   Copy: Hold Option \(macOS\) or Ctrl \(Windows\) while dragging to copy.
-   Multi-select: Hold Cmd \(macOS\) or Ctrl \(Windows\) and select multiple files, or use Shift+click for a range.

