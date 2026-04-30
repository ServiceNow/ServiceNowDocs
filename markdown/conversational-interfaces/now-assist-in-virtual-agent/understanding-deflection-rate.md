---
title: Understanding conversation deflection rate
description: Now Assist in Virtual Agent Analytics calculates the conversation deflection rate based on the resolution status associated with Now Assist query responses.
locale: en-US
release: xanadu
product: Now Assist in Virtual Agent
classification: now-assist-in-virtual-agent
topic_type: reference
last_updated: "2024-11-05"
reading_time_minutes: 1
keywords: [Virtual Agent, Now Assist, conversation, deflection]
breadcrumb: [Analyzing Now Assist in Virtual Agent, Now Assist in Virtual Agent, Conversational Interfaces]
---

# Understanding conversation deflection rate

Now Assist in Virtual Agent Analytics calculates the conversation deflection rate based on the resolution status associated with Now Assist query responses.

## Sample conversation scenario

|Conversation flow|Query|Resolution status|
|-----------------|-----|-----------------|
|The user enters "New laptop"|Query 1|None|
|Now Assist returns a choice list|Query 1|None|
|The user selects **Show next answer**|Query 1|None|
|Now Assist presents a non-conversational item "New phone"|Query 1|None|
|The user selects **Show more results"**|Query 1|None|
|The user selects one of the SRs|Query 1|None|
|The user selects the thumbs up icon on one of the SR cards.|Query 1|Resolved|
|The user enters "parental leave policy"|Query 2|None|
|Now Assist presents a QA card for parental leave policy for US|Query 2|None|
|The user enters "parental leave policy for Canada"|Query 2|None|
|The user selects **Something else**|Query 3|Resolved|
|The user enters "iPhone broken"|Query 3|None|
|Now Assist presents a choice list of items|Query 3|None|
|The user selects one of the list items|Query 3|Resolved|
|The user enters "outage"|Query 4|None|
|Now Assist presents a list of SRs|Query 4|None|
|The user selects **Get more help**|Query 4|Not resolved|

In the sample conversation scenario, the deflection rate is calculated as \(Number of resolved queries/Total number of query responses\) x 100, which is, \(3/4\) x 100 = 75%.

