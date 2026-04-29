---
title: Application assessment
description: Set up indicators to measure the usability, cost, quality, performance, and risk of applications. Evaluate and score your business applications based on qualitative inputs. You can translate abstract information of applications based on surveys and assessments into more tangible concrete metrics. These assessments help you make strategic decisions on whether to replace or upgrade applications.You can create indicators and score profiles based on which you can assess your applications. Application indicators are business metrics that help derive application scores.The preconfigured Enterprise Architecture indicators and the applications they have been sourced from help you to assess the applications across dimensions such as cost, quality, and risk. You can create additional indicators, apart from the preconfigured indicators, by copying and modifying them.Use performance analytic \(PA\) indicators to know the count of incidents, problems, and changes logged against a business application and use this insight to improve the performance of your applications.After you set up indicators, create score profile, and attach profile indicators, schedule a job to periodically compute the application scores.The indicators and their respective weights are used to calculate application score profiles for each configuration item. Use the score profile to calculate application scores and assess the applications. Apply these scores to compare applications and make strategic decisions about which ones to keep, replace, maintain, or invest more in.If the source of the indicator is Assessments in the Data source field, then the Target maximum, Target minimum, Application weight, and Total weight values are considered as zero.Visualization of the performance of applications in different dimensions on a bubble chart, in a dashboard, and in an application 360 view helps you to take decisions on the applications.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 18
breadcrumb: [Exploring Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Application assessment

Set up indicators to measure the usability, cost, quality, performance, and risk of applications. Evaluate and score your business applications based on qualitative inputs. You can translate abstract information of applications based on surveys and assessments into more tangible concrete metrics. These assessments help you make strategic decisions on whether to replace or upgrade applications.

You can use existing assessment metric types or configure them per your requirements.

**Related topics**  


[View all application scores](../task/view-application-scores.md)

[View application indicator scores](../task/view-application-indicator-scores.md)

[Add or edit a scoring profile](../task/eaw-task/eaw-create-scoring-profile.md)

[Add or edit an application indicator](../task/eaw-task/eaw-create-indicator.md)

[Activate or turn off an application or capability indicator](../task/eaw-task/eaw-enable-or-disable-an-application-indicator.md)

[Add a business capability](../task/add-a-capability.md)

[Update the hierarchy of a business capability](../task/update-hierarchy.md)

## Framework setup for application assessment

You can create indicators and score profiles based on which you can assess your applications. Application indicators are business metrics that help derive application scores.

Enterprise Architecture is integrated with key applications in the ServiceNow platform to provide a deep insight into the applications. These integrations help you:

-   **Identify cost saving opportunities**

    The Hierarchy of Segments in the Financial Management application tracks the cost allocations at the application level, which provides a complete cost breakdown for the application.

-   **Organize applications to determine their rationalization**

    You can identify multiple applications assigned to the same application category, region, or business. This information helps you to know who is using the applications, the usage frequency, the application status, and make informed decisions.

-   **Identify opportunities for modernizing and investing in application**

    You can identify applications that have contracts to renew, low usage, or low customer satisfaction based on surveys results.


Use the preconfigured indicators or create your indicators to assess applications with dimensions such as cost, quality, technical risk, investments, user satisfaction, and business value. [Preconfigured indicators](application-assessment.md#) are sourced from Financial Management, IT Service Management, project portfolio management, surveys, assessments, SQL queries, performance analytics, and custom scripts.

**Note:** Enterprise Architecture supports only the Fiscal Calendar type, Standard.

**Related topics**  


[Create or edit an indicator to assess an application](../task/create-application-indicators.md)

[Create an application score profile and attach profile indicators](../task/create-an-appln-score-profile.md)

[Job schedule to compute application scores](application-assessment.md#)

### Preconfigured indicators and their source applications

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
-   To see the impacted business applications for the **Number of Incidents via Service** and **Number of Changes via Service** indicators, you must refresh the **Impacted Services and CIs** related list for that record. For instructions, see [Refresh impacted services and CIs for Change](https://www.servicenow.com/docs/access?context=refresh-impacted-services-cis&version=australia&pubname=australia-it-service-management&ft:locale=en-US) and [Refresh impacted services and CIs for incident](https://www.servicenow.com/docs/access?context=refresh-impacted-cis&version=australia&pubname=australia-it-service-management&ft:locale=en-US).

**Related topics**  


[Assessments](https://www.servicenow.com/docs/access?context=r_Assessments&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

[Get started with Survey Management](https://www.servicenow.com/docs/access?context=r_SurveyManagementLandingPage&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US)

#### Performance Analytic indicators to measure application performance

Use performance analytic \(PA\) indicators to know the count of incidents, problems, and changes logged against a business application and use this insight to improve the performance of your applications.

Enterprise Architecture uses indicators that are sourced from Performance Analytics \(PA\). These indicators give a count of incidents, problems, changes, and the number of change requests that were closed on a given day. Follow the given order to run the PA jobs at the scheduled time, and get the scores of the indicators to evaluate the performance of your business applications.

##### Order in which to run PA jobs and generate scores

You should run the scheduled jobs in the following order:

1.  \[PA Incident\] Daily Data Collection.
2.  \[PA Change\] Daily Data Collection.
3.  \[PA Problem\] Daily Data Collection.
4.  \[Enterprise Architecture Scheduled job\] Load Application Indicators and compute Application Scores.

If there are historic data, then run them in the following order:

**Note:**

You require Performance Analytics Premium for Enterprise Architecture \(com.snc.pa.premium.apm\) plugin to retrieve historic data that are older than six months.

1.  \[PA Incident\] Historic Data Collection.
2.  \[PA Change\] Historic Data Collection.
3.  \[PA Problem\] Historic Data Collection.
4.  Regenerate Enterprise Architecture scores for required time period. This action deletes the existing scores including daily scores and generates new scores instead of just updating the existing scores.

##### Frequency at which indicator scores are generated

Scores are generated as per the scheduled run of the job that executes the script. If the indicator frequency is:

-   **Monthly**

    scores are generated only on the last day of a month.

-   **Quarter**

    scores are generated only on the last day of a quarter.

-   **Yearly**

    scores are generated only on the last day of a year.


**Note:** Fiscal periods should be generated in the same time zone in which the scores are generated.

##### Collection of PA indicator score data

The period unit \(days, weeks, or month\) at which the PA indicator scores are collected and preserved depends on the frequency of the data source indicator. However, the frequency at which the application indicator collects the PA indicator data source scores varies.

In Enterprise Architecture, the frequency of the application indicator must be greater than or equal to the frequency of the data source indicator.

The following table describes the frequency at which Enterprise Architecture collects data from the data source indicators after the job runs:

|Enterprise Architecture frequency|Data source indicator frequency|
|---------------------------------|-------------------------------|
|Monthly|Monthly|
|Quarterly|Monthly and Quarterly|
|Yearly|Monthly, Quarterly, and Yearly|

If you are an Enterprise Architecture customer, who has upgraded to the Australia release, then the **Daily** frequency of Performance Analytics data source indicator is not available. RemoveDailyFreqAndUpdatePAIndicator fix script automatically removes the **Daily** frequency of PA indicators and updates the frequency to **Monthly**.

##### Limitations to display application breakdowns in PA scoresheet

If there is a large number of business applications installed, then all the breakdowns are not displayed in the **Performance Analytics** &gt; **Scoresheet**, as there is a limitation set in the system properties: **com.snc.pa.scoresheet.max\_elements** and **com.snc.pa.scorecards.max\_breakdown\_elements**. To reconfigure the property limitation:

1.  Navigate to **Performance Analytics** &gt; **System** &gt; **Properties**.
2.  Enter the maximum number in the **Maximum number of elements of a breakdown in Scoresheet** field. The number must be greater than or equal to the number of business applications installed in your system.
3.  Enter the maximum number in the **Maximum number of breakdown elements in scorecard lists** field.
4.  Click **Save**.

## Job schedule to compute application scores

After you set up indicators, create score profile, and attach profile indicators, schedule a job to periodically compute the application scores.

Understand how the system calculates application scores and create your application score profile per your requirements.

The assessment framework [calculates the application score for each application](application-assessment.md#) on a scale of 1–10, where 10 is a good score and 1 is a low score. Assessments are based on various configured indicators, which you can configure. Each of these indicators periodically captures the related application data, which is used to derive the application score. These indicators with their respective value \(weightage\) are added to an application profile. The application is then associated with the application profile, which calculates the application score.

### Normalization of application scores

The indicators and their respective weights are used to calculate application score profiles for each configuration item. Use the score profile to calculate application scores and assess the applications. Apply these scores to compare applications and make strategic decisions about which ones to keep, replace, maintain, or invest more in.

The preconfigured indicators or the indicators that you created retrieve their related data based on the frequency set at the indicator definition stage. This data is captured in the **Application weight** column of the Application Indicator Score \[apm\_app\_indicator\_score\] table. The **Target maximum** and **Target minimum** that are set while creating an application indicator are for calculating the applications normalized value.

**Note:** The **Target maximum** and **Target minimum** are not available when the data source is Assessments.

The normalized value of the application score, which is measured on a scale of 1–10, is derived from the following formula:

```
(Application Weight - Target minimum)/(Target maximum - Target minimum) * 9+1
```

**Note:**

-   If the **Target maximum** and **Target minimum** are not set, then the maximum value within the range of applications is taken as the target maximum value. Similarly, the minimum value within the range of applications is taken as the target minimum value.
-   If the  **Target maximum ** and  **Target minimum ** are set and the **Consider Absolute Values** check box is selected, the entered values are considered.
-   If the **Target maximum ** and  **Target minimum ** are set and the **Consider Absolute Values** check box is cleared, the values are considered based on the following intelligent logic.

    ```
    Target maximum = Minimum value of (Target maximum value defined in the Indicator [apm_metric] table, Maximum value of Application Weights for the fiscal period)
    ```

    For example, consider a scenario where:

    -   The application weights are 10, 20, 30,.…., and 1000.
    -   Value entered in the Target maximum field is 100.
    With these assumptions, the Target maximum value considered is 100, as the defined Target maximum value \(100\) is lesser than the maximum application weight \(1000\).

    ```
    Target minimum = Maximum value of (Target minimum value defined in the Indicator [apm_metric] table, Minimum value of Application Weights for the fiscal period)
    ```

    For example, consider a scenario where:

    -   The application weights are 10, 20, 30,.…., and 1000.
    -   Value entered in the Target minimum field is 100.
    With these assumptions, the Target minimum value considered is 10, as the defined Target minimum value \(100\) is greater than the minimum application weight \(10\).


The **Application Weight** that is lesser than or equal to the target minimum is given the lower score, which is 1.

The **Application Weight** that is greater than or equal to the target maximum is given the maximum score, which is 10.

When you set the application indicators, you can also configure the **Direction** as Maximize or Minimize. The application with the maximum value gets the minimum score when the direction is Minimize. The application with the minimum value gets the maximum score when the direction is Maximize.

If the **Direction** in the indicator is **Minimize**:

```
(10 - above calculated Normalized value) + 1
```

Application profile weightage is then applied on the Normalized value to derive the **Indicator Score**:

```
Normalized Value * Weightage as in application score profile %
```

After the indicator score is calculated for each of the indicators, the application score is calculated by summing up all the indicator scores used in the profile.

If the source of the indicator is **Indicators** in the **Data source** field, then the application weight is calculated as the sum of the normalized scores of all its dependent indicators.

**Note:**

-   The normalized score of the parent indicators is then calculated in a similar manner as it is calculated for all the other indicators.
-   The normalized value, indicator score, application weight, target maximum, target minimum, and total weight are all rounded to two decimal places only.

In the figure, since the Cost and Incident indicators are set to minimize, the applications with lower costs and lower number of incidents have higher scores.

### Normalized value and application score for an assessment

If the source of the indicator is **Assessments** in the **Data source** field, then the Target maximum, Target minimum, Application weight, and Total weight values are considered as zero.

For a business application to be considered for scoring, it must be mapped to a respective application profile to which the indicator is associated. You can check the scoring profiles in the apm\_application\_profile list.

All the business application related Assessment Category Results having assessment groups created within a fiscal period are considered for calculating the score. You can check the assessment category results for a business application in the asmt\_category\_result list.

For an assessment group to be considered for computing scores, all the related assessment instances must be either in completed or cancelled state.

```
scaleFactor = (9/ scale factor on metric type)
```

```
appAsmtScoreSUM = SUM of ratings of category results groupedBY source for each assessment group
```

```
appWeight=((scaleFactor * appAsmtScoreSUM )+1;
```

```
Normalized value = total app weight of BA/appOccurences.
```

```
totalIndicatorsWeightage = the sum of all indicator weightage mapped to a scoring profile.
```

```
appIndWeightage = weightage of the current indicator
```

```
Indicator Score = normalizedValue * appIndWeightage / totalIndicatorsWeightage
```

The app occurrence is the occurrences of a business application.

## Visualization of application performance

Visualization of the performance of applications in different dimensions on a bubble chart, in a dashboard, and in an application 360 view helps you to take decisions on the applications.

Having set up indicators and attaching application score profiles and running the scheduled job to calculate its scores periodically, your application scores are now ready for viewing.

-   Use bubble charts to visualize your business application data plotted on a chart in three dimensions, which helps you to compare and evaluate applications based on their indicator scores.
-   Use Application 360 to focus on the business applications that require your attention.
-   Use Application Assessments dashboard to view the trends of indicators for different applications.

**Related topics**  


[View application indicator scores](../task/view-application-indicator-scores.md)

[View all application scores](../task/view-application-scores.md)

[Analyze application scores in a bubble chart](../task/strategies-using-bubble-charts.md)

[Monitor performance, costs, and workloads in Application 360](../task/applications-360-dashboard.md)

[Assess the performance of applications in the dashboard](../task/use-appln-assessment-dashboard.md)

