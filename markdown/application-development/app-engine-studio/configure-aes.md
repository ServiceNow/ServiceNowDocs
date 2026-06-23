---
title: Configure App Engine Studio
description: App Engine Studio \(AES\) guided setup provides a sequence of tasks that help you configure AES on your ServiceNow instance.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/application-development/app-engine-studio/configure-aes.html
release: xanadu
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configuring App Engine Studio and related apps, Build apps using App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure App Engine Studio

App Engine Studio \(AES\) guided setup provides a sequence of tasks that help you configure AES on your ServiceNow instance.

App Engine Studio must be installed on the instances where you expect to be developing your applications. In earlier versions, you were required to install AES on all instances in your pipeline.

If you plan on cloning your production instance to one or more non-production instances, you should also install the AES product on your production instance prior to cloning. For more information, see [System clone](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-administration/c_SystemClone.md).

<table id="table_pdv_qb1_15b"><thead><tr><th>

Learn more about AES configuration

</th><th>

Additional ServiceNow resources

</th></tr></thead><tbody><tr><td rowspan="3">

ServiceNow provides several additional resources on configuring and administering App Engine Studio.

</td><td>

\[Omitted image "bus-try-a-demo.svg"\] Alt text: [App Engine Studio release notes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/release-notes/app-engine-studio-rn.md)

</td></tr><tr><td>

\[Omitted image "bus-3-person.svg"\] Alt text: [ServiceNow Community site](https://community.servicenow.com/community?id=community_search&q=app%20engine%20studio&spa=1)

</td></tr><tr><td>

\[Omitted image "bus-webinar.svg"\] Alt text: [App Engine Studio video on adding security](https://www.youtube.com/watch?v=7qdHbzVcmoI&list=PLCOmiTb5WX3ptBi7tdjmAGwx8EhgcTp9o&index=7)

</td></tr></tbody>
</table>## Guided setup to configure AES

To open App Engine Studio guided setup, navigate to **All** &gt; **App Engine** &gt; **App Engine Studio** &gt; **Configuration** &gt; **Guided Setup**.

The landing page provides information on the different tools and user access. Select the **Get Started** button in the top, right corner to start your configuration. \[Omitted image "aes-guided-setup-sections.png"\] Alt text: App Engine Studio guided setup configuration categories

The App Engine Studio Guided Setup page provides a list of different categories. Select the **Get Started** button under each category to start configuring App Engine Studio.

**Note:** If you have previously started any of the guided setup tasks, and then exited without completing them, the **Get Started** button is labeled **Continue**.

For detailed instructions on any of the tasks initiated from guided setup, see the [Perform AES configuration tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/aes-config-tasks.md).

-   **[Configure AES personas and roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/aes-personas-roles.md)**  
The responsibilities of your staff are controlled by roles assigned to each member. Personas aren’t explicitly part of App Engine Studio \(AES\) but administrators assign roles to give team members permission to configure or use AES.
-   **[Perform AES configuration tasks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/aes-config-tasks.md)**  
As you work through the App Engine Studio \(AES\) guided setup, you must perform different configuration tasks.
-   **[Delegate developers using AES](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/aes-app-dev-workflow.md)**  
Delegated development enables designated users without a system admin role to develop or deploy applications on the ServiceNow AI Platform. This enables administrators and delegated developers to work together to deliver custom applications through App Engine Studio \(AES\).
-   **[AES integration with a Git source control repository](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/aes-source-control-integration.md)**  
Enable application developers to integrate App Engine Studio \(AES\) with a Git source control repository to save and manage multiple versions of an application from a non-production instance.

**Parent Topic:**[Configuring App Engine Studio and related apps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/application-development/app-engine-studio/aes-setup.md)

