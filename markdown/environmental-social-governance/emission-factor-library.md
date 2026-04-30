---
title: Emission factor library
description: Setting up your emission factor library is important for calculating your emissions accurately. An emission factor library consists of emission factors, emission activities and emission activity sources.
locale: en-US
release: zurich
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Explore, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Emission factor library

Setting up your emission factor library is important for calculating your emissions accurately. An emission factor library consists of emission factors, emission activities and emission activity sources.

Emission factors, emission activities and emission activity sources are different aspects of the emission factor library.

## Emission factor

An emission factor is a coefficient that quantifies the emissions released per unit of activity or output. It is used extensively in environmental science, engineering, and regulatory contexts to estimate the amount of pollutants or greenhouse gases emitted into the atmosphere from various sources.

An example of an emission factor is Carbon dioxide \(CO₂\) emissions from the combustion of diesel fuel. Its value, is 2.68 kilograms of CO₂ per liter of diesel fuel burned. If an organization consumes 10,000 liters of diesel fuel in a year, the total CO₂ emissions can be estimated as: Total CO₂ Emissions=Diesel Fuel Consumed×Emission Factor. Total CO₂ Emissions=10,000 liters×2.68 kg CO₂/liter. Total CO₂ Emissions=26,800 kg CO₂. In this case, the organization would emit approximately 26,800 kilograms \(or 26.8 metric tons\) of CO₂ annually from diesel fuel combustion.

Emission factors can be used for:

-   Estimation of emissions
-   Environmental reporting and disclosures
-   Life-cycle assessment

Audit tracking is enabled by default on Emission Factor tables, so all modifications are systematically recorded in an audit log. Access to this log is restricted to authorized users, who can review detailed entries for compliance and traceability. The audit log captures:

-   User details initiating the change
-   Timestamp of the modification
-   Type of change performed
-   Modified data entries

## Emission activity

An emission activity is any process or action that produces pollutants or greenhouse gases released into the atmosphere. These activities can occur in various sectors such as industry, transportation, agriculture, and residential areas. Some examples of emission activities are:

-   Burning coal in a power plant to generate electricity
-   Cement production
-   Activities such as livestock farming

## Emission activity sources

The **Source** field in the Emission activity \[sn\_esg\_emission\_activity\] table identifies the external database or methodology used to estimate greenhouse gas \(GHG\) emissions for an activity. Some examples of values for this field are:

-   Greenhouse Gas \(GHG\) emission sources
-   Department for environment, food and rural affairs \(DEFRA \)
-   Environmentally extended input-output models \(EEIO\)
-   Emissions and generation resource integrated database \(eGRID\)

**Parent Topic:**[Exploring Operational Sustainability Management \(formerly ESG Management\)](esg-new-explore.md)

**Related topics**  


[Set up the emission factor library](set-up-the-emission-factor-library.md)

