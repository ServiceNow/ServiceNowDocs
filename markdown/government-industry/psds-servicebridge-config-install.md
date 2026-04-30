---
title: Configure Service Exchange for Public Sector Digital Services
description: To set up and configure the Service Exchange for Public Sector Digital Services application, follow these steps.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-12-10"
reading_time_minutes: 2
breadcrumb: [Service Exchange, Case Management, Configure agent workspaces, Configure, Public Sector Digital Services \(PSDS\)]
---

# Configure Service Exchange for Public Sector Digital Services

To set up and configure the Service Exchange for Public Sector Digital Services application, follow these steps.

<table id="table_xkj_nxd_yxb"><thead><tr><th>

Task

</th><th>

Link

</th></tr></thead><tbody><tr><td>

Install the Service Exchange for Public Sector Digital Services application.

</td><td>

See [Install Service Exchange for Public Sector Digital Services](../task/psds-servicebridge-config-install-prov.md).

</td></tr><tr><td>

Set up the Government Service Portal, the consumer-facing portal for Public Sector Digital Services.

</td><td>

See [Customize the Government Service Portal](../task/customize-government-service-portal.md).

</td></tr><tr><td>

Set up a new provider record.

</td><td>

1.  Navigate to **User Administration** &gt; **Companies**and select the company record.
2.  Add a user or contact with the sn\_sb\_pro.consumer role.

    1.  To add one or more users to a company on the provider instance, navigate to **User Administration** &gt; **Companies**and select the company record.
    2.  Under the Users related list, select **New**.
    3.  On the form, fill in the fields with the user information, and select **Submit**.
    4.  Once the user record is created, navigate to the Roles related list and select **Edit**.
    5.  Select the roles you wish to add to the user using the arrows, and select **Save**.
**Note:** A user or contact with the sn\_sb\_pro.consumer role must be associated with the company before the company can be associated with a provider record.

3.  Navigate to **All** &gt; **Service Bridge Provider** &gt; **Provider**
4.  Enter a name for the provider, and enter the company associated with.

**Note:** To create a new company record, select \[magnifying glass\] to open the Companies related list, and select **New**. On the form, fill in the fields. Select **Submit** to save and associate the Company record to the Provider record.


See [Set up a Service Exchange provider record](https://www.servicenow.com/docs/access?context=service-bridge-v2-new-provider&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US).**Note:** If a new Company record has not yet been created, navigate to **User Administration** &gt; **Companies** and select **New**. Enter the Company details, then select **Submit**.

</td></tr><tr><td>

Set up a Service Bridge connection between a Provider and a Consumer.

</td><td>

See [Connect a provider instance to a consumer instance](psds-servicebridge-config-connect-prov-consu.md).

</td></tr><tr><td>

Assign Service Exchange roles for providers.

</td><td>

See [User roles for providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-personas&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Create catalog personas.

</td><td>

See [Create catalog personas](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-catalog-persona&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Create remote choice definitions.

</td><td>

See [Create remote choice definitions in Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-remote-choice-fld-defs&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US)

</td></tr><tr><td>

Create remote catalog items.

</td><td>

See [Create remote catalogs in Service Exchange for providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-remote-catalog&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Create remote task definitions.

</td><td>

See [Create a remote task definition in Service Exchange for Providers](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-remote-tasks-defs&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Create transforms.

</td><td>

See [Create a transform in Service Exchange](https://www.servicenow.com/docs/access?context=service-bridge-v2-create-transform&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US).

</td></tr><tr><td>

Update Authorized Users settings.

</td><td>

See [Update settings for authorized users](https://www.servicenow.com/docs/access?context=service-bridge-v2-configure-settings&version=zurich&pubname=zurich-service-bridge&ft:locale=en-US).

</td></tr></tbody>
</table>