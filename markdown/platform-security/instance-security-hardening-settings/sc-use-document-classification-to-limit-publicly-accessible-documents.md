---
title: Use Document Classification to limit publicly accessible documents \[New in Security Center 7.0\]
description: Control public access to permalinked documents using system properties.
locale: en-US
release: australia
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Use Document Classification to limit publicly accessible documents \[New in Security Center 7.0\]

Control public access to permalinked documents using system properties.

**Note:** This hardening setting is not a part of the hardening baseline. It does not appear in Security Center hardening pages and affect your hardening score.

By default, the Document Management plugin includes these classifications:

-   **public**
-   **restricted**
-   **confidential**
-   **none** \(no classification provided\)

Use the **com.snc.documents.permalink.allowed\_classifications** to create a list of document classifications. Documents under these classifications \(and documents without classification\) are publicly accessible to any unauthenticated users with an appropriate link.

Use this property to control public access to document permalinks. Previously, these links were publicly accessible to anyone with the link. The value of this property depends on your specific needs. You may have additional custom document categories that may need to be added to this property to enable public access.

Set the **com.snc.documents.permalink.allowed\_classifications** property value to a comma-separated list of document classifications. Documents with these classifications are publicly accessible by unauthenticated users.

If this property isn't present in the System Properties \[sys\_properties\] table, it defaults to an empty list. In this case, only documents with no classification are publicly accessible by unauthenticated users. The default value of this property is **public**, meaning that only documents classified as **public** or documents with no classification are accessible to unauthenticated users.

## More information

<table id="table_hhv_dvg_1xb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Configuration name

</td><td>

**com.snc.documents.permalink.allowed\_classifications**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Data type

</td><td>

String list

</td></tr><tr><td>

Recommended value

</td><td>

public

</td></tr><tr><td>

Default value

</td><td>

public

</td></tr><tr><td>

Fallback value

</td><td>

&lt;empty&gt;

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Security risk

</td><td>

-   Severity score: 5.3
-   CVSS score: Medium
-   If a document category containing documents which shouldn’t be publicly accessible is added to this property, it may expose sensitive information to unauthenticated users.

</td></tr><tr><td>

Functional impact

</td><td>

If a document category containing documents which should be publicly accessible isn’t added to this property, it prevents those documents from being accessed.

</td></tr><tr><td>

Dependencies and prerequisites

</td><td>

None

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=australia&pubname=australia-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

