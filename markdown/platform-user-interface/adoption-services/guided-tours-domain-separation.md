---
title: Domain separation and guided tours
description: With the ServiceNow Platform, service providers \(SPs\) can provide their customers with faster onboarding, meet compliance, and protect their data using domain separation. You can separate client data, processes, and reports into logical groupings called domains. SPs control who sees and accesses what content. You can create and modify guided tours that apply to specific domains in your instance as well as tours that are available to users globally.Once you create a guided tour, you can specify a domain to which it applies. You can also copy the tour so that you can modify it for a specific domain.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/platform-user-interface/adoption-services/guided-tours-domain-separation.html
release: xanadu
product: Adoption Services
classification: adoption-services
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Guided tours, Adoption services, Configure user experiences]
---

# Domain separation and guided tours

With the ServiceNow Platform, service providers \(SPs\) can provide their customers with faster onboarding, meet compliance, and protect their data using domain separation. You can separate client data, processes, and reports into logical groupings called domains. SPs control who sees and accesses what content. You can create and modify guided tours that apply to specific domains in your instance as well as tours that are available to users globally.

## Create domain-separated guided tours

Once you create a guided tour, you can specify a domain to which it applies. You can also copy the tour so that you can modify it for a specific domain.

### Before you begin

Role required: guided\_tour\_admin or admin. To use domain separation in guided tours, you must [request domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/platform-security/servicenow-ai-platform-security/t_ActivateDomainSeparation.md).

**Note:** The Guided Tour Designer requires Core UI. For more information, see [Activate Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-user-interface/configure-user-experiences/t_ActivateUI16.md).

### Procedure

1.  Navigate to **All** &gt; **Embedded Help** &gt; **Guided Tour Designer** &gt; **Guided Tours**.

2.  Click the gear icon to personalize list columns and add the Domain and Overrides columns.

    The **Domain** column indicates the domain to which a tour belongs, either Global, or the domain specified for the tour.

3.  Click the gear icon next to the user name to open System Settings.\[Omitted image "system-settings-cog.png"\] Alt text: System settings gear icon

4.  Enable the **Show domain picker in header** option.\[Omitted image "show-domain-picker.png"\] Alt text: Enable Domain Picker option in System Settings

    This option is enabled when the switch appears green and is toggled to the right.

5.  Use the domain picker to select the domain to add the modified tour to.\[Omitted image "domain-picker.png"\] Alt text: Domain picker choice list

6.  Select the guided tour.

    You can edit the tour here or simply

7.  Click **Update** to create the domain-specific version of the tour.


### Result

In the specified domain, the saved version of the tour overrides the original for users in that domain. You can edit this tour to be specific for that domain. For more information, see [Edit a guided tour](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/platform-user-interface/adoption-services/edit-guided-tour.md).

