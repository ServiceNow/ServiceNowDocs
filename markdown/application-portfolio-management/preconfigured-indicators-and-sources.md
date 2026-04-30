---
title: Preconfigured indicators and their source applications
description: The preconfigured Enterprise Architecture indicators and the applications they have been sourced from help you to assess the applications across dimensions such as cost, quality, and risk. You can create additional indicators, apart from the preconfigured indicators, by copying and modifying them.
locale: en-US
release: yokohama
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 5
breadcrumb: [Framework setup for application assessment, Application assessment, Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Preconfigured indicators and their source applications

The preconfigured Enterprise Architecture indicators and the applications they have been sourced from help you to assess the applications across dimensions such as cost, quality, and risk. You can create additional indicators, apart from the preconfigured indicators, by copying and modifying them.

<table id="table_zcp_hw4_px"><thead><tr><th>

Indicator name

</th><th>

Frequency

</th><th>

Type

</th><th>

Source

</th><th>

How is it calculated?

</th><th>

Description

</th><th>

Jobs

</th></tr></thead><tbody><tr><td>

Facilities cost

</td><td>

Quarter

</td><td>

Custom Script

</td><td>

ITFM product. ITFM\_Allocation\_Aggregate table

</td><td>

Data will be available in the ITFM tables only after the financial modeling process is completed

</td><td>

Facilities cost for business application

</td><td>

 

</td></tr><tr><td>

Hardware cost

</td><td>

Quarter

</td><td>

Custom Script

</td><td>

ITFM product. ITFM\_Allocation\_Aggregate table

</td><td>

Data will be available in ITFM tables only after the financial modeling process is completed

</td><td>

Hardware cost for business application

</td><td>

 

</td></tr><tr><td>

Labor cost

</td><td>

Quarter

</td><td>

Custom Script

</td><td>

ITFM product. ITFM\_Allocation\_Aggregate table

</td><td>

Data will be available in the ITFM tables only after the financial modeling process is completed

</td><td>

Labor cost for business application

</td><td>

 

</td></tr><tr><td>

Other cost

</td><td>

Quarter

</td><td>

Custom Script

</td><td>

ITFM product. ITFM\_Allocation\_Aggregate table

</td><td>

Data will be available in the ITFM tables only after the financial modeling process is completed

</td><td>

Other cost for business application

</td><td>

 

</td></tr><tr><td>

Services cost

</td><td>

Quarter

</td><td>

Custom Script

</td><td>

ITFM product. ITFM\_Allocation\_Aggregate table

</td><td>

Data will be available in the ITFM tables only after the financial modeling process is completed

</td><td>

Services cost for business application

</td><td>

 

</td></tr><tr><td>

Software cost

</td><td>

Quarter

</td><td>

Custom Script

</td><td>

ITFM product. ITFM\_Allocation\_Aggregate table

</td><td>

Data will be available in the ITFM tables only after the financial modeling process is completed

</td><td>

Software cost for business application

</td><td>

 

</td></tr><tr><td>

Application TCO

</td><td>

Quarter

</td><td>

Custom Script

</td><td>

ITFM product. ITFM\_Allocation\_Aggregate table

</td><td>

Data will be available in the ITFM tables only after the financial modeling process is completed

</td><td>

Total application cost from all the buckets

</td><td>

 

</td></tr><tr><td>

Application's Incident Count

</td><td>

Quarter

</td><td>

Custom Script

</td><td>

incident

</td><td>

Data will be available in the incident table only after the business application is associated to the incident.

</td><td>

Indicator that gets the count of all incidents associated to the business application tied to the scoring profile of which the indicator is part.

</td><td>

 

</td></tr><tr><td>

Application's Instance – Incident Count

</td><td>

Quarter

</td><td>

Custom Script

</td><td>

incident

</td><td>

Gets incident count attached to all Application Instances, which are mapped to a business application and rolls it up to application.

</td><td>

Indicator that gets the count of all incidents associated with application instances. The application instances, in turn, are associated to a business application tied to a scoring profile of which the indicator is a part.The incident count is calculated first at the application instance or application service level, and then it is rolled up to the business application level.

</td><td>

 

</td></tr><tr><td>

Usage

</td><td>

Month

</td><td>

Query Condition

</td><td>

APM product. cmdb\_ci\_business\_app table

</td><td>

Calculated from the **Active User Count** field

</td><td>

Number of user sessions and users for the application for a given fiscal period.

</td><td>

 

</td></tr><tr><td>

Number of Incidents via Service

</td><td>

Daily

</td><td>

Performance Analytics

</td><td>

Mapped to **Performance Analytics** &gt; **Indicators** &gt; **Automated Indicators** &gt; **Number of new incidents** Source = Incidents.New \(Incident table\)

</td><td>

Number of incidents opened today. Calculated from the Impacted Business Applications of the incident record.

</td><td>

Number of new incidents. Daily and historic data collection

</td><td>

\[PA Incident\] Daily Data Collection\[PA Incident\] Historic Data Collection

</td></tr><tr><td>

Number of Problems via Service

</td><td>

Daily

</td><td>

Performance Analytics

</td><td>

Mapped to **Performance Analytics** &gt; **Indicators** &gt; **Automated Indicators** &gt; **Number of new problems** Source = Problems.New \(Problem table\)

</td><td>

Problems created today. Calculated from the **Service** field of the problem record.

</td><td>

Number of problems opened today. Daily and historic data collection

</td><td>

\[PA Problem\] Daily Data Collection\[PA Problem\] Historic Data Collection

</td></tr><tr><td>

Number of Changes via Service

</td><td>

Daily

</td><td>

Performance Analytics

</td><td>

Mapped to **Performance Analytics** &gt; **Indicators** &gt; **Automated Indicators** &gt; **Number of new changes** Source = Changes.New \(change\_request table\)

</td><td>

Number of changes with a registration date \(change\_request.opened\_at\) on collection date. Calculated from the Impacted Business Applications of the change request record.

</td><td>

Number of changes opened today. Daily and historic data collection

</td><td>

\[PA Change\] Daily Data Collection\[PA Change\] Historic Data Collection

</td></tr><tr><td>

Customer satisfaction \(CSAT\)

</td><td>

Quarter

</td><td>

Assessments

</td><td>

Assessment Metric Type: Customer SatisfactionAssessment Metric Category: CSAT

</td><td>

 

</td><td>

Template NPS

</td><td>

 

</td></tr><tr><td>

Functional fit

</td><td>

Month

</td><td>

Assessments

</td><td>

Assessment Metric Type: Functional FitAssessment Metric Category: Functional Fit

</td><td>

 

</td><td>

Template Net Promoter Score \(NPS\)

</td><td>

 

</td></tr><tr><td>

Technical risk

</td><td>

Month

</td><td>

Assessments

</td><td>

Assessment Metric Type: Technical RiskAssessment Metric Category: Performance

</td><td>

 

</td><td>

Technical risk captured through survey for the fiscal period.Template NPS

</td><td>

 

</td></tr><tr><td>

Technology Lifecycle Risk

</td><td>

Month

</td><td>

Custom Script

</td><td>

Assessment Metric Type: Functional FitAssessment Metric Category: Functional Fit

</td><td>

 

</td><td>

Get the technology lifecycle risk of a business application for a selected fiscal period.

</td><td>

 

</td></tr><tr><td>

Business value

</td><td>

Quarter

</td><td>

Assessments

</td><td>

Consolidation: Average

</td><td>

 

</td><td>

Template NPS

</td><td>

 

</td></tr><tr><td>

Total change hours

</td><td>

Month

</td><td>

Performance Analytics

</td><td>

Mapped to **Performance Analytics** &gt; **Indicators** &gt; **Automated Indicators** &gt; **Summed duration of closed changes** Source = Changes.Closed \(Change\_Request table\)

 Fields: Opened, Closed

 State = Closed, Business Application = any of the Enterprise Architecture Business Applications, Closed today

</td><td>

Script: Change.CloseTime.Hours. All Change Requests closed today considered

</td><td>

Summed duration of closed changes for an application for the given fiscal period.Time taken to close the changes in hours. Daily and historical data collection.

</td><td>

-   \[PA Change\] Daily Data Collection
-   \[PA Change\] Historic Data Collection

</td></tr></tbody>
</table>**Note:** Ensure the following system properties are set to True for Incident and Change indicators.

-   To set the properties, navigate to All &gt; System Properties &gt; All Properties and search for the following properties:
    -   Populate Impacted Services based on Affected CIs \(com.snc.incident.refresh\_impacted.include\_affected\_cis\)
    -   Populate Business Application related list for incidents \(com.snc.incident.populate\_business\_application\)
    -   Populate the Business Application related list for change requests \(com.snc.change\_request.populate\_business\_application\)
-   To show up the **Impacted Business Applications** &gt; **Related List** &gt; **Additional actions** &gt; **Configure** &gt; **Related Lists** &gt; **Impacted Business Applications** &gt; **Available** &gt; **Selected** &gt; **Save**.
-   To see the impacted business applications for the **Number of Incidents via Service** and **Number of Changes via Service** indicators, you must refresh the **Impacted Services and CIs** related list for that record. For instructions, see [Refresh impacted services and CIs for Change](https://www.servicenow.com/docs/access?context=refresh-impacted-services-cis&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US) and [Refresh impacted services and CIs for incident](https://www.servicenow.com/docs/access?context=refresh-impacted-cis&version=yokohama&pubname=yokohama-it-service-management&ft:locale=en-US).

-   **[Performance Analytic indicators to measure application performance](../concept/pa-indicators-jobs.md)**  
Use performance analytic \(PA\) indicators to know the count of incidents, problems, and changes logged against a business application and use this insight to improve the performance of your applications.

**Parent Topic:**[Framework setup for application assessment](../concept/applications-assessment-overview.md)

**Related topics**  


[Assessments](https://www.servicenow.com/docs/access?context=r_Assessments&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

[Get started with Survey Management](https://www.servicenow.com/docs/access?context=r_SurveyManagementLandingPage&version=yokohama&pubname=yokohama-servicenow-platform&ft:locale=en-US)

