---
title: Post-clone Discovery configuration
description: When a clone occurs, Discovery schedules are copied from the source instance to the target instance. Additional configuration is necessary for these schedules to function correctly on the target instance, helping you properly configure Cloud-based and IP-based Discovery schedules and maintain optimal performance.
locale: en-US
release: australia
product: Discovery
classification: discovery
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Advanced Discovery configuration, Configuring Discovery, Discovery, ITOM Visibility, IT Operations Management]
---

# Post-clone Discovery configuration

When a clone occurs, Discovery schedules are copied from the source instance to the target instance. Additional configuration is necessary for these schedules to function correctly on the target instance, helping you properly configure Cloud-based and IP-based Discovery schedules and maintain optimal performance.

**Note:**

For general information about instance cloning, see the [Clone FAQS-Frequently Asked Questions \[KB0715621\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0715621) article in the Now Support Knowledge Base.

For instructions on how to deactivate or cancel a Discovery schedule after creating a clone, see the [A Post-Clone script to Deactivate and Cancel Discovery Schedules \[KB0789119\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0789119) article in the Now Support Knowledge Base.

## Post-clone target configuration for IP-based Discovery schedules

After completing the [Request a clone](https://www.servicenow.com/docs/access?context=t_StartAClone&version=australia&pubname=australia-platform-administration&ft:locale=en-US) process, post-clone configuration is determined by the MID Server selection method you chose in the Discovery schedule on the source instance.

<table id="table_yb1_v45_nfc"><thead><tr><th>

MID Server selection method

</th><th>

Next steps

</th></tr></thead><tbody><tr><td>

Specific MID

</td><td>

Update the MID Server record for each Discovery schedule.

</td></tr><tr><td>

Cluster

</td><td>

Create the cluster, attach the MID Server to the cluster, and then update the cluster name in the Discovery schedule.Alternatively, remove the MID cluster \[ecc\_agent\_cluster\] record from the Clone Exclude Tables \[clone\_data\_exclude\]. For more information, see [Exclude a table from cloning](https://www.servicenow.com/docs/access?context=t_ExcludeATableFromCloning&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Use Behavior

</td><td>

Create the behaviors, create a functionality or attach an existing functionality, then go back to the Discovery schedule and attach the behavior to the Discovery schedule.**Note:** Discovery functionalities aren’t cloned with an instance.

</td></tr><tr><td>

Auto-select

</td><td>

Verify all MID Servers on the target instance are set up with target IP ranges, supported applications, and capabilities.

</td></tr></tbody>
</table>## Post-clone target configuration for Cloud Discovery schedules

After completing the [Request a clone](https://www.servicenow.com/docs/access?context=t_StartAClone&version=australia&pubname=australia-platform-administration&ft:locale=en-US) process, you must access the Cloud Service Account \[cmdb\_ci\_cloud\_service\_account\] table and update the service accounts with the proper reference to the Discovery credentials. You must also update the MID Servers for the Discovery schedule. Additional post-clone configuration is determined by the MID Server selection method that you chose in the original Discovery schedule.

<table id="table_pkd_skl_kfc"><thead><tr><th>

MID Server selection method

</th><th>

Next steps

</th></tr></thead><tbody><tr><td>

Specific MID

</td><td>

Update the MID Server record for each Discovery schedule.

</td></tr><tr><td>

Cluster

</td><td>

Create the cluster, attach the MID Server to the cluster, and then update the cluster name in the Discovery schedule.Alternatively, remove the MID cluster \[ecc\_agent\_cluster\] record from the Clone Exclude Tables \[clone\_data\_exclude\]. For more information, see [Exclude a table from cloning](https://www.servicenow.com/docs/access?context=t_ExcludeATableFromCloning&version=australia&pubname=australia-platform-administration&ft:locale=en-US).

</td></tr><tr><td>

Use Behavior

</td><td>

Create the behaviors, create a functionality or attach an existing functionality, then go back to the Discovery schedule and attach the behavior on the target instance.**Note:** Discovery functionalities aren’t cloned with an instance.

</td></tr><tr><td>

Auto-select

</td><td>

Verify that all MID Servers are set up with target IP ranges, supported applications, and capabilities.

</td></tr></tbody>
</table>For more information, see the [Cloud discovery schedules fail after the instance clone \[KB1759363\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1759363) article in the Now Support Knowledge Base.

## Clone Exclusions

Credential aliases are cloned but their credentials aren’t cloned. If Discovery schedules have credential aliases, you must go to the Connection &amp; Credential Aliases \[sys\_alias\] table and confirm the alias points to the correct credentials. After cloning, update the Discovery schedules and add credentials within the target instance.

Additionally, no MID Server related tables are cloned. For more details, see the [MID Servers and Clones \[KBKB0786475\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB0786475) article in the Now Support Knowledge Base.

**Parent Topic:**[Advanced Discovery configuration](c_DiscoveryExtendedCapabilities.md)

**Related topics**  


[Managing Instance Clone](https://www.servicenow.com/docs/access?context=using-instance-clone&version=australia&pubname=australia-platform-administration&ft:locale=en-US)

