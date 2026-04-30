---
title: Configure HR Service Delivery Integration with SuccessFactors properties
description: System properties control system behavior. The integrations source properties can be used to configure the HR Service Delivery Integration with SuccessFactors. You can access system properties for HR Service Delivery Integration with SuccessFactors by navigating to All &gt; HRSD SuccessFactors Integration &gt; System Properties. These system properties are only applicable for HR Service Delivery Integration with SuccessFactors and cannot be leveraged with SuccessFactors spoke.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Configuring HR Service Delivery Integration with SuccessFactors, HR Service Delivery Integration with SuccessFactors, Integration of HR Service Delivery with third-party systems, HR Service Delivery, Employee Service Management]
---

# Configure HR Service Delivery Integration with SuccessFactors properties

System properties control system behavior. The integrations source properties can be used to configure the HR Service Delivery Integration with SuccessFactors. You can access system properties for HR Service Delivery Integration with SuccessFactors by navigating to All &gt; HRSD SuccessFactors Integration &gt; System Properties. These system properties are only applicable for HR Service Delivery Integration with SuccessFactors and cannot be leveraged with SuccessFactors spoke.

|Field|Description|
|-----|-----------|
|sn\_hr\_sf.Retrieve Departments Service \(Retrieve Departments Service subflow\)|Makes retrieve departments service subflow customer configurable.|
|sn\_hr\_sf.Retrieve Effective Workers Service|Makes retrieve effective workers subflow customer configurable.|
|sn\_hr\_sf.Retrieve Job Profiles Service|Makes retrieve job profiles subflow customer configurable.|
|sn\_hr\_sf.Retrieve Jobs Service|Makes retrieve jobs service subflow customer configurable.|
|sn\_hr\_sf.Retrieve Locations Service|Makes retrieve locations service subflow customer configurable.|
|sn\_hr\_sf.Retrieve Todos Service|Makes retrieve todo service subflow customer configurable.|
|sn\_hr\_sf.Retrieve Workers Service|Makes retrieve workers serice subflow customer configurable.|

**Note:** These system properties are only applicable for HR Service Delivery Integration with SuccessFactors and cannot be leveraged with SuccessFactors spoke. Ensure that the property is set to use the OOB sub-flow exclusively. If you've introduced any new sub-flows, verify that they are compatible with HR use cases before updating the property value.

