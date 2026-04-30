---
title: Guardrails for PDF generation and accessibility
description: Static and dynamic guardrails are safeguards that help maintain stability during PDF generation. Static guardrails enforce fixed limits like maximum PDF size, while dynamic guardrails monitor real-time memory usage and terminate exports when memory pressure exceeds a defined threshold.
locale: en-US
release: zurich
product: Document Management Services
classification: document-management-services
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [PDF generation and accessibility, Document Services, Manage content capabilities, Extend ServiceNow AI Platform capabilities]
---

# Guardrails for PDF generation and accessibility

Static and dynamic guardrails are safeguards that help maintain stability during PDF generation. Static guardrails enforce fixed limits like maximum PDF size, while dynamic guardrails monitor real-time memory usage and terminate exports when memory pressure exceeds a defined threshold.

## Static guardrail for PDF generation and accessibility

A static guardrail helps prevent instance instability during PDF generation. If the size of a generated PDF exceeds a maximum threshold the export process is automatically terminated to help prevent large PDF exports from consuming excessive memory.

The system property **com.snc.pdf.generation.maxsize\_mb** limits the generated PDF size in MB. The default maximum PDF size is 30MB.

**Note:** If the value is increased might create memory pressure on the instance to generate the PDF and the node may crash

.

## Dynamic guardrail for PDF generation and accessibility

A dynamic guardrail helps prevent instability in PDF generation by monitoring and responding to excessive memory consumption. Dynamic guardrails are triggered only when certain memory usage thresholds are crossed during PDF generation.

The dynamic guardrail can be enabled for PDF generation by adding system properties. When enabled, the system continuously monitors the node's memory usage.

To enable accessibility for PDF generation, in the navigation filter, enter sys\_properties.list, and add the following properties:

-   **__glide.robustness.memory\_guard\_enabled__**

    When set to `true`, this enables the dynamic guardrails for PDF generation and accessibility

    -   Type: true \| false
    -   Default Value: false
-   **__glide.robustness.memory\_guard\_thresholdpercentage__**
    -   Type: integer
    -   Default Value: 90
    -   Minimum threshold percentage = 1
    -   Maximum threshold percentage = 100
-   **__glide.robustness.memory\_guard\_time__**
    -   Type: integer
    -   Default Value: 60
    -   Minimum memory guard time = 1
    -   Maximum memory guard time = 900

If the memory usage reaches the configured value \(default value is 90%\) for the system property, the platform automatically terminates the ongoing PDF export and new PDF export requests are rejected. The guardrail continues to block PDF exports until the memory usage drops below the safe threshold.

**Parent Topic:**[PDF generation and accessibility](pdf-generation-accessibility.md)

