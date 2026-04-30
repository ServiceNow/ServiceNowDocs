---
title: Guidance based recommendations in Recommended Actions for ITSM
description: ITSM base system includes the following guidance based recommendations.
locale: en-US
release: xanadu
product: Service Operations Workspace
classification: service-operations-workspace
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Recommended Actions for ITSM reference, Reference, Service Operations Workspace for ITSM, IT Service Management]
---

# Guidance based recommendations in Recommended Actions for ITSM

ITSM base system includes the following guidance based recommendations.

<table id="table_drv_vtn_cyb"><thead><tr><th>

Recommendation

</th><th>

Description

</th></tr></thead><tbody><tr><td>

AI Search Recommendation

</td><td>

Returns AI-powered recommendations across various records in the Service Operations Workspace, including Incident, Incident task, Problem, Problem task, Change request, Change task, Interaction, and Request.

</td></tr><tr><td>

Create Problem Record for a major incident

</td><td>

Returns guidance-based recommendation.

 Select **Create Problem** action to create a problem record for major incident.

</td></tr><tr><td>

Open incidents \(CI &amp; Service\)

</td><td>

Returns guidance-based recommendations. The open incidents which have matching Configuration item or Service with the current incident record and which were created within the last six months appear. Atmost five recommendations for such type for an incident appear. Select **Make parent** action to make the incident as the parent to the recommended incident.

</td></tr><tr><td>

Open PRBs \(CI &amp; Service\)

</td><td>

Returns guidance-based recommendations. The problems which have matching Configuration item or Service with the current incident record and which were created within last seven days appear. Atmost five recommendations for such type for an incident appear.

 Select **Link to Problem** action- to associate the incident with the recommended problem.

</td></tr><tr><td>

Similar Change Requests \(TI\)

</td><td>

Returns similar change request records as guidance-based recommendations, with up to five suggestions provided. Change requests with matching CI fields are prioritized, followed by those with matching fields. Lastly, change requests linked to open incidents with matching fields are displayed.

</td></tr><tr><td>

Similar Problems \(TI\)

</td><td>

Returns problem records as guidance-based recommendations, with up to five suggestions provided. Problems with similar fields are prioritized, followed by problems associated with open incidents are displayed.

</td></tr><tr><td>

Similar Incidents \(TI\)

</td><td>

Returns guidance-based recommendations. The records with similar fields appear.

</td></tr><tr><td>

Similar KB Articles \(Similarity\)

</td><td>

Returns guidance-based recommendations. Based on the similarity, this returns KB articles as recommendations.

 Select **Attach KB** to attach the KB article to the current incident.

</td></tr><tr><td>

Propose Major Incident \(Trend\)

</td><td>

Returns guidance-based recommendations. Based on the similarity with Trend, this returns incidents as recommendations. Select **Propose as Major Incident** to propose the incident as major incident.

</td></tr><tr><td>

Similar Major Incident \(Trend\)

</td><td>

Returns guidance-based recommendations. Based on the similarity with Trend, this returns major incidents as recommendations.

 Select **Link Major incident as Parent** to link the recommended major incident to the current incident.

 The current incident becomes child of the recommended major incident.

</td></tr><tr><td>

Similar Open Incidents \(Similarity\)

</td><td>

Returns guidance-based recommendations. Based on the similarity, this returns open incidents.

 Select **Link as parent** to link the recommended incident to current incident.

 The current incident becomes child of the recommended open incident.

</td></tr><tr><td>

Similar Open PRBs \(Similarity\)

</td><td>

Returns guidance-based recommendations. Based on the similarity model, this returns open problems.

 Select **Link Problem as Parent** to link the current incident to the recommended open problem.

 The current incident has a problem field, which gets linked to the recommended problem.

</td></tr><tr><td>

Similar Resolved Incidents \(Similarity\)

</td><td>

Returns guidance-based recommendations. Based on the similarity, this returns resolved incidents.

 Select **Copy resolution** to copy the resolution of the resolved recommended incidents to the current incident.

</td></tr><tr><td>

Similar Resolved incidents \(CI &amp; Service\)

</td><td>

Returns guidance-based recommendations. The resolved incidents which have matching Configuration item or Service with the current incident and which were created within the last six months appear. Atmost five recommendations for such type for an incident appear.

 Select **Copy resolution** action to copy the resolution and associate the incident with the recommended resolved incident.

</td></tr></tbody>
</table>**Parent Topic:**[Recommended Actions for ITSM reference](../concept/recommended-actions-for-itsm-reference.md)

