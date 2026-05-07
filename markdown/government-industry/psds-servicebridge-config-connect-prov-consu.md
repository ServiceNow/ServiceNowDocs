---
title: Set up a Service Exchange connection between a Provider and a Consumer
description: Establish an instance-to-instance integration between a provider and a consumer using Service Exchange for Public Sector Digital Services.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Exchange, Case Management, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Set up a Service Exchange connection between a Provider and a Consumer

Establish an instance-to-instance integration between a provider and a consumer using Service Exchange for Public Sector Digital Services.

## Before you begin

Role required: admin

A provider record must have been created. See [Set up a Service Exchange provider record](https://www.servicenow.com/docs/access?context=service-bridge-v2-new-provider&version=australia&pubname=australia-service-exchange&ft:locale=en-US).

A business or account must exist for the consumer in the provider’s instance, and a user or contact with the sn\_sb\_pro.consumer role must be associated with the company. A business or account must exist for the provider in the consumer’s instance.​ If this is a production instance, the user must have a valid email address to receive the registration email.

Run the **Key Management** &gt; **Health \(Diagnostics\)** to ensure that the Key Management Framework health check has passed. Your administrator must have the sn\_kmf.admin and sn\_kmf.cryptographic\_manager roles to access the health diagnostics. If your administrator does not have access, follow the instructions in [Assign Key Management Framework roles](https://www.servicenow.com/docs/access?context=assign-kmf-roles&version=australia&pubname=australia-platform-security&ft:locale=en-US) to grant the required roles.

## About this task

Before proceeding, the provider should have requested the contact details of an admin to set as the main point of contact on their registration record. This designated contact person will receive an email either from the provider's instance or directly from the provider's admin, containing a registration link. Selecting on this link will generate a Provider Connection record in your consumer instance.

## Procedure

1.  Navigate to **All** &gt; **Service Bridge Provider** &gt; **Consumer Registrations** and select **New**.

2.  On the form, fill in the fields:

    -   Select the Company associated with the consumer instance being registered.
    -   Select the contact details associated with the Company you have selected.

        **Note:** This contact must be an admin user in the consumer instance, otherwise the registration process cannot be completed. On the provider instance, only a Service Bridge Consumer role is required.

    -   Select the **Lock** icon on the URL field and enter the URL of the consumer ServiceNow instance.
3.  Select **Save**.

    An email is generated and sent to the Consumer Contact specified during registration if email sending is enabled. If not, the admin must either copy the link from the work notes and manually send it to the consumer admin. The Consumer Contact must follow the steps listed in the [Connect to a provider](https://www.servicenow.com/docs/access?context=service-bridge-v2-register&version=australia&pubname=australia-service-exchange&ft:locale=en-US) to complete the registration process on the consumer instance.

4.  Select the **Connect to Provider** link sent in the provider's registration email or follow the link given to you directly by the provider’s admin.

    This link will generate the Provider connection record.

    **Note:** The consumer admin completing the registration process must be the named contact on the provider’s registration task or an admin in the provider's instance. Registration will fail during the OAUTH authentication step if attempted by another user.

5.  Navigate to **All** &gt; **Service Bridge Consumer** &gt; **Provider Connections**.

6.  On the Provider Connection form in the consumer instance, select the name of the Company that the provider is associated with and select **Save**.

    The Provider Connection record is displayed.

7.  Select **Connect to Provider** in the Provider connection record page.

8.  Select **Authenticate** when the Service Exchange registration message appears.

    The OAuth authentication page appears.

9.  Select **Allow** and then select **Submit** to proceed with the registration.

    You are redirected to the Registration task where you can view the status. When registration is completed, a connection is established between the provider and the consumer instances, and the registration task State is set to **Closed Complete** on the provider's instance.


