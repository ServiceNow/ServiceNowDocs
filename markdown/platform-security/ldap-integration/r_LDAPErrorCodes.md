---
title: LDAP error codes
description: The LDAP Log file lists industry standard error codes for both LDAP and Active Directory \(AD\).
locale: en-US
release: xanadu
product: LDAP integration
classification: ldap-integration
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [LDAP integration troubleshooting, LDAP integration, Authentication, Access Management]
---

# LDAP error codes

The LDAP Log file lists industry standard error codes for both LDAP and Active Directory \(AD\).

## Standard error codes

|Error / data code|Text|Description|
|-----------------|----|-----------|
|0|LDAP\_SUCCESS|Indicates the requested client operation completed successfully.|
|2|LDAP\_PROTOCOL\_ERROR|Indicates that the server has received an invalid or malformed request from the client.|
|3|LDAP\_TIMELIMIT\_EXCEEDED|Indicates that the operation's time limit specified by either the client or the server has been exceeded. On search operations, incomplete results are returned.|
|4|LDAP\_SIZELIMIT\_EXCEEDED|Indicates that in a search operation, the size limit specified by the client or the server has been exceeded. Incomplete results are returned.|
|5|LDAP\_COMPARE\_FALSE|Does not indicate an error condition. Indicates that the results of a compare operation are false.|
|6|LDAP\_COMPARE\_TRUE|Does not indicate an error condition. Indicates that the results of a compare operation are true.|
|7|LDAP\_AUTH\_METHOD\_NOT\_SUPPORTED|Indicates that during a bind operation the client requested an authentication method not supported by the LDAP server.|
|8|LDAP\_STRONG\_AUTH\_REQUIRED|Indicates one of the following: In bind requests, the LDAP server accepts only strong authentication. In a client request, the client requested an operation such as delete that requires strong authentication. In an unsolicited notice of disconnection, the LDAP server discovers the security protecting the communication between the client and server has unexpectedly failed or been compromised.|
|9| |Reserved.|
|10|LDAP\_REFERRAL|Does not indicate an error condition. In LDAPv3, indicates that the server does not hold the target entry of the request, but that the servers in the referral field may.|
|11|LDAP\_ADMINLIMIT\_EXCEEDED|Indicates that an LDAP server limit set by an administrative authority has been exceeded.|
|12|LDAP\_UNAVAILABLE\_CRITICAL\_EXTENSION|Indicates that the LDAP server was unable to satisfy a request because one or more critical extensions were not available. Either the server does not support the control or the control is not appropriate for the operation type.|
|13|LDAP\_CONFIDENTIALITY\_REQUIRED|Indicates that the session is not protected by a protocol such as Transport Layer Security \(TLS\), which provides session confidentiality.|
|14|LDAP\_SASL\_BIND\_IN\_PROGRESS|Does not indicate an error condition, but indicates that the server is ready for the next step in the process. The client must send the server the same SASL mechanism to continue the process.|
|15| |Not used.|
|16|LDAP\_NO\_SUCH\_ATTRIBUTE|Indicates that the attribute specified in the modify or compare operation does not exist in the entry.|
|17|LDAP\_UNDEFINED\_TYPE|Indicates that the attribute specified in the modify or add operation does not exist in the LDAP server's schema.|
|18|LDAP\_INAPPROPRIATE\_MATCHING|Indicates that the matching rule specified in the search filter does not match a rule defined for the attribute's syntax.|
|19|LDAP\_CONSTRAINT\_VIOLATION|Indicates that the attribute value specified in a modify, add, or modify DN operation violates constraints placed on the attribute. The constraint can be one of size or content \(string only, no binary\).|
|20|LDAP\_TYPE\_OR\_VALUE\_EXISTS|Indicates that the attribute value specified in a modify or add operation already exists as a value for that attribute.|
|21|LDAP\_INVALID\_SYNTAX|Indicates that the attribute value specified in an add, compare, or modify operation is an unrecognized or invalid syntax for the attribute.|
|22-31| |Not used.|
|32|LDAP\_NO\_SUCH\_OBJECT|Indicates the target object cannot be found. This code is not returned on following operations: Search operations that find the search base but cannot find any entries that match the search filter. Bind operations.|
|33|LDAP\_ALIAS\_PROBLEM|Indicates that an error occurred when an alias was dereferenced.|
|34|LDAP\_INVALID\_DN\_SYNTAX|Indicates that the syntax of the DN is incorrect. \(If the DN syntax is correct, but the LDAP server's structure rules do not permit the operation, the server returns code 53: LDAP\_UNWILLING\_TO\_PERFORM.\)|
|35|LDAP\_IS\_LEAF|Indicates that the specified operation cannot be performed on a leaf entry. \(This code is not currently in the LDAP specifications, but is reserved for this constant.\)|
|36|LDAP\_ALIAS\_DEREF\_PROBLEM|Indicates that during a search operation, either the client does not have access rights to read the aliased object's name or dereferencing is not allowed.|
|37-47| |Not used.|
|48|LDAP\_INAPPROPRIATE\_AUTH|Indicates that during a bind operation, the client is attempting to use an authentication method that the client cannot use correctly. For example, either of the following cause this error: The client returns simple credentials when strong credentials are required...OR...The client returns a DN and a password for a simple bind when the entry does not have a password defined.|
|49|LDAP\_INVALID\_CREDENTIALS|Indicates that during a bind operation one of the following occurred: The client passed either an incorrect DN or password, or the password is incorrect because it has expired, intruder detection has locked the account, or another similar reason. See the data code for more information.|
|49 / 52e|AD\_INVALID CREDENTIALS|Indicates an Active Directory \(AD\) AcceptSecurityContext error, which is returned when the username is valid but the combination of password and user credential is invalid. This is the AD equivalent of LDAP error code 49.|
|49 / 525|USER NOT FOUND|Indicates an Active Directory \(AD\) AcceptSecurityContext data error that is returned when the username is invalid.|
|49 / 530|NOT\_PERMITTED\_TO\_LOGON\_AT\_THIS\_TIME|Indicates an Active Directory \(AD\) AcceptSecurityContext data error that is logon failure caused because the user is not permitted to log on at this time. Returns only when presented with a valid username and valid password credential.|
|49 / 531|RESTRICTED\_TO\_SPECIFIC\_MACHINES|Indicates an Active Directory \(AD\) AcceptSecurityContext data error that is logon failure caused because the user is not permitted to log on from this computer. Returns only when presented with a valid username and valid password credential.|
|49 / 532|PASSWORD\_EXPIRED|Indicates an Active Directory \(AD\) AcceptSecurityContext data error that is a logon failure. The specified account password has expired. Returns only when presented with valid username and password credential.|
|49 / 533|ACCOUNT\_DISABLED|Indicates an Active Directory \(AD\) AcceptSecurityContext data error that is a logon failure. The account is currently disabled. Returns only when presented with valid username and password credential.|
|49 / 568|ERROR\_TOO\_MANY\_CONTEXT\_IDS|Indicates that during a log-on attempt, the user's security context accumulated too many security IDs. This is an issue with the specific LDAP user object/account which should be investigated by the LDAP administrator.|
|49 / 701|ACCOUNT\_EXPIRED|Indicates an Active Directory \(AD\) AcceptSecurityContext data error that is a logon failure. The user's account has expired. Returns only when presented with valid username and password credential.|
|49 / 773|USER MUST RESET PASSWORD|Indicates an Active Directory \(AD\) AcceptSecurityContext data error. The user's password must be changed before logging on the first time. Returns only when presented with valid user-name and password credential.|
|50|LDAP\_INSUFFICIENT\_ACCESS|Indicates that the caller does not have sufficient rights to perform the requested operation.|
|51|LDAP\_BUSY|Indicates that the LDAP server is too busy to process the client request at this time but if the client waits and resubmits the request, the server may be able to process it then.|
|52|LDAP\_UNAVAILABLE|Indicates that the LDAP server cannot process the client's bind request, usually because it is shutting down.|
|52e|AD\_INVALID CREDENTIALS|Indicates an Active Directory \(AD\) AcceptSecurityContext error, which is returned when the username is valid but the combination of password and user credential is invalid. This is the AD equivalent of LDAP error code 49: LDAP\_INVALID\_CREDENTIALS.|
|53|LDAP\_UNWILLING\_TO\_PERFORM|Indicates that the LDAP server cannot process the request because of server-defined restrictions. This error is returned for the following reasons: The add entry request violates the server's structure rules...OR...The modify attribute request specifies attributes that users cannot modify...OR...Password restrictions prevent the action...OR...Connection restrictions prevent the action.|
|54|LDAP\_LOOP\_DETECT|Indicates that the client discovered an alias or referral loop, and is thus unable to complete this request.|
|55-63| |Not used.|
|64|LDAP\_NAMING\_VIOLATION|Indicates that the add or modify DN operation violates the schema's structure rules. For example, The request places the entry subordinate to an alias. The request places the entry subordinate to a container that is forbidden by the containment rules. The RDN for the entry uses a forbidden attribute type.|
|65|LDAP\_OBJECT\_CLASS\_VIOLATION|Indicates that the add, modify, or modify DN operation violates the object class rules for the entry. For example, the following types of request return this error: The add or modify operation tries to add an entry without a value for a required attribute. The add or modify operation tries to add an entry with a value for an attribute which the class definition does not contain. The modify operation tries to remove a required attribute without removing the auxiliary class that defines the attribute as required.|
|66|LDAP\_NOT\_ALLOWED\_ON\_NONLEAF|Indicates that the requested operation is permitted only on leaf entries. For example, the following types of requests return this error: The client requests a delete operation on a parent entry. The client request a modify DN operation on a parent entry.|
|67|LDAP\_NOT\_ALLOWED\_ON\_RDN|Indicates that the modify operation attempted to remove an attribute value that forms the entry's relative distinguished name.|
|68|LDAP\_ALREADY\_EXISTS|Indicates that the add operation attempted to add an entry that already exists, or that the modify operation attempted to rename an entry to the name of an entry that already exists.|
|69|LDAP\_NO\_OBJECT\_CLASS\_MODS|Indicates that the modify operation attempted to modify the structure rules of an object class.|
|70|LDAP\_RESULTS\_TOO\_LARGE|Reserved for CLDAP.|
|71|LDAP\_AFFECTS\_MULTIPLE\_DSAS|Indicates that the modify DN operation moves the entry from one LDAP server to another and requires more than one LDAP server.|
|72-79| |Not used.|
|80|LDAP\_OTHER|Indicates an unknown error condition. This is the default value for NDS error codes which do not map to other LDAP error codes.|
|775|USER\_ACCOUNT\_LOCKED|Indicates users are unable to log in because the user account is locked.|

## Customized error codes

|Error / data code|Text|
|-----------------|----|
|10000|LDAP\_ERROR\_GENEREL|
|10001|LDAP\_ERROR\_MAL\_FORMED\_URL|
|10002|LDAP\_ERROR\_UNAUTHENTICATED\_BIND|
|10300|LDAP\_ERROR\_COMMUNICATION\_EXCEPTION|
|10301|LDAP\_ERROR\_SOCKET\_TIMEOUT|
|10302|LDAP\_ERROR\_CONNECTION\_REFUSED|
|10303|LDAP\_ERROR\_CONNECTION\_RESET|
|10304|LDAP\_ERROR\_NO\_ROUTE|
|10305|LDAP\_ERROR\_UNKNOW\_HOST|
|10400|LDAP\_ERROR\_SSL\_EXCEPTION|
|10401|LDAP\_ERROR\_SSL\_EMPTY\_CERT\_STORE|
|10402|LDAP\_ERROR\_SSL\_CERT\_NOT\_FOUND|
|10403|LDAP\_ERROR\_SSL\_CERT\_EXPIRED|
|10500|LDAP\_ERROR\_INVALID\_SEARCH\_FILTER\_EXCEPTION|

