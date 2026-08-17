---
title: Example instructions for ServiceNow Otto for RPA Hub
description: Example instructions you can use with Now Assist for RPA Hub to get relevant, accurate responses. Refer to these examples when crafting instructions to guide automation tasks.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/rpa-hub/example-instructions-rpa.html
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2026-07-02"
reading_time_minutes: 4
breadcrumb: [Reference, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Example instructions for ServiceNow Otto for RPA Hub

Example instructions you can use with Now Assist for RPA Hub to get relevant, accurate responses. Refer to these examples when crafting instructions to guide automation tasks.

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

Follow these general guidelines when writing AI instructions:

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


**Parent Topic:**[Robotic Process Automation \(RPA\) Hub reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/rpa-hub/rpa-reference.md)

