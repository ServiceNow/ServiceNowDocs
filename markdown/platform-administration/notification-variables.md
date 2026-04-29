---
title: Notification variables
description: Use notification variables to display dynamic information in the body of a notification such as a field value, a link to a record, or a link to system preferences.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Create an email notification, Email and SMS notifications, System notifications, Notifications, Configure core features, Administer the ServiceNow AI Platform]
---

# Notification variables

Use notification variables to display dynamic information in the body of a notification such as a field value, a link to a record, or a link to system preferences.

## Syntax

Specify a notification variable using this syntax:

```
${variable-name+variable-parameters}
```

The **variable-name** portion is always required. Not all notification variables support the variable-parameters portion. When available, most variable parameters are optional. See the list of available notification variables for variable names and available parameters.

## Available variables

The system provides these notification variables.

<table id="table_ojr_mjc_ww"><thead><tr><th>

Variable

</th><th>

Description

</th><th>

Available parameters

</th></tr></thead><tbody><tr><td>

$\{`field-name`\}

</td><td>

Display the value of the specified field.

</td><td>

None

</td></tr><tr><td>

$\{`image-field-name`\}

</td><td>

Display an image associated with a record. This variable is typically used with HTML to specify the source of an image element.

</td><td>

None

</td></tr><tr><td>

-   $\{URI\}
-   $\{URI\_REF\}

</td><td>

Display a link to the current record.-   **URI**: The link text is the word `LINK`.
-   **URI\_REF**: The link text is the display value of the record.

 **Note:** These variables don't apply to records in Workspace. To link to a record in Workspace, create a mail script that prints a URL to a notification. For more information, see [Linking to a record in Workspace](c_EnablingLinksToServiceNowRecords.md#link-to-workspace-record).

</td><td>

Any valid **sysparm** URL parameter. For example:-   sysparm\_scriptlet
-   sysparm\_view

</td></tr><tr><td>

-   $\{`reference-field`.URI\}
-   $\{`reference-field`.URI\_REF\}

</td><td>

Display a link to the record listed in a reference field.-   **URI**: The link text is the word `LINK`
-   **URI\_REF**: The link text is the display value of the record.

</td><td>

Any valid **sysparm** URL parameter. For example:-   sysparm\_scriptlet
-   sysparm\_view

</td></tr><tr><td>

$\{CMS\_URI\}

</td><td>

Display a link to the specified record within a CMS page.

</td><td>

**&lt;CMS-site&gt;/&lt;CMS-page&gt;**: The required relative path to the CMS page.

</td></tr><tr><td>

$\{notification:body\}

</td><td>

Display the body contents of an email template or email notification. Use this notification variable to specify where to display body content in an email layout.

</td><td>

None

</td></tr><tr><td>

$\{mail\_script:`script-name`\}

</td><td>

Run the specified mail script.

</td><td>

None

</td></tr><tr><td>

$\{NOTIF\_UNSUB\}

</td><td>

Display a link unsubscribe from this notification.

</td><td>

**link\_text**: specify the text to display as a link within quotation marks.

</td></tr><tr><td>

$\{NOTIF\_PREFS\}

</td><td>

Display a link to set notification preferences.

</td><td>

**link\_text**: specify the text to display as a link within quotation marks.

</td></tr><tr><td>

$\{comments:n\}

</td><td>

Display the most recent comments that were made on the target record. The number of comments to display is n. For example, `${comments:3}` displays the last three comments that were made to the record.

 To display all comments, use the variable `${comments}`.

</td><td>

Any number greater than 0.

</td></tr><tr><td>

$\{comments\_and\_work\_notes:n\}

</td><td>

Display the most recent comments and work notes that were made on the target record. The number of comments and work notes to display is n. For example, `${comments_and_work_notes:3}` displays the last three comments and work notes that were made to the record.

 To display all comments and work notes, use the variable `${comments_and_work_notes}`.

</td><td>

Any number greater than 0.

</td></tr></tbody>
</table>## Examples

Refer to the following examples to see how each notification variable is rendered in the output:

<table id="table_kpc_n33_53b"><thead><tr><th>

Variable

</th><th>

Example

</th></tr></thead><tbody><tr><td>

$\{`field-name`\}

</td><td>

Source: `Incident ${number} - comments added`

 Output: `Incident INC1000001 - comments added`

</td></tr><tr><td>

$\{`image-field-name`\}

</td><td>

Source: `<img src='${picture}?t=medium'/>`

 Output:![notification image variable](../image/apple-watch.png)

</td></tr><tr><td>

-   $\{URI\}
-   $\{URI\_REF\}

</td><td>

$\{URI\} Source: `Click here to view incident: ${URI}`

 $\{URI\} Output: ![Example that shows how the link text word Link serves as the link to the current record](../image/variable-uri.png)

 $\{URI\_REF\} Source: `Click here to view incident: ${URI_REF}`

 $\{URI\_REF\} Output: ![Example that shows how the link text displayed is the value of the record](../image/variable-uri-ref.png)

</td></tr><tr><td>

-   $\{`reference-field`.URI\}
-   $\{`reference-field`.URI\_REF\}

</td><td>

Source:

```
Click here to view Incident: ${URI_REF}
Click here to view Related Problem: ${problem_id.URI_REF}
```

 Output: ![Example that shows a link to a record listed in a reference field](../image/RelatedRecordLink.png)

</td></tr><tr><td>

$\{CMS\_URI\}

</td><td>

Source: `${CMS_URI+ess/incident_detail}`

 Output: a link to a target CMS page such as `https://<instance name>.service-now.com/ess/incident_detail.do?sysparm_document_key=incident,46e18c0fa9fe19810066a0083f76bd56`

</td></tr><tr><td>

$\{notification:body\}

</td><td rowspan="4">

Source: ![How a variable for the email body works in an email layout.](../image/email-layout-go-to-instance-button.png)

 Output:![How the variable for the link to notification preferences works.](../image/email-preview-with-layout.png)

</td></tr><tr><td>

$\{mail\_script:`script-name`\}

</td></tr><tr><td>

$\{NOTIF\_UNSUB\}

</td></tr><tr><td>

$\{NOTIF\_PREFS\}

</td></tr></tbody>
</table>**Parent Topic:**[Create an email notification](../task/t_CreateANotification.md)

