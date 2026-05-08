---
title: Configure App Engine Studio
description: App Engine Studio \(AES\) guided setup provides a sequence of tasks that help you configure AES on your ServiceNow instance.
locale: en-US
release: australia
product: App Engine Studio
classification: app-engine-studio
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Configure, App Engine Studio, Building low-code applications, Developing your application, Building applications]
---

# Configure App Engine Studio

App Engine Studio \(AES\) guided setup provides a sequence of tasks that help you configure AES on your ServiceNow instance.

App Engine Studio must be installed on the instances where you expect to be developing your applications. In earlier versions, you were required to install AES on all instances in your pipeline.

If you plan on cloning your production instance to one or more non-production instances, you should also install the AES product on your production instance prior to cloning. For more information, see Instance Clone.

<table id="table_pdv_qb1_15b"><thead><tr><th>

Learn more about AES configuration

</th><th>

Additional ServiceNow resources

</th></tr></thead><tbody><tr><td rowspan="3">

ServiceNow provides several additional resources on configuring and administering App Engine Studio.

</td><td>

![](../../../reuse/icons/brand-icons/bus-try-a-demo.svg) App Engine Studio release notes

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-3-person.svg) [ServiceNow Community site](https://community.servicenow.com/community?id=community_search&q=app%20engine%20studio&spa=1)

</td></tr><tr><td>

![](../../../reuse/icons/brand-icons/bus-webinar.svg) [App Engine Studio video on adding security](https://www.youtube.com/watch?v=7qdHbzVcmoI&list=PLCOmiTb5WX3ptBi7tdjmAGwx8EhgcTp9o&index=7)

</td></tr></tbody>
</table>## Guided setup to configure AES

To open App Engine Studio guided setup, navigate to **All** &gt; **App Engine** &gt; **App Engine Studio** &gt; **Configuration** &gt; **Guided Setup**.

The landing page provides information on the different tools and user access. Select the **Get Started** button in the top, right corner to start your configuration. ![App Engine Studio guided setup configuration categories](../image/aes-guided-setup-sections.png)

The App Engine Studio Guided Setup page provides a list of different categories. Select the **Get Started** button under each category to start configuring App Engine Studio.

**Note:** If you have previously started any of the guided setup tasks, and then exited without completing them, the **Get Started** button is labeled **Continue**.

For detailed instructions on any of the tasks initiated from guided setup, see the [Perform AES configuration tasks](../reference/aes-config-tasks.md).

-   **[Configure AES personas and roles](aes-personas-roles.md)**  
The responsibilities of your staff are controlled by roles assigned to each member. Personas aren’t explicitly part of App Engine Studio \(AES\) but administrators assign roles to give team members permission to configure or use AES.
-   **[Perform AES configuration tasks](../reference/aes-config-tasks.md)**  
As you work through the App Engine Studio \(AES\) guided setup, you must perform different configuration tasks.
-   **[Delegate developers using AES](aes-app-dev-workflow.md)**  
Delegated development enables designated users without a system admin role to develop or deploy applications on the ServiceNow AI Platform. This enables administrators and delegated developers to work together to deliver custom applications through App Engine Studio \(AES\).
-   **[AES integration with a Git source control repository](aes-source-control-integration.md)**  
Enable application developers to integrate App Engine Studio \(AES\) with a Git source control repository to save and manage multiple versions of an application from a non-production instance.

**Parent Topic:**[Configuring App Engine Studio and related apps](aes-setup.md)

