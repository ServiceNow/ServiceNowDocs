---
title: Establishing connection between SPO and the supplier punchout system
description: SPO and the supplier punchout system use PunchOutRequest and PunchOutResponse payloads to establish the connection.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Understanding punchout, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Establishing connection between SPO and the supplier punchout system

SPO and the supplier punchout system use PunchOutRequest and PunchOutResponse payloads to establish the connection.

The PunchOut system returns a PunchOutResponse, which contains the start URL for the PunchOut session. The SPO endpoint parses this response and opens the URL in a new tab. This parsing can be implemented using the XML Parser action step.

**Note:** The PunchOutRequest and PunchOutResponse payloads are expected to follow the same structure across all PunchOut systems.

The following figure illustrates the connection flow:

![How SPO communicates with a punchout system.](../image/punchout-establish-conn.png "How SPO communicates with the supplier punchout system")

**Parent Topic:**[Understanding Punchout](punchout-overview.md)

