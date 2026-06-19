---
title: Now Assist in Platform Analytics terms
description: Now Assist in Platform Analytics uses terms that describe AI-assisted data exploration, query generation, and the semantic layer that connects natural language questions to instance data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/now-intelligence/platform-analytics/now-assist-platform-analytics-glossary.html
release: zurich
product: Platform Analytics
classification: platform-analytics
topic_type: concept
last_updated: "2026-05-20"
reading_time_minutes: 4
keywords: [Now Assist Platform Analytics glossary, query generation terms, Now Assist Explorer terms, Analytics Assist, Now Assist panel, automated segment, query generation, dimension, semantic layer, query generation, entity, semantic layer, query generation, executable query, query generation, exploration, Now Assist Explorer, exploration creator, Now Assist Explorer, exploration goal, Now Assist Explorer, exploration participant, Now Assist Explorer, exploration viewer, Now Assist Explorer, extended analysis, Now Assist Explorer, facts table, semantic layer, query generation, LLM, large language model, query generation, manual segment, query generation, Now Assist Explorer, AI data explorer, Query Generation, natural language query, segment, semantic layer, query generation, semantic description, semantic metadata, query generation, semantic label, semantic metadata, query generation, semantic layer, query generation, semantic usage instructions, semantic metadata, query generation, utterance, natural language, query generation]
breadcrumb: [Now Assist in Platform Analytics, Platform Analytics]
---

# Now Assist in Platform Analytics terms

Now Assist in Platform Analytics uses terms that describe AI-assisted data exploration, query generation, and the semantic layer that connects natural language questions to instance data.

## Analytics Assist

A set of Now Assist skills in the Now Assist panel that let users generate data visualizations and export dashboards and visualizations through conversational interactions.

## automated segment

A segment generated automatically by the system from existing data sources such as reports, dashboards, saved filters, app modules, and indicator sources. Automated segments are created and maintained by the Query Generation Sync Segments scheduled job.

## dimension

A semantic layer record that represents a column on a database table. Dimensions can follow reference fields across tables. Query Generation uses dimensions to identify the correct fields when processing a natural language question.

## entity

A semantic layer record that represents a database table. Query Generation uses entities to identify the correct facts table when processing a natural language question.

## executable query

A query produced by Query Generation that contains the data source, filter conditions, aggregation method, and visualization instructions needed to answer a user's natural language question.

## exploration

An editable, collaborative document in Now Assist Explorer where users analyze data with AI assistance. An exploration contains questions, AI-generated data visualizations, summaries, and participant commentary.

## exploration creator

A user who creates a new exploration in Now Assist Explorer. The creator sets the exploration goal, generates the initial data visualizations, and controls sharing rights. Requires the now\_assist\_explorer\_user role or higher.

## exploration goal

A statement of intent that describes the outcome a user wants to achieve from a data exploration. The goal guides the AI to generate queries and summaries that move the exploration toward that outcome.

## exploration participant

A user with whom an exploration has been shared with editing rights. Participants can generate additional data visualizations, add commentary, and may be able to share the exploration further. Requires the now\_assist\_explorer\_user role or higher.

## exploration viewer

A user with read-only access to a shared exploration. Viewers can read the exploration content but cannot ask questions of the AI or add text. A user becomes a viewer when shared an exploration without editing rights or without the now\_assist\_explorer\_user role.

## extended analysis

A deeper level of AI analysis in Now Assist Explorer that aggregates records related to a response to reveal additional insights. Extended analysis examines Choice, Reference, and Boolean columns and drills down automatically to avoid repeating the same findings.

## facts table

A database table included in the Query Generation semantic layer as a data source. Query Generation searches facts tables to answer user questions. Not all instance tables are included; administrators control which tables are added.

## LLM \(large language model\)

An AI model trained on large volumes of text data to understand and generate natural language. Query Generation uses an LLM to interpret user questions and produce semantic queries.

## manual segment

A segment created by an administrator to map user-friendly business terminology to specific query filter conditions. Manual segments receive a scoring boost over automated segments and can be shipped with applications via update sets.

## Now Assist Explorer

An AI-powered application in Platform Analytics that lets users ask natural language questions about data, receive data visualizations and summaries, and collaborate with others in shared explorations.

## Query Generation

A shared backend service used by Now Assist in Platform Analytics applications to translate natural language user questions into executable database queries. Query Generation relies on a semantic layer to identify the correct tables, fields, and filters for each question.

## segment

A predefined filter condition in the Query Generation semantic layer that maps business terminology to specific query filters. Segments help the system translate natural language questions into accurate database queries. Segments can be automated or manual.

## semantic description

A natural-language description of what an entity or dimension represents in business terms. Query Generation uses semantic descriptions to distinguish between similar tables or fields when processing a user question.

## semantic label

A short name or alias for an entity or dimension in the semantic layer. Functions as a search keyword that helps AI search identify the correct table or field when a user's question does not match the default field label.

## semantic layer

A flat representation of database tables and columns used by Query Generation to identify the correct data sources when processing a natural language question. The semantic layer consists of entities \(tables\), dimensions \(columns\), and segments \(filter conditions\).

## semantic usage instructions

Instructions associated with an entity or dimension that are injected directly into the LLM prompt when that entity or dimension is selected. Semantic usage instructions teach the system how to query the data — for example, which operators to use, how to handle abbreviations, or how to expand hierarchical values.

## utterance

A natural language question or input submitted by a user to an AI system. Query Generation processes utterances to identify the correct entities, dimensions, and segments needed to construct an executable query.

