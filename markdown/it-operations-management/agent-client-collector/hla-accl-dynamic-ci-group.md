---
title: CI association to a dynamic CI Group in Agent Client Collector Log Analytics
description: When the Agent Client Collector Log Analytics \(ACC-L\) application discovers a CI that is not associated to an application service, the application creates a dynamic CI Group and associates the CI to it.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Agent Client Collector Log Analytics, Agent Client Collector, IT Operations Management]
---

# CI association to a dynamic CI Group in Agent Client Collector Log Analytics

When the Agent Client Collector Log Analytics \(ACC-L\) application discovers a CI that is not associated to an application service, the application creates a dynamic CI Group and associates the CI to it.

A dynamic CI Group is a group of CIs that are organized by attribute, such as the CI type. By default, Agent Client Collector log policy checks monitor only CIs that are associated to an application service. The Agent Client Collector Log Analytics application inspects the CIs that the Agent Client Collector discovers. When it discovers a CI that is not associated to an application service, the application creates a dynamic CI Group and associates the CI to it.

If the CI is later associated to an actual application service, its association to the dynamic CI Group is automatically deleted. The baseline for the CI is lost in this process. While the system is establishing the new baseline, it doesn't issue alerts for the application service to which the CI is now associated.

You can choose to disable the association of unassociated CIs to a dynamic CI group by changing the default setting of the relevant system property, **sn\_accl.dynamic\_service.creation.enabled**, to false. The Agent Client Collector Log Analytics application will then not associate unassociated CIs to dynamic CI Groups. In this case, logs are not streamed for CIs that are not associated to an application service.

