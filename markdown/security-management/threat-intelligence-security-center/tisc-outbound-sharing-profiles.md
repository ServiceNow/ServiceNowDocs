---
title: Configuring Outbound Intel Sharing Profiles
description: Use this section to create new Outbound Intelligence Profiles. The outbound intelligence profiles specify the endpoint details to which threat intelligence data is sent.
locale: en-US
release: australia
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exploring Outbound Intel Sharing, Configuring Threat Intelligence External Sharing, Administer, Threat Intelligence Security Center, Security Operations]
---

# Configuring Outbound Intel Sharing Profiles

Use this section to create new Outbound Intelligence Profiles. The outbound intelligence profiles specify the endpoint details to which threat intelligence data is sent.

## Before you begin

Role required: sn\_sec\_tisc.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Threat Intelligence Security Center** &gt; **Administration** &gt; **Outbound Intel Sharing**.

2.  Select **Outbound Intel Sharing Profiles**.

3.  Select **New** to create an Outbound Intelligence Profile.

4.  On the form, fill in the fields.

<table id="table_syl_ztc_mfc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the outbound intelligence profile.

</td></tr><tr><td>

Industry

</td><td>

Select the industry category such as Aerospace, Agriculture for which the outbound intelligence profile is applicable to.

</td></tr><tr><td>

Description

</td><td>

Description of the outbound intelligence profile.

</td></tr><tr><td colspan="2">

**Outbound Intelligence Settings**

</td></tr><tr><td>

Data Format

</td><td>

Supported data formats for outbound intelligence sharing profile.Currently, the following two data formats are supported for outbound intelligence sharing:

-   **STIX 2.1**: Supports various endpoint types, including basic authentication endpoints and open-source endpoints. To accommodate this, two authentication types are available for STIX 2.1.
-   **MISP**: For MISP, authentication is handled exclusively through an API key.
    -   When MISP is selected as the format, the Authentication Required option is automatically enabled.
    -   The authentication type is fixed as API Key, and users must provide a valid API key to connect to the MISP instance.


</td></tr><tr><td>

API Endpoint URL

</td><td>

Enter the API endpoint URL to which the data needs to be sent.

</td></tr><tr><td>

Authentication Required

</td><td>

Select this check box if the authentication is required.

</td></tr><tr><td>

Authentication Type

</td><td>

Select the required option from the drop down list if the authentication is required. The available option is:**Basic**: Select this option to provide user name and password.

</td></tr><tr><td>

Headers to be passed with request

</td><td>

Any headers to be passed with the requests can be provided for the outbound intelligence profile.Header should be provided in key-value pair separated by colon\(':'\). Each header key value pair should be provided in a new line. For providing authentication parameters as header values, enclose the required authentication with '$\{' and '\}$'. \(for example : username:$\{Username\}$\)

</td></tr></tbody>
</table>5.  Once the profile and authentication details are provided, click **Save**.

6.  Select **Validate Connection** to confirm the setup by testing the endpoint URL configured under Intelligence Outbound Sharing.

    This option enables you to provide a request body to validate the specific endpoint defined in the profile section.

    **Note:** A sample request body is displayed based on the selected format, and you can modify it as needed.

    Make the necessary changes to the request body and click **Save and Validate** button. In case if you want to reset to the original sample request body then you can select **Reset** button to reset it back to the original request body.

    A confirmation message is displayed indicating that the connection to endpoint is successful.

    If the connection to the endpoint is not successful, then check the error logs and resolve any issues before retrying.

7.  Select the **Enable** button to enable the outbound intelligence sharing profile.

    **Note:** When you select **Enable** button, then the validation to the end point checks occur automatically.

    Whenever you create a sharing profile, **Enable** button appears only when the connection is successfully validated otherwise this button will not be visible until the connection to the endpoint is successful.

    A confirmation message is displayed indicating the sharing profile is successfully enabled.

    **Note:** You must enable the sharing profile to use it for sharing intelligence.

8.  Additionally, select **Disable** to disable the profile if it is not needed for sharing intelligence.


**Parent Topic:**[Exploring Outbound Intel Sharing](../concept/tisc-outbound-intel-sharing.md)

**Related topics**  


[Configuring Outbound Intel Sharing Controls](tisc-outbound-sharing.md)

[Configuring Outbound Intel Data Exclusion Rule](tisc-outbound-data-exclusion.md)

[Configuring Outbound Intel Sharing Groups](tisc-config-inbound-sharing-groups.md)

[Defining Approval Rule for Outbound Intel](tisc-approval-outbound-intel.md)

[Configuring Outbound Intel Sharing Templates](tisc-intel-sharing-templates.md)

[Working on the Redaction Library](tisc-redaction-library.md)

