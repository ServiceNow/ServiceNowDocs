---
title: Manage risk events
description: Risk events are potential or actual financial and non-financial losses, near misses, and gains that occur within an organization. Risk events are also known as loss events or loss entries.After a risk event is created, the event goes through a life cycle where risk managers analyze it and send it for approval.Relating risk events to risks and relating a risk statement to a risk is important for all organizations that use the Risk Management application. Properties to enable these relationships are provided under Risk Event Properties and Risk Management properties.The risk event response template automates the process of adding approvers, issues, and owners to a risk event. This automation is based on the conditions defined in the template.Train a similarity solution definition that uses machine learning by activating the Governance, Risk, and Compliance: Predictive Intelligence plugin. The solution enables the system to display similar risk events automatically.
locale: en-US
release: xanadu
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Explore, Risk Management, Governance, Risk, and Compliance]
---

# Manage risk events

Risk events are potential or actual financial and non-financial losses, near misses, and gains that occur within an organization. Risk events are also known as loss events or loss entries.

To effectively manage risks, it's essential to monitor risk events. You must relate them to existing risks, perform a root-cause analysis, and track the remedial tasks. Organizations use risk events to understand their losses and to manage their risks more efficiently. Risk events do not only lead to losses. At times, risk events also result in gains for an organization. For example, in the banking industry, if there’s an error in a trading algorithm, it might result in a gain for an organization.

Any employee can report a risk event. After a risk event is reported, it is analyzed by the risk manager.

Risk events can be of two types:

-   **Internal risk events**

    Events that occur within your organization.

-   **External risk events**

    Events that occur in other organizations but are shared with the industry to ensure that other organizations can prevent them.


You can create a risk event using either the Service Portal or your ServiceNow instance. Risk events provide the following:

-   Concrete data that enables you to better quantify and validate existing risks.
-   Visibility into new risks because risk events often recur.

You can view the risk events dashboards by navigating to **Risk Events** &gt; **Overview**.

For information on how to configure risk event integration in the Risk Workspace, see the [Risk event integration in workspace \[KB0966898\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB0966898) article in the Now Support Knowledge Base.

**Related topics**  


[Risk events life cycle](manage-risk-events.md#)

## Risk events life cycle

After a risk event is created, the event goes through a life cycle where risk managers analyze it and send it for approval.

The life cycle for risk events goes through the following stages:

1.  Creating a risk event: A new event is reported by a business user. The event is pending validation by the event owner or risk manager who has the sn\_risk.manager role.
2.  Analyzing the risk event: The risk manager analyses if the event is legitimate and adds all the important information such as the event’s loss entries, approvers, the root cause of the event, and the preventative and remedial action for the event. In this state, additional information can be requested from the event creator. You can then create an issue to ensure that similar events do not occur in the future. The issues are assigned to the respective issue owners who can then either accept the issue as is or create a remediation task.
3.  Awaiting approval for the risk event: After all the data is entered and validated, the risk manager may request that the event be approved. The need for approval is determined by the loss threshold defined by the organization. For example, your organization may decide that if a risk event leads to a loss of $100000, then it must be approved by the senior risk management teams. Each event might go through several rounds of approval.
4.  Approving, rejecting, or canceling a risk event: After the event is approved, the risk manager ensures that the issues created for the risk event are closed and that the root-cause analysis \(RCA\) is complete before the event is closed. At this stage, the approver can also choose to reject or cancel the event with adequate reasons.
5.  Closing a risk event: After a user with the sn\_risk.manager role is certain that the event has been captured and that the RCA has been completed, the event coordinator can close the risk event. If a risk event has open issues and tasks, then the risk event cannot be closed until the associated issues and tasks are closed.

The risk events workflow is summarized in the following figure:

![Workflow of the risk event life cycle](../image/risk-events.png "Risk events workflow")

**Related topics**  


[Create a risk event in the Risk Workspace](../../grc-workspace-risk/task/create-risk-event-workspace.md)

## Relationship between risks, risk events, and risk statements

Relating risk events to risks and relating a risk statement to a risk is important for all organizations that use the Risk Management application. Properties to enable these relationships are provided under **Risk Event Properties** and Risk Management properties.

### Relationship of risk events to risk

Consider relating risk events to risks if you use the Risk Management application. This relationship provides data for future risk assessment and is also useful for accurate reporting. For example, if the management of an organization wants to know the total loss incurred due to internal fraud, it can only be reported if all the risks are related to the internal fraud risk event. To relate risks events to risk, set the **Make risk event to risk relationship mandatory** property to Yes. By default, this property is not turned on.

### Relationship of risk statement to risk

Consider relating each risk statement to a risk. Establishing this relationship prevents the creation of orphan risks. An orphan risk is a risk that does not have a corresponding risk statement associated with it. For example, if all the business units within an organization understand the risk of employee attrition in different terms, it is difficult for the organization to maintain comprehensive data on the risk of attrition. It is easier if the risk statement of Employee Attrition is attributed to all events that relate to this risk. Establishing the relationship between a risk statement and a risk is vital for correct reporting and prevention. To relate risks to risk statements, set **sn\_risk.risk\_statement\_mandatory** to True.

### Add Basel categories to risk statements

The Basel categorization is specific to the banking industry. This categorization helps customers comply with the Basel regulations by automating their loss event reporting. This particular setting enables the users to view the Basel Dashboards. The Basel Dashboard shows the number of loss events and net loss based on the Basel business lines and categories. Enabling this setting enables the users to view the Basel categorization tab where users can select one of the following Basel categories that apply.

-   Internal fraud
-   External fraud
-   Employment practices and workplace safety
-   Clients, products, and business practice
-   Damage to physical assets
-   Business disruption and system failures
-   Execution, delivery, and process management

For more information, see [Properties installed with Advanced Risk](../../grc-common/reference/advanced-risk-properties.md) and [Properties installed with Risk Management](r_PropInstallWRisk.md)

To enable Basel categorization, set **Show Basel attributes and reports** to **Yes**.

## Risk event response template

The risk event response template automates the process of adding approvers, issues, and owners to a risk event. This automation is based on the conditions defined in the template.

The risk event response template provides these primary benefits:

-   reduces the need for human handling of risk events during risk event creation.
-   automatically defines the risk event life cycle and how users respond to that risk event.
-   saves time with a predefined template.

For example, consider that a health and safety risk event has occurred. If the template is defined, the template can be used to assign the event to the person responsible for health and safety. The template facilitates the automatic assignment of risk events by enabling you to choose event types, entities, categories, and so on.

Users can define the threshold amount for risk event approvers. The threshold is defined based on the risk appetite of the customers. For example, an organization decides that a risk event resulting in a loss of $1000, does not need an approver. This threshold of $1000 can be defined in the template. If the organization determines that any amount greater than $1000 dollars needs approval, the template can automatically assign an approver.

You can define the template for any entity. All the child entities of the parent entity inherit the rules defined in the risk event response templates. Defining a template saves the time and effort required to define the rules for each entity separately.

For more information on how to set up risk event ingestion, see [KB0780985](https://support.servicenow.com/kb_view.do?sysparm_article=KB0780985) article in the Now Support Knowledge Base.

## Associate similar risk events

Train a similarity solution definition that uses machine learning by activating the Governance, Risk, and Compliance: Predictive Intelligence plugin. The solution enables the system to display similar risk events automatically.

The Governance, Risk, and Compliance: Predictive Intelligence plugin uses Artificial Intelligence \(AI\) and Machine Learning \(ML\) to manage the risk events more efficiently. You can identify similar risk events and group them to capture and analyze the actual impact of the risk event.

For example, in an organization with operations in multiple locations, the risk event teams across different locations may be working on similar types of risk events. This challenge results in duplicate efforts to manage the risk events within the organization. This capability reduces the manual effort in managing similar risk events and improves overall organizational efficiency.

You can associate similar risk events only when the main risk event is in the **Analyze** state. Also, the Associate risk event button is unavailable for similar risk events that are in the **New** or **Rejected** state.![Similar risk events](../../grc-workspace-risk/image/similar-risk-event.png)

The platform machine learning administrator \(ml\_admin\) can create a solution definition and modify an existing one. You can navigate to **Risk Events** &gt; **Administration** &gt; **Properties** to update the risk event property with the new solution definition name.

