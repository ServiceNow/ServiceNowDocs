---
title: Version control
description: Version control is how you track, manage, and protect every change made to your application across its entire development lifecycle on the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/application-development/version-control.html
release: australia
topic_type: concept
last_updated: "2026-04-15"
reading_time_minutes: 1
keywords: [version control, application repositories, update sets, Git, development lifecycle]
breadcrumb: [Getting Started guide for developers, Building applications]
---

# Version control

Version control is how you track, manage, and protect every change made to your application across its entire development lifecycle on the ServiceNow AI Platform®.

Building apps on the ServiceNow AI Platform entails working with scripts, configurations, workflows, UI policies, business rules, and many other artifacts. This work usually happens across multiple instances and involves more than one person. Without version control, you have no reliable way to answer questions such as what changed, who changed it, when it changed, and whether you can undo it. Version control, whether through application repositories, update sets, or both, is the baseline that makes safe, traceable, and collaborative ServiceNow development possible.

ServiceNow supports two mechanisms for version control:

-   Application repositories: Git-based version control for scoped applications built in ServiceNow Studio. Every file in the app is tracked in an external Git repository such as GitHub or GitLab. This gives you full commit history, branching, pull requests, and integration with automated pipelines. This is the recommended approach for all scoped app development.
-   Update sets: XML-based change logs that capture configuration changes made on a ServiceNow instance. When you're ready to move those changes to another instance, you export the update set as an XML file, import it on the target instance, preview it, and then commit it. Update sets are best suited for non-scoped customizations and admin-driven configuration work.

-   **[Updating your app for a ServiceNow platform version](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/upgrading-your-app.md)**  
When ServiceNow releases a new platform version, your app may need updates to keep working correctly. Learn how platform upgrades affect your app helps you plan and complete the upgrade with confidence.

**Parent Topic:**[Getting Started guide for developers](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/application-development/getting-started-landing-page.md)

