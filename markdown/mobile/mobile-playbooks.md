---
title: Mobile App Bridge
description: Learn about Mobile App Bridge, which can be used to enable seismic pages, service portal pages, or classic web pages on mobile web screens. You can use this feature to support a playbook on mobile web screens and to enable other components.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Considerations before implementation, ServiceNow Mobile Platform configuration detail, Configuring the Mobile Platform, Mobile Platform]
---

# Mobile App Bridge

Learn about Mobile App Bridge, which can be used to enable seismic pages, service portal pages, or classic web pages on mobile web screens. You can use this feature to support a playbook on mobile web screens and to enable other components.

The ServiceNow® platform provides a playbook feature that is supported on mobile devices by using the seismic component called Mobile App Bridge. Mobile App Bridge imports a new npm package that includes the Cabrillo JS module, creating a controller component that wraps the Mobile App Bridge data resource. This controller component enables access to the mobile/native bridge within the [UI Builder](https://www.servicenow.com/docs/access?context=ui-builder-overview&version=yokohama&pubname=yokohama-application-development&ft:locale=en-US) environment. It exposes all events and operations that you want end users to have access to on their mobile devices. This feature is designed to support a playbook on mobile web screens but can be used for other components. You can configure Now Experience Framework pages that contain playbook components in UI Builder.

For more information about platform playbooks, see [About Playbook Experience](https://www.servicenow.com/docs/access?context=playbook-ui&version=yokohama&pubname=yokohama-build-workflows&ft:locale=en-US).

-   **[Configure mobile web screens with Mobile App Bridge](../task/configure-mobile-playbooks.md)**  
Configure mobile web screens with Mobile App Bridge to enable seismic pages, classic web pages, or service portal pages that are hosted within embedded web views. Using this feature, you can access native mobile functionality on ServiceNow® mobile apps.

**Parent Topic:**[Considerations before implementation](imp-considerations.md)

