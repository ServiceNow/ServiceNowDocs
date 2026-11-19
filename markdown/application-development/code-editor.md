---
title: Code editor
description: The Code Editor is the central workspace in Lux Lab. It provides syntax highlighting, context-aware code completion, multi-file navigation, and integration with the Lux platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/application-development/code-editor.html
release: australia
topic_type: concept
last_updated: "2026-09-30"
reading_time_minutes: 5
keywords: [Code editor, Editor layout and tabs, Syntax highlighting and language support, IntelliSense and code completion, Code folding and minimap, Multi-cursor and multi-selection, Find and replace in a file, Editor keybindings, Diff view]
breadcrumb: [Exploring Lux Lab, Lux Lab, Building pro-code applications, Developing your application, Building applications]
---

# Code editor

The Code Editor is the central workspace in Lux Lab. It provides syntax highlighting, context-aware code completion, multi-file navigation, and integration with the Lux platform.

## Editor layout and tabs

## Tabs

Each open file is represented by a tab in the tab bar. Tabs support the following interactions:

-   Dragging to reorder
-   Right-click for tab-specific actions, such as close, close others, close to the right, pin, and copy path
-   Middle-click to close a tab
-   Pinned tabs, which stay in the tab bar and cannot be closed accidentally

## Preview mode

Files you open with a single click in the Project Explorer open in preview mode, with the tab title in italics. The next file you open replaces a preview tab. Double-click the tab or start typing to promote it to a permanent tab.

## Tab groups and split views

You can split the editor to view multiple files side by side in the following ways:

-   Split Right: Select and hold \(or right-click\) a tab and select **Split Editor Right**, or press Cmd+\\ \(macOS\) / Ctrl+\\ \(Windows/Linux\).
-   Split Down: Right-click a tab and select **Split Editor Down**.

You can open as many editor groups as you need, and there's no enforced limit. Each group maintains its own tab list and scroll position. Drag tabs between groups to reorganize them. To close a split group, close all its tabs or drag the remaining tabs to another group.

For the steps to split the editor, see [Split the editor](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/application-development/split-the-editor.md).

## Breadcrumb navigation

A breadcrumb trail in each editor group shows the file path and the current symbol, such as a function, class, or component. Select any segment to navigate to that location.

## Syntax highlighting and language support

Lux Lab includes built-in grammar and highlighting support for the languages in the following table.

|Language|Extensions|
|--------|----------|
|TypeScript|`.ts`, `.tsx`|
|JavaScript|`.js`, `.jsx`, `.mjs`|
|HTML|`.html`|
|CSS and SCSS|`.css`, `.scss`|
|JSON|`.json`, `.jsonc`|
|Markdown|`.md`|
|YAML|`.yaml`, `.yml`|
|XML|`.xml`|

Language detection is automatic, based on the file extension. To override the detected language, select the language indicator in the status bar.

## IntelliSense and code completion

Lux Lab provides language server-based, context-aware completions as you type, using the same IntelliSense engine as VS Code.

## Triggering completions

-   Completions appear automatically after a short delay.
-   Press Ctrl+Space to trigger the completion list manually at any time.
-   Use Tab or `Enter` to accept the selected suggestion.
-   Press Escape to dismiss.

## Parameter hints

When calling a function, press Cmd+Shift+Space \(macOS\) / Ctrl+Shift+Space \(Windows/Linux\) to see parameter documentation inline.

## Go to definition

The following table lists the shortcuts for navigating to a definition.

|Action|macOS|Windows|
|------|-----|-------|
|Go to definition|F12 or Cmd+Click|F12 or Ctrl+Click|
|Peek definition \(inline pop-up\)|Option+F12|Alt+F12|

## Code folding and minimap

## Folding

Folding collapses blocks of code to reduce visual noise. The following table lists the folding shortcuts.

|Action|Shortcut|
|------|--------|
|Fold the current block|Cmd+Option+\[ / Ctrl+Shift+\[|
|Unfold the current block|Cmd+Option+\] / Ctrl+Shift+\]|
|Fold all|Cmd+K, Cmd+0|
|Unfold all|Cmd+K, Cmd+J|
|Fold level N \(1–7\)|Cmd+K, Cmd+N|

Folding indicators, shown as chevrons, appear in the gutter when you hover over a foldable region.

## Minimap

The minimap in the editor gives a condensed view of the entire file. Select anywhere on the minimap to jump to that position. To hide the minimap, right-click it and select **Hide Minimap**, or toggle it in **App Settings** &gt; **Editor** &gt; **Show Minimap**.

## Multi-cursor and multi-selection

## Adding cursors

The following table lists the shortcuts for adding cursors.

|Action|Shortcut|
|------|--------|
|Add cursor above|Cmd+Option+↑ / Ctrl+Alt+↑|
|Add cursor below|Cmd+Option+↓ / Ctrl+Alt+↓|
|Add cursor at click position|Option+Click / Alt+Click|
|Add cursors to all occurrences of selection|Cmd+Shift+L / Ctrl+Shift+L|
|Add next occurrence of selection|Cmd+D / Ctrl+D|
|Skip current occurrence|Cmd+K, Cmd+D / Ctrl+K, Ctrl+D|

## Column \(box\) selection

Hold `Shift+Option` \(macOS\) or Shift+Alt \(Windows/Linux\) and drag to create a rectangular selection across multiple lines.

## Find and replace in a file

The following table lists the find and replace shortcuts.

|Action|Shortcut|
|------|--------|
|Open Find|Cmd+F / Ctrl+F|
|Open Find and Replace|Cmd+H / Ctrl+H|
|Next match|Enter or F3|
|Previous match|Shift+Enter or Shift+F3|
|Toggle case sensitive|Cmd+Option+C / Alt+C|
|Toggle whole word|Cmd+Option+W / Alt+W|
|Toggle regex|Cmd+Option+R / Alt+R|
|Replace current|Cmd+Option+E / Alt+E|
|Replace all|Cmd+Option+A / Alt+A|

## Editor keybindings

The following table lists the essential editor shortcuts for macOS and Windows/Linux.

|Action|macOS|Windows/Linux|
|------|-----|-------------|
|Open command palette or quick open|`Cmd+Shift+P`|`Ctrl+Shift+P`|
|Go to file|`Cmd+P`|`Ctrl+P`|
|Search in all files|`Cmd+Shift+F`|`Ctrl+Shift+F`|
|Save file|`Cmd+S`|`Ctrl+S`|
|Undo|`Cmd+Z`|`Ctrl+Z`|
|Redo|`Cmd+Shift+Z`|`Ctrl+Y`|
|Cut line|`Cmd+X`|`Ctrl+X`|
|Copy line|`Cmd+C`|`Ctrl+C`|
|Delete line|`Cmd+Shift+K`|`Ctrl+Shift+K`|
|Move line up|`Option+↑`|`Alt+↑`|
|Move line down|`Option+↓`|`Alt+↓`|
|Duplicate line down|`Shift+Option+↓`|`Shift+Alt+↓`|
|Comment or uncomment|`Cmd+/`|`Ctrl+/`|
|Block comment|`Shift+Option+A`|`Shift+Alt+A`|
|Format document|`Shift+Option+F`|`Shift+Alt+F`|
|Go to line|`Cmd+G`|`Ctrl+G`|
|Navigate back|`Cmd+[`|`Alt+←`|
|Navigate forward|`Cmd+]`|`Alt+→`|
|Split editor|`Cmd+\`|`Ctrl+\`|
|Toggle file explorer|`Cmd+B`|`Ctrl+B`|
|Toggle AI chat panel|`Cmd+Shift+B`|`Ctrl+Shift+B`|
|Toggle bottom panel|`Cmd+J`|`Ctrl+J`|
|Toggle terminal|`Ctrl+`` \| `Ctrl+``| |

## Diff view

You can compare two files or check changes against the last committed version in the following ways:

-   Compare with saved: Right-click a modified file in the Explorer and select **Compare with Saved**.
-   Compare with branch: Right-click and select **Compare with Branch…** to diff against any Git ref.
-   Source control diff: Select a changed file in the Source Control panel to open an inline diff.

In the diff view, use F7 / Shift+F7 to jump between changed hunks.

