---
title: Installed with approval with e-signature
description: Installing approval with e-signature installs certain properties.
locale: en-US
release: australia
product: Approvals
classification: approvals
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Approval with e-signature, Classic approvals, Build workflows]
---

# Installed with approval with e-signature

Installing approval with e-signature installs certain properties.

-   Module - E-Signature Registry
-   UI Action - Approve \(on table sysapproval\_approver, with no action name\)
-   UI Action - Approve \(on table sysapproval\_approver, with no action name\)
-   UI Action - Approve \(on table sysapproval\_approver, with the action name authenticated\_list\_approval\)
-   UI Page - form\_login\_validate\_dialog
-   UI Page - login\_validate\_dialog
-   UI page: saml2\_esignature\_login, the re-authentication page that appears when an approver tries to approve a request.
-   Properties: see E-signature SAML properties
-   Client Script - Authenticate Approver
-   Script Include - User
-   Script Include - UserAuthentication
-   Processor: eSigSaml2AssertionConsumer

Installing the plugin also disables the two out-of-the-box Approve UI Actions on the `sysapproval_approver` table.

