---
title: Registering with a provider
description: Complete the registration process to establish a connection to the provider instance.
locale: en-US
release: xanadu
product: Service Bridge
classification: service-bridge
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Installing and configuring Service Exchange for Consumers, Service Exchange for Consumers, Service Exchange]
---

# Registering with a provider

Complete the registration process to establish a connection to the provider instance.

## Before you begin

-   Role required: admin
-   Run the **Key Management** &gt; **Health \(Diagnostics\)** to ensure that the Key Management Framework health check has passed. Your administrator must have the sn\_kmf.admin and sn\_kmf.cryptographic\_manager roles to access the health diagnostics. If your administrator does not have access, follow the instructions in [Assign KMF roles](https://www.servicenow.com/docs/access?context=kmf-roles&version=xanadu&pubname=xanadu-platform-security&section=assign-kmf-roles&ft:locale=en-US) to grant the required roles.

## About this task

Before proceeding, the provider should have requested the contact details of an admin to set as the main point of contact on their registration record. This designated contact person will receive an email either from the provider's instance or directly from the provider's admin, containing a registration link. Clicking on this link will generate a Provider Connection record in your consumer instance. The following steps assume that you have already clicked the registration link.

## Procedure

1.  Click the **Connect to Provider** link sent in the provider's registration email or follow the link given to you directly by the provider’s admin.

    This link will generate the Provider connection record.

    **Note:** The consumer admin completing the registration process must be the named contact on the provider’s registration task or an admin in the provider's instance. Registration will fail during the OAUTH authentication step if attempted by another user.

2.  Navigate to **All** &gt; **Service Exchange Consumer** &gt; **Provider Connections**.

3.  On the Provider Connection form in the consumer instance, select the name of the Company that the provider is associated with and click **Save**.

    The Provider Connection record is displayed.

4.  Click **Connect to Provider** in the Provider connection record page.

5.  Click **Authenticate** when the Service Exchange registration message appears.

    The OAuth authentication page appears.

6.  Click **Allow** and then click **Submit** to proceed with the registration.

    You are redirected to the Registration task where you can view the status. When registration is completed, a connection is established between the provider and the consumer instances, and the registration task State is set to **Closed Complete** on the provider's instance.


