---
title: Configuring field visibility in the Create questionnaire modal
description: The Create questionnaire modal supports dynamic field visibility based on page parameters. When specific parameters are passed to the page, certain fields are automatically hidden.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/retail-industry/retail-operations/rahi-retail-configuring-field-visibility-questionnaire-modal.html
release: australia
product: Retail Operations
classification: retail-operations
topic_type: concept
last_updated: "2026-06-05"
reading_time_minutes: 1
breadcrumb: [Configure, Retail]
---

# Configuring field visibility in the Create questionnaire modal

The Create questionnaire modal supports dynamic field visibility based on page parameters. When specific parameters are passed to the page, certain fields are automatically hidden.

The modal checks for two page parameters at load time:

-   `assessmentTarget`
-   `assessmentTemplateCategory`

If both parameters are present, the following fields are hidden in the modal:

-   Purpose
-   Assessment target

If the parameters are absent, both fields display as usual, allowing users to set values manually.

Use this behavior when launching the modal from a context where the assessment target and template category are already known — for example, from a record page or a guided workflow that pre-populates these values. Hiding the fields reduces redundancy and streamlines the questionnaire creation experience.

