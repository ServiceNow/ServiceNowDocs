---
title: Predictive Intelligence roles
description: Predictive Intelligence is installed with these roles.Can create, read, write or delete the ml\_predictor\_results table and the ml\_predictor\_results\_task table.Can create, read, write or delete the ml\_label\_candidate table.Can read the ml\_predictor\_results table and the ml\_predictor\_results\_task table.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Predictive Intelligence references, Predictive Intelligence, Enable AI experiences]
---

# Predictive Intelligence roles

Predictive Intelligence is installed with these roles.

To learn more about managing per-user subscriptions, see Managing per-user subscriptions in Subscription Management and contact your account representative.

**Parent Topic:**[Predictive Intelligence references](reference-predictive-intelligence.md)

**Related topics**  


[Domain separation and Predictive Intelligence](../concept/domain-separation-predictive-intelligence.md)

[Data Encryption in Predictive Intelligence](predictive-intelligence-encryption.md)

[Predictive Intelligence language support](../concept/predictive-intelligence-localization.md)

[Predictive Intelligence properties](predictive-intelligence-properties.md)

## ML Admin \[ml\_admin\]

Can create, read, write or delete the ml\_predictor\_results table and the ml\_predictor\_results\_task table.

### Contains Roles

List of roles contained within the role.

-   pa\_data\_collector
-   pa\_viewer

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

Avoid granting an admin role when more specialized roles are available.

## ML Labeler \[ml\_labeler\]

Can create, read, write or delete the ml\_label\_candidate table.

### Contains Roles

List of roles contained within the role.

-   sn\_ace.ace\_user
-   nlu\_user

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

## ML Report User \[ml\_report\_user\]

Can read the ml\_predictor\_results table and the ml\_predictor\_results\_task table.

### Contains Roles

List of roles contained within the role.

pa\_viewer

### Groups

List of groups this role is assigned to by default.

None.

### Special considerations

None.

