---
title: Enforced Restrictions for case\(s\)
description: Use this feature to restrict a case and provide list of groups and users who can access it.
locale: en-US
release: xanadu
product: Threat Intelligence Security Center
classification: threat-intelligence-security-center
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Creating cases using Threat Analyst Workbench, Threat Analyst Workbench, Use, Threat Intelligence Security Center, Security Operations]
---

# Enforced Restrictions for case\(s\)

Use this feature to restrict a case and provide list of groups and users who can access it.

Role required:

-   sn\_sec\_tisc\_admin
-   sn\_sec\_tisc.restriction\_access\_manager

## Key considerations

1.  Restrict a case and provide list of groups/users who can access it.
2.  Enable Enforce restriction field on the Case form page.
3.  Modify members of allowed group and allowed members.
4.  Once a case is marked as restricted, only members of allowed groups, member of allowed user list and user with sn\_sec\_tisc.admin role can access this case.
5.  Grant access to the analyst \(sn\_sec\_tisc.restriction\_access\_manager\) who needs to access to the Enforce restriction field.
6.  Existing assigned\_to analyst and analyst who marked it as restricted will also loose access if they are not added to the allowed groups or members.
7.  Restriction of case within CTI team is implemented on per-case basis. Allowed members can access restricted cases if they are in allowed list. Putting them in one of the cases allowed list doesn’t imply that they can access all other restricted cases.
8.  If case is marked restricted and allowed members or allowed group is left empty then only sn\_sec\_tisc.admin can access those restricted cases.
9.  Only the groups who has the analyst \(sn\_sec\_tisc.analyst\) role assigned, are allowed in the allowed members and allowed groups list.

    **Note:** A worknote is posted if a case is marked as restricted.


-   **[Access controls for a case](tisc-access-controls.md)**  
Allow access controls specific to a case.
-   **[External user access for case tasks](tisc-external-users-access.md)**  
This section describes the external user access for case tasks.

**Parent Topic:**[Creating cases using Threat Analyst Workbench](../concept/create-cases-using-threat-analyst-workbench.md)

