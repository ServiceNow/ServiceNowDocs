---
title: Guidance for proper HR Service Delivery domain separation
description: Additional guidance to successfully deploy HR Service Delivery in a domain separated environment.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 4
breadcrumb: [Domain Separation and HR Service Delivery, HR Service Delivery, Employee Service Management]
---

# Guidance for proper HR Service Delivery domain separation

Additional guidance to successfully deploy HR Service Delivery in a domain separated environment.

The following sections explain how to successfully set up domain separation on your instance.

![Domain separation hierarchy](../image/domain-separation-hierarchy.png "Example of a domain separation hierarchy")

## HR Services

While you set up HR services in a global domain, note the following points:

-   **Limitations**
    1.  Administrator of any domain can edit the global HR services, which impacts all other domains.
    2.  An HR service that is created in a global domain will be present in all others domains.
-   **Instructions**
    -   This instruction applies to the first limitation: You can create or update write ACL on an HR service table so that the global HR services are only editable by HR admins in a global domain.
    -   This instruction applies to the second limitation: By using HR criteria, you can restrict global HR services to be used for certain domains only. However, this will not stop access for an global service to view and modify the global HR service by HR administrators.

## HR Approvals

While you set up HR approvals for domain separation, note the following points:

-   **Limitations**

    When the users of parent domain and child domain are added to same approval group:

    -   The parent domain's HR case is going for approval to a child domain even when the users of the child domain do not have access to the case. For example, the HR case in Domain \(Parent\) is going for approval to Domain 1 and Domain 2 users even when they do not have access to the case \(Refer to the domain hierarchy image\).
    -   The child domain's HR case is not going for approval to the parent domain even when the users of parent domain have access to the case. For example, the HR case in Domain 1 is not going for approval to users in Domain \(Parent\) even when they have access to the case.
-   **Instructions**

    Do not use global groups or groups in a parent domain for approvals. While using these groups for approval, verify that you use a flat domain hierarchy, otherwise use domain specific approval groups.


## HR Assignment rules

While you set up HR assignment rules for domain separation, note the following points:

-   **Limitations**

    When the users of parent domain and child domain are added to same approval group:

    -   The parent domain's HR case might be assigned to a child domain even when the users of the child domain do not have access to the case. For example, the HR case in Domain \(Parent\) might be assigned to Domain 1 and Domain 2 users even when they do not have access to the case \(Refer to the domain hierarchy image\).
    -   The child domain's HR case might not be assigned to the parent domain even when the users of parent domain have access to the case. For example, the HR case in Domain 1might not go for approval to Domain \(Parent\) users even when they have access to the case.
-   **Instructions**
    -   For an assignment rule in a domain, use group from the same domain.
    -   While using global groups for an assignment, use a flat domain hierarchy, otherwise use the domain specific assignment groups.

## HR Assignment group

While you set up HR assignment groups for domain separation, note the following:

-   **Limitation**

    For an HR case that is created in parent domain, assignment group from child domain can be selected. For example, for an HR case in Domain \(Parent\), user can select an assignment group from Domain 1.

-   **Instructions**

    Select the correct assignment group for a parent domain. Do not select an assignment group from a child domain.


## HR SLAs

While you set up HR SLAs for domain separation, note the following points:

As an administrator:

-   Set up domain specific SLA as per your requirement.
-   Set up global SLA definition if all domains require the same SLA definition.

## HR Response templates

While you set up HR response templates for domain separation, note the following points:

You can set up response templates with either global or a specific domain. Global templates will be accessible to all other domains, while a specific domain template will be accessible to that domain only.

## Advanced Work Assignment \(AWA\) for HR

While you set up HR live agent chat \(AWA\) for domain separation, note the following points:

-   **Limitations**

    When you have AWA set up with a global group, users from a specific domain are getting the **Connect to the live agent** option even when an agent from that domain is not available. For example, if available agents are only from Domain 1 and user from Domain 2 tries to connect to the live agent, user will get option to **Connect to a live agent**, but the actual routing to any agent will not happen.

-   **Instructions**

    AWA can be set up for both global or domain specific groups. If you are using global group for AWA setup, verify at least one of the global agent is always available.


## Escalation rules

While you set up escalation rules for domain separation, note the following point:

Set up escalation rules either at global or a domain specific layer. For an escalation rule in parent domain, do not select a group from child domains.

## Enterprise Service Management Integrations Framework

While you set up Enterprise Service Management Integrations Framework for domain separation, note the following points:

-   Maintain a separate connection record per domain.
-   Copy the default scheduled flow in to respective domain for each integrations.
-   Copy default Trigger external interface flow into respective domain.

