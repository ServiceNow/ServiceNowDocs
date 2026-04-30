---
title: Extract data from utility invoices
description: The AI-driven document intelligence for utility invoices skill automates the extraction of utility bill data, including consumption, billing dates, and amounts. The extracted data is mapped to the correct metric definitions and entities using configurable mapping tables within the Operational Sustainability Workspace.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-09-11"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist for Operational Sustainability, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Extract data from utility invoices

The AI-driven document intelligence for utility invoices skill automates the extraction of utility bill data, including consumption, billing dates, and amounts. The extracted data is mapped to the correct metric definitions and entities using configurable mapping tables within the Operational Sustainability Workspace.

## Before you begin

Role required: sn\_esg\_gen\_ai.docintel\_user

## About this task

-   The fields from which the data is extracted are based on the extraction use case selected. One predefined use case is provided for utility invoices. If necessary, you can create a custom extraction use case. After the data is extracted and mapped to the required fields, you can use it as is or update it as required.
-   The system must have a valid entity mapping or the extraction might fail. Mapping links source data, such as billing address or utility type, to the correct entity in the metric definition.

**Important:** Be sure to check AI-extracted information for accuracy.

**Important:** This Now Assist skill is turned on by default. The skill will be automatically available to appropriate role users for the application. For more information, see [Now Assist skills, agents, and agentic workflows on by default](https://www.servicenow.com/docs/access?context=now-assist-skills-on-by-default&version=zurich&pubname=zurich-intelligent-experiences&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Environmental, Social, and Governance** &gt; **ESG Workspace** &gt; **Lists** &gt; **Document intelligence** &gt; **Metric document extraction**.

2.  Select **Upload document**.

3.  Select the **+ Add file** link and open the utility invoice document that exists in your local machine.

    The name of the uploaded file defaults as the title of the file in the **Upload a file** pop-up. If necessary, you can change the name of the file in the **Title** field.

    **Note:** You can upload only one file at a time to the folder.

4.  Select **Upload**.

5.  Select **Done**.

    The new metric document extraction opens automatically.

6.  Select **Initiate extraction**.

    The extraction process starts, and eventually the extracted data is mapped to the corresponding fields. The AI-extracted fields are marked so you can verify the extracted information.

7.  Review the extracted data and either save or delete the created record.

    |Option|Description|
    |------|-----------|
    |**Reprocess**|Initiates a rerun of the extraction and mapping process for a utility bill using the latest metric definition and entity-mapping records. This option appears only when extraction fails, enabling you to retry after correcting errors.|
    |**Review in Docintel**|Enables review of key details extracted from utility bills. It displays the mapping of extracted fields to their respective data points, facilitating verification and accuracy checks.|
    |**Save**|Save the mapped data in the record.|
    |**Delete**|Delete the record.|


**Parent Topic:**[Using Now Assist for Operational Sustainability skills](using-now-assist-for-esg-skills.md)

