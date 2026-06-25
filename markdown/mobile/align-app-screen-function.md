---
title: Set up and align the app, screen, and function hierarchy for offline mode
description: ServiceNow mobile apps are organized into three hierarchical levels, apps, screens, and functions that work together to define the mobile experience for each user role. You can configure offline mode at each level, controlling what users can access and work on without network connectivity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/mobile/align-app-screen-function.html
release: australia
topic_type: concept
last_updated: "2026-05-31"
reading_time_minutes: 2
breadcrumb: [Offline mode setup options, Offline mode, Before implementation, Configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Set up and align the app, screen, and function hierarchy for offline mode

ServiceNow mobile apps are organized into three hierarchical levels, apps, screens, and functions that work together to define the mobile experience for each user role. You can configure offline mode at each level, controlling what users can access and work on without network connectivity.

ServiceNow mobile apps are structured at three levels: the app type, its screens and its functions.

-   **App level**

    The app level defines the overall mobile experience: who can use the app, its navigation tabs and their inner sections, themes, and whether it supports offline mode. For more information, see [ServiceNow mobile applications for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/apps-offline.md).

-   **Screen level**

    Multiple screens are contained within each app, which represent what users see and interact with, for example, lists, forms, and record views. For more information, see [Supported screens for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/screens-offline.md).

-   **Function level**

    Functions are contained within each screen. Functions define writeback actions, such as submitting a form, adding an attachment, or navigating to another screen. For more information, see [Supported functions for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/functions-offline.md).


Together, these elements create a complete and tailored mobile experience for every user role, both online and offline. You can enable or disable offline mode at the application, screen and function configuration level, determining what users can work on without network connectivity.

-   **[ServiceNow mobile applications for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/apps-offline.md)**  
Consider which native applications are available in offline mode. The available apps are Mobile Agent app, Now Mobile app or a custom branded app created through the Mobile Publishing plugin.
-   **[Supported screens for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/screens-offline.md)**  
Consider which screen types to use in offline mode.
-   **[Supported functions for offline mode](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/functions-offline.md)**  
Functions define the actions users can perform from a screen, such as tapping a button, icon, or menu option. In offline mode, only functions configured as available on offline are accessible to users without network connectivity.

**Parent Topic:**[Offline mode setup options](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/mobile/offline-setup-options.md)

