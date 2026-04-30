---
title: Establishing connection between SPO and the supplier punchout system
description: SPO and the supplier punchout system use PunchoutRequest and PunchoutResponse payloads to establish the connection.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Understanding punchout, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Establishing connection between SPO and the supplier punchout system

SPO and the supplier punchout system use PunchoutRequest and PunchoutResponse payloads to establish the connection.

The Punchout system returns a PunchoutResponse, which contains the start URL for the Punchout session. The SPO endpoint parses this response and opens the URL in a new tab. This parsing can be implemented using the XML Parser action step.

**Note:** The PunchoutRequest and PunchoutResponse payloads are expected to follow the same structure across all Punchout systems.

The following figure illustrates the connection flow:

![How SPO communicates with a punchout system.](../image/punchout-establish-conn.png "How SPO communicates with the supplier punchout system")

**Parent Topic:**[Understanding punchout](punchout-overview.md)

