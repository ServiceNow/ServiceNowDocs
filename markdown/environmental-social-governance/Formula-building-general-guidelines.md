---
title: General guidelines for formula building
description: While building a custom formula in a calculated metric definition, keep these general guidelines in mind to easily create your formulas.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Formula building in a calculated metric definition, Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# General guidelines for formula building

While building a custom formula in a calculated metric definition, keep these general guidelines in mind to easily create your formulas.

## Overview of formula building

A formula consists of operands, operators, and functions. Examples of operators include addition \(+\), subtraction \(-\), multiplication \(\*\), and division \(/\).

## Tips to use the formula builder

-   As an administrator, when you start using the formula builder, you must begin by typing \\ \(slash\) in the text area.
-   It’s better to select the operands from the available list instead of typing the operand names.
-   Ensure that before you build a formula, the configurations are done by specifying the formula context, the tables, and the identifiers.
-   If there are large formulas, it’s easier to use the **Copy** button instead of manually selecting the whole formula as manual copy may result in an omission of certain parts of the formula.
-   To reset the formula, use the **Reset** button to revert the formula to its last saved state.
-   Use the **Preview** button to view the formula in a neat format without the visual clutter of identifiers.
-   While each identifier is an abbreviated two-letter combination of lowercase letters, don’t use fn as an identifier because generally the fn refers to a function
-   Use the formula builders on all browsers except Safari.
-   Specify the primary and the secondary columns to identify the right emission factors in case of emission factors with duplicate names. When defining calculated metric definitions, you can use emission factors with different units than the collected data.

**Parent Topic:**[Formula building in a calculated metric definition](../../metrics/concept/formula-building-at-metric-definition-and-entity-level.md)

