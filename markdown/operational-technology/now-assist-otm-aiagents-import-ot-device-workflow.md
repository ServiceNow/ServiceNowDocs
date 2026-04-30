---
title: Import the OT device spreadsheet into OT CMDB agentic workflow
description: Use the Import OT device spreadsheet into OT CMDB agentic workflow to automate the upload, validation, and import of your OT device data into the OT CMDB.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-11-07"
reading_time_minutes: 2
breadcrumb: [Use agentic AI in the OTM application, Now Assist for OTM, Operational Technology]
---

# Import the OT device spreadsheet into OT CMDB agentic workflow

Use the Import OT device spreadsheet into OT CMDB agentic workflow to automate the upload, validation, and import of your OT device data into the OT CMDB.

## Import OT device spreadsheet into OT CMDB overview

Using the Import OT device spreadsheet into OT CMDB agentic workflow, you can import the OT device inventory spreadsheet and map the spreadsheet data to the OT staging table. After importing and creating an OT staging table record, you can validate the staging record, remediate invalid records, and import all the validated records into the OT CMDB. For more information about how to use this agentic workflow, see [Upload, validate, and import the OT device inventory spreadsheet](../task/upload-import-validate-ot-device-inventory-spreadsheet.md).

**Important:** This agentic workflow is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

To modify the Import OT device spreadsheet into OT CMDB agentic workflow, [duplicate it](https://www.servicenow.com/docs/access?context=clone-aia-usecase&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US), and adjust the settings according to your requirements.

**Important:** When you modify an agentic workflow, AI agent, or a tool, make sure that you update all instructions accordingly.

## Import OT device spreadsheet into OT CMDB agentic workflow

The workflow helps you complete the following process:

1.  Import the OT device inventory spreadsheet with an OT Excel SGC Import Task record.
2.  Map the spreadsheet data to the SG OT Excel Stagings table.
3.  Validate the OT staging table records.
4.  Remediate invalid records if needed.
5.  Import all validated records into the OT CMDB.

To access the agentic workflow:

1.  Navigate to **All** &gt; **AI Agent Studio** &gt; **Create and manage**.
2.  Under the **Agentic workflows** tab, select the **Import OT device spreadsheet into OT CMDB** agentic workflow.

## AI agents used in the Import OT device spreadsheet into OT CMDB agentic workflow

The Import OT device spreadsheet into OT CMDB agentic workflow uses the OT Excel import task AI agent. Once you upload the device inventory spreadsheet, the agent processes the spreadsheet, creates an OT Excel SGC Import Task record, and maps the data to the SG OT Excel Stagings table. The agent then runs validations on the staging records, creates a remediation task for all invalid records, and imports the valid records into the OT CMDB.

**Important:** This agent is turned on by default. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

-   **[Upload, validate, and import the OT device inventory spreadsheet](../task/upload-import-validate-ot-device-inventory-spreadsheet.md)**  
Chat with an AI agent in the Now Assist panel to begin the process for uploading, validating, and importing your Operational Technology \(OT\) device data into the OT CMDB.

**Parent Topic:**[Use agentic AI for Now Assist for Operational Technology Manager \(OTM\)](now-assist-for-otm-use-cases.md)

