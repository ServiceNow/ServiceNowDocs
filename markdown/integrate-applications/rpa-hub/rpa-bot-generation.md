---
title: Robotic Process Automation \(RPA\) bot generation
description: Use the RPA bot generation skill to create automations, activities, and automation logic additions from text instructions and preview options. RPA developer \(sn\_rpa\_fdn.rpa\_developer\) or RPA admin \(sn\_rpa\_fdn.rpa\_admin\) roles are required to use this skill.
locale: en-US
release: xanadu
product: RPA Hub
classification: rpa-hub
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 6
keywords: [Now Assist, generative AI]
breadcrumb: [Exploring Now Assist for RPA Hub, Now Assist for RPA Hub, Robotic Process Automation \(RPA\) Hub, Creating integrations with applications]
---

# Robotic Process Automation \(RPA\) bot generation

Use the RPA bot generation skill to create automations, activities, and automation logic additions from text instructions and preview options. RPA developer \(sn\_rpa\_fdn.rpa\_developer\) or RPA admin \(sn\_rpa\_fdn.rpa\_admin\) roles are required to use this skill.

These roles contain the Now Assist Admin user role \(sn\_nowassist\_admin.user\).

## Activation

Install the Now Assist for RPA Hub application from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website. For more information, see [Configure Now Assist for RPA Hub](../task/configure-now-assist-rpa-hub.md).

Then, turn on the RPA bot generation skill to use generative AI for creating automations and activities, and extending automation logic. For more information, see [Turn on the RPA bot generation skill](../task/turn-rpa-bot-generation-skill.md).

You must have a subscription for Now Assist for Creator and RPA Hub applications. For more information, see [Supporting information for Now Assist for RPA Hub](now-assist-rpa-hub-supporting-info.md).

## Example instructions

The following examples show how you can create automations, activities, and automation logic additions.

-   **Example instruction 1: Retrieve and process meeting emails**

    You can use this instruction to create an automation for retrieving and processing meeting emails in Microsoft Outlook.

    `Retrieve a list of meeting-related emails from the 'Calendar' folder in Outlook. For each email, store all attachments in a separate folder named 'Meeting Attachments'. Lastly, mark the email as read.`

-   **Example instruction 2: Split and convert PDF pages to excel**

    You can use this instruction to create an automation for splitting and converting PDF pages to Microsoft Excel.

    `Split each page of a PDF into a separate PDF files into the folder path 'C:\Users\Input', then retrieve all files from this folder, now iterate over each file then convert each PDF document into an Excel.`

-   **Example instruction 3: Add property to JSON object**

    You can use this instruction to create an automation for adding a property to a JSON object.

    `I have a sample JSON object represented as a string as follows: { "name": "Jane Doe", "id": 12345" } I want to add a new property called "Designation" and set its value to "Engineer".`

-   **Example instruction 4: Find and replace text in a Word document**

    You can use this instruction to create an automation for finding and replacing text in a Microsoft Word document.

    `Open a word document, find and replace the value #NAME with 'ServiceNow' in the word document. Save the word document at 'C:\Users\Desktop\test.docx'.`

-   **Example instruction 5: Modify and export data as CSV**

    You can use this instruction to create an automation for modifying and exporting data as a CSV file.

    `Load a DataTable from the list, set the name of the first column to 'Name', and update the row data. Finally, export the table as a CSV file.`

-   **Example instruction 6: Generate and send excel data as PDF**

    You can use this instruction to create an automation for generating and sending the Microsoft Excel data as a PDF in an email via Microsoft Outlook.

    `Open Excel from 'C:\Reports\Sales\Monthly_Sales_Data.xlsx'. Generate a chart based on sales data in sheet named Saleschart and then save this excel sheet as a PDF document at 'C:\Reports\Sales\Reports\Monthly_Sales_Data.pdf'. Now send an email to team@xyz.com using Outlook.`

-   **Example instruction 7: Extract and summarize work emails with attachments**

    You can use this instruction to create an automation for extracting and summarizing work emails with attachments.

    `Extract a list of work related emails from outlook with attachments from the 'Projects' folder. Save all the attachments to a designated folder on your system. Generate a summary email listing all the saved attachments and their respective emails. Send this email to the project manager.`

-   **Example instruction 8: Split and read PDF pages**

    You can use this instruction to create an automation for splitting and reading PDF pages.

    `Load a PDF file from the 'C:\input\test.pdf', split the PDF file, save them to 'C:\output folder', generate one PDF for each page, and then read the text from the first page.`

-   **Example instruction 9: Fetch and save unread emails**

    You can use this instruction to create an automation for fetching and saving unread emails.

    `Fetch all the unread mails from the 'AI-inbox' folder of the email account. Iterate through each email and save the mail to the folder 'C:\Mails'.`

-   **Example instruction 10: Retrieve and set application credentials**

    You can use this instruction to create an automation for retrieving and setting application credentials.

    `From the ServiceNow instance, get the application credentials for the app named 'SAP' application. Now, set the value into the Username field and password field. Then, click on the login element.`


## General guidelines

Follow these general guidelines when writing Now Assist instructions:

-   **Be clear and specific**

    State exactly what you want. Use direct and clear sentences for the expected actions.

-   **Avoid vague language**

    Don't use jargon or abbreviations. Avoid ServiceNow jargon, such as FD - Flow Designer. For example, avoid instructions such as `Trigger a FD action named 'Action1', retrieve its output, and insert it into an existing Word`. Instead, use the phrase `Trigger a flow designer action named 'Action1', retrieve its output, and insert it into an existing Word file located at 'C:\Users\Worddocs\wordoc1.doc'`.

-   **Avoid ambiguity**

    Be specific for the context related to methods. For example, avoid instructions such as `Open file from file path 'C:\Users\Analysis\DataAnalysis.xlsx'`. Instead, use the phrase `Open an excel file from file path 'C:\Users\Analysis\DataAnalysis.xlsx'`.

-   **Set expectations and constraints**

    Specify component parameters wherever possible. For example, avoid instructions such as `Read the content of the file located in C drive and copy that content as the body of an email and then send it to 'email@ss.ss'`. Instead, use the phrase `Read the content of the file 'c:/d/f1/txt', and use the content as body to compose an outlook email with subject "my email text", and send this email to 'email@ss.ss'`.

-   **Use step-by-step instructions**

    Break down complex tasks into smaller, manageable steps. For example, use the phrase, `Open a Microsoft Word document located at 'C:\Marketing\Templates\Promo_Letter_Template.docx.', delete a specific page based on its index, add a new column to a table at a particular position, and close the document with changes saved` to make it clear and simple.


## Limitations of the RPA bot generation skill

For more information about the limitations of the Robotic Process Automation \(RPA\) bot generation skill, see [Limitations of Robotic Process Automation \(RPA\) bot generation skill](../reference/limitations-rpa-bot-gen-skill.md).

## Accessing the generative AI capability in RPA Desktop Design Studio

If you log in to the RPA Desktop Design Studio with either RPA Developer or RPA Admin after enabling the RPA bot generation skill, the generative AI capability is available. In this scenario, you can create and edit automations, activities, and extend automation logic flow through text instructions and preview options.

If you log in to the RPA Desktop Design Studio with a role other than RPA Developer or RPA Admin after enabling the RPA bot generation skill, the generative AI capability will not be available. In this scenario, you will not be able to create and edit automations, activities, or extend automation logic flow through text instructions and preview options.

If you log in to the RPA Desktop Design Studio with a role other than RPA Developer or RPA Admin and then switch to one of these roles, you won't be able to access the generative AI capability. Restart the RPA Desktop Design Studio and log in with RPA Admin or Developer.

If you log in to the RPA Desktop Design Studio with either RPA Developer or RPA Admin, and then switch to any other user roles apart from these, you will encounter an error message when attempting to access the generative AI capability.

**Related topics**  


[bundle-crint.bundle-platai.now-assist-rpa-bot-generation]

