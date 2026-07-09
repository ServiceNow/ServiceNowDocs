---
title: EMR Provider Directory Sync and domain separation
description: EMR Provider Directory Sync does not support domain separation.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/healthcare-life-sciences/hco-fhir-domain-separation.html
release: australia
topic_type: reference
last_updated: "2026-06-30"
reading_time_minutes: 1
keywords: [domain separation, EMR Provider Directory Sync]
breadcrumb: [EMR Provider Directory Sync, Healthcare Integrations, Healthcare and Life Sciences]
---

# EMR Provider Directory Sync and domain separation

EMR Provider Directory Sync does not support domain separation.

EMR Provider Directory Sync does not support domain separation. The application operates in the global domain and writes all imported FHIR data to the global domain. Instances with domain separation enabled should be aware that imported organization, location, and practitioner records are created in the global domain and are visible to all domains.

For more information about domain separation in ServiceNow, see .

