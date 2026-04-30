---
title: Update indicators in Microsoft Defender for Endpoint
description: Update the existing indicators in Microsoft Defender for Endpoint from the list context-menu or from the form view of the Microsoft Defender Indicator respectively.
locale: en-US
release: yokohama
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create indicators in Microsoft Defender for Endpoint, Microsoft Defender for Endpoint integration, Security Incident Response integrations, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# Update indicators in Microsoft Defender for Endpoint

Update the existing indicators in Microsoft Defender for Endpoint from the list context-menu or from the form view of the Microsoft Defender Indicator respectively.

## Before you begin

Role required: sn\_si.admin, sn\_si.analyst

## Procedure

1.  Navigate to **Security Incidents** &gt; **Show All Incidents**.

2.  Click **Show All Related Lists** and then click the **Microsoft Defender Indicators** tab.

    **Note:**

    You must configure the related list for the Microsoft Defender Indicators, which would appear in the Security Incident related lists. For more information, see [Form UI actions](../../../security-incident-response/concept/sir-new-ui-setup-form-uiaction.md).

3.  Update the Microsoft Defender for Endpoint indicators in one of the following ways:

    -   To update the indicators from the list context-menu, select the row of the indicator that you want to update and click **Update Indicator in the Microsoft Defender** option.

        ![Update Indicators in Microsoft Defender for Endpoint from Microsoft Defender Indicator's list context-menu](../image/indicator_contextmenu.png "Update Indicators using list context-menu")

    -   To update the indicators from the form view, click **Update Indicator in Microsoft Defender** in the form view.

        ![Update Indicator in Microsoft Defender for Endpoint from the Microsoft Defender Indicator's form view](../image/Indicator_formview.png "Update Indicators using form view")

4.  On the form, fill in the fields.

<table id="table_sx2_kbl_jsb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Title

</td><td>

Title for the indicator.

</td></tr><tr><td>

Description

</td><td>

Description for the indicator.

</td></tr><tr><td>

Expiration Time

</td><td>

Expiration time for the indicator.

</td></tr><tr><td>

Recommended Actions

</td><td>

Recommended actions to be performed for the indicator.

</td></tr><tr><td>

Source

</td><td>

Integration configuration to create the indicator.

</td></tr><tr><td>

Action

</td><td>

Actions that are performed if the indicator is discovered in the organization. The possible values are as follows:-   **Warn**
-   **Block**
-   **Audit**
-   **BlockAndRemediate**
-   **Allowed**


</td></tr><tr><td>

Application

</td><td>

The Microsoft Defender for Endpoint application that is associated with the indicator. This field is applicable only for a new indicator and cannot be used for an existing indicator.

</td></tr><tr><td>

Severity

</td><td>

Severity of the Indicator. Possible values are as follows:-   **Low**
-   **Medium**
-   **High**


</td></tr><tr><td>

RBAC Group Names

</td><td>

RBAC group names that the indicator is applied to. The names are in a comma-separated list.

</td></tr></tbody>
</table>5.  Click **Update Indicator**.

6.  Validate the activity and UI messages.


