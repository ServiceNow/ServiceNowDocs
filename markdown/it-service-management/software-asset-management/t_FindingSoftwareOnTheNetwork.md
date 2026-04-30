---
title: Find software on the network using the legacy Software Asset Management plugin
description: After using a discovery tool, you can find a definitive list of all the software found on the network using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.
locale: en-US
release: xanadu
product: Software Asset Management
classification: software-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Determine where software is installed using the legacy Software Asset Management plugin, Legacy Software Asset Management plugin, ITSM Software Asset Management, Asset Management, IT Service Management]
---

# Find software on the network using the legacy Software Asset Management plugin

After using a discovery tool, you can find a definitive list of all the software found on the network using the legacy Software Asset Management \(com.snc.software\_asset\_management\) plugin.

## Before you begin

Role required: sam

## About this task

**Note:** A user with the Asset role can delete software installations, but it is not recommended. As an alternative, archive software installation information.

## Procedure

1.  Navigate to **All** &gt; **Software Asset** &gt; **Discovery** &gt; **Discovery Models**.

    A software administrator can, for example, look at the list and see that Adobe Acrobat 9.0, 9.2, 9.3, and 9.5 were found. Then, the administrator can edit software discovery models so all the dot versions are considered version 9.0 when doing reconciliation.

2.  Click a **Display Name** in a row.

    All installations that map to an individual software discovery model are displayed.

    All fields on the form are read-only.

    |Field|Description|
    |-----|-----------|
    |Display name|Name of the software installation as it appears in record lists.|
    |Publisher|Publisher of the software.|
    |Version|Version of the software.|
    |Discovery model|Software discovery model that represents the installed software.|
    |Prod id|Number created by the publisher to identify the software.|
    |Install location|Path under which the software is installed.|
    |Install date|Date on which the software was installed.|
    |Revision|Revision of the software.|
    |Instance key|Encrypted credentials for the software installation.|
    |Installed on|Hardware on which the software is installed.|
    |Uninstall string|Identifier used to uninstall the software.|
    |ISO serial number|ISO number of the software.|
    |Foreground|Duration of foreground usage of the software.|
    |Background|Duration of background usage of the software.|
    |Last scanned|Date and time on which the software was last discovered on this hardware.|
    |Last used|Date and time on which the software was last used on this hardware.|
    |Counted by|The counter summary name that the installation is counted on.|
    |Entitlement|Entitlement that is associated with the software installation.|
    |Inferred suite|Software suite inferred by the inference parameters.|
    |Valuation|Indicates the number of rights the install has.|
    |Cached|If checked, the license installation has already been counted.|
    |Omit from suites|If checked, the license is ignored for any suite calculations. This box is automatically checked if the install finds a possible entitlement of the exact software model for this configuration item.|

    **Note:** Third-party discovery tools can use software normalization to more effectively manage the software installation database. Software normalization allows you to standardize your software installation data, such as the display name, publisher, revision, and version. You can personalize the software installation form to include these normalization fields. For more information, see [Personalize a form](https://www.servicenow.com/docs/access?context=t_PersonalizeAForm&version=xanadu&pubname=xanadu-platform-user-interface&ft:locale=en-US).


**Parent Topic:**[Determine where software is installed using the legacy Software Asset Management plugin](../concept/c_DeterminWhereSWInstalled.md)

