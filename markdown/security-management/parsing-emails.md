---
title: Create email parsers in Security Operations
description: Email Parsing creates Security Operations records from your email for security, vulnerability, and observables to expedite threat response and remediation.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Security Operations email parsing, Security Operations email processing, Security Operations common functionality, Security Operations]
---

# Create email parsers in Security Operations

Email Parsing creates Security Operations records from your email for security, vulnerability, and observables to expedite threat response and remediation.

## Before you begin

-   Set up external detection tools to send emails to a central email address.
-   Set the email address in Security Operations properties. For more information, see [Create Security Operations email properties](create-email-properties.md).
-   Assign a user account to this email address and give that user security access controls to create and update the email event records.
-   Have a copy of the relevant email from your external detection tool in front of you.
-   Decide what type of record you want to create, a security incident, vulnerability record, task and so on. This choice determines the table you select.

Role required: sn\_sec\_cmn.admin

## Procedure

1.  Navigate to **All** &gt; **Security Operations** &gt; **Email Parsing**.

2.  Select **New**.

3.  Fill in the fields on the form, as appropriate.

    **Note:** If more than one field is specified, all fields must match the email to create a record.

    |Field|Description|
    |-----|-----------|
    |Name|The name of the email parser.|
    |Email is from|If filled in, only emails from this address are transformed by this email parser.|
    |Email is to|If filled in, only emails from this address are transformed by this email parser.|
    |Email subject contains|If filled in, only emails where the subject contains this phrase are transformed by this email parser.|
    |Duplication rule|Governs how to handle duplicate emails for any email this transform handles. For more information, see [Shared data transformation](../concept/shared-data-transformation.md).|
    |Order|In what order to consider the transforms. The first matching email transform is used. Typically, you want to set up the most specific email parsers in the lower numbers, with some fallback. Give catchall email parsers higher **Order** numbers so they run if nothing else matches. Default is 100. When everything matches, the most specific email parser \(matches **from**, **to**, and **subject**\) is used.|
    |Destination table|The table where you want to create records.|
    |Active|Whether this transform is active, in use, or not active. If unchecked, no emails are transformed with this code.|
    |Record Separator|When emails handled by this email parser create multiple records, this field contains the separator between the information for those records. See [Security Operations email parsing](../concept/email-parsing.md) for more information.|
    |Description|Description of this email parser, which tool it works with, the purpose, and so on.|

4.  When you have completed your entries, select and hold \(or right-click\) in the form header and select **Save**.

    A **Field Transforms** tab appears. This tab shows how individual fields within the destination table are set based on the email contents.

    ![Field transforms form](../image/EmailTransforms.png)

5.  To add **Field Transforms**, perform these steps.

    1.  In the **Field Transforms** tab, select **New**.

    2.  Fill in the fields on the form, as appropriate.

<table id="choicetable_nhl_vjt_zv"><tbody><tr><td id="d304582e349">

**Field**

</td><td>

Description

</td></tr><tr><td id="d304582e361">

**Store value in a field or a related list**

</td><td>

Select where to find the value. Choices include:-   Store the value into a field in the new record
-   Link to this value in a related list
-   Link to this value, creating a new record if a matching record does not exist

**Note:** If the destination table does not have any related lists, this field is not displayed.

</td></tr><tr><td id="d304582e384">

**Field**

</td><td>

Select the field to fill in with this value. **Note:**

For choice fields, matches are made to existing choices using the underlying choice label or value. If no match is found, the field is set, but no new entry is added to the choice list. For more information, see [Choice lists](https://www.servicenow.com/docs/access?context=c_ChoiceLists&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

For reference fields, an entry is set only when a value matching the display name of the record or a valid `sys_id` is found. For more information, see [Reference fields](https://www.servicenow.com/docs/access?context=c_ReferenceField&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td id="d304582e417">

**Related list**

</td><td>

When **Store value in a field or related list** is set to **Link to this value in a related list** or **Link to this value, creating a new record if a matching record does not exist**, this field specifies the related list to add information to.

</td></tr><tr><td id="d304582e438">

**Value field**

</td><td>

When **Store value in a field or related list** is set to **Link to this value in a related list** or **Link to this value, creating a new record if a matching record does not exist**, this field specifies the field within the table displayed in the related list. It is used to look up and find an existing record. For example, if your related list is **Affected CIs**, this field can contain **Name** or **Fully Qualified Domain Name**, or any other field in the CI record to be used to look up the CI added to the **Affected CIs** list.

</td></tr><tr><td id="d304582e473">

**Relationship data**

</td><td>

When **Store value in a field or related list** is set to **Link to this value in a related list**, a record is created to link that record \(such as a security incident\) to the value \(a CI, an Observable, and so on.\). This field specifies any additional information \(field and value pairs\) that should be added to the linking record. For example, adding an Observable for a source IP, specify that this IP is the source, rather than destination IP. For multiple values, use a ^ separator, for example, type= Source IP^Active=true.

</td></tr><tr><td id="d304582e491">

**New record data**

</td><td>

When **Store value in a field or related list** is set to **Link to this value, creating a new record if a matching record does not exist**, if no related record matching the parsed value is found, a record is created. This field specifies the static data to add to that record. For **Affected CI**s, if no matching CIs are found a CI record is created. When that happens, the value found in the email, is set to the **Value** field in the CI record. You can set additional data – a note indicating why the CI was created, some information about what type of CIs you're working with and, so on. A sample would be: description=Created by Malware Scanner email parser^type=autodetect.

</td></tr><tr><td id="d304582e515">

**Search for value**

</td><td>

Select the location in the email to search. Choices include:-   **At the start of a line in the email body**
-   **Anywhere in the email body**
-   **In the email subject line**
-   **Always the static value**
 When you have defined a **Record Separator**, more options \(**Anywhere within the record section** and **At the start of a line within the record section**\) enable you to search only within the current section instead of in the entire email body \(See [Security Operations email parsing](../concept/email-parsing.md) for more information\).

 Information that is in a header or footer, applying to all records, is searched for in the entire email body. The information that differs between records is searched for only within the section.

</td></tr><tr><td id="d304582e571">

**Value separator**

</td><td>

When **Store value in a field or related list** is set to **Link to this value in a related list** or **Link to this value, creating a new record if a matching record does not exist**, this field specifies the separator to use for lists of items. for example a comma or semicolon when the data from the email is a list of IP addresses.

</td></tr><tr><td id="d304582e592">

**Value prefix**

</td><td>

The text that always precedes the value placed within this field to extract.

</td></tr><tr><td id="d304582e604">

**End of value**

</td><td>

Select what indicates the end of the value. Choices include: **End of line**, **End of email** \(brings in all remaining text in the email\), or **Until** \(stops when it finds the specified text\), or **Until** \(stops when it finds the specified text\).

</td></tr><tr><td id="d304582e629">

**Value suffix**

</td><td>

When the **End of Value** is set to **Until**, this field specifies what text always follows the value placed within this field.

 For example, looking for a value that comes after “The affected computer is” and before “.” will parse out “AB123” from “The demented bunny virus has been found. The affected computer is AB123. Estimated time of infection was 3:45PM” in an email.

</td></tr><tr><td id="d304582e650">

**Value transform**

</td><td>

Choose the field transformation entry to apply. Converts the value found in the email into a different value, used to fill in choice fields, occasionally reference, and other fields.

</td></tr><tr><td id="d304582e662">

**Order**

</td><td>

The order in which the field transforms run, from lowest to highest. A field transform with an order entry of 100 is attempted first. Only if that field transform fails to find a value will a field transform with a higher order \(200\) on the same field run.

</td></tr><tr><td id="d304582e671">

**Email transform**

</td><td>

The transform this field transform belongs to.

</td></tr><tr><td id="d304582e680">

**Destination table**

</td><td>

Destination table of the email transform. It contains informational data from the email transform.

</td></tr><tr><td id="d304582e689">

**Active**

</td><td>

The default is checked. When checked, the field transform is activated. Clear this box to deactivate the field transform.

</td></tr></tbody>
</table>    1.  Select **Submit**.

        The new record is used to parse the information in the email into a new record.


**Parent Topic:**[Security Operations email parsing](../concept/email-parsing.md)

**Related topics**  


[Create duplication rules in Security Operations](create-duplication-rules.md)

[Create Security Operations field value transforms](create-field-value-transforms.md)

[Define Vulnerability Response email notifications](../../vulnerability-response/task/t_DefineEmailNotifications.md)

