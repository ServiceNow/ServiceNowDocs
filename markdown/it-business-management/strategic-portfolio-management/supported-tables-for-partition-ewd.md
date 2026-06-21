---
title: Supported tables for partition
description: Several tables are supported for partition using Enterprise-Wide Deployment, including direct and indirect related tables for each entity.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-business-management/strategic-portfolio-management/supported-tables-for-partition-ewd.html
release: australia
product: Strategic Portfolio Management
classification: strategic-portfolio-management
topic_type: reference
last_updated: "2026-06-21"
reading_time_minutes: 1
breadcrumb: [Reference, SPM Enterprise-Wide Deployment, Strategic Portfolio Management]
---

# Supported tables for partition

Several tables are supported for partition using Enterprise-Wide Deployment, including direct and indirect related tables for each entity.

The following tables list the tables and their related entities that are supported for segregating data using the partition feature in Enterprise-Wide Deployment.

|Table label|Table ID|
|-----------|--------|
|Project|pm\_project|
|Demand|dmn\_demand|
|Program|pm\_program|
|Portfolio|pm\_portfolio|

|Table ID|Category|Parent partition\(s\)|
|--------|--------|---------------------|
|**Tasks**|
|pm\_project\_task|Task|pm\_project|
|pm\_program\_task|Task|pm\_program|
|dmn\_demand\_task|Task|dmn\_demand|
|**Status**|
|project\_status|Status|pm\_project|
|program\_status|Status|pm\_program|
|**RIDAC and Workflow**|
|risk|RIDAC|pm\_project / dmn\_demand / pm\_program|
|issue|RIDAC|pm\_project / dmn\_demand / pm\_program|
|dmn\_decision|RIDAC|pm\_project / dmn\_demand|
|dmn\_requirement|RIDAC|pm\_project / dmn\_demand|
|project\_change\_request|RIDAC|pm\_project / dmn\_demand|
|project\_action|RIDAC|pm\_project / dmn\_demand|
|ridac\_m2m|RIDAC|pm\_project / dmn\_demand|
|**Stakeholders and Goals**|
|pm\_m2m\_project\_stakeholder|Stakeholder|pm\_project|
|dmn\_m2m\_demand\_stakeholder|Stakeholder|dmn\_demand|
|dmn\_stakeholder\_register|Stakeholder|pm\_portfolio|
|sn\_gf\_goal\_m2m\_relationship|Goal|pm\_project / dmn\_demand / pm\_program|
|**Financial — Plans and Breakdowns**|
|cost\_plan|Financial|pm\_project / dmn\_demand|
|cost\_plan\_breakdown|Financial|pm\_project / dmn\_demand / pm\_program / pm\_portfolio|
|benefit\_plan|Financial|pm\_project / dmn\_demand|
|benefit\_plan\_breakdown|Financial|pm\_project / dmn\_demand / pm\_program / pm\_portfolio|
|nm\_benefit\_plan\_breakdown|Financial|pm\_project / dmn\_demand / pm\_program / pm\_portfolio|
|fm\_expense\_line|Financial|pm\_project / dmn\_demand|
|fm\_expense\_allocation|Financial|pm\_project / dmn\_demand|
|sn\_invst\_pln\_invst\_investment|Financial|pm\_project|
|sn\_invst\_pln\_invst\_budget|Financial|pm\_project \(via investment\)|
|project\_funding|Financial|pm\_project / dmn\_demand / pm\_program / pm\_portfolio|
|**Baselines**|
|planned\_task\_baseline|Baseline|pm\_project|
|planned\_task\_baseline\_item|Baseline|pm\_project|
|pm\_project\_baseline|Baseline|pm\_project|
|project\_funding\_baseline|Baseline|pm\_project|
|cost\_plan\_baseline|Baseline|pm\_project / dmn\_demand|
|cost\_plan\_breakdown\_baseline|Baseline|pm\_project / dmn\_demand|
|benefit\_plan\_baseline|Baseline|pm\_project / dmn\_demand|
|benefit\_plan\_breakdown\_baseline|Baseline|pm\_project / dmn\_demand|
|nm\_benefit\_plan\_breakdown\_baseline|Baseline|pm\_project / dmn\_demand|
|dmn\_demand\_baseline\_header|Baseline|dmn\_demand|
|dmn\_demand\_baseline|Baseline|dmn\_demand|
|sn\_invst\_pln\_invst\_investment\_baseline\_header|Baseline|pm\_project \(via investment\)|
|sn\_invst\_pln\_invst\_investment\_baseline|Baseline|pm\_project \(via investment\)|
|sn\_invst\_pln\_invst\_budget\_baseline|Baseline|pm\_project \(via investment\)|
|**Resource and Capacity**|
|sn\_plng\_att\_core\_resource\_assignment|Resource|pm\_project / dmn\_demand|
|sn\_plng\_att\_core\_cpaam\_effort|Resource|pm\_project / dmn\_demand|
|sn\_plng\_att\_core\_cpaam\_capacity|Resource|pm\_project / dmn\_demand|
|resource\_aggregate\_daily|Resource|pm\_project / dmn\_demand|
|resource\_aggregate\_weekly|Resource|pm\_project / dmn\_demand|
|resource\_aggregate\_monthly|Resource|pm\_project / dmn\_demand|
|**Time and Timesheets**|
|time\_card|Time|pm\_project|
|time\_card\_daily|Time|pm\_project \(via time\_card\)|
|time\_sheet|Time|pm\_project|
|project\_timecard\_exception|Time|pm\_project|
|**Assessments**|
|asmt\_assessment\_instance|Assessment|pm\_project / dmn\_demand|
|asmt\_category\_result|Assessment|pm\_project / dmn\_demand|
|**Strategic Planning Workspace or Portfolio Planning Workspace integration**|
|sn\_align\_core\_planning\_item|Strategic Planning Workspace or Portfolio Planning Workspace|Strategic Planning or Portfolio Planning integration \(partition enforcement applies when internal integration is enabled\)|

**Parent Topic:**[SPM Enterprise-Wide Deployment reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-business-management/strategic-portfolio-management/ewd-reference.md)

