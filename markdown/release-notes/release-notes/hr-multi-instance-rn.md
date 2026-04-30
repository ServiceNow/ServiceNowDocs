---
title: HR Multi Instance Integration release notes
description: The ServiceNowHR Multi Instance Integration centralizes the delivery of HR services in a shared services model, enabling consumers and providers to connect their instances to securely build business workflows across the ServiceNow ecosystem. HR Multi Instance Integration is a new application in the Zurich release.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 4
---

# HR Multi Instance Integration release notes

The ServiceNow®HR Multi Instance Integration centralizes the delivery of HR services in a shared services model, enabling consumers and providers to connect their instances to securely build business workflows across the ServiceNow ecosystem. HR Multi Instance Integration is a new application in the Zurich release.

## HR Multi Instance Integration highlights for the Zurich release

-   Collaborate with service providers and consumers through bidirectional workflows.
-   Increase the security of records in consumer instances and provider instances by limiting access based on user roles.
-   Enable an employee to place an HR service request from a consumer instance and fulfill the request from provider instance, making it easy to raise and fulfill HR requests while working in their own ServiceNow instance.
-   Create HR tasks, approval tasks, and document tasks from a provider instance for users in a consumer instance.
-   Enable consumer users to complete the assigned tasks via magic links. Magic links enable consumer users to directly access the linked resource in the provider instance without having to manually log in.
-   Use Universal Task as the remote tasking medium in both provider instance and consumer instance.

See [HR Multi Instance Integration](https://www.servicenow.com/docs/access?context=multi-instance-int&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US) for more information.

**Important:** HR Multi Instance Integration is available in the ServiceNow Store. For details, see the "Activation information" section of these release notes.

## HR Multi Instance Integration features

-   **[HR Multi Instance Integration](https://www.servicenow.com/docs/access?context=multi-instance-int&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Partners and service providers for HR service fulfillment often are running their own instance of HR Service Delivery. HR Multi Instance Integration provides inter-instance communication and hybrid HR services with fulfillment in different instances through the following capabilities:

    -   Ability to control your organization employee’s experience and interactions per your organization's culture, branding, and policies.
    -   Ability to outsource services.
    -   Consistent user experience for employees across the entire HR catalog, regardless of whether they are interacting locally or remotely from any third-party provider.
    -   Because HR workflows or business process are not restricted to a single instance, they can flow seamlessly across instances.
    -   Uniformity and standardization for HR agents on the provider instance enables them to work on local cases or remote HR cases from the provider’s ServiceNow AI Platform instance with a minimal learning curve.
    -   Managing and controlling access at the remote catalog level to meet security and compliance requirements.
    -   Synchronization of relevant information such as submitted request \(provider task\) status, comments, and attachments by service providers.
    -   Ability to fulfill an HR case partially by providers and partially by consumers.
    -   Ability to create HR tasks and approval tasks for remote HR cases.

        **Note:** Only manual approval flow is supported, and not the automatic approval flow.

    -   Initiate document signing tasks for remote users via universal tasks. This feature is available only when the Document Template plugin is installed along with the HR Multi Instance Integration for Provider application.
    -   Enable remote users \(consumer users\) to complete HR tasks, document tasks, and approval tasks via magic links shared in universal tasks. Magic links route remote users to the provider instance for completing the assigned tasks.
    -   Support the **URL** task type in Universal Task. This task type enables you to specify a URL link that is shared in the universal task assigned to a local or remote user.
    -   Support the **External** field in the HR Profile data. When the HR profile belongs to an employee in consumer company, the **External** field is marked True.

## Activation information

If you are an HR service consumer, install the HR Multi Instance Integration for Consumer \(sn\_hr\_mii\_provider\) application, and if you are an HR service provider, install the HR Multi Instance Integration for Provider \(sn\_hr\_mii\_provider\) application by requesting them from the ServiceNow Store. Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Related ServiceNow applications and features

-   **[HR Service Delivery](https://www.servicenow.com/docs/access?context=hr-service-delivery-overview&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    Improve the employee service experience by automating HR interactions and providing a single platform for all HR services. Replace manual and siloed processes with cross-functional digital workflows for increased efficiency. Align business goals with employee needs, including onboarding, career growth, and other transitions.

-   **[Agent Workspace for HR Case Management](https://www.servicenow.com/docs/access?context=agent-ws-hr-case-mgmt-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    The ServiceNow® Agent Workspace for HR Case Management application enables you to interact with employees, respond to inquiries, and resolve issues quickly.

-   **[Employee Center](https://www.servicenow.com/docs/access?context=employee-center-landing-page&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    The ServiceNow® Employee Center portal connects systems across an enterprise within one destination site to provide a centralized employee portal. It requires minimal configuration and a wide variety of features to extend portal functionality.

-   **[Document Templates](https://www.servicenow.com/docs/access?context=document-templates-overview&version=zurich&pubname=zurich-employee-service-management&ft:locale=en-US)**

    With the ServiceNow® Document Templates application, you can create HTML and PDF document templates to generate standard letters or documents. You can automate and simplify the process of filling, signing, and reviewing a document online.


**Parent Topic:**[HR Service Delivery release notes](hr-service-delivery-landing.md)

