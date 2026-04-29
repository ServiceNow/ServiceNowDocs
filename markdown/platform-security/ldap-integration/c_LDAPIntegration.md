---
title: Lightweight Directory Access Protocol integration
description: An LDAP integration allows your instance to use your existing LDAP server as the primary source of user data.
locale: en-US
release: australia
product: LDAP integration
classification: ldap-integration
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Authentication, Access Management]
---

# Lightweight Directory Access Protocol integration

An LDAP integration allows your instance to use your existing LDAP server as the primary source of user data.

Administrators integrate with a Lightweight Directory Access Protocol \(LDAP\) directory to streamline the user login process and to automate administrative tasks such as creating users and assigning them roles. An LDAP integration allows the system to use your existing LDAP server as the primary source of user data. Typically, an LDAP integration is also part of a single sign-on implementation.

The integration uses the LDAP service account credentials to retrieve the user distinguished name \(DN\) from the LDAP server. Given the DN value for the user, the integration then rebinds with LDAP with the user's DN and password. The password that the user enters is contained entirely in the HTTPS session. The integration never stores LDAP passwords.

The integration uses a read-only connection that never writes to the LDAP directory. The integration only queries for information, and then updates its internal database accordingly.

**Note:** For detailed information about setting up the integration, see [LDAP integration setup](c_LDAPIntegrationSetup.md).

**Note:** If your instance is using an LDAP integration and the Active Directory settings require users to reset their password upon login, your users will not be able to log in the instance. The instance cannot change any user's active directory password.

## Features of LDAP integration

LDAP integration features include the following.

-   **Scheduled LDAP refresh**

    A scheduled scan of your LDAP server is usually run once a night. It queries all applicable user records' attributes and compares them with the account on our servers. If there is a difference, we modify our user record with the changed attribute. The load placed upon the LDAP server during the refresh depends on how many records are queried, and the number of attributes being compared. We recommend scheduling the refresh during off-peak hours. A large refresh operation can affect other scheduled operations, such as running reports, and should be planned to minimize any conflicts.

-   **LDAP listener**

    LDAP listener is our version of a persistent query \(or persistent search\). We issue a standing query for changes made to your LDAP server, and constantly listen for a response. Assuming your server supports a persistent search, any changes made to any of your applicable LDAP accounts are returned to the LDAP listener and sent to your instance within approximately 10 seconds. This is an extremely useful tool, allowing us to have a nearly real-time copy of your users' account details, without having to wait for the next scheduled refresh.

-   **On-demand LDAP login**

    After an LDAP integration is established, the instance can allow new users to log in to the system even if they do not yet have an account on the instance. When a new user attempts to log in to the instance, the integration checks to see if this user has an account in the instance. If the integration does not find an existing user account, it automatically queries the LDAP server for the username that was entered. If a matching LDAP account is found, the integration tries to authenticate with the password the user entered. If the password is valid, the instance creates an account for the user, populates the account with all applicable LDAP information, and logs the user in to the instance.

    On-demand login uses the LDAP User Import transform map. For more information on transform map requirements, see [LDAP transform maps](c_LDAPTransformMaps.md).

-   **LDAP data population**

    **Note:** Functionality described in this integration is not available by default. This integration involves post-deployment customization performed by an experienced administrator or by ServiceNow professional services consultants.

    An integration to the LDAP servers allows you to quickly and easily populate the instance's database with user records from the existing LDAP database. To prevent data inconsistencies, you can create, ignore, or skip incoming LDAP records.

    You can also limit the data the integration imports by specifying LDAP attributes, thereby importing only the data that you want to expose to an instance. Typically, the LDAP attributes you specify become part of the integration [transform map](c_LDAPTransformMaps.md). If you do not specify any LDAP attributes, the integration imports all available object attributes from the LDAP server. The instance stores imported LDAP data in temporary import set tables, so the more attributes you import, the longer the import time. For more information, see [Specify the LDAP attributes](../task/t_SpecifyLDAPAttributes.md).

-   **LDAP authentication**

    Use LDAP authentication to access using LDAP credentials.

    When a user enters network credentials in the login page:

    1.  The instance passes the credentials to an LDAP server to find the instance.
    2.  With RDNs, it validates the user's DN string. It validates only if at least one of the LDAP OU configurations with `table=sys_user` has an RDN configured.
    3.  The LDAP server responds with an authorized or unauthorized message that the system uses to determine whether access should be granted.
    By authenticating against your LDAP server, users access the platform with the same credentials that they use for other internal resources on your network domain. Also, you can reuse any existing password and security policies that are already in place. For example, the LDAP server may already have account lockout and password expiration policies.

    When you enable LDAP, the system updates user records with these fields.

    |Field|Description|
    |-----|-----------|
    |Source|Identifies whether or not LDAP is used to validate a user. If the source starts with ldap, then the user is validated via LDAP. If the source does not start with ldap, then the password on the user record is used to validate the user upon login.|
    |LDAP Server|Identifies which LDAP server authenticates the user when there are multiple LDAP servers.|

    **Note:** The system does not support LDAP password authentication through a MID Server. An instance must be able to directly connect with an LDAP server to support password authentication.


