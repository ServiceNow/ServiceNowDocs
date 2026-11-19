---
title: Establishing connection between SPO and the supplier punchout system
description: SPO and the supplier punchout system use PunchoutRequest and PunchoutResponse payloads to establish the connection.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/source-to-pay-operations/sourcing-and-procurement-operations/spo-punchout-connection.html
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Understanding punchout, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Establishing connection between SPO and the supplier punchout system

SPO and the supplier punchout system use PunchoutRequest and PunchoutResponse payloads to establish the connection.

The Punchout system returns a PunchoutResponse, which contains the start URL for the Punchout session. The SPO endpoint parses this response and opens the URL in a new tab. This parsing can be implemented using the XML Parser action step.

**Note:** The PunchoutRequest and PunchoutResponse payloads are expected to follow the same structure across all Punchout systems.

The following figure illustrates the connection flow:

\[Omitted image "punchout-establish-conn.png"\] Alt text: How SPO communicates with a punchout system.

**Parent Topic:**[Understanding punchout](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/source-to-pay-operations/sourcing-and-procurement-operations/punchout-overview.md)

