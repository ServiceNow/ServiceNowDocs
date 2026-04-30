---
title: Configure alumni job preferences
description: Set the questions that the alumni can choose to receive tailored job recommendations.
locale: en-US
release: yokohama
product: HR Service Delivery
classification: hr-service-delivery
topic_type: task
last_updated: "2025-11-26"
reading_time_minutes: 1
breadcrumb: [Configure, Alumni Center, HR Service Delivery, Employee Service Management]
---

# Configure alumni job preferences

Set the questions that the alumni can choose to receive tailored job recommendations.

## Before you begin

Role required: sn\_asc.admin

## Procedure

1.  Navigate to **All** &gt; **Tables** &gt; **Alumni job preference configs**.

2.  Select **New**.

3.  In the form, fill in the following details.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the preference.|
    |Active|Make the preference active or in active.|
    |Application|The application where this preference question is displayed. Alumni center in this case.|
    |Domain|The scope of this preference. For example, global.|
    |Display type|The selection type for the preference options. For example, single select or multi select.|
    |Display question|The question that is displayed to the alumni for this preference.|
    |Order|The order in which this question is displayed to the alumni. For example, 1 displays the question as first.|
    |Weight|The weightage for this question. Based on this weightage the jobs are scored and displayed to the alumni. For example, entering 100 for this question has more weight compared to 80 for another question. Any number you enter here is normalized internally.|
    |Field|The options for the preference question are extracted from this field. This field refers to the field values in the Job postings \(sn\_ta\_hiring\_core\_job\_posting\) table.|

4.  Select **Save**.


