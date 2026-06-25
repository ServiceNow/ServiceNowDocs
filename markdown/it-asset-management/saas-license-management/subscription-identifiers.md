---
title: Subscription identifiers for SaaS and SSO applications
description: Use the SaaS License Management application to view, manage, and resolve subscription identifiers for your SaaS and SSO applications.Keep your SaaS and SSO license positions accurate and up to date by managing the updated subscription identifiers that are detected by the ServiceNow AI Platform.Maintain accurate license positions for your subscription software by resolving unrecognized subscription identifiers that are detected by the ServiceNow AI Platform.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/saas-license-management/subscription-identifiers.html
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [SaaS License Management, Software Asset Management, IT Asset Management]
---

# Subscription identifiers for SaaS and SSO applications

Use the SaaS License Management application to view, manage, and resolve subscription identifiers for your SaaS and SSO applications.

Subscription identifiers uniquely identify your SaaS and SSO applications. Each subscription identifier is associated with a discovery map and software model that help to normalize the software that is installed in your environment. You can use this information to track your software subscriptions and understand your license positions.

**Parent Topic:**[SaaS License Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/saas-license-management/sam-subscription-management.md)

**Related topics**  


[Request SaaS License Management]()

[SaaS License Management setup for large companies]()

[SaaS Overview dashboard]()

[Integrate with SaaS applications]()

[Integrate with SSO providers]()

[Playbook for SaaS integrations]()

[Viewing your SaaS and SSO subscriptions]()

[Review a software reclamation rule]()

[Reclaiming user subscriptions]()

[Create a child alias to set up multiple integration profiles]()

[Create a child alias to set up multiple Cisco Webex integration profiles]()

[Create a child alias to set up multiple Confluence Cloud integration profiles]()

[Create a child alias to set up multiple Jira integration profiles]()

[Associate a user with subscription records]()

[Disconnect SSO apps]()

[Delete an integration profile]()

[Subscription exclusions for SaaS and SSO applications]()

## Manage updated subscription identifiers

Keep your SaaS and SSO license positions accurate and up to date by managing the updated subscription identifiers that are detected by the ServiceNow AI Platform.

### Before you begin

Role required: sam\_integrator or admin

### About this task

When a SaaS or SSO provider updates an existing subscription identifier, the ServiceNow AI Platform automatically detects and pushes the changes to your ServiceNow instance through twice a week content updates. Changes include the product name, edition, version, platform, and language. Your instance uses this information to update subscription identifiers on existing software models, which can help prevent the creation of multiple software models for the same subscription software.

Subscription identifiers update either automatically or manually depending on the associated software model type. If a subscription identifier is associated with an auto-generated software model, it updates automatically. If a subscription identifier is associated with a customized software model, you must update it manually using software model suggestions. Software model suggestions identify changes to your existing subscription identifiers. You can use this information to determine whether you should update your customized software models based on the latest subscription identifiers. For example, if a SaaS provider updates the product name for an application, the software model suggestions identify both the current and updated values of the product name. If the changes are correct, you can accept the software model suggestions to update your software model with the latest product name.

**Note:** The navigation mentioned in the following procedure is in the Core UI and is available when the Software Asset Workspace isn't installed.

### Procedure

1.  Navigate to **All** &gt; **SaaS License** &gt; **Software Models**.

2.  Select a software model that is marked with a dot.

    A dot indicates that there are discrepancies between the associated subscription identifier and data that is provided in the latest content updates.

3.  On the Software Model form, open the software model suggestions by clicking the warning icon \[Omitted image "warning-icon.png"\] next to the **Display name** field.

    The Software Model Suggestions dialog box opens.

4.  In the dialog box, view the **Suggested discovery map** field to verify that your software model is using the discovery map for the updated subscription identifier.

    This field is read-only. However, you can select the preview icon \[Omitted image "preview-icon.png"\] to view additional information about the discovery map.

5.  Verify the changes to the subscription identifier.

    The Software Model Suggestions dialog box displays both the current and updated values of all subscription identifier fields. Although these fields are read-only, you can compare the values to understand how the subscription identifier has changed. Use this information to determine whether the changes are correct and should be applied to your software model.

    |Field|Description|
    |-----|-----------|
    |Suggested publisher|Updated software publisher.|
    |Publisher|Current software publisher.|
    |Suggested product|Updated software product name.|
    |Product|Current software product name.|
    |Suggested Version condition|Updated qualifier that you can use to compare the value of the software model **Version** field against the value of the discovery model **Version** field. Your instance uses qualifiers such as **is** or **is anything** to determine whether your discovered software applies to the software model.|
    |Version condition|Current qualifier that you can use to compare the value of the software model **Version** field against the value of the discovery model **Version** field. Your instance uses qualifiers such as **is** or **is anything** to determine whether your discovered software applies to the software model.|
    |Suggested version|Updated software version.|
    |Version|Current software version.|
    |Suggested Edition condition|Updated qualifier that you can use to compare the value of the software model **Edition** field against the value of the discovery model **Edition** field. Your instance uses qualifiers such as **is** or **is anything** to determine whether your discovered software applies to the software model.|
    |Edition condition|Current qualifier that you can use to compare the value of the software model **Edition** field against the value of the discovery model **Edition** field. Your instance uses qualifiers such as **is** or **is anything** to determine whether your discovered software applies to the software model.|
    |Suggested edition|Updated software edition.|
    |Edition|Current software edition.|
    |Suggested Platform condition|Updated qualifier that you can use to compare the value of the software model **Platform** field against the value of the discovery model **Platform** field. Your instance uses qualifiers such as **is** or **is anything** to determine whether your discovered software applies to the software model.|
    |Platform condition|Current qualifier that you can use to compare the value of the software model **Platform** field against the value of the discovery model **Platform** field. Your instance uses qualifiers such as **is** or **is anything** to determine whether your discovered software applies to the software model.|
    |Suggested platform|Updated platform on which you can install or run the software.|
    |Platform|Current platform on which you can install or run the software.|
    |Suggested Language condition|Updated qualifier that you can use to compare the value of the software model **Language** field against the value of the discovery model **Language** field. Your instance uses qualifiers such as **is** or **is anything** to determine whether your discovered software applies to the software model.|
    |Language condition|Current qualifier that you can use to compare the value of the software model **Language** field against the value of the discovery model **Language** field. Your instance uses qualifiers such as **is** or **is anything** to determine whether your discovered software applies to the software model.|
    |Suggested language|Updated language in which you want to run the software.|
    |Language|Current language in which you're running the software.|

6.  Accept or reject the changes.

    -   If the changes are correct, select **Accept** to update the software model with the suggested field values.
    -   If the changes are not correct, select **Reject** to ignore the suggested field values. The software model continues to use the existing subscription identifier.
    You automatically return to the Software Model form.

7.  Select **Update** to save your changes and clear the software model suggestions.


## Resolve unrecognized subscription identifiers

Maintain accurate license positions for your subscription software by resolving unrecognized subscription identifiers that are detected by the ServiceNow AI Platform.

### Before you begin

Role required: admin

### About this task

The ServiceNow AI Platform marks a subscription identifier as unrecognized when it is not associated with a software model. By associating the unrecognized subscription identifier with a software model, you can track subscription usage for the associated subscription software.

**Note:** The navigation mentioned in the following procedure is in the Core UI and is available when the Software Asset Workspace isn't installed.

### Procedure

1.  Send unrecognized subscription identifiers back to the ServiceNow content team by opting in to the Software Asset Management content service.

    When you opt in to the Software Asset Management content service, verify that the **Unrecognized Subscription Identifier** KPI is enabled. See [Enable sharing information with Software Asset Management content service](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/t_EnableSAMContentService.md) for detailed instructions.

2.  Navigate to **SaaS License** &gt; **Unrecognized Subscription Identifiers**.

3.  Select an unrecognized subscription identifier.

4.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Subscription identifier|Name of the unrecognized subscription identifier. This field populates automatically.|
    |Software model|Software model that you want to associate with the subscription identifier.|
    |Subscription profiles|Direct integration profiles that are associated with the subscription identifier. This field populates automatically.|
    |Number of subscriptions|Number of subscriptions that are associated with the subscription identifier. This field populates automatically.|
    |Exclude from content service|Option that prevents your ServiceNow instance from sending the unrecognized subscription identifier back to the ServiceNow content team. This option is applicable only if you opted in to the Software Asset Management content service.|

5.  Select **Update**.


### Result

After the subscription identifier associates with the specified software model, all related software subscriptions automatically update with that software model.

If you opted to share your unrecognized subscription identifier data with ServiceNow, your ServiceNow instance sends the unrecognized subscription identifier back to the ServiceNow content team. The content team can use this information to further research and improve the normalization process.

