---
title: Scoring results
description: After an assessment is completed, scores are calculated and stored based on the scoring configuration defined in the template.
locale: en-US
release: zurich
product: Smart Assessment Engine
classification: smart-assessment-engine
topic_type: concept
last_updated: "2026-02-27"
reading_time_minutes: 1
breadcrumb: [Scoring assessments, Use template designer, Manage, Smart Assessment Engine, Governance, Risk, and Compliance]
---

# Scoring results

After an assessment is completed, scores are calculated and stored based on the scoring configuration defined in the template.

Scoring results are available at multiple levels such as assessment, section, subsection, and question, depending on how scoring was configured in the template. Each level captures a different granularity of the assessment outcome, allowing upstream applications to surface the most relevant scores to end users. The final scores are displayed according to the requirements of the upstream application, providing flexibility in how scores are visualized and presented to end users.

Each section and assessment level has a metric record connected to it through a metric\_mapping record. You can use metric\_mapping to identify the metric associated with each section, and from the associated metric record, locate the corresponding metric\_instance.

Once the scoring is completed, the final scores are available as follows:

-   Question level scores are stored in the question instance \(sn\_smart\_asmt\_question\_instance\) table for individual questions.
-   Section, subsection, and assessment level scores are stored in the \(sn\_smart\_scoring\_metric\_instance\) table.

