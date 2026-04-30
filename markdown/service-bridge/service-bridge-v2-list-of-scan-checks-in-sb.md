---
title: List of scan checks
description: Multiple scan checks are available in Service Exchange to help you identify issues and system inconsistencies, enabling you to maintain system health and reduce downtime.
locale: en-US
release: zurich
product: Service Bridge
classification: service-bridge
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Reference, Service Exchange]
---

# List of scan checks

Multiple scan checks are available in Service Exchange to help you identify issues and system inconsistencies, enabling you to maintain system health and reduce downtime.

|Check|Description|Suite|Check Type|Execution Type|
|-----|-----------|-----|----------|--------------|
|\[PRO\] All dependent apps installation versions are correct|Dependent application's installation versions are incorrect|Service Exchange Post-Clone, Post-Upgrade, Pre-Onboarding, Connection Health|PRO|On-Demand, Scheduled|
|\[PRO\] Check Entitlement Consumer Active Revision is 0|Entitlement was not activated by consumer|Service Exchange Entitlements, Post-Clone, Post-Upgrade, Post-Onboarding|PRO|On-Demand, Scheduled|
|\[PRO\] Checking Entitlements Stuck in Pending|Entitlement in "pending" state longer than expected|Service Exchange Entitlements, Post-Clone, Post-Upgrade, Post-Onboarding|PRO|On-Demand, Scheduled|
|\[PRO\] Connection status is not active or valid|Consumer Connection status isn’t active or valid|Service Exchange Connection Health|PRO|Scheduled|
|\[PRO\] Entitlement with invalid entity reference|Entitlement doesn’t reference a valid entity|Service Exchange Entitlements, Post-Clone, Post-Upgrade, Post-Onboarding|PRO|On-Demand, Scheduled|
|\[PRO\] Entitlement with invalid identity reference|Entitlement doesn’t reference a valid identity|Service Exchange Post-Upgrade, Post-Onboarding, Post-Clone|PRO|On-Demand|
|\[PRO\] Entitlements missing connection|Entitlement doesn’t reference a consumer connection|Service Exchange Entitlements, Post-Onboarding, Post-Upgrade, Post-Clone|PRO|On-Demand, Scheduled|
|\[PRO\] Integration user name does not start with sb\_user|Integration user name doesn’t start with "sb\_user."|Service Exchange Post-Clone, Post-Onboarding|PRO|On-Demand|
|\[PRO\] Magic Links is not configured|Magic Links is not correctly configured|Service Exchange Magic Links Configurations|PRO|Scheduled|
|\[PRO\] Magic Links is not fully enabled|Magic Links is not fully enabled|Service Exchange Magic Links Configurations|PRO|Scheduled|
|\[PRO\] Process Sync Definition configuration is valid|Service Exchange connections' RPS Process Sync Definition is missing|Service Exchange Connection Health, Post-Clone, Pre-Onboarding|PRO|On-Demand, Scheduled|
|\[PRO\] Provider \(sn\_sb\_pro\_provider\) is missing|Provider \(sn\_sb\_pro\_provider\) is missing|Service Exchange Pre-Onboarding|PRO|On-Demand|
| | | | | |
| | | | | |
|\[PRO\] Provider Task parent domain mismatch|Provider Task domain doesn’t match parent task domain|Service Exchange Post-Clone, Provider Task Configurations|PRO|On-Demand, Scheduled|
|\[PRO\] Provider task missing Connection reference|Provider Task doesn’t reference a consumer connection|Service Exchange Post-Clone, Post-Upgrade, Provider Task Configurations|PRO|On-Demand, Scheduled|
|\[PRO\] Provider task missing Parent reference|Provider Task doesn’t reference a parent task|Service Exchange Post-Upgrade, Provider Task Configurations, Post-Clone|PRO|On-Demand, Scheduled|
|\[PRO\] RRP consumer criteria matches no consumers|No consumers are being entitled to published Remote Record Producer|Service Exchange Remote Record Producer Configurations|PRO|Scheduled|
|\[PRO\] RTD consumer criteria matches no consumers|No consumers are being entitled to published Remote Task Definition|Service Exchange Remote Task Definition Configurations|PRO|Scheduled|
|\[PRO\] Remote Record Producer is invalid|Remote Record Producer doesn’t reference a valid identity|Service Exchange Remote Record Producer Configurations|PRO|Scheduled|
|\[PRO\] Remote Task Definition is invalid|Remote Task Definition has one or more issues|Service Exchange Remote Task Definition Configurations|PRO|Scheduled|
|\[PRO\] Remote choice definition is missing or unpublished|Remote Catalog Variable references a missing or unpublished remote choice definition|Service Exchange Post-Clone, Remote Record Producer Configurations|PRO|On-Demand, Scheduled|
|\[PRO\] Remote choice dependent variable is invalid|Remote Choice variable is referencing an invalid or missing dependency|Service Exchange Remote Record Producer Configurations|PRO|Scheduled|
|\[PRO\] Remote task domain matching parent task domain|Remote Task domain doesn’t match parent task domain|Service Exchange Post-Clone, Remote Task Configurations|PRO|On-Demand, Scheduled|
|\[PRO\] Remote task missing Connection reference|Remote task doesn’t reference a connection|Service Exchange Remote Task Configurations, Post-Clone, Post-Upgrade|PRO|On-Demand, Scheduled|
|\[PRO\] Remote task missing Parent reference|Remote task doesn’t reference a parent task|Service Exchange Post-Clone, Post-Upgrade, Remote Task Configurations|PRO|On-Demand, Scheduled|
|\[PRO\] Settings synced with Provider and Consumer version available|Service Exchange Settings is missing or invalid|Service Exchange Connection Health, Post-Onboarding|PRO|On-Demand, Scheduled|
|\[PRO\] Stale Consumer Connection records|Stale \(unused\) Consumer Connection records|Service Exchange Post-Clone, Pre-Onboarding, Base Configurations|PRO|On-Demand, Scheduled|
|\[PRO\] Stale OAuth registry records|Stale \(unused\) OAuth registry record|Service Exchange Base Configurations, Pre-Onboarding, Post-Clone|PRO|On-Demand, Scheduled|
|\[PRO\] Stale Service Exchange service account records from onboarding retries|Stale \(Unused\) Service Exchange integration user|Service Exchange Pre-Onboarding, Post-Clone|PRO|On-Demand|
|\[CON\] All dependent apps installation versions are correct|Dependent applications installation versions are incorrect|Service Exchange Post-Clone, Post-Upgrade, Pre-Onboarding, Connection Health|CON|On-Demand, Scheduled|
|\[CON\] Check Entitlement Consumer Active Revision is 0|Entitlement hasn’t been activated by the consumer|Service Exchange Entitlements, Post-Onboarding, Post-Upgrade, Post-Clone|CON|On-Demand, Scheduled|
|\[CON\] Connection status is not active or valid|Provider Connection status isn’t active or valid|Service Exchange Connection Health|CON|Scheduled|
|\[CON\] Entitlement with invalid entity reference|Entitlement doesn’t reference a valid entity|Service Exchange Entitlements, Post-Onboarding, Post-Upgrade, Post-Clone|CON|On-Demand, Scheduled|
|\[CON\] Entitlement with invalid identity reference|Entitlements does not reference a valid identity|Service Exchange Entitlements, Post-Onboarding, Post-Upgrade, Post-Clone|CON|On-Demand, Scheduled|
|\[CON\] Entitlements missing connection|Entitlement does not reference a provider connection|Service Exchange Entitlements, Post-Onboarding, Post-Upgrade, Post-Clone|CON|On-Demand, Scheduled|
|\[CON\] Inbound RRP Timed Out|Remote Record Producer did not finish building Variables and UI Policies|Service Exchange Remote Record Producer Configurations|CON|Scheduled|
|\[CON\] Integration user name does not start with sb\_user|Integration user name does not start with "sb\_user."|Service Exchange Post-Clone, Post-Onboarding|CON|On-Demand|
|\[CON\] Process Sync Definition configuration is valid|Service Exchange Consumer RPS Process Sync Definition is missing|Service Exchange Pre-Onboarding, Connection Health, Post-Clone|CON|On-Demand, Scheduled|
|\[CON\] Provider services catalog category missing|The Provider Services category is missing|Service Exchange Remote Record Producer Configurations|CON|Scheduled|
|\[CON\] Provider Task parent domain mismatch|Provider Task domain does not match its parent task domain|Service Exchange Provider Task Configurations, Post-Clone|CON|On-Demand, Scheduled|
|\[CON\] Provider task missing Connection reference|Provider Task does not reference a provider connection|Service Exchange Provider Task Configurations, Post-Clone, Post-Upgrade|CON|On-Demand, Scheduled|
|\[CON\] Remote Record Producer is invalid|Remote Record Producer is missing identity or entitlement|Service Exchange Remote Record Producer Configurations|CON|Scheduled|
|\[CON\] Remote Task Definition is invalid|Remote Task Definition has one or more issues|Service Exchange Remote Task Definition Configurations|CON|Scheduled|
|\[CON\] Remote task domain matching parent task domain|Remote task domain does not match its parent task domain|Service Exchange Remote Task Configurations, Post-Clone|CON|On-Demand, Scheduled|
| | | | | |
| | | | | |
|\[CON\] Remote task missing Connection reference|Remote task does not reference a Connection|Service Exchange Post-Clone, Post-Upgrade, Remote Task Configurations|CON|On-Demand, Scheduled|
|\[CON\] Remote task missing Parent reference|Remote task does not have reference to a parent task|Service Exchange Post-Upgrade, Post-Clone, Remote Task Configurations|CON|On-Demand, Scheduled|
|\[CON\] Settings synced with Provider and Consumer version available|Service Exchange Settings is not valid|Service Exchange Post-Onboarding, Connection Health|CON|On-Demand, Scheduled|
|\[CON\] Stale OAuth registry records|Stale \(Unused\) OAuth registry record|Service Exchange Base Configurations, Pre-Onboarding, Post-Clone|CON|On-Demand, Scheduled|
|\[CON\] Stale Provider Connection records|Stale \(Unused\) Provider Connection record|Service Exchange Base Configurations, Pre-Onboarding, Post-Clone|CON|On-Demand, Scheduled|
|\[CON\] Stale Service Exchange service account records from onboarding retries|Stale \(Unused\) Service Exchange integration user records|Service Exchange Pre-Onboarding, Post-Upgrade, Post-Clone|CON|On-Demand|
|\[PRO\]\[CON\] Attachment is too large|Attachment size is unsupported|Service Exchange Attachment Handling, Performance|Both|Scheduled|
|\[PRO\]\[CON\] Attachments are very large|Large, performance degrading attachments found|Service Exchange Attachment Handling|Both|Scheduled|
|\[PRO\]\[CON\] Capture Definitions state is invalid|Required RPS connection Capture Definitions are missing|Service Exchange Connection Health, Post-Clone|Both|On-Demand, Scheduled|
|\[PRO\]\[CON\] Global script include version check|Global Service Exchange script include needs updating|Service Exchange Post-Clone, Post-Upgrade, Pre-Onboarding, Base Configurations|Both|On-Demand, Scheduled|
|\[PRO\]\[CON\] KMF is unhealthy|KMF Key Management is not healthy|Service Exchange Pre-Onboarding, Post-Clone, Post-Upgrade|Both|On-Demand|
|\[PRO\]\[CON\] Large number of attachments|Unusally large number of attachments|Service Exchange Performance, Attachment Handling|Both|Scheduled|
|\[PRO\]\[CON\] OAuth crypto module access policy check|OAuth crypto module has incorrect access policy|Service Exchange Pre-Onboarding|Both|On-Demand|
|\[PRO\]\[CON\] Provider and Consumer app versions are same on the instance|Service Exchange Provider and Consumer app installed versions are not matching|Service Exchange Pre-Onboarding, Base Configurations, Post-Upgrade, Post-Clone|Both|On-Demand, Scheduled|
|\[PRO\]\[CON\] Remote System Inbound and Outbound state is valid|Connection's RPS Remote System not in active state|Service Exchange Post-Clone, Connection Health|Both|On-Demand, Scheduled|
|\[PRO\]\[CON\] Skipped files listed in Upgrade History|Skipped files are present in Upgrade History|Service Exchange Post-Upgrade|Both|On-Demand|
|\[PRO\]\[CON\] Transport inbound queue processing is slow|Some inbound records are taking abnormally long to process|Service Exchange Base Configurations|Both|Scheduled|
|\[PRO\]\[CON\] Transport System user domain and user\_id is not modified|The sn\_transport\_system user's domain or user\_id was modified|Service Exchange Connection Health|Both|Scheduled|
|\[PRO\]\[CON\] User Not Authenticated error with RPS|OAuth Client tokens have expired \("User Not Authenticated"\)|Service Exchange Base Configurations|Both|Scheduled|
|\[PRO\]\[CON\] glide.servlet.uri is empty|System property "glide.servlet.uri" is empty|Service Exchange Pre-Onboarding|Both|On-Demand|

**Parent Topic:**[Service Exchange reference](service-bridge-v2-reference.md)

