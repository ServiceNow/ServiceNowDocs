---
title: Enterprise Architecture \(formerly APM\) Cloud Assessment Scoring Profile
description: The Cloud Assessment scoring profile in Enterprise Architecture helps you to evaluate a business application for its cloud migration readiness.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Reference, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Enterprise Architecture \(formerly APM\) Cloud Assessment Scoring Profile

The Cloud Assessment scoring profile in Enterprise Architecture helps you to evaluate a business application for its cloud migration readiness.

## Indicator for Enterprise Architecture Cloud Assessment Scoring Profile

<table id="table_emm_t3g_dvb"><thead><tr><th>

Indicator name

</th><th>

Frequency

</th><th>

Type

</th><th>

Source

</th><th>

How is it calculated

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Strategic Importance

</td><td>

Year

</td><td>

Custom Script

</td><td>

Enterprise Architecture product. cmdb\_ci\_business\_app table

</td><td>

Calculated from the **Emergency tier** \(emergency\_tier\) field of the business application record.

</td><td>

Evaluates the emergency tier of the business application.

</td></tr><tr><td>

Data Classification

</td><td>

Year

</td><td>

Custom Script

</td><td>

Enterprise Architecture product. cmdb\_ci\_business\_app table

</td><td>

Calculated from the **Data classification** \(data\_classification\) field of the business application record.

</td><td>

Evaluates data classification of the business application.

</td></tr><tr><td>

Cloud Version Available

</td><td>

Year

</td><td>

Custom Script

</td><td>

Enterprise Architecture product. cmdb\_ci\_business\_app table

</td><td>

Calculated from the **Cloud version available** \(cloud\_version\_available\) field of the business application record.

</td><td>

Evaluates if there is an available version of this application that fits cloud deployment.

</td></tr><tr><td>

Core Architecture

</td><td>

Year

</td><td>

Custom Script

</td><td>

Enterprise Architecture product. cmdb\_ci\_business\_app table

</td><td>

Calculated from the **Core architecture** \(core\_architecture\) field of the business application record.

</td><td>

Evaluates if this business application is part of the core architecture.

</td></tr><tr><td>

Business Criticality

</td><td>

Year

</td><td>

Custom Script

</td><td>

Enterprise Architecture product. cmdb\_ci\_business\_app table

</td><td>

Calculated from the **Business criticality** \(business\_criticality\) field of the business application record.

</td><td>

Evaluates the business criticality of the business application.

</td></tr><tr><td>

Regulatory Implications

</td><td>

Year

</td><td>

Custom Script

</td><td>

Enterprise Architecture product. cmdb\_ci\_business\_app table

</td><td>

Calculated from the **Regulatory implications** \(regulatory\_implications\) field of the business application record.

</td><td>

Evaluates the regulatory implications of the business application.

</td></tr><tr><td>

Business Impact

</td><td>

Year

</td><td>

Indicators

</td><td>

Not applicable

</td><td>

Calculated from the sum of the following indicators:

-   **Core architecture** \(core\_architecture\)
-   **Strategic importance** \(emergency\_tier\)
-   **Business criticality** \(business\_criticality\)

</td><td>

Evaluates the business impact score for the business application, based on other indicators.

</td></tr><tr><td>

Cloud Readiness

</td><td>

Year

</td><td>

Indicators

</td><td>

Not applicable

</td><td>

Calculated from the sum of the following indicators:

-   **Data classification** \(data\_classification\)
-   **Cloud version available** \(cloud\_version\_available\)
-   **Complexity of integration** \(integration\_complexity\)
-   **Regulatory implications** \(regulatory\_implications\)

</td><td>

Evaluates the cloud readiness score for the business application based on other indicators.

</td></tr><tr><td>

Complexity of Integration

</td><td>

Year

</td><td>

Custom Script

</td><td>

Enterprise Architecture product. cmdb\_ci\_business\_app table

</td><td>

Calculated from the **Integration complexity** \(integration\_complexity\) field of the business application record.

</td><td>

Evaluates the complexity of integration to the business application.

</td></tr><tr><td>

User Base

</td><td>

Year

</td><td>

Custom Script

</td><td>

Enterprise Architecture product. cmdb\_ci\_business\_app table

</td><td>

Calculated from the **User base** \(user\_base\) field of the business application record.

</td><td>

Evaluates the user base of the business application.

</td></tr><tr><td>

Cloud Readiness Assessment

</td><td>

Year

</td><td>

Assessments

</td><td>

Enterprise Architecture product. cmdb\_ci\_business\_app table

</td><td>

Calculated from the **Assessment instances** of the business application record.

</td><td>

Evaluates the cloud readiness assessment score \(based on a survey\).

</td></tr></tbody>
</table>**Parent Topic:**[Enterprise Architecture \(formerly Application Portfolio Management\) reference](apm-reference.md)

**Related topics**  


[Enterprise Architecture Cloud Assessment - Legacy](../concept/apm-cloud-readiness-score-prof.md)

