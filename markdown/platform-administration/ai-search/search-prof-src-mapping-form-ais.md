---
title: Search Profile - Search Source Mapping form
description: The Search Profile - Search Source Mapping form contains information about relationships between search sources and search profiles in AI Search. Use this form when linking search sources to search profiles.
locale: en-US
release: xanadu
product: AI Search
classification: ai-search
topic_type: reference
last_updated: "2024-10-09"
reading_time_minutes: 1
breadcrumb: [Reference, AI Search, Search administration, Configure core features, Administer the ServiceNow AI Platform]
---

# Search Profile - Search Source Mapping form

The Search Profile - Search Source Mapping form contains information about relationships between search sources and search profiles in AI Search. Use this form when linking search sources to search profiles.

For details on linking search sources to your search profiles, see [Link a search source to a search profile](../task/link-search-source-profile-ais.md).

<table id="table_i1h_y1z_lnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Profile

</td><td>

The search profile that you want to link the search source to. This field is automatically set to the profile that you edited.

</td></tr><tr><td>

Search source

</td><td>

The search source that you want to link to the specified search profile.

</td></tr><tr><td>

Exclude in Regular Search

</td><td>

Option to exclude content from this search source when generating standard search results for searches that use the selected search profile.

</td></tr><tr><td>

Application

</td><td>

Application scope for the search source mapping record. This field is automatically set.

</td></tr><tr><td>

Exclude in Now Assist Genius Results

</td><td>

Option to exclude content from this search source when generating Genius Result answers for searches that use the selected search profile. This option applies to all Genius Results, not just Now Assist Genius Results.

</td></tr><tr><td>

Exclude Attachments in Now Assist Genius Results

</td><td>

Option to exclude attachments from this search source when generating Genius Result answers for searches that use the selected search profile. If **Exclude in Now Assist Genius Results** is not selected, selecting this option has no effect. This option applies to all Genius Results, not just Now Assist Genius Results.**Note:** Selecting this option has no effect on search sources created from external indexed sources \(those that index external content\). It only affects search sources created from internal indexed sources \(those that index content from ServiceNow AI Platform® tables\).

</td></tr></tbody>
</table>**Parent Topic:**[AI Search reference](../concept/reference-ais.md)

