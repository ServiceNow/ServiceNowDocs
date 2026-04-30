---
title: Troubleshooting LDAP integration via MID Server
description: You may encounter issues in the following areas while integrating LDAP via MID Server.
locale: en-US
release: yokohama
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [LDAP integration via MID Server, LDAP integration setup, LDAP integration, Authentication, Access Management]
---

# Troubleshooting LDAP integration via MID Server

You may encounter issues in the following areas while integrating LDAP via MID Server.

You can troubleshoot these issues by viewing the outputs found in the External Communication Channel \(ECC\) Queue \(**Discovery** &gt; **Output and Artifacts** &gt; **ECC Queue**\).

## Test Connection Issues

When defining OUs within the server, there is a **Test connection** related list that is used to verify the LDAP connection. When you click this link, the ECC Queue should show a single output message with a topic name of **LDAPConnectionTesterProbe**. After the test has completed on the MID Server, the ECC Queue should show an input message with the same topic name. If the **Name** column for the input message shows **true**, the test was successful. Drill down into the record to view the payload and ensure it does not contain error messages.

![](../image/TestConnection1.png "Test Connection")

## Browse Issues

When defining OUs within the server, there is a **Browse** related list that is used to view the LDAP directory records that the OU definition returns. When you click this link, the ECC Queue should show a single output message with a topic name of **LDAPBrowseProbe**. After data has been returned from the MID Server, the ECC Queue should show an input message with the same topic name. If the **Name** column for the input message shows **true**, the test was successful. Drill down into the record to view the payload and ensure it does not contain error messages.

## Load Import Issues

When uploading data \(for example, using the Test Load 20 Records feature\), the ECC Queue should show a single output message with a topic name of **LDAPProbe**.

After data has been returned from the MID Server, the ECC Queue should show another input message called **LDAPProbeCompleted**. The **Name** column for this input message shows the total number of records returned.

An additional input messages, also named **LDAPProbe**, is displayed. The **Name** column for this input message displays the highest record number in the batch. If the total number of records returned is 258 and the batch size is 200 \(the default\), two LDAPProbe \(200, 258\) incoming messages will be received, and one LDAPProbeCompleted \(258\) incoming message will be received.

Drill down into the record to view the payload and ensure it does not contain error messages.

![](../image/ImportLoad.png "Import Load")

Also keep an eye out for an output message called **LDAPProbeError**.

![](../image/Error.png "Error message")

Click the link in the **Name** column to view the details of the error.

## LDAP paging

LDAP paging does not work if the paging size on the LDAP server is less than 1000. Set the MID Server property **glide.ldap.max\_results** to a value less than or equal to the LDAP server paging size.

## LDAP fails to import binary data

To import binary data via LDAP, such as a user photo, you must include the binary attribute in the MID Server property **glide.ldap.binary\_attributes**. For the user photo example, the attribute may be `jpegphoto`.

