---
title: ServiceNow Studio user interface
description: Use the ServiceNow Studio interface to build, manage, and deploy custom, base system, or global applications and global metadata records. Customize the interface to match your workflow.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/servicenow-studio-classic/servicenow-studio-user-interface.html
release: brazil
product: ServiceNow Studio Classic
classification: servicenow-studio-classic
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Explore, ServiceNow Studio, Developing your application, Building applications]
---

# ServiceNow Studio user interface

Use the ServiceNow Studio interface to build, manage, and deploy custom, base system, or global applications and global metadata records. Customize the interface to match your workflow.

Access requires an admin or delegated\_developer role with access to at least one application.

## What is on the ServiceNow Studio home page?

The home page provides access to all tools and services in ServiceNow Studio.

-   The main home page shows the Build Agent chat panel, where you can begin creating, updating, or enhancing applications with AI. For more information, see [Exploring Build Agent](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/exploring-build-agent.md).

    \[Omitted image "sn-studio-ba-chat.png"\] Alt text: Start creating and updating apps directly from the home page.

-   The Navigator panel enables you to access Build Agent, apps, metadata records, recently opened files, and more. Plan and create apps, create collections, and manage deployments from the Navigator panel. Filter or sort the lists, or select **Open list** to open any list in the platform view.

    \[Omitted image "sn-studio-full-nav-panel.png"\] Alt text: The navigator panel contains apps, metadata records, collections, and much more.

-   The Activity bar enables you to switch between features to access development tools.

    \[Omitted image "sn-studio-activity-bar.png"\] Alt text: Access the activity bar in the navigator panel.

    |Icon|Navigation item|Description|
    |----|---------------|-----------|
    |\[Omitted image "sn-studio-home-icon.png"\] Alt text:|Home|Return home to the ServiceNow Studio homepage from other tabs.|
    |\[Omitted image "sn-studio-explorer-icon.png"\] Alt text:|Explorer|Work on apps in source code.|
    |\[Omitted image "sn-studio-conversations-icon.png"\] Alt text:|Conversations|Navigate to conversations you have had with Build Agent.|
    |\[Omitted image "sn-studio-plans-icon.png"\] Alt text:|Plans|View all the plans Build Agent has created during conversations.|
    |\[Omitted image "sn-studio-search-icon.png"\] Alt text:|Search|Search for any file, app, metadata, or tool in any scope on the platform.|
    |\[Omitted image "sn-studio-create-icon.png"\] Alt text:|Create|Create an app or file.|
    |\[Omitted image "sn-studio-apps-icon.png"\] Alt text:|Apps|View all apps.|
    |\[Omitted image "sn-studio-file-categories-icon.png"\] Alt text:|File Categories|View, sort, and filter all files and metadata.|
    |\[Omitted image "sn-studio-collections-icon.png"\] Alt text:|Collections|Access organized collections of bookmarks, files, and apps.|
    |\[Omitted image "sn-studio-recent-icon.png"\] Alt text:|Recent|Access recently opened files.|
    |\[Omitted image "sn-studio-deployment-icon.png"\] Alt text:|Deployment|Access a list of deployment requests, update sets, and applications.|
    |\[Omitted image "sn-studio-changes-icon.png"\] Alt text:|Changes|View changes associated with source control.|
    |\[Omitted image "sn-studio-settings-icon.png"\] Alt text:|User profile|Open the user profile menu, where you can elevate your role and view the ServiceNow Studio command palette, keyboard shortcuts, and user preferences.|

-   The **User profile** icon \[Omitted image "sn-studio-settings-icon.png"\] Alt text: in the activity bar provides access to the ServiceNow Studio command palette, a list of keyboard shortcuts, and user preferences. You can elevate your role, select light or dark theme, andchoose whether you want to use Build Agent as your default AI-assisted app generation tool.

    **Note:** For more information about elevating your role to security\_admin, see [Elevate your role in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/elevate-your-role-in-servicenow-studio.md).

    For more information, see [ServiceNow Studio settings](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/servicenow-studio-settings.md).

    \[Omitted image "sn-studio-settings-menu.png"\] Alt text: The user profile menu provides access to the Command palette, keyboard shortcuts, and preferences.


## How do I view the scope and update set?

When you have an app or file open, the status bar shows the current scope and the update set associated with the application. To change the update set or create one, open the default update set and select a different one directly within the app.To see all updates associated with the current update set, select **View update set**.

For more information, see [Update sets in ServiceNow Studio](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/application-development/servicenow-studio-classic/working-with-update-sets-in-servicenow-studio.md).

\[Omitted image "sn-studio-scope-update-set-bs1.png"\] Alt text: Each app shows its scope and update set at the bottom of the canvas. Select a new update set or create one to change it.

