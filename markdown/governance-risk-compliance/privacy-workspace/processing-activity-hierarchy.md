---
title: Processing activity hierarchy
description: Each processing activity involves multiple information objects classified as personal information. These objects exchange data with various other entities, making it essential to establish a data lineage or hierarchy that tracks where personal data is shared. This understanding helps mitigate privacy-related risks.
locale: en-US
release: xanadu
product: Privacy Workspace
classification: privacy-workspace
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Processing activities, Explore, Privacy Management, Governance, Risk, and Compliance]
---

# Processing activity hierarchy

Each processing activity involves multiple information objects classified as personal information. These objects exchange data with various other entities, making it essential to establish a data lineage or hierarchy that tracks where personal data is shared. This understanding helps mitigate privacy-related risks.

## Methods to create data lineage

You can create a data lineage in the following ways:

-   From the Hierarchy tab of a processing activity.
-   From the Data lineage button on a processing activity. For more information see, [Create a data lineage for a processing activity](../task/create-a-data-lineage-for-a-processing-activity.md).

## Importance of data lineage

To understand why data lineage is important, consider the following example of data management in a Human Resources organization. Any HR organization contains information such as the following.

-   Employee records: These include personal details like names, addresses, phone numbers, and email addresses.
-   Prospective interview candidate records: Contains candidate names, interview dates, and times.

The entities involved in this example could be:

-   Internal departments such as Talent acquisition, Recruiters, People Management teams.
-   External tools and applications to track time off, benefits, and so on.

When a new candidate registers, their personal information is entered into the HR organization's database. This information is shared with the administrative staff for appointment scheduling. Data lineage helps track the flow and transformation of data through various processes. In this example, the following could be a workflow:

1.  Candidate registration:
    -   A person registers on the careers portal and submits their resume.
    -   The candidate's details such as name, email, phone number are entered into the applicant tracking system \(ATS\).
2.  Scheduling an interview:
    -   The Talent Acquisition team selects the candidate for an interview and enters the interview date and time into the calendar application.
    -   The calendar application sends an email to the candidate with the interview details.
3.  Conducting the interview:
    -   The recruiters access the candidate’s profile on the ATS, review the resume, and conduct the interview.
    -   Post-interview, they add their feedback to the candidate's ATS profile.
4.  Hiring process:
    -   The candidate is selected for the position.
    -   The candidate details are transferred from the ATS to the HR database, and additional information is collected and updated.
    -   The HR database uses other external applications to create the candidate’s employee profile, including time-off records and benefits information.

By establishing a data lineage, the HR organization can track where each piece of personal data originates, how it’s processed, and where it’s shared. Understanding the data flow helps identify potential privacy risks, such as unauthorized access or data breaches at any point where data is shared. By establishing the data lineage in this way, the HR organization can ensure that they’re aware of all points where personal data is exchanged. This understanding helps them implement appropriate safeguards to mitigate privacy-related risks.

## Information displayed on the data lineage page

After you establish the relationship of the data flow, the data lineage page displays the following key information on the right side pane.

-   Description of the processing activity along with its owner and the type.
-   Criticality score of the processing activity if the score is High.
-   Risk rating of the processing activity if the score is High and Critical.
-   Compliance score of the processing activity.
-   Number of open issues.
-   Number of critical open issues.
-   On going assessments.

If a selected CMDB record already has a processing activity linked to it, then that information is also displayed during the hierarchy creation. A toggle switch **View roll-up** is provided to view the rollup of personal information objects. If this switch is turned on, then the personal information objects associated with the selected asset and its associated destinations are displayed.

## Data lineage example

The following image shows a sample data lineage hierarchy.![Hierarchy of a processing activity.](../image/data-lineage-example.png)

**Parent Topic:**[Processing activities](ropa-record.md)

**Related topics**  


[Create a data lineage for a processing activity](../task/create-a-data-lineage-for-a-processing-activity.md)

