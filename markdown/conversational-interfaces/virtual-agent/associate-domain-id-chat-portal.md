---
title: Associate a domain ID with a chat portal
description: The Service Portal platform is not domain-separated, but you can create different versions of a portal and restrict each version's use to a single domain for chat purposes. For example, you could create two employee service portals and define a different domain for each.
locale: en-US
release: zurich
product: Virtual Agent
classification: virtual-agent
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
keywords: [Associate, Domain, ID, chat, portal]
breadcrumb: [Domain separation and Virtual Agent, Virtual Agent technical reference, Virtual Agent reference, Virtual Agent, Conversational Interfaces]
---

# Associate a domain ID with a chat portal

The Service Portal platform is not domain-separated, but you can create different versions of a portal and restrict each version's use to a single domain for chat purposes. For example, you could create two employee service portals and define a different domain for each.

## Before you begin

Role required: admin

## About this task

Elements of the Service Portal platform such as settings, portals, pages and widgets are not domain-separated. However, the data within widgets does display when based on the appropriate domain. To provide different experiences, admins should create separate service portals, each with unique URLs, that they can redirect users to. For a domain-separated chat experience in the chat widget channel, create a portal and use the **sysparm\_domain\_id** parameter in the URL to designate the domain. For more information, see [Virtual Agent URL parameters](../reference/va-sysparm.md).

## Procedure

1.  [Create a new domain](https://www.servicenow.com/docs/access?context=t_CreateADomain&version=zurich&pubname=zurich-platform-security&ft:locale=en-US) and assign roles to the domain as needed.

2.  Copy the domain's sys ID.

    1.  Navigate to **All** &gt; **Domain Admin** &gt; **Domains**.

    2.  Right-select the name of a domain, and then select **Copy sys\_id**.

        ![Copy the sys ID for the domain.](../images/copy-domain-sys-id.png)

    3.  Paste the ID in a text editor and save it for later.

3.  Navigate to **All** &gt; **Service Portal** &gt; **Agent Chat**.

4.  Select the name of the portal that you want to restrict to a domain, or [create a new one](https://www.servicenow.com/docs/access?context=create-a-portal&version=zurich&pubname=zurich-platform-user-interface&ft:locale=en-US).

    If prompted, open the record for editing.

5.  In the **Server script** area, add the **domain\_id** parameter and the domain's sys ID that you copied earlier.

    ![Add the domain_id parameter to the portal script.](../images/add-domain-id-chat-portal.png)

6.  Select **Update** or **Submit** to save your changes.


## Result

The **sysparm\_domain\_id** parameter gets passed in the portal URL.

**Parent Topic:**[Domain separation and Virtual Agent](../concept/domain-separation-virtual-agent.md)

