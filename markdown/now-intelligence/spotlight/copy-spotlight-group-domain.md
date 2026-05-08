---
title: Copy a Spotlight group to domains
description: You can copy a Spotlight group to other domains, saving the effort of reproducing the group manually for each domain.
locale: en-US
release: australia
product: Spotlight
classification: spotlight
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Ranking records with Spotlight, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Copy a Spotlight group to domains

You can copy a Spotlight group to other domains, saving the effort of reproducing the group manually for each domain.

## Before you begin

Finish configuring the Spotlight group that you want to copy.

Role required: admin, pa\_spotlight\_copy\_domain

## About this task

When you first create a Spotlight group, it is created in the domain that you are logged in to. To create identical Spotlight groups in other domains, use the copying function. The copying function follows the ServiceNow AI Platform® domain separation.

## Procedure

1.  Locate and open the Spotlight group record from the **Spotlight Groups** list.

2.  Click **Copy to Domain**.

3.  In the Copy Spotlight Group dialog, select a value for **Name Preference**.

<table id="choicetable_vdg_jsl_dhb"><thead><tr><th align="left" id="d199166e85">

Value

</th><th align="left" id="d199166e88">

Description

</th></tr></thead><tbody><tr><td id="d199166e94">

**Do not change the name**

</td><td>

All copies will have the same name as the original Spotlight group.

</td></tr><tr><td id="d199166e103">

**Change the name**

</td><td>

Manually write a new name that will be given to all copies of the Spotlight group.

</td></tr><tr><td id="d199166e112">

**Add domain name to new name as prefix**

</td><td>

For each copy of the Spotlight group, the domain name is added to the beginning of the Spotlight group name. You can keep the base name from the original Spotlight group or specify a new one.The **New Name** field does not show these prefixes.

</td></tr><tr><td id="d199166e127">

**Add domain name to new name as suffix**

</td><td>

For each copy of the Spotlight group, the domain name is added to the end of the Spotlight group name. You can keep the base name from the original Spotlight group or specify a new one.The **New Name** field does not show these suffixes.

</td></tr></tbody>
</table>4.  Fill out the remaining fields of the **Copy Spotlight Group** dialog as follows:

    |Field|Description|
    |-----|-----------|
    |New Name|Editable field showing the name of the Spotlight group copies you are creating. This field appears if you select any value for **Name Preference** other than **Do not change the name**. All copies have the same name unless you select **Add domain name to new name as prefix** or **Add domain name to new name as suffix**. The domain name prefixes or suffixes do not appear in this field.|
    |Domain|Select any number of domains. The choices include the parent domain and all subdomains. A copy of the Spotlight group is made for each selected domain.|

5.  Click **OK**.

    The Spotlight group is copied. If copying is successful, a list of the Spotlight groups that you have just created opens. If any error messages or warnings appeared during the copying process, read the [Spotlight group copy logs](../concept/spotlight-copy-logs.md#).

6.  Open each of the Spotlight groups you have just created and perform the following steps:

    1.  Verify that the **Run as** user has access to the domain of the Spotlight group and change this user if necessary.

    2.  Review the Spotlight job schedule and adjust as necessary.

    3.  Activate the Spotlight group.


## Copying a Spotlight group to multiple domains

In this example, the ACME - Incident Spotlight group, which was created in the ACME domain, is copied to the subdomains for the ACME company product divisions.

1.  Open the Spotlight Groups list and click **ACME - Incident Spotlight.**.

    ![The Spotlight Groups list with ACME - Incident Spotlight highlighted](../image/spotlight-select-group-domain.png)

2.  The Incident Spotlight group record opens, and you click **Copy to domain**.![Spotlight group record with the Copy to Domain button highlighted](../image/spotlight-copy-to-domain.png)
3.  In the **Copy Spotlight Group** dialog, you select the ACME - Metallurgy and ACME - Rocketry subdomains. Only ACME and ACME subdomains are available because the original Spotlight group was created in the ACME domain. You want the domain names to appear at the beginning of the group names, so you also select **Add domain name to new name as prefix**.![Copy Spotlight Group dialog, with the ACME - Metallurgy and ACME - Rocketry subdomains about to be selected.](../image/spotlight-copy-group-domains.png)
4.  Because the domain names that will be added as prefixes begin with ACME, you do not need ACME in the base name of the group. Therefore, you remove it.![The filled-out Copy Spotlight Group dialog with the new group name shortened](../image/spotlight-copy-group-short-name-domains.png)
5.  You click **OK**, and you are taken to a list showing you the Spotlight groups that you have just created. Note that both have the base name Incident Spotlight, as shown in the New Name field of the **Copy Spotlight Group** dialog, with the domain name added as a prefix. ![List of the new Spotlight groups you have created by copying a group.](../image/spotlight-new-group-copies-domain.png)
6.  In the **Run as** field, you browse for a user in the ACME - Metallurgy domain and select Wiley C. Latrans. Only global users and users in the domain of the Spotlight group are available. Spotlight jobs run more efficiently with a **Run as** user in the same domain as the Spotlight group, because only the records visible to this domain are evaluated.

    ![Selecting a TOP/ACME/ACME - Metallurgy user as the Run As user.](../image/spotlight-acme-employee-domain.png)

7.  Review the Spotlight job run schedule, and activate the Spotlight group.

    ![Activating the ACME - Metallurgy - Incident Spotlight group](../image/spotlight-group-domain-activate.png)

8.  You verify the schedule for the ACME - Rocketry - Incident Spotlight group and activate the group.

## What to do next

If any error messages or warnings appeared during the copying process, read the [Spotlight group copy logs](../concept/spotlight-copy-logs.md#).

**Parent Topic:**[Ranking records with Spotlight](../concept/spotlight.md)

