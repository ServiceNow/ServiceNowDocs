---
title: Disclosures in ESG Management
description: ESG disclosures are the information and reports that companies and organizations provide on their environmental, social, and governance \(ESG\) performance. These disclosures offer insights into how a company manages and addresses various ESG-related issues.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 5
breadcrumb: [Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Disclosures in ESG Management

ESG disclosures are the information and reports that companies and organizations provide on their environmental, social, and governance \(ESG\) performance. These disclosures offer insights into how a company manages and addresses various ESG-related issues.

## Disclosure requirements

Disclosure requirements are the specific expectations or obligations an organization must meet when preparing ESG \(Environmental, Social, and Governance\) reports. These requirements contribute to organizations transparently communicating their sustainability performance, risks, and impacts. These prerequisites are often defined by external regulatory bodies or frameworks. The two types of disclosure requirements are authority documents and citations.

-   **Authority document**

    An authority document is a regulatory framework or standard that outlines what an organization should report in its ESG disclosures. It acts as a reference point for compliance and reporting. Examples include GRI \(Global Reporting Initiative\), SASB \(Sustainability Accounting Standards Board\), and CSRD \(Corporate Sustainability Reporting Directive\).

-   **Citations**

    Citations are the individual reporting requirements or metrics defined within an authority document that organizations respond to in their ESG reports, often with quantitative or qualitative data. Each authority document can have multiple citations, forming a one-to-many relationship. An example of a citation from the GRI is “Energy consumption from renewable sources” or from the SASB is “Total energy consumed \(TCSI 220\).”


## Importance of ESG disclosures

-   Transparency and accountability: ESG disclosures enhance transparency, enabling stakeholders such as investors, customers, employees, and the public to understand a company's performance in key ESG areas.
-   Risk management: Companies that disclose ESG information can better identify and manage potential risks associated with environmental, social, and governance factors.
-   Investor decision-making: ESG disclosures provide investors with information to assess a company's sustainability, ethical practices, and long-term viability.
-   Corporate reputation: Positive ESG performance can enhance a company's reputation and brand value. Conversely, poor ESG practices can lead to reputational damage, affecting customer and investor confidence.
-   Regulatory compliance: Some regions have regulatory requirements for companies to disclose ESG information. Compliance with these regulations is essential to avoid legal and financial consequences.
-   Stakeholder engagement: ESG disclosures demonstrate to stakeholders a company's commitment to responsible business practices. Engaging with stakeholders on ESG issues can lead to improved relationships and collaboration.

## Narrative disclosures

Narrative disclosures are created using the Microsoft 365 for ServiceNow Reporting add-in. When you create a narrative disclosure, you have the option to store the disclosure either on Microsoft SharePoint or on your local system. Microsoft SharePoint integration in narrative disclosures is available starting with ESG Management version 18.0.3 and the Zurich release.

**Note:** If you're running a version of ESG Management prior to version 18.0.3, continue to use the existing disclosure capability to create disclosures and export data used in the disclosures in Microsoft Excel format.

The document that is generated when you create a narrative disclosure can be opened using Microsoft Word and the data points that are configured can be inserted in the document using the ServiceNow Reporting add-in.

If any change is made in the data that is inserted, an email is automatically sent to the owners of the disclosure data notifying them that the data has changed and that they must refresh the Microsoft Word document.

Additional information about narrative disclosures:

-   Automatically generated documents are considered the primary document. You can also attach secondary documents as part of the disclosure process.
-   Multiple collaborators can contribute to create the disclosure.
-   You can define templates for each type of disclosure report. For information about report types, see [Types of disclosure reports](types-of-disclosure-reports.md).
-   Each disclosure can be approved by one or more approvers.
-   To create narrative disclosures on remote storage, you must install and activate the sn\_docs\_onedrive plugin.

For information about how to integrate your ServiceNow® instance and Microsoft OneDrive, refer to the following articles:

-   [Setup Microsoft OneDrive for Document Services](https://www.servicenow.com/docs/access?context=configure-ms-onedrive-doc-services&version=zurich&pubname=zurich-servicenow-platform&ft:locale=en-US)
-   [Connecting to Microsoft Sharepoint \[KB1646310\]](https://hi.service-now.com/kb_view.do?sysparm_article=KB1646310%20) article in the Now Support Knowledge Base.

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
-   **[Create an authority document using Operational Sustainability Workspace](../task/create-a-authority-document-using-esg-workspace.md)**  
Create an authority document that outlines the reporting obligations for ESG disclosures.
-   **[Define a citation using Operational Sustainability Workspace](../task/create-a-citation-using-esg-workspace.md)**  
Define a citation within an authority document to specify the exact data points or qualitative information an organization must disclose.

**Parent Topic:**[Using Operational Sustainability Management \(formerly Environmental, Social, and Governance\)](using-esg.md)

**Related topics**  


[Types of disclosure reports](types-of-disclosure-reports.md)

[Create a narrative disclosure on remote storage](../task/create-disclosure.md)

[Create a narrative disclosure on local system](../task/create-a-disclosure-on-local.md)

