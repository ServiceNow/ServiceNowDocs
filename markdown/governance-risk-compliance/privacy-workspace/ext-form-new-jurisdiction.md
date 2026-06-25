---
title: Personal Data Rights external facing form location configuration
description: Populate a new location configuration record. Field choices determine whether requesters in the mapped jurisdictions see authorized agent paths, what URLs the form links to, and what introductory text appears at the start of the Personal Data Rights \(PDR\) form.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/governance-risk-compliance/privacy-workspace/ext-form-new-jurisdiction.html
release: australia
product: Privacy Workspace
classification: privacy-workspace
topic_type: reference
last_updated: "2026-05-25"
reading_time_minutes: 2
breadcrumb: [Configure jurisdiction, Configure external-facing PDR form, Configure, Personal Data Rights \(PDR\), Privacy Management, Governance, Risk, and Compliance]
---

# Personal Data Rights external facing form location configuration

Populate a new location configuration record. Field choices determine whether requesters in the mapped jurisdictions see authorized agent paths, what URLs the form links to, and what introductory text appears at the start of the Personal Data Rights \(PDR\) form.

<table id="table_dsf_pt3_jjc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

**Jurisdictions**

</td><td>

Countries, states, or provinces that this location configuration applies to. In most cases, the country alone is enough. For United States and Canada, add both the country and the specific state, because privacy rights vary by state.

</td></tr><tr><td>

**Allow authorized agent**

</td><td>

Option that permits a third party to submit a personal data rights request on behalf of a data subject from this location. When cleared, the form doesn't show the authorized agent option for any requester who selects this jurisdiction.

</td></tr><tr><td>

**Public facing form config**

</td><td>

Reference to the parent external form configuration record. Automatically set to the parent record when you create the location configuration from the parent record.

</td></tr><tr><td>

**Active**

</td><td>

Activation state of the location configuration. You can select this option only after at least one active data subject type is mapped to the location.After mapping an active data subject, return to this record, and select **Active**.

**Note:** To map a data subject type for a jurisdiction, see [Configure the data subject types for a jurisdiction](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-ds-types.md).

</td></tr><tr><td>

**Introduction**

</td><td>

Introductory text, such as a description of the rights available in that jurisdiction, disclaimers, or information about personal data rights, shown on the first page of the form after a requester selects their location.

</td></tr><tr><td>

**Privacy statement URL**

</td><td>

Location-specific URL to the privacy statement of your organization. If you leave this field empty, the form uses the URL set on the parent external form configuration record.

</td></tr><tr><td>

**Legal terms URL**

</td><td>

Location-specific URL to the legal terms of your organization. If you leave this field empty, the form uses the URL set on the parent external form configuration record.

</td></tr><tr><td>

**Terms of service URL**

</td><td>

Location-specific URL to the terms of service of your organization. If you leave this field empty, the form uses the URL set on the parent external form configuration record.

</td></tr></tbody>
</table>**Parent Topic:**[Configure jurisdictions for the external-facing Personal Data Rights form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-location.md)

**Related topics**  


[Configure jurisdictions for the external-facing Personal Data Rights form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/config-pdr-location.md)

[Personal Data Rights \(PDR\) external-facing form](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/governance-risk-compliance/privacy-workspace/pdr-external-facing.md)

