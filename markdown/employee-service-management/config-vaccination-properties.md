---
title: Set up Vaccination Status properties
description: Set up Vaccination Status properties to define the data retention period for user-reported vaccination status data, manage reminder emails, and enable exemptions.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 7
breadcrumb: [Vaccination Status, Safe Workplace, Health and Safety, Employee Service Management]
---

# Set up Vaccination Status properties

Set up Vaccination Status properties to define the data retention period for user-reported vaccination status data, manage reminder emails, and enable exemptions.

## Before you begin

Role required: sn\_imt\_vaccine.admin

## Procedure

1.  Navigate to **All** &gt; **Vaccination Status** &gt; **Properties**.

2.  Set the following property values.

<table id="table_vhc_j5n_cnb"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Vaccination Status data retention period \(in days\).\[sn\_imt\_vaccine.data.retention.period\]

</td><td>

Sets the number of days that user-reported vaccination status data is available in the Vaccine response table \[sn\_imt\_vaccine\_vaccine\_response\] before it is deleted automatically. The **Data Retention Job for Vaccination Status** scheduled job runs daily to delete records that have an updated date past the specified retention period.

 The default value is **90 days** and you can't set the property to **0**. If the property is left empty, the default value is used. To retain data indefinitely, set the **Data Retention Job for Vaccination Status** scheduled job to **Inactive**. Refer to your organization's data retention policy for guidelines on how long data should be retained.

**Note:** Attachments, such as QR codes, are also removed if a user's vaccine response is deleted prior to the deadline set by an organization's data retention policy.

</td></tr><tr><td>

Prevent admin from accessing attachments.\[sn\_imt\_vaccine.prevent\_admin\_access\_to\_attachments\]

</td><td>

Enable this property to limit the visibility of attachments in vaccination records to scoped administrators only. This limitation prevents system administrators from viewing these attachments. The property is inactive by default.

</td></tr><tr><td>

Frequency of reminders after 1st reminder. Default is set to 1, this will keep reminding users until they acknowledge.\[sn\_imt\_vaccine.reminder\_after\_1st\_reminder\]

</td><td>

Sets how often users receive reminder emails about their second dose after receiving their first reminder. For example, a value of `1` sends a reminder every day, and a value of `4` sends a reminder every 4 days.The reminder emails are sent until the user reports their second dose. The Vaccine 2nd dose reminder email notification is sent until the due date. The Vaccine 2nd dose follow-up passed email notification is sent after the due date.

 The value of this property can't be **0**.

</td></tr><tr><td>

Number of days before 2nd dose due date reminder.\[sn\_imt\_vaccine.days\_before\_2nd\_dose\_due\_date\]

</td><td>

Sets when to start sending reminder emails to users for their second dose of a vaccine. A user's due date for their second dose is determined by the date that they received the first dose plus the **Number of days between doses** field on the Vaccine response definition record. This property sets the number of days before the due date that a user receives their first reminder email.The default value is 10 days before the due date.

</td></tr><tr><td>

Number of days to send past due reminder before giving up.\[sn\_imt\_vaccine.past\_due\_reminder\_limit\]

</td><td>

Number of days to send past due vaccination reminders before reminders are no longer sent. Reminder emails are no longer sent once the user reports their last dose.

</td></tr><tr><td>

Set reminders for booster.\[sn\_imt\_vaccine.send\_reminders\_for\_booster\]

</td><td>

Enable this property to send reminders to users to report their vaccine booster. Booster reminders are not sent until a user reports their last vaccine dose. Organizations might need to extend or update their data retention policies to ensure enough time to send a reminder. If the data retention policy is not long enough, the date a final dose was administered could be erased before the reminder is sent.

</td></tr><tr><td>

Frequency of booster reminders.\[sn\_imt\_vaccine.booster\_reminder\_frequency\]

</td><td>

Sets how often users receive reminder emails about their vaccine booster.

</td></tr><tr><td>

Number of days before booster due date reminder.\[sn\_imt\_vaccine.remind\_days\_before\_booster\_due\_date\]

</td><td>

Sets the number of days before the due date that users receive their first reminder email about getting their vaccine booster. -   A vaccine's booster dose due date is equal to the date of the user's last vaccination dose, plus the value in the **Recommended days until booster required** field on the Vaccine response definition record, plus 14 days.

-   A booster's dose due date is equal to the date of the user's last vaccination dose, plus the value in the **Recommended days until booster required** field on the Vaccine response definition record for the user's last reported booster.

</td></tr><tr><td>

Number of days to send booster past due reminder before giving up.\[sn\_imt\_vaccine.booster\_past\_due\_reminder\_limit\]

</td><td>

Number of days to send past due vaccine booster reminders before reminders are no longer sent.

</td></tr><tr><td>

Set vaccine completed to false for users without booster.\[sn\_imt\_vaccine.enforce\_vaccination\_complete\_for\_booster\]

</td><td>

Enable this property to force the **false** status for the vaccine completed value when a booster is due and a user has not reported receiving their booster.

</td></tr><tr><td>

Number of days to wait after booster due date before setting vaccine completed to false.\[sn\_imt\_vaccine.set\_covid19\_completed\_to\_false\_this\_many\_days\_after\_booster\_due\_date\]

</td><td>

Sets the number of days to wait before setting vaccine completed to **false** when a booster is due and a user has not reported receiving their booster.

</td></tr><tr><td>

Reset Covid 19 Vaccine Complete to false if Vaccine Review Outcome is Rejected\[sn\_imt\_vaccine.reset\_covid\_19\_vaccine\_complete\_to\_false\_if\_vaccine\_review\_outcome\_is\_rejected\]

</td><td>

Enable this property to set **Covid 19 Vaccine Complete** to **false** in the vaccine profile if a Vaccination Status admin rejects a vaccine response during the review. This property is inactive by default.

</td></tr><tr><td>

Use country-specific data retention policy for Vaccination Status.\[sn\_imt\_vaccine.use\_country\_specific\_data\_retention\_policy\]

</td><td>

Enable this property to use country-specific data retention policies for Vaccination Status. When enabled, records are compared to data retention policy of the user's location to determine how long records are retained.For example, one country may have a 90-day retention period while another has a 120-day policy.

 When there is no country-specific policy, the policy defaults to the value in the **Vaccination Status data retention period \(in days\)** property. This property is inactive by default.

</td></tr><tr><td>

Allow managers the ability to update vaccine response records.\[sn\_imt\_vaccine.allow\_managers\_ability\_to\_update\_vaccine\_response\_records\]

</td><td>

Enable this property to provide managers with the ability to update vaccine response records of their direct reports.All managers receive the Approval Portal manager \[sn\_imt\_core.approval\_portal\_manager\] role.This property is inactive by default.

</td></tr><tr><td>

Allow managers the ability to update vaccine exemption requests.\[sn\_imt\_vaccine.allow\_managers\_ability\_to\_update\_vaccine\_exemption\_records\]

</td><td>

Enable this property to provide managers with the ability to update vaccine exemption request records of their direct reports.All managers receive the Approval Portal manager \[sn\_imt\_core.approval\_portal\_manager\] role.This property is inactive by default.

</td></tr><tr><td>

Allow vaccine exemptions.\[sn\_imt\_vaccine.allow\_vaccine\_exemptions\]

</td><td>

Enable this property to give users the ability to submit vaccine exemption requests. Exemptions do not affect the vaccine profile's **Covid 19 Vaccine Complete** status. This property is inactive by default.**Note:** If you do not want users to access the **Request vaccine exemption** module because it is not active, you can inactivate the module. For more information, see [Enable or disable an application menu or module](https://www.servicenow.com/docs/access?context=t_EnDisableAppMenuOrMod&version=yokohama&pubname=yokohama-platform-user-interface&ft:locale=en-US).

</td></tr><tr><td>

Newly approved vaccine exemptions will have an expiration date set.\[sn\_imt\_vaccine.new\_vaccine\_exemptions\_temporary\]

</td><td>

Enable this property for vaccine exemptions to have an expiration set once approved. This property is inactive by default.

</td></tr><tr><td>

Days for temporary exemption if vaccine exemption expiration set to yes.\[sn\_imt\_vaccine.temporary\_exemption\_days\_until\_expire\]

</td><td>

Automatically sets the number of days for a vaccine exemption to remain valid before it expires. The default is **360 days**.

</td></tr><tr><td>

Allow users to see Vaccine response work notes.\[sn\_imt\_vaccine.allow\_users\_to\_see\_vaccine\_response\_work\_notes\]

</td><td>

Enable this property to give users the ability to see work notes entered on their vaccine response records. This property is inactive by default.

</td></tr><tr><td>

Allow users to see Vaccine exemption work notes.\[sn\_imt\_vaccine.allow\_users\_to\_see\_vaccine\_exemption\_work\_notes\]

</td><td>

Enable this property to give users the ability to see work notes entered on their vaccine exemption request records. This property is inactive by default.

</td></tr><tr><td>

Allow validation engine approvals to update Vaccine Review Outcome records.\[sn\_imt\_vaccine.allow\_automated\_response\_approval\]

</td><td>

Enable this property to automatically update vaccine review outcomes when a validator service, such as CommonTrust Network, reviews a user's vaccination status. The user's submitted attachment, such as a Smart Health card QR code, is read, and the Auto-validate vaccine response flow approves the submitted vaccine response if there is a match on the following items:

 -   First and last name
-   Date received
-   Vaccine code, such as a CVX code, to verify the vaccine's manufacturer
 This property is inactive by default. For more information on enabling automated vaccine response reviews, see [Automating vaccine response reviews](../concept/vaccination-status-vaccine-validation.md).

</td></tr><tr><td>

Azure Form Recognizer confidence threshold, a decimal value between 0 and 1.\[sn\_imt\_vaccine.azure\_form\_recognizer\_confidence\_threshold\]

</td><td>

If your organization is using the Azure Form Recognizer service to automatically validate CDC Vaccination Cards, this property sets the default confidence threshold that a submitted vaccination card must meet for the vaccine response to be approved. The default value is 0.90, indicating a 90% confidence threshold.

 Your organization must also enable the \[**sn\_imt\_vaccine.allow\_automated\_response\_approval**\] property to enable automated vaccine review outcomes based on the Azure Form Recognizer service and confidence threshold.

 For more information, see [Automating vaccine response reviews with the Azure Form Recognizer service](../concept/automate-vaccine-validation-with-azure-form-recognizer.md).

</td></tr></tbody>
</table>3.  Click **Save**.


**Parent Topic:**[Vaccination Status](../concept/vaccination-status.md)

