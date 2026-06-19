---
title: Now Assist Data Kit roles \(sn\_data\_kit.admin\)
description: Users with this role can create, update, and publish datasets and data collections in Now Assist Data Kit. This role includes all permissions granted by sn\_data\_kit.analyst.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/intelligent-experiences/now-assist-data-kit/data-kit-admin-role.html
release: australia
product: Now Assist Data Kit
classification: now-assist-data-kit
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Now Assist Data Kit reference, Now Assist Data Kit, Enable AI experiences]
---

# Now Assist Data Kit roles \(sn\_data\_kit.admin\)

Users with this role can create, update, and publish datasets and data collections in Now Assist Data Kit. This role includes all permissions granted by `sn_data_kit.analyst`.

## Contains Roles

List of roles contained within the role.

None.

## Groups

List of groups this role is assigned to by default.

None.

## Special considerations

The `sn_aia.viewer` role \(Now Assist AI Agents viewer\) inherits `sn_data_kit.admin`. As a result, any user assigned `sn_aia.viewer` — for example, to grant read-only access to the AI Agent Analytics dashboard — also receives full Now Assist Data Kit admin permissions. This behavior is unintended and is tracked under PRB2003416. Until the defect is resolved, review the roles assigned to `sn_aia.viewer` users before deploying that role broadly in governance-sensitive environments.

