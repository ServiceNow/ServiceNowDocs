---
title: Enforce SOAP request strict security \[Updated in Security Center 1.3\]
description: Use the glide.soap.strict\_security property to enforces web service security.
locale: en-US
release: xanadu
product: Instance Security Hardening Settings
classification: instance-security-hardening-settings
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Access control, Hardening settings, Platform Security]
---

# Enforce SOAP request strict security \[Updated in Security Center 1.3\]

Use the **glide.soap.strict\_security** property to enforces web service security.

This property uses a combination of:

-   Basic authentication challenge/response over the HTTP protocol and
-   System level access controls in the .

If you set this property to **true**, it performs the following actions:

-   If the user has appropriate role to perform the operation, it checks incoming SOAP request for role authorization to validate. It occurs during SOAP web service calls/requests made against ServiceNow AI Platform tables when performing CREATE, READ, UPDATE or DELETE operations.
-   Checks the system-level ACLs while retrieving data in the form of SOAP data on the table.
-   Checks the field-level ACLs for any CRUD operation performed against a field of table.

ACL checks are only complete for standard Table API calls and not web services.

## More information

<table id="table_ajc_b43_3kb"><thead><tr><th>

Attribute

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Property name

</td><td>

**glide.soap.strict\_security**

</td></tr><tr><td>

Configuration type

</td><td>

System Properties \(/sys\_properties\_list.do\)

</td></tr><tr><td>

Category

</td><td>

[Access control](sc-access-control.md)

</td></tr><tr><td>

Default value

</td><td>

true

</td></tr><tr><td>

Recommended value

</td><td>

true

</td></tr><tr><td>

Functional Impact

</td><td>

This remediation enforces the system-level access control while retrieving data from tables/pages in the form of SOAP data on the instance. If there are users currently accessing this data, they are restricted/allowed to access the data based on the ACL rules. For the default roles that have access to the SOAP data, see [SOAP web service](https://www.servicenow.com/docs/access?context=c_SOAPWebService&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US).

</td></tr><tr><td>

Security risk

</td><td>

\(Moderate\) Without appropriate authorization configured on the incoming SOAP requests, an unauthorized user can get access to sensitive content/data on the target instance.

</td></tr><tr><td>

References

</td><td>

[Enforce strict security for inbound SOAP](https://www.servicenow.com/docs/access?context=t_EnforceStrictSecurityWebSvcConns&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

 [SOAP web service](https://www.servicenow.com/docs/access?context=c_SOAPWebService&version=xanadu&pubname=xanadu-api-reference&ft:locale=en-US)

</td></tr></tbody>
</table>To learn more about adding or creating a system property, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

**Parent Topic:**[Access control](sc-access-control.md)

