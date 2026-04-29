---
title: Merge tool
description: The Diff Merge tool enables administrative users to compare differences between two versions of a record.
locale: en-US
release: australia
product: Team Development
classification: team-development
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Version records, Versions, Administer, Team Development, Planning your application, Building applications]
---

# Merge tool

The Diff Merge tool enables administrative users to compare differences between two versions of a record.

Administrators can compare field-level changes between two versions, apply changes using Move Right field-level copy functionality and then merge results, or choose to revert to the non-current version. You can access the Diff Merge tool by comparing versions, resolving conflicts, or resolving collisions, during development or after upgrades.

![Diff Merge tool allows you to Compare to Current.](../image/MergeToolComparetoVersion.png)

![Use the Script Editor for large text-based fields.](../image/MergeToolScriptEditor.png)

![Diff Merge tool - Compare to Current Script](../image/MergeToolComparetoCurrentScript.png)

## Accessibility Functions

The platform includes accessibility features that support [Web Content Accessibility Guidelines \(WCAG\) 2.0 level A](https://www.w3.org/WAI/WCAG20/quickref/?currentsidebar=%23col_customize&levels=aa%2Caaa) and make the interface accessible to users with disabilities. These features improve the user experience when accessing platform functions with [Using accessibility features](https://www.servicenow.com/docs/access?context=keyboard-accessibility&version=australia&pubname=australia-platform-user-interface&ft:locale=en-US).

In general, you can use the following set of standard keyboard navigation functions:

-   Press **Tab** to navigate major groupings in a pre-defined sequence, including moving between standard interface controls \(fields and lists\) in a module, or between records within a tab.
-   Press **Shift** **Tab** to move backwards in a pre-defined sequence.

Visually impaired users can navigate the Diff Merge tool. Screen readers can read all critical page content. All links and buttons can be reached when a section that is critical must be read. VoiceOver audible cues describe the content of the section that is necessary to read.

To enable accessibility functions, administrators should set these sys\_properties:

1.  Setting **glide.ui.javascript\_editor** to false makes the following functions accessible:
    -   Script fields \(such as Script Include\).
    -   Side-by-side script comparison.
2.  Setting sys\_properties color settings enables high contrast visibility, which makes the left and right columns more accessible and easier to read by visually impaired users.
    -   **mergetool.bg.left.highlight** - Left column cell color when values differ between versions.
    -   **mergetool.bg.right.highlight** - Right column cell color when values differ between versions.
    -   **mergetool.bg.left** - Left column cell color when version values are the same.
    -   **mergetool.bg.right** - Right column cell color when version values are the same.

**Parent Topic:**[Version records](../reference/r_VersionRecords.md)

**Related topics**  


[Compare to the current version](../task/t_CompareToCurrentVersion.md)

[Compare a pushed version to a local version](../task/t_ComparePushedVerLocalVer.md)

[Compare two versions of an article](https://www.servicenow.com/docs/access?context=compare-two-article-versions&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Resolve conflicts for an individual record](https://www.servicenow.com/docs/access?context=um-resolve-conflict&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

[Resolve a collision in Team Development](../task/t_ResolveACollision.md)

[Revert a change](../task/t_RevertAChange.md)

[View customizations and compare with current version](../../system-update-sets/task/view-customer-update-records.md)

