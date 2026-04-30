---
title: Validate vaccine responses automatically
description: Configure Vaccination Status so that validator services can validate vaccine responses automatically with information from supported attachments.
locale: en-US
release: xanadu
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Automating vaccine response reviews, Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Validate vaccine responses automatically

Configure Vaccination Status so that validator services can validate vaccine responses automatically with information from supported attachments.

## Before you begin

Integrate with the validator service by doing the following:

-   Obtain credentials for a validator service.
-   Create a connection and credentials alias. For more information, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

If your organization is using an integration that is already supported, such as the CommonTrust Network, then you need only to add your organization's credentials to the validator service record.

Role required: admin

## Procedure

1.  Configure the validator service.

    1.  Navigate to **Vaccination Status** &gt; **Validator services**.

    2.  Select an existing validator service or, if you are creating a new one, click **New**.

        If you are selecting an integration that is already supported, such as the CommonTrust Network, you must enter your Connection alias and confirm the form is correct for your validator service.

    3.  Fill in the fields on the form.

<table id="table_qq5_d5c_wrb"><thead><tr><th>

Field

</th><th>

Action

</th></tr></thead><tbody><tr><td>

Name

</td><td>

The name of the validator service.

</td></tr><tr><td>

Connection alias

</td><td>

The connection alias for your validator service. For more information on creating a connection alias, see [Create a Connection and Credential alias](https://www.servicenow.com/docs/access?context=connection-alias&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Validation subflow

</td><td>

The subflow used to confirm whether a submitted attachment is valid. A template flow is provided by default or you may create a flow and add it to this field. For more information on creating flows, see [Create a flow](https://www.servicenow.com/docs/access?context=create-flow&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).If you create your own subflow, it must have the same inputs and outputs as the template subflow.

</td></tr><tr><td>

Initial validator state

</td><td>

The initial state the validator service starts in prior to the completion of the review, such as **Ready**. The recommended state is **Ready** unless there is a preprocessing step.**Note:** If the initial state is **Preprocessing**, then the redirect page must set the response record validator state to **Ready** so it works with the built-in validation flow.

</td></tr><tr><td>

Redirect page

</td><td>

\(Optional\) A reference to a service portal page the user will be redirected to after they report their vaccination.

</td></tr><tr><td>

Active

</td><td>

Option to activate the service.

</td></tr><tr><td>

Domain

</td><td>

The domain required for the validator service, such as **global**.

</td></tr></tbody>
</table>    4.  Click **Submit**.

2.  Configure a vaccine code system used to read vaccine codes and validate submitted data.

    The vaccine code your system uses might be provided with Vaccination Status. Refer to your validator service's requirements for more information.

    1.  Navigate to **Vaccination Status** &gt; **Vaccine code systems**.

    2.  Select **New**.

    3.  Enter the name of the vaccine code system.

    4.  Enter the URL for the vaccine code system.

    5.  Select **Submit**.

3.  Configure the vaccine response attachment type supported by the validator service.

    This attachment type users should use when they submit their vaccine responses.

    1.  Navigate to **Vaccination Status** &gt; **Attachment types**.

    2.  Select **New**.

    3.  Enter the name of the attachment type.

    4.  Enter the name of the validator service.

    5.  Enable the attachment type by selecting the **Active** check box.

    6.  Set the domain to **global**.

    7.  Select **Submit**.

4.  Add common vaccine codes required by the vaccine code system and service.

    Common codes are provided with Vaccination Status. Refer to [COVID-19 Vaccine Related Codes](https://www.cdc.gov/vaccines/programs/iis/COVID-19-related-codes.html) for additional common codes and the third-party service for codes their system supports.

    1.  **Vaccination Status** &gt; **Vaccine codes**.

    2.  Select **New**.

    3.  In the **Code System** field, add the corresponding system.

    4.  In the **Code** field, enter the code used to identify information about the vaccine.

    5.  Enter a description.

    6.  Select **Submit**.

5.  Activate the Auto-validate vaccine response flow.

    1.  Navigate to **Process Automation** &gt; **Flow Designer**.

    2.  Search for the Auto-validate vaccine response flow.

    3.  Select the flow.

    4.  Select **Activate**.


## Result

You have enabled automated vaccine response validation. Work notes in the vaccine response record are updated with information on whether the attachments, and therefore the response, are valid. You can use this information to manually review vaccine responses in the approval portal.

## What to do next

To automate vaccine response reviews so that they are set to **Approved** if validation was successful or left in the state **Not yet reviewed** \(a manual review is required\), see [Automate reviews of vaccine responses](enable-automated-vaccine-response-reviews.md).

**Parent Topic:**[Automating vaccine response reviews](../concept/vaccination-status-vaccine-validation.md)

