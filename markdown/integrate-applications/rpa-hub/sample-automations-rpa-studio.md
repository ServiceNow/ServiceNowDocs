---
title: Sample automations
description: The RPA Desktop Design Studio provides multiple sample automations that cater to different use cases.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Use a sample automation, Use, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Sample automations

The RPA Desktop Design Studio provides multiple sample automations that cater to different use cases.

## Sample automations descriptions

A sample automation is a prebuilt automation that shows how different components are configured for a specific use case.

Use the following unattended and attended sample automations that were added to the Sample Automations page of RPA Desktop Design Studio. You can also view them in the Sample Explorer section.

|Sample automation|Description|
|-----------------|-----------|
|Add Word Footer|This automation downloads Word files from a specified URL. The robot further adds a footer to each page, using dynamically retrieved information from an Excel file.|
|Automate Offer Letters|This automation streamlines the process of generating offer letters for selected candidates. It extracts data from an Excel file, populates a predefined offer letter template, and distributes the letters via email, ensuring accurate and efficient candidate communication.|
|City Weather Reports|This automation retrieves weather information \(temperature, wind, cloudiness, humidity\) for various cities and countries listed in an Excel file. The automation loops through each city-country pair, fetches the corresponding weather details from Weather.com, and updates the relevant data fields in the Excel file. This data is collated into a comprehensive weather report, with all the information organized and populated in the same Excel sheet for easy reference.|
|Clear Browser Cache|This automation clears the all-time cookies, other site data, cached images, and files from the browsers like Microsoft Edge and Google Chrome.|
|Consolidated Invoices|This automation extracts information from each Excel file within the Invoice Data folder and consolidates all the data into a single Excel file.|
|Convert Excel to Json|This automation reads data from an Excel file \(including password-protected ones\) and converts the Excel file into a JSON file.|
|DataTable extraction from PDF to Excel|This automation efficiently identifies and extracts the first table from a PDF document. Once the table is extracted, the script seamlessly converts the data into a structured format and writes it to an Excel file.|
|Date Delta Across Apps|This automation calculates the delta between two dates and updates the relevant systems or documents accordingly.|
|Decision Component|This automation takes the provided input as a number, checks whether the number is greater than 100 using the Decision component, and displays the corresponding text in a message box in the provided format.|
|Decode Barcode and QR Code to Text|This automation extracts data from barcode or QR code images in a specified project folder, stores the information in an organized Excel file, and ensures accurate and efficient capture for easy access and analysis.|
|Download attachments from outlook|This automation monitors email accounts for messages with specific subjects, ensuring that only relevant emails are processed. On identifying an email that matches the criteria, it downloads the attachments and saves them to a designated local project folder.|
|Download File from URL|This automation simplifies the file download process from a web application. It provides a consistent and reliable method for downloading files from any URL, saving them to a specified local folder, and sending an email with the downloaded file as an attachment, ensuring you have a seamless and efficient experience.|
|Email Archiving or Deletion|This automation archives or deletes emails based on provided parameters: MailID, Sender, Subject, and FolderName on Outlook. The solution streamlines the process, reduces errors, and saves time.|
|Excel Conversion|This automation reads data from an Excel file and converts it into an XML file. It facilitates the transfer of data from the Excel table into a SQL database table.|
|Excel Operations|This automation demonstrates various tasks in Microsoft Excel, including searching for text, creating pivot tables, and exporting charts. It showcases a sequential flow to help users understand seamless integration within an automation workflow.|
|Expression Component|This automation performs addition using the Expression component and displays the result in a message box.|
|Extract Data from a Table and Saving to Excel|This automation is customized for a specific website because the elements that must be captured on different websites vary. When creating comparable automations for different websites, this automation can be used as a guide.|
|Extract Data from JSON to Excel|This automation streamlines data handling by efficiently extracting and logging JSON data into structured formats, reducing manual intervention. The bot creates work items in a designated queue, retrieves those items, and extracts JSON values based on specific property names. The extracted values are then organized and updated into an Excel sheet, ensuring accurate and easy access to the data.|
|Extract Excel Table to Embed in Email Body|This automation extracts the data from the specified sheet in the Excel file and sends an Microsoft Outlook email to the recipient with the Excel data included in the body of the email.|
|ExtractDataFromPDF|This automation extracts table data from a PDF and generates an Excel file with the extracted information.|
|Fetch contact info from email|This automation identifies relevant emails based on specific subjects and updates the extracted information \(FirstName, LastName, and EmailAddress\) into an Excel spreadsheet. This automation enhances data management efficiency and reduces manual data entry errors.|
|File Operations|This automation checks whether the provided file exists or not. If file exists, automation provides a new incremental filename which doesn't exist already. Ex: If a file "C:\\Users\\Public\\XYZ.txt" already exists, automation returns the filename as C:\\Users\\Public\\XYZ\_1.txt and so on.|
|File Ops Copy, Delete, Move|This automation copies, moves, and deletes files according to user-defined rules. It enhances file management by minimizing manual effort and errors and can be customized to handle specific conditions such as file type, timestamps, or folder locations, ensuring improved organization and efficiency.|
|For Each Component|This automation sets a list of values, retrieves each item's value using the For Each component, displays the item value in a message box, and checks whether the item value is equal to the provided value. If it’s equal, the automation breaks out of the For Each loop.|
|For Loop|This automation obtains each index value using the For Loop component with provided inputs for "From" and "To," and then displays the index values in a message box.|
|Format Text|This automation accepts the provided input and displays the text in a message box using the specified format.|
|Health Check Bot|This automation verifies system prerequisites on Remote Desktop Protocol \(RDP\) machines before executing specific tasks. It ensures all necessary system conditions are met, reducing the risk of process failures due to configuration issues.|
|Highlight Excel Rows|This automation highlights rows in an Excel sheet based on information extracted from a Word document. It’s useful for tasks such as data validation, report generation, and automating document processing involving both Excel and Word.|
|HTML to CSV|This automation converts multiple HTML table data files into a single CSV file, storing the converted files in the specified output folder path.|
|Invoice Data Extraction to Excel|This automation extracts the necessary data from invoices, populates the extracted information into an Excel sheet, and sends the Excel file as an email attachment to designated recipients. By streamlining the process, it reduces errors and enhances efficiency, ensuring accurate and timely data management.|
|Merge CSV files|This automation merges two or more same CSV files into 1 main CSV with all the required details.|
|Merge Excel Sheets|This automation merges two or more Excel files into one main Excel file, with all the required details. To use the automation, you need to provide the folder path containing the Excel files as input and then execute the automation. It automatically merges all the .xlsx files into the main Excel file.|
|OneDrive Operations|This automation includes various activities that perform actions like 'Upload,' 'Download,' and 'Share'. The Upload activity uploads a local file specified in the process parameter to the ServiceNow® table or uploads a file to OneDrive using the OneDrive action. The Download activity downloads file from OneDrive to the local folder. The Share activity generates a link of a OneDrive file and shares it via email.|
|Oracle EBS Password Reset|This automation resets passwords for third-party applications or systems. The RPA Oracle Password Reset subflow queues the password reset request, which is automatically created from the Password Reset Request to the queue. The Update Password Reset subflow updates the status as Completed with Success.|
|Oracle Operations|This automation enables you to define employees in the Oracle EBS ERP system. Employment of a candidate is confirmed when the recruitment process is completed. If the recruitment of a candidate is performed through a manual system such as email, spreadsheets, and so on, you can use this automation to define employees from the manual system to the Oracle EBS ERP system. You can also use this automation if the recruitment process is performed through a different ERP system and then define the employees in the Oracle EBS ERP system.|
|PDF Text to Images|This automation searches for a specific text within a PDF file and saves the corresponding pages as images in a designated folder. Supported image formats include JPEG, JPG, and PNG. Provide the text to be searched, the path to the PDF file, and the destination folder path where the images must be saved.|
|PDF to Word|This automation converts multiple PDF files into separate Word files. Provide the path to the folder containing the PDF files, and the automation converts them to the Word file format.|
|Resume Skill Matcher|This automation automates the resume screening process, saving recruiters valuable time and effort.|
|Shipping Orders|This automation retrieves details from an Excel file, opens a Windows application, inputs the details into the application, submits the information, and finally, once all details are processed, closes the Windows application.|
|Start App|This automation launches a webpage in the Chrome application with the provided URL.|
|Streamlining Report Data Analysis|This automation extracts tables from the Word document and creates sheets in Excel.|
|Summarize Sales Data|This automation summarizes sales data using Excel Macros and sends the results to the recipient via email as an unattended automation.|
|Tiff to PDF|This automation converts multiple TIFF images into a single PDF file. It processes TIFF files from a specified input location and generates a consolidated PDF document. After completing the conversion, the resulting PDF file is automatically saved in the designated output folder, for easy access. This process streamlines document handling by combining multiple image files into a single, organized PDF output.|
|Universal Timezone Converter|This automation converts time from one-time zone to another using the VB.Net Connector, ensuring accurate adjustment to the specified target time zone.|
|User Creation in Badging App|This automation streamlines the interaction with BadgeTool application by using the Universal App Connector to automate user management tasks based on data from an Excel file.|
|V\_LookUp|This automation reads data from the Department Excel file, retrieves values from column A, and adds them to a list. It then reads Employee Excel file, takes column A values one by one, and compares them with the department list values. If a match is found, it retrieves the corresponding row details from the Employee Excel file and sets the values into the Department Excel file.|
|While Loop|This automation reads values from a variable, checks a condition using the While Component and Decision Component, and displays formatted text in a message box. If the decision matches, the automation breaks out of the while loop.|
|Word Operations|This automation demonstrates various tasks in Microsoft Word, such as setting tables, inserting tables and pictures, and exporting Word to PDF. It showcases a sequential flow to help you understand seamless integration within an automation workflow.|
|Word to PDF Converter|This automation converts multiple Word files \(.docx\) from the Source folder path \(default Project folder\) to separate PDF files and stores them in the same location.|
|XML to Excel Conversion|This automation converts multiple XML files to separate XLSX files. Converted XLSX files are stored in the processed folder path.|
|Zip and UnZip files|This automation streamlines file management by providing compress and decompress functionalities.|

|Sample automation|Description|
|-----------------|-----------|
|Copying a Range from One Excel File to Another|This automation copies a range of data from one Excel file to another. The automation is designed to identify the specific range of cells in the source Excel file, extract the data, and then paste it into the designated range in the destination Excel file. This use case is useful for tasks such as data consolidation, report generation, and data migration, where manual copying and pasting can be time-consuming and prone to errors.|

**Parent Topic:**[Use sample automations in RPA Desktop Design Studio](../task/use-sample-automation.md)

