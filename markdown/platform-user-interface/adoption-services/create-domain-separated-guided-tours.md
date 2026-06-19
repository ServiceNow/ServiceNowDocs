---
title: Domain separation and Guided Tours
description: You can assign a domain to a guided tour during its creation or edit the domain of the tour at any time.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/platform-user-interface/adoption-services/create-domain-separated-guided-tours.html
release: zurich
product: Adoption Services
classification: adoption-services
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure Guided Tours, Guided Tours, Adoption services, Configure user experiences]
---

# Domain separation and Guided Tours

You can assign a domain to a guided tour during its creation or edit the domain of the tour at any time.

## Before you begin

Role required: guided\_tour\_admin or admin.

To use domain separation in Guided Tours, you must request domain separation.

**Note:** The Guided Tour Designer requires Core UI. For more information, see [Activate Core UI](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/configure-user-experiences/t_ActivateUI16.md).

## About this task

With the ServiceNow AI Platform®, service providers \(SPs\) can provide their customers with faster onboarding, meet compliance, and protect their data using domain separation. You can separate client data, processes, and reports into logical groupings called domains. SPs control who sees and accesses what content. You can create and modify guided tours that apply to specific domains in your instance as well as tours that are available to users globally. You can also copy the tour so that you can modify it for a specific domain.

## Procedure

1.  Add the **Domain** column to the list:
2.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Guided Tours**.

3.  Select the gear icon \[Omitted image "gtd-gear-icon.png"\] Alt text: Gear icon and add the **Domain** columns.

    The **Domain** column indicates the domain to which a tour belongs.

4.  Set a **Domain** for the guided tour:
5.  Select the globe icon and then select **Domain scope**.

    \[Omitted image "gtd-domain-picker.png"\] Alt text: Domain picker

6.  From the Domain scope list, select a domain.

7.  Create a guided tour.

    For more information, see [Create Guided Tours](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/adoption-services/add-guided-tour.md).

8.  Change the **Domain** of a guided tour:
9.  Navigate to **All** &gt; **Guided Tour Designer** &gt; **Guide Tours**.

10. Select the tour for which you want to change the domain.

11. Select the **Form context menu \(\[Omitted image "hamburger-icon.png"\] Alt text: Form context menu\)** &gt; **Configure** &gt; **Form Design**.

    \[Omitted image "guided-tour-form-design.png"\] Alt text: Select form design.

12. On the **Form Design** page, drag the **Domain** element and drop it at an appropriate spot on the form.

13. Select **Save**.

14. Return to the Form view and confirm that the **Domain** field has been included in the form.

    \[Omitted image "guided-tour-domain-element.png"\] Alt text: The Domain field is added to the form.

15. Select any domain that you prefer and save the record.


## Result

Within the specified domain, the saved version of the tour replaces the original for users in that domain.

**Parent Topic:**[Configuring Guided Tours](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/platform-user-interface/adoption-services/configure-guided-tours.md)

