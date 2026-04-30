---
title: Name suggestions for application service candidates
description: Automated Service Suggestions provides meaningful name suggestions for service identification, which you can access on the Application Service Suggestions tab in the Service Mapping workspace.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Service Mapping reference, Service Mapping, ITOM Visibility, IT Operations Management]
---

# Name suggestions for application service candidates

Automated Service Suggestions provides meaningful name suggestions for service identification, which you can access on the **Application Service Suggestions** tab in the Service Mapping workspace.

<table id="table_tkd_rjd_gxb"><thead><tr><th>

Name suggestion

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Candidate name suggestion

</td><td>

The primary candidate name suggestion prioritizes the Service Fingerprints name, then defers to other name suggestions as needed.

</td></tr><tr><td>

Service Fingerprint

</td><td>

Name suggestions taken from a maximum of three Service Fingerprints related to the candidate.

</td></tr><tr><td>

Load balancer

</td><td>

Name suggestions taken from the names of the top three load balancer services associated with the candidate.

</td></tr><tr><td>

Process

</td><td>

Name suggestions taken from the process entry point command lines for the candidate. An algorithm identifies the most relevant words and provides the top three name suggestions.

</td></tr><tr><td>

Entry point

</td><td>

Name suggestions taken from all the entry point IP addresses associated with the candidate.Entry point name suggestions is deprecated beginning with version 1.12.3. This column is still displayed but is no longer populated with data. It will eventually be removed.

</td></tr><tr><td>

AFP \(Application fingerprint\)

</td><td>

Name suggestions taken from the top three application fingerprints associated with the candidate.

</td></tr></tbody>
</table>**Parent Topic:**[Service Mapping reference](service-mapping-reference.md)

**Related topics**  


[Automated Service Suggestions](../concept/auto-serv-suggest.md)

[Map application services based on Automated Service Suggestions](../task/map-application-suggestion.md)

