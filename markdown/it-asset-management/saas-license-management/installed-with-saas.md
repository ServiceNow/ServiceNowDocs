---
title: Installed with SaaS License Management
description: User roles and tables are installed with SaaS License Management. Demo data is available for the Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) plugin.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Request SaaS License Management, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Installed with SaaS License Management

User roles and tables are installed with SaaS License Management. Demo data is available for the Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) plugin.

## User roles

|Role|Description|
|----|-----------|
|sam\_integrator|Inherits the sam\_user role and can also create and manage SaaS integration profiles.|

## Tables

|Table|Description|
|-----|-----------|
|Custom Subscription Product Definitions \[samp\_sw\_custom\_subscription\_product\_definition\]|Enables you to create and update customized software models for SaaS and SSO applications.|
|Custom Subscription Integration \[samp\_sw\_custom\_subscription\_integration\]|List of SaaS and SSO providers for your custom integration profiles.|
|Product profile types \[samp\_sw\_product\_profile\_type\]|Provides a mapping between integration profile types and products in the Software Product \[samp\_sw\_product\] table.|
|SAM Subscription Script Routes \[sam\_saas\_script\_route\]|Stores which script includes and scopes implement a given integration type to register available integrations from separate scoped apps.|
|SSO Application \[samp\_sso\_application\]|List of all SSO applications for all SSO integrations.|
|SSO Application Groups \[m2m\_sso\_group\_application\]|Provides a mapping between connected SSO applications and the directory groups that have access to them.|
|SSO Application Role \[samp\_sso\_application\_role\]|List of SSO users and groups for all connected SSO applications.|
|SSO Application Users \[m2m\_sso\_user\_application\]|Provides a mapping between connected SSO applications and the directory users that have access to them.|
|SSO Integration Profile \[samp\_sso\_integration\_profile\]|List of all SSO integration profiles.|
|SSO Subscription \[samp\_sso\_subscription\]|List of SSO subscriptions for all connected SSO applications.|
|Subscription Consumption Summaries \[sam\_saas\_consumption\_summary\]|Consumption summary information including units consumed, monthly consumption, and contract dates.|
|Subscription Integration \[samp\_sw\_subscription\_integration\]|List of SaaS and SSO providers that is mapped to subscription products in the Subscription Product Definition \[samp\_sw\_subscription\_product\_definition\] table.|
|Subscription Product Definitions \[samp\_sw\_subscription\_product\_definition\]|SaaS License Management uses this table to automatically create software models for SaaS and SSO applications. Software models are automatically created for applications with an **External Catalog ID** that matches an **Identifier** in this table.|
|Subscription Usage Summary \[samp\_subscription\_usage\_summary\]|Software usage summary information including rights owned, rights assigned, stale rights, available rights, and cost.|
|Unrecognized Subscription Identifiers \[samp\_sw\_unrecognized\_subscription\_identifier\]|List of subscription identifiers that are not associated with a software model.|

**Parent Topic:**[Request SaaS License Management](../task/request-saas-license-management.md)

