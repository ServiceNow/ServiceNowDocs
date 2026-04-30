---
title: Cascade rules for cleaning data
description: Cascade rules determine a thorough cleanup of the outdated data and its related counterparts at source from the system.
locale: en-US
release: zurich
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
---

# Cascade rules for cleaning data

Cascade rules determine a thorough cleanup of the outdated data and its related counterparts at source from the system.

|Scenario|Outcome|
|--------|-------|
|A job requisition is deleted.|All the job applications for that job requisition are deleted.|
|A job requisition is deleted.|All the job postings for that job requisition are deleted.|
|A job requisition is deleted.|All the associated records within the hiring team for that job requisition are deleted.|
|A job application is deleted.|All extracted skills associated with the job application are deleted.|
|A job application is deleted.|All the details from the applicant profile are deleted.|

**Parent Topic:**[Modify purge policies to clean up data](../task/set-up-purge-pollicies-ta.md)

