---
title: ServiceNow IDE release notes
description: Version history for the ServiceNow IDE application on the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/store-release-notes/store-platcap-rn-servicenow-ide.html
release: store
topic_type: reference
last_updated: "2026-06-11"
reading_time_minutes: 10
breadcrumb: [ServiceNow Store - Other ServiceNow AI Platform Capabilities applications, ServiceNow Store - ServiceNow AI Platform Capabilities release notes, ServiceNow Store release notes]
---

# ServiceNow IDE release notes

Version history for the ServiceNow® IDE application on the ServiceNow Store.

**Important:** For details on system requirements and family compatibility, view the application listing on the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website.

## Version history

-   **Version 4.3.2 - June 2026**
    -   New:
        -   Collections Management is now available in ServiceNow Studio. Users can create, rename, and delete collections to organize applications and files, add items from multiple entry points, and initiate Build Agent conversations directly from a collection. Collections persist across sessions, display in a dedicated tab, and unify workspace navigation.
        -   Collections pane now integrated. The Collections pane replaces Bookmarks in navigation, providing accessible, well-formatted collection display with loading, error, and empty states. All collection-related interactions and data now use the unified Collections model.
        -   Build Agent supports deep linking from the Developer Site to ServiceNow Studio. When redirected from the Developer Site, Build Agent now accepts and executes deep-linked text prompts for creating or editing applications, preserving the original prompt and context without requiring a new conversation.
-   **Version 4.2.5 - May 2026 \(Australia\)**
    -   New:
        -   ServiceNow Studio
            -   Switch between all UI pages within your application scope from a menu in the preview header.
            -   Share or bookmark a specific UI page preview state with your team with deep links for preview tabs.
            -   Configure preview URLs and paths in application taxonomy builder records to control how your application pages are previewed.
            -   Open and navigate between multiple Flow Designer pages with improved performance and rendering.
            -   Get diagnostics automatically when a UI page is created or updated.
            -   Get a notification when you reach the maximum number of open tabs.
    -   Fixed:
        -   ServiceNow Studio
            -   Record URLs weren't updating to reflect newly created records when using the Insert and Stay option.
        -   ServiceNow IDE
            -   Applications required syncing after creation before they could be built or deployed.
            -   Table schemas didn't display in the source code view of a table.
-   **Version 4.2.4 - May 2026**
    -   New:
        -   ServiceNow Studio
            -   Switch between all UI pages within your application scope from a menu in the preview header.
            -   Share or bookmark a specific UI page preview state with your team with deep links for preview tabs.
            -   Configure preview URLs and paths in application taxonomy builder records to control how your application pages are previewed.
            -   Open and navigate between multiple Flow Designer pages with improved performance and rendering.
            -   Get diagnostics automatically when a UI page is created or updated.
            -   Get a notification when you reach the maximum number of open tabs.
    -   Fixed:
        -   ServiceNow Studio
            -   Record URLs weren't updating to reflect newly created records when using the Insert and Stay option.
        -   ServiceNow IDE
            -   Applications required syncing after creation before they could be built or deployed.
            -   Table schemas didn't display in the source code view of a table.
-   **Version 4.1.1 - April 2026**
    -   Fixed:
        -   ServiceNow IDE
            -   Changed lines of code were not visually highlighted in the Git diff view.
            -   The Select All \(Cmd+A / Ctrl+A\) keyboard shortcut was unresponsive in the editor.
            -   VS Code terminal panel incorrectly appeared on every open tab instead of only when explicitly opened.
            -   Opening a UI Page without existing ServiceNow Fluent source files attempted to open the source code view instead than the Core UI view.
            -   Reopening a UI page that already had Fluent source files would incorrectly re-install all dependencies from scratch.
            -   Race conditions caused file and editor tabs to enter an inconsistent state when opening multiple UI pages simultaneously or closing a tab mid-installation.
            -   Multiple stability fixes including: status bar spinner during builds, corrected scope status bar on project open, auto-build on open to resolve dependency path issues, selective error display for Build Automation, and proper activity bar visibility in SNS mode.
        -   ServiceNow Studio
            -   Deep links to the ServiceNow Studio home page weren't resolving correctly.
            -   Missing translation support across the ServiceNow Studio interface.
            -   Newly created Catalog Items couldn't be saved due to an error during the save operation.
            -   Metadata records opened in new tabs instead of the existing active tab.
-   **Version 4.0.6 - March 2026**
    -   Changed:
        -   ServiceNow Studio and ServiceNow IDE are now available together in a single plugin and installed simultaneously.
        -   ServiceNow Studio and ServiceNow IDE are compatible with the freemium and full versions of Build Agent, available as a separate plugin. See the Build Agent listing in the ServiceNow Store for more information.
-   **Version 3.3.0 - January 2026**
    -   Fixed:
        -   The Git commit history tree could block extensions in the ServiceNow IDE.
        -   REST API size limits could be deleted.
        -   Application conversion could fail when required dependencies were not installed.
-   **Version 3.1.4 - November 2025**

    Fixed: Minor bug fixes.

-   **Version 3.1.3 - October 2025**

    Fixed: Minor bug fixes.

-   **Version 3.1.1 - September 2025**
    -   Fixed:
        -   ServiceNow SDK version displayed in output logs didn't match the version loaded.
        -   Deleting staged files also removed them from the staged state.
        -   Deleted files couldn't be staged.
        -   Applications couldn't be converted after a reset.
        -   Infinite streaming in the Git output when building applications.
        -   Button styles didn't match the new now-button design system for Developer themes.
-   **Version 3.0.0 - August 2025**
    -   New:
        -   Clone a Git repository that contains multiple applications that support development in source code.
        -   Use the Developer Light \(default\) and Developer Dark themes in the ServiceNow IDE.
        -   Use the ServiceNow IDE in any supported left-to-right language.
        -   Use the latest version of the ServiceNow SDK in new or converted applications by default.
    -   Fixed:
        -   Cloning pulled only the last commit.
        -   Converted applications appeared as Code ready: False and couldn't be re-converted.
        -   Git operations performance issues.
-   **Version 2.1.2 - June 2025**

    Minor stability fixes. No major features or breaking changes.

-   **Version 2.1.1 - May 2025**
    -   ServiceNow IDE version 2.1 delivers meaningful improvements across the board-faster syncs, better Fluent handling, and a cleaner development experience. With key improvements and a stack of resolved issues, this release is all about making your workflow smoother and smarter.
    -   New:
        -   Uninstall and reinstall an application \(now-sdk deploy -r\) in the IDE.
        -   Load specific versions of Fluent and Fluent extensions.
        -   Build fails if Fluent diagnostics contain errors.
        -   Removed duplicate commands for cleaner UI.
        -   Git repository initialization prompt added for first-time syncs to allow user to integrate changes.
        -   Sync now only retrieves changes by default instead of complete application to speed up the process.
    -   Fixed:
        -   Fixed issues with sync triggering unnecessarily after app conversion.
        -   Git credential issues and unreadable token errors resolved.
        -   Corrected package.json link behavior and Git file permission bugs.
        -   Resolved various sync issues and context menu glitches.
        -   Numerous stability improvements and UI polish.
-   **Version 2.0.4 - March 2025**
    -   Fixed:
        -   Problem and Short description:
            -   PRB1859983: Convert directory not working on Windows
            -   PRB1851283: Sync not working properly for user with sn\_glider.ide\_git\_user role only
            -   PRB1847972: Metadata Explorer: Create View Can't Load
            -   PRB1845595: Builder unexpectedly launches new window in Metadata Explorer
            -   PRB1845567: Metadata Explorer not updating after new record creation
            -   PRB1845566: Missing DOM/Document library types in TypeScript language server
            -   PRB1845564: \[Metadata Explorer\] Do not ask user to select an app if there's only 1 app open or if it's launched from the app
            -   PRB1844801: Users should have an option to forcibly remove all files for an application
            -   PRB1844793: Metadata Exporer: Flows and Subflows incorrectly grouped
            -   PRB1844742: Flow Designer not loading in Metadata Explorer
            -   PRB1842719: \[Git Source Control\] Not able to push to git through MID server
            -   PRB1840612: Dependencies package.json section giving warnings despite valid pinned versions inputted
            -   PRB1839658: Error when installing dependencies with scopedRegistry
            -   PRB1838789: Package manager doesn't update dependency if version is changed in package.json
            -   PRB1837455: \[Git Source Control\] Git pull with merge conflicts overwrite/overlap current changes
            -   PRB1827524: Git Relay Attachment file extension being nil
            -   PRB1827023: Create Metadata: Application filter is case sensitive
-   **Version 2.0.1 - February 2025**
    -   New:
        -   Convert existing scoped applications to develop them in source code from the ServiceNow IDE
        -   Use packages from private NPM registries as third-party libraries
        -   Use TypeScript to create JavaScript modules
    -   Fixed: General stability and performance improvements
-   **Version 1.1.20 - January 2025**
    -   New: Introduced the sn\_glider.ide\_git\_user role for using source control in the ServiceNow IDE
    -   Fixed:
        -   Issues with Git connectivity for certain Git operations
        -   Fluent Language Server error messages
-   **Version 1.1.4 - December 2024**
    -   Fixed:
        -   PRB1826451: Reopening IDE misses sync alert for off-time metadata updates
        -   PRB1826261: Navigating metadata or clicking "IDE home" icon causes a page error
        -   PRB1825978: Auto-sync is still working
        -   PRB1825945: IDE now should be available to all instance types
        -   PRB1825448: Upgrading pre-1.1.1 app version to 1.1.1 version breaks workspace
        -   PRB1825427: glide.disable.coop\_and\_coep is set to false
        -   PRB1825303: Fix metadata explorer UI - Update Create Metadata Component to latest design
        -   PRB1824948: \[Eslint\] Initial eslint file not created with '.json' extension
        -   PRB1824859: \[GIT\] Resolved changes not picked by GIT
        -   PRB1824229: \[Git Source Control\] Git repositories not initialized on incognito
        -   PRB1824222: Issues with manual sync for an app when workspace has multiple apps .
        -   PRB1824197: \[GIT\] Performance issue when multiple apps with git repos opened in one workspace
        -   PRB1824185: Missed logo \(browser tab\) for IDE
        -   PRB1822225: \[GIT\] Failed to bootstrap a scoped app based on that repo. Could not find HEAD
        -   PRB1821922: Re-clone breaks source control and related features
        -   PRB1821915: IDE not working for on-prem and regulated markets
        -   PRB1810980: Cannot create new asset in metadata explorer
        -   PRB1805744: Building Llama App in IDE deleting the app
        -   PRB1800287: Store Application icons do not load on application manager due to COEP property set as false by IDE
        -   PRB1795880: \[Git Source Control\] Cloning from gitlab requires ".git" suffix
        -   PRB1762551: \[Git Source Control\] Source Control diff does not differentiate between staged and unstaged changes
-   **Version 1.1.0 - November 2024**
    -   New:
        -   Install and use the ServiceNow IDE on personal developer instances \(PDIs\) obtained from developer.servicenow.com.
        -   Connect to Azure Repos using OAuth 2.0 authentication.
    -   Fixed:
        -   PRB1802818: Cannot clone repo where now.config.json uses "fluentDir" key
        -   PRB1810386: Broken IDE Welcome page
        -   PRB1797490: On windows machine, Fluent language server doesn't work properly
        -   PRB1806943: No watcher found - console error
        -   PRB1793051: Interacting with IDE should keep user session alive
-   **Version 1.0.17 - October 2024**
    -   Fixed:
        -   PRB1802920 - Support Azure Repos
        -   PRB1802818 - Cannot clone repo where now.config.json uses "fluentDir" key
-   **Version 1.0.16 - September 2024**
    -   New: OAuth now supported for git authentication
    -   Fixed:
        -   PRB1796331: IDE - Git Checkout is not working
        -   PRB1795880: \[Git Source Control\] Cloning from gitlab requires ".git" suffix
        -   PRB1795878: \[Git Credentials\] Rename different command palette credentials options
        -   PRB1795845: Last opened workspace will not open again
        -   PRB1795416: Oauth flow should work for more git providers
        -   PRB1795411: Hanging progress messages on remote git operations
        -   PRB1794847: Loading spinner doesn't spin when loading iFrames
        -   PRB1794301: Restrict the IDE on self hosted/on-prem instances
        -   PRB1793781: \[Git source control\] Escape button error message while git clone
        -   PRB1792783: \[Git source control\] Git pull operation does not provide details on completion
        -   PRB1792174: User information does not refresh unless browser cache is completely cleared
        -   PRB1792148: IDE should inform user that PDI instances are not supported
        -   PRB1791914: Fix the OAuth flow for GitHub integration with the IDE
        -   PRB1789092: \[Git\] Shallow clone not purged from IndexedDB after sanity check
        -   PRB1788968: \[Git source control\] Invalid git branch name notification "Configure" button
        -   PRB1788707: No active scoped application in the workspace should display no scope information
        -   PRB1788451: Issues with Discard Changes in Command Palette
        -   PRB1788442: Can edit code when session is already expired
        -   PRB1788150: Cloned repo is not recognized as a fluent application
        -   PRB1783495: \[Eslint\] IDE settings for eslint does not work
        -   PRB1774809: Glider workspace should be by user and not shared
        -   PRB1765102: "'Null Extension Description" when opening app in IDE
        -   PRB1762993: \[linting\] using gs without importing module does not present linting error
-   **Version 1.0.14 - August 2024**

    Create and develop scoped applications in source code in an integrated development environment \(IDE\) on the ServiceNow AI Platform to improve collaboration across development teams and accelerate application development. The ServiceNow IDE is an implementation of Visual Studio Code for the Web on the ServiceNow AI Platform. With the ServiceNow IDE, you can get started building scoped applications quickly using familiar tools and industry-standard development practices. With ServiceNow Fluent, a domain-specific language for defining application metadata, you can manage and maintain the source code for your applications in your favorite Git-based source control provider directly from the ServiceNow IDE.


**Parent Topic:**[ServiceNow Store - Other ServiceNow AI Platform Capabilities applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/store/markdown/store-release-notes/store-platcap-rn-other-landing.md)

