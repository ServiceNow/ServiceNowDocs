---
title: Extract data from utility invoices
description: The AI-driven Document Intelligence for utility invoices feature automates the extraction of utility bill data, including consumption, billing dates, and amounts. Then the extracted data is mapped to the correct metric definitions and entities using configurable mapping tables within the Operational Sustainability Workspace. This streamlines data processing and enhances accuracy.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Use generative AI skills, Now Assist, Use, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Extract data from utility invoices

The AI-driven Document Intelligence for utility invoices feature automates the extraction of utility bill data, including consumption, billing dates, and amounts. Then the extracted data is mapped to the correct metric definitions and entities using configurable mapping tables within the Operational Sustainability Workspace. This streamlines data processing and enhances accuracy.

## Before you begin

Role required: sn\_esg\_gen\_ai.docintel\_user

## About this task

-   The fields from which the data is extracted is based on the extraction use case selected. One predefined use case is shipped for utility invoices, if necessary you can create a custom extraction use case. After the data is extracted and mapped to the required fields, you can directly use it or update as required.
-   To avoid utility bill extraction failures, the system must have a valid entity mapping. This mapping links source data such as billing address or utility type to the correct entity in the metric definition.

**Important:** Be sure to check AI-extracted information for accuracy.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Lists** &gt; **Document intelligence** &gt; **Metric document extraction**.

2.  Select **Upload document**.

3.  Select the **+ Add file** link to browse and open the utility invoice document that exists in your local machine.

    The name of the uploaded file defaults as the Title of the file in the **Upload a file** pop-up. If necessary, you can change the name of the file in the **Title** field.

    **Note:** You can upload only one file at a time to the folder.

4.  Select **Upload**.

    The selected file from your local machine is uploaded.

5.  Select **Done**.

    The newly created metric document extraction opens automatically.

6.  Select **Initiate extraction**.

    The extraction process is initiated, and after a short while, the extracted data is accurately mapped to its corresponding fields. The AI-extracted fields are clearly marked for verification, confirming transparency and facilitating review.

7.  Review the extracted data and complete any of the following options.

    |Option|Description|
    |------|-----------|
    |**Reprocess**|Initiates a rerun of the extraction and mapping process for a utility bill using the latest metric definition and entity-mapping records. This option appears only when extraction fails, allowing users to retry after correcting errors.|
    |**Review in Docintel**|Enables review of key details extracted from utility bills. It displays the mapping of extracted fields to their respective data points, facilitating verification and accuracy checks.|
    |**Save**|Save the mapped data in the record.|
    |**Delete**|Delete the record.|

    The fields extracted by AI must be verified for accuracy before use.


**Parent Topic:**[Using Now Assist for Operational Sustainability \(formerly ESG\) skills](using-now-assist-for-esg-skills.md)

