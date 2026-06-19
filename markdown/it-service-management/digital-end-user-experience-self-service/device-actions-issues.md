---
title: Device action diagnosis and checks
description: Common device action symptoms, and the tables and configurations to check during diagnosis.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-service-management/digital-end-user-experience-self-service/device-actions-issues.html
release: australia
product: Digital End-user Experience Self-service
classification: digital-end-user-experience-self-service
topic_type: reference
last_updated: "2026-05-19"
reading_time_minutes: 1
breadcrumb: [Reference, Digital End-user Experience Self-service, Digital End-User Experience, IT Service Management]
---

# Device action diagnosis and checks

Common device action symptoms, and the tables and configurations to check during diagnosis.

<table id="table_ujt_l5r_hjc"><thead><tr><th>

Symptom

</th><th>

Checks

</th></tr></thead><tbody><tr><td>

Action doesn't appear in Employee Center

</td><td>

Confirm the following:-   Employee Center \(ec\_enabled\) is enabled.
-   User applicability \(user\_applicability\) is set to End user.
-   Device OS matches the OS of the target device.

</td></tr><tr><td>

Action doesn't appear in Now Assist

</td><td>

Check that Now Assist \(va\_enabled\) is enabled or set to true. This setting is inactive by default.

</td></tr><tr><td>

Issue configuration is not available when creating a device action

</td><td>

Confirm that the issue configuration is:-   Not already associated with another device action.
-   Enabled for end users through the User applicability setting.
-   Linked to remedial action resolution type.
-   Not linked to unsupported or silent engagement type.

</td></tr><tr><td>

Action runs but reports failure

</td><td>

Check the execution record for the user and device, and review the associated task for details about the failure.

</td></tr><tr><td>

Action completes without visible result \(macOS\)

</td><td>

Confirm that the sudoers file grants the required permissions to `_servicenow`.For more information, see [Configure ServiceNow sudoers file](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-service-management/digital-end-user-experience-dex/config-sudoers-file.md).

</td></tr><tr><td>

Battery replacement action repeats without resolving the issue

</td><td>

Before creating or modifying this action, confirm that the battery replacement resolution record is correctly configured. The battery replacement action has a specific configuration requirement.

</td></tr><tr><td>

Action triggers unexpectedly or does not trigger at all

</td><td>

Check the metric source on the metric definition record. If the metric source does not match the expected evaluation method, the action may trigger incorrectly or not at all.

</td></tr></tbody>
</table>**Note:** If a symptom persists, contact ServiceNow support.

