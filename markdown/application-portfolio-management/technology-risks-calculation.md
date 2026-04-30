---
title: Technology risk calculation
description: Assess the technology risks of your business applications by calculating their risks at the software product \(considering the model and full version\) level and then at the business application level.
locale: en-US
release: xanadu
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Explore, Enterprise Architecture \(formerly Application Portfolio Management\), Enterprise Architecture \(formerly Application Portfolio Management\)]
---

# Technology risk calculation

Assess the technology risks of your business applications by calculating their risks at the software product \(considering the model and full version\) level and then at the business application level.

**Important:**

Starting with the Xanadu release, the legacy Technology Portfolio Management module is moved to the Enterprise Architecture Workspace. To learn more, see [Managing the Technology Portfolio Management \(TPM\) in Enterprise Architecture Workspace](eaw-concept/eaw-tpm.md).

Technology risks are calculated at the hardware model and software product \(considering the model and full version\) levels to determine the risk at the business application level.

## Lifecycle stage - Internal and External

The range set for a risk value at each level such as very high, late, moderate, low, and none vary from one organization to another. You can set the risk value for each lifecycle phase based on your organizational requirements. Use the software product lifecycle form to associate the lifecycle phase for each software model with a risk. Based on the selected risk the parameter risk is determined.

The risk values in the lifecycle table are very high, high, moderate, low, and none. Accordingly the risk is also very high, high, moderate, low, or none.

For lifecycle stage parameters, only the risk value is considered irrespective of the lifecycle phase.

## Aging - Internal and External

Similarly, the aging internal and external has the following risk values:

-   0–90 days is high risk.
-   90–180 days is moderate risk.
-   More than 180 days is low risk.

Based on the internal and publisher lifecycle stages and the internal and publisher aging stages, the risk of the hardware and software models are calculated as follows:

-   If there is a single High risk, then the risk of the software model is High.
-   If there is a single Moderate risk, then the risk of the software model is Moderate.
-   The risk of the software model is Low only if the risk of all the underlying components are Low.
-   If there is a single High risk, then the risk of the hardware model is High.
-   If there is a single Moderate risk, then the risk of the hardware model is Moderate.
-   The risk of the hardware model is Low only if the risk of all the underlying components are Low.

**Note:** The engine first calculates the risk at the hardware and software models, it then calculates risk at the application service level, based on the risks of all the underlying hardware and software models. Finally it calculates the risk at the business application level based on the risk of the production instances which are nothing but production application service.

The risk calculation for aging parameters are scripted and you can edit as required.

## Parameters to determine software product risk

![An example showing how parameters are used in calculating risk at the software model level](../image/RiskEngineBusAppSW_v2.png "Parameters to determine risk at software model level")

Risk on a software model is calculated based on four parameters, namely internal lifecycle stage, external lifecycle stage, internal aging, and external aging.

## Parameters to determine hardware model risk

![Illustration showing how parameters are used in calculating risk at hardware model level](../image/RiskEngineBusAppHW.png "Parameters to determine risk at hardware model level")

Risk on a hardware model is calculated based on four parameters. The parameters are internal stage risk, publisher stage risk, internal aging risk, and publisher aging risk.

## Calculating technology risk at business application level

A business application can run on many software models. The risk of a business application due to its underlying software models is derived from the risk of the individual software models.

![Calculating technology risk at the business application level](../image/RiskEngineBusApp.png "Calculating risk at the business application level")

-   **Risk at hardware model level**

    Based on the four hardware risk parameters, the technology model suggestion engine calculates the risk of the hardware model and the highest risk value is assigned to the hardware model. If the risk of hardware is high, then the risk of the application service, which runs on the hardware, is evaluated to be high. The engine stores the risk data of the hardware model in the Hardware Model Risks \[sn\_apm\_tpm\_hardware\_model\_risk\] table.

-   **Risk at software model level**

    Based on the four software risk parameters, the technology model suggestion engine calculates the risk of the software model. If the risk of software is high, then the risk of the application service, which runs on the software, is evaluated to be high. The engine stores the risk data of the software model in the Software Model Risks \[sn\_apm\_tpm\_software\_model\_risk\] table. This data is rendered on the software model timeline.

-   **Risk at application service level**

    If any of the hardware or software models on which the application service runs is evaluated to be on high risk, then the application service is determined to be at a high risk.

-   **Risk at business application level**

    If the application service is of high risk, then the business application which runs on the application service is also high.


-   If one of the software models is at High risk, then the business application is at High risk.
-   If one of the software models is at Medium risk, then the business application is at Medium risk.
-   The risk of the business application is Low only if all the underlying software models have a Low risk.
-   If one of the hardware models is at High risk, then the business application is at High risk.
-   If one of the hardware models is at Medium risk, then the business application is at Medium risk.
-   The risk of the business application is Low only if all the underlying hardware models have a Low risk.

You can customize the script that is executed to calculate the risks at the product model risk level \(hardware and software models\), application service risk level, and business application risk level. For more information, see [Configure risk bubble up logic](../task/configure-risk-bubble.md).

**Related topics**  


[Configure script to customize risk calculation](../task/configure-risk-bubble.md)

[Run scheduled job to generate risk values](../task/run-scheduled-job-to-calculate-risks.md)

