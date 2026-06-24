---
title: Configure Legal Investigations
description: Configure the foundation data required for managing the complaints for legal investigations.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/legal-investigations/setting-up-legal-investigations.html
release: australia
product: Legal Investigations
classification: legal-investigations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Legal Investigations, Legal Service Delivery Practice Applications, Legal Service Delivery, Legal and Contract Operations, Employee Service Management]
---

# Configure Legal Investigations

Configure the foundation data required for managing the complaints for legal investigations.

The following components are installed with Legal Investigations:

-   Practice area: Ethics
-   Category: Ethics Complaints
-   Assignment group: Legal — Ethics
-   Record producer: Ethics Complaints

    For more information, see [Record producers for legal investigations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-investigations/record-producers-legal-investigation.md).

-   Matter template: Ethics Template

As an administrator, you can review the installed base system components and modify them or add new ones as applicable.

-   [Configure allegation types and allegation subtypes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-investigations/configure-allegation-type-legal.md) that will be used by the legal fulfillers when adding new allegations during investigations as needed.
-   [Add or modify subcategories](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-request-management/add-subcategories-intakeform.md) for the base system Ethics Complaints intake form of the Ethics practice area. These subcategories appear in the **Complaint type** field of the [Ethics complaints intake form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-investigations/ethics-complaint-intake-form.md).
-   Enable anonymous complaint submission by completing the following tasks:
    -   Install the Anonymous Report Center plugin \(com.sn\_anonymous\_report\_center\) to enable the Anonymous Reporting Center portal for submitting complaints to Legal.
    -   Install the HR Scoped Security plugin \(com.snc.hr.scoped\_security\) to enable the text verification code on the Ethics Complaints intake form on the Anonymous Report Center portal.

        **Note:** If HR Service Delivery is not installed, you have to modify the permission settings. For more information, see the [Anonymous Report Center \(ARC\) dependency for Legal Services Delivery \[KB1171443\]](https://support.servicenow.com/kb?id=kb_article_view&sysparm_article=KB1171443) article in the Now Support Knowledge Base.

    -   Enable the base system Ethics Complaints [record producers for legal investigations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-investigations/record-producers-legal-investigation.md) for ARC.
-   [Create a legal matter template](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/legal-matter-management/create-legal-matter-template.md) to standardize the process of investigating a complaint.
-   Configure an interview template for legal matter tasks of type interview to capture consistent information from the interviews. For example, if you set a questionnaire in the template, the assigned task fulfiller can view a list of predefined questions to ask the interviewees.

    For more information, see [Interview Management for Employee Relations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/employee-service-management/hr-service-delivery/hr-er-interview-1.md).


