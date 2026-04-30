---
title: Walk-up Experience portal security and access
description: Security is built into the application to prevent end-user facing devices at the Walk-up Experience on-site portal from offering elevated role privileges to users. The Walk-up Experience on-site portal is accessed by an account containing only the sn\_walkup.walkup\_login role.
locale: en-US
release: xanadu
product: Walk-Up Experience
classification: walk-up-experience
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Configure, Walk-up Experience, IT Service Management]
---

# Walk-up Experience portal security and access

Security is built into the application to prevent end-user facing devices at the Walk-up Experience on-site portal from offering elevated role privileges to users. The Walk-up Experience on-site portal is accessed by an account containing only the sn\_walkup.walkup\_login role.

## Understanding Walk-up Experience portal security

Activate the Explicit Role \(com.glide.explicit\_roles\) plugin to assign users security roles, either snc\_internal or snc\_external. This plugin was introduced in the ServiceNow AI Platform Paris release. With the Quebec release, for new installations, Walk-up Experience added a dependency on this plugin to explicitly set the Walk-up Experience user as an external user.

When upgrading Walk-up Experience installations prior to Rome, the Walk-up Experience user is assigned snc\_internal instead of snc\_external. This is because the Explicit Role plugin assigns all users, including Walk-up Experience users, to snc\_internal. Walk-up Experience cannot remove snc\_internal during upgrade. For new installations of Walk-up Experience, this process works automatically.

**Note:** Refer to [Explicit roles plugin](https://www.servicenow.com/docs/access?context=explicit-roles-plugin&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US) for details about the plugin and [Explicit Roles](https://www.servicenow.com/docs/access?context=explicit-roles&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for more information about this upgrade process.

## Access to Walk-up Experience

Agents opening up the on-site Walk-up location for business, or joining the support team during operation hours, access the user record account with sn\_walkup.walkup\_login role to log into the Walk-up Experience portal. Internal and external users can access the on-site Walk-up Experience portal via a check-in device, typically a tablet, to enter a queue. Internal, authenticated users can also access an online queue check-in via desktop or mobile device.

## Important information for upgrading Walk-up Experience to Xanadu

The Explicit Role \(com.glide.explicit\_roles\) plugin was introduced in the ServiceNow AI Platform Paris release. When installed, users are assigned security roles, either snc\_internal or snc\_external. With the Xanadu, release Walk-up Experience has added a dependency on this plugin to explicitly set the Walk-up Experience user as an external user.

When upgrading Walk-up Experience to Xanadu, the Walk-up Experience user is assigned snc\_internal instead of snc\_external. This is because the Explicit Role plugin assigns all users, including the Walk-up Experience user, to snc\_internal. Walk-up Experience cannot remove snc\_internal during upgrade. For new installs of Walk-up Experience, this process works without issue because the Explicit Role plugin installs first, assigns all users to snc\_internal, then the Walk-up Experience user account is created with the snc\_external role already assigned.

**Note:** Refer to [Explicit roles plugin](https://www.servicenow.com/docs/access?context=explicit-roles-plugin&version=xanadu&pubname=xanadu-source-to-pay-operations&ft:locale=en-US) for complete details about the plugin and ServiceNow AI Platform explicit roles.

After upgrading to Xanadu, you need to remove the snc\_internal role from the Walk-up Experience user account, or any users created to log into the Walk-up Experience kiosk. Then you need to add the snc\_external role to the users. This process is not necessary for upgrades after Xanadu.

**Note:** Refer to [Explicit Roles](https://www.servicenow.com/docs/access?context=explicit-roles&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US) for complete details about this process.

**Parent Topic:**[Configuring Walk-up Experience](walkup-experience-configuration.md)

