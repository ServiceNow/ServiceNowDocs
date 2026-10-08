---
title: Exploring the HRBP productivity assistant
description: The HRBP productivity assistant helps HR business partners manage and resolve employee cases through conversation. Learn who uses the assistant, what it does, and how an HR case moves from submission to resolution.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/employee-service-management/hr-service-delivery/hrbp-pa-explore.html
release: brazil
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 7
keywords: [explore]
breadcrumb: [HRBP productivity assistant, HR Service Delivery, Employee Service Management]
---

# Exploring the HRBP productivity assistant

The HRBP productivity assistant helps HR business partners manage and resolve employee cases through conversation. Learn who uses the assistant, what it does, and how an HR case moves from submission to resolution.

## HRBP productivity assistant overview

HR business partners receive HR cases from managers, employees, recruiters, and other parts of the organization. Many of those cases are routine and repetitive, which leaves less time for the strategic work the role exists to do.

The HRBP productivity assistant, which runs in the EmployeeWorks Web App, moves that case work into a conversation. After an HR case is assigned to an HR business partner, AI enrichment adds an urgency, a summary, a resolution recommendation, and a confidence score to the case. A weekly digest email lists the open cases that need attention and links to the assistant. From there, the HR business partner can request their cases, review the recommendation, and act on the case through a conversation with the assistant.

Content that the assistant and AI enrichment generate can be inaccurate. HR business partners should review each summary, urgency, and recommendation before acting on a case.

The assistant reads and writes HR case records on your instance. Data access records and their rules determine which employees each HR business partner covers and which HR cases are assigned to them.

## HRBP productivity assistant users

<table id="table_hlr_kbm_hkc"><thead><tr><th>

User

</th><th>

Description

</th></tr></thead><tbody><tr><td>

HR business partner

</td><td>

Manages the HR cases assigned to them. Receives the weekly digest and opens the assistant from it. They use the conversational interface to review AI-generated summaries and recommendations, approve or decline requests, defer and resume cases, and schedule meetings.Requires the sn\_hrbp\_hub.user role.

</td></tr><tr><td>

HRBP administrator

</td><td>

Configures the application before HR business partners use it. Sets the link to the assistant in notification emails, defines the data access rules that assign cases to HR business partners, and manages the weekly digest scheduled job and notification.Requires the sn\_hrbp\_hub.admin role.

</td></tr></tbody>
</table>## HRBP productivity assistant workflow

An HR case moves through the following sequence, from creation to resolution.

1.  An employee or a manager opens an HR case.
2.  If auto-assignment is enabled for the HR service, data access rules assign the case to each HR business partner who covers the subject person. Administrators can also assign an HR business partner to a case manually.
3.  If the HR Case Enrichment skill is active, the enrichment process runs after an HR business partner is assigned to the case. The enrichment process generates an urgency, a summary, a resolution recommendation, a confidence score, and a sensitivity level for the case.
4.  The enrichment process also sets a resolution track that reflects how much judgment it needs from an HR business partner.
5.  If the enrichment process sets the urgency to critical, an email notifies each assigned HR business partner without waiting for the weekly digest.
6.  Each Monday, a digest email lists the HR business partner's open cases, the number that are high priority, and the most urgent items. The digest links to the assistant.
7.  The HR business partner opens the assistant, asks for their open cases, reviews case summaries and recommendations, and interacts with the assistant to take action.

## HRBP productivity assistant benefits

|Benefit|Feature|Users|
|-------|-------|-----|
|Understand a case without reviewing its full history.|[AI case summarization and resolution recommendations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/review-hr-cases-pa.md)|HR business partner|
|Focus on the most time-sensitive work first, based on AI-assessed urgency.|[AI case enrichment and resolution tracks](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/hrbp-case-assignment-enrichment.md)|HR business partner|
|Act on a case directly from the conversation instead of opening the case record.|[Case actions in the conversation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/review-hr-cases-pa.md)|HR business partner|
|Start the week with a summary of the cases that need attention and a direct link to the assistant.|[Weekly digest](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/configure-hrbp-weekly-digest.md)|HR business partner|
|Arrange the follow-up a case requires without leaving the conversation.|[Meeting scheduling](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/schedule-meeting-using-pa.md)|HR business partner|
|See a case in its entirety, with its request details and AI insights side by side.|[Case page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/work-hr-case-using-case-page.md)|HR business partner|
|Answer questions about the employees you support without opening their records.|[Employee questions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/ask-about-employee-using-pa.md)|HR business partner|
|See which policies an employee can access before providing guidance.|[Knowledge search as an employee](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/ask-about-employee-using-pa.md)|HR business partner|
|Route cases to the appropriate HR business partner as your organization changes, without manually reassigning cases.|[HRBP data access rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown)|HRBP administrator|

## What to explore next

To learn more about configuring and using HRBP productivity assistant, see:

-   [Configuring the HRBP productivity assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/hrbp-pa-configure.md)
-   [Review and act on cases with the HRBP productivity assistant](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/review-hr-cases-pa.md)
-   [Work an HR case on the case page](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/work-hr-case-using-case-page.md)
-   [Schedule a meeting for an HR case](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/schedule-meeting-using-pa.md)
-   [Ask about the employees you support](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/ask-about-employee-using-pa.md)
-   [HRBP productivity assistant reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/hrbp-pa-reference.md)

-   **[HR case assignment and enrichment for HR business partners](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/hrbp-case-assignment-enrichment.md)**  
One or more HR business partners are assigned to an HR case through data access rule or manual assignment. The enrichment process then adds an urgency, a summary, and a recommended resolution to the case. This sequence determines which HR business partner is assigned to a case and why the summary is generated after the assignment rather than with it.

**Parent Topic:**[HR Service Delivery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/employee-service-management/hr-service-delivery/hr-service-delivery.md)

