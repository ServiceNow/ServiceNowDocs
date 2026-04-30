---
title: Disclosures in Operational Sustainability Management \(formerly ESG Management\)
description: An Operational Sustainability Management disclosure refers to the practice of companies and organizations providing information and reports on their operational sustainability performance. These disclosures are designed to offer insights into how a company manages and addresses various sustainability-related issues. Users with the sn\_esg.reporting\_disclosure\_manager role are responsible to manage the disclosure reports.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Disclosures in Operational Sustainability Management \(formerly ESG Management\)

An Operational Sustainability Management disclosure refers to the practice of companies and organizations providing information and reports on their operational sustainability performance. These disclosures are designed to offer insights into how a company manages and addresses various sustainability-related issues. Users with the sn\_esg.reporting\_disclosure\_manager role are responsible to manage the disclosure reports.

## Disclosure requirements

Disclosure requirements refer to the specific expectations or obligations an organization must meet when preparing operational sustainability reports. These requirements ensure that the organization transparently communicates its sustainability performance, risks, and impacts. They are prerequisites for creating disclosures and are often defined by external regulatory bodies or frameworks. In your context, these are surfaced in the Operational Sustainability Workspace as a separate entity to guide what needs to be reported. There are two types of disclosure requirements:

-   **Authority document**

    An Authority Document is a regulatory framework or standard that outlines what an organization should report in its operational sustainability disclosures. It acts as a reference point for compliance and reporting. Examples include: GRI \(Global Reporting Initiative\), SASB \(Sustainability Accounting Standards Board\), and CSRD \(Corporate Sustainability Reporting Directive\).

-   **Citations**

    Citations are the individual reporting requirements or metrics defined within an authority document. They represent the specific items an organization must disclose. Each authority document can have multiple citations, forming a one-to-many relationship. These citations are what the organization responds to in its operational sustainability report, often with quantitative or qualitative data. For example, from GRI: “Energy consumption from renewable sources” and from SASB: “Total energy consumed \(TCSI 220\)”.


## Importance of Operational Sustainability Management disclosures

Operational Sustainability Management disclosures are important for several reasons.

-   Transparency and accountability: Operational sustainability disclosures enhance transparency, allowing stakeholders such as investors, customers, employees, and the public to understand a company's performance in key sustainability areas. This transparency fosters accountability and trust.
-   Risk management: Companies that disclose operational sustainability information can better identify and manage potential risks associated with operational sustainability factors. This is crucial for long-term sustainability and resilience.
-   Investor decision-making: Investors are increasingly considering operational sustainability factors in their decision-making processes. Operational Sustainability Management disclosures provide investors with information to assess a company's sustainability, ethical practices, and long-term viability.
-   Corporate reputation: Positive operational sustainability performance can enhance a company's reputation and brand value. Conversely, poor operational sustainability practices can lead to reputational damage, affecting customer and investor confidence.
-   Regulatory compliance: In some regions, there are regulatory requirements for companies to disclose operational sustainability information. Compliance with these regulations is essential to avoid legal and financial consequences.
-   Stakeholder engagement: Operational sustainability disclosures facilitate communication with various stakeholders by demonstrating a company's commitment to responsible business practices. Engaging with stakeholders on sustainability issues can lead to improved relationships and collaboration.

## Narrative disclosures

Starting with version 18.0.3, all new users of ESG Management have access to only narrative disclosures. Narrative disclosures refer to disclosures that are created using the Microsoft 365 for ServiceNow Reporting add in. When you create a narrative disclosure, you have the option to store the disclosure either on Microsoft SharePoint or on your local system. Microsoft SharePoint integration in narrative disclosures is available for ESG Management version 18.0.3 and the Yokohama release. The document that is generated when you create a narrative disclosure can be opened using Microsoft Word and the data points that are configured can be inserted in the document using the ServiceNow Reporting add-in. If there is any change in the data that is inserted, an email is automatically sent to the owners of the disclosure data notifying them that the data has changed and that they must refresh the Microsoft Word document.

In a narrative disclosure, multiple collaborators can contribute to create the disclosure. You can also define templates for each type of disclosure report. Refer to [Types of disclosure reports](types-of-disclosure-reports.md) to understand each report type. Each disclosure can be approved by one or more approvers.

When generating a disclosure, it is important to note that the automatically generated document is considered the primary document. Additionally, you have the option to attach secondary documents as part of the disclosure process.

To create narrative disclosures on remote storage, you must install and activate the sn\_docs\_onedrive plugin.

For steps to integrate the ServiceNow® instance and Microsoft OneDrive, refer to the following articles.

-   [Setup Microsoft OneDrive for Document Services](https://www.servicenow.com/docs/access?context=configure-ms-onedrive-doc-services&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)
-   [Connecting to Microsoft Sharepoint \[KB1646310\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1646310%20) article in the Now Support Knowledge Base.

You can download the disclosures in an Excel format from the overview tab in the Operational Sustainability Workspace.

## Additional information about disclosures

The following list provides detailed information about disclosures.

-   **[Types of disclosure reports](types-of-disclosure-reports.md)**  
The ESG Management application provides the multiple types of disclosures reports and each type is used for a specific purpose.
-   **[Approval workflow of a disclosure](approval-workflow-of-a-disclosure.md)**  
If a narrative disclosure specifies a single approver or multiple approvers during its creation, it is mandatory for those designated approvers to grant approval before the disclosure can transition to the next state.
-   **[Create a disclosure template](../task/create-a-disclosure-template.md)**  
Create your own unique Microsoft Word disclosure templates tailored to different types of disclosures. Utilize these templates that you create when you generate specific disclosures. The templates help to streamline the disclosure process by implementing customized templates for efficiency and consistency.
-   **[Create a narrative disclosure on remote storage](../task/create-disclosure.md)**  
Create an ESG Management narrative disclosure for your organization and store it on remote storage such as Microsoft SharePoint. Disclosures can be of several types such as ESG report, annual report, and so on.
-   **[Create a narrative disclosure on local system](../task/create-a-disclosure-on-local.md)**  
Create an ESG Management narrative disclosure for your organization and store it on your local system. After you create a disclosure, you can download the document, edit it, add metrics to it, and upload it back into the ESG Management instance.
-   **[Add disclosure documents](../task/add-disclosure-related-docs.md)**  
Add secondary related or supporting documents to any disclosure you create. Supporting documents may include sustainability reports, corporate governance documents, third-party certifications, and relevant policies such as those on ethics and supply chain practices. These documents provide additional context and validation for environmental, social, and governance disclosures.
-   **[Add metrics to a disclosure](../task/add-related-metric-to-a-disclosure.md)**  
Add any metrics to the disclosure that would help to contribute to the disclosure data.
-   **[Create a authority document using Operational Sustainability Workspace](../task/create-a-authority-document-using-esg-workspace.md)**  
The authority document is a regulatory framework or standard issued by a recognized organization or governing body that outlines the reporting obligations for operational sustainability disclosures.
-   **[Create a citation using Operational Sustainability Workspace](../task/create-a-citation-using-esg-workspace.md)**  
The citations are the individual reporting requirements or metrics defined within an authority document. They specify the exact data points or qualitative information an organization must disclose.

**Parent Topic:**[Using Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](using-esg.md)

