---
title: Forecasting planning and analysis
description: You can use the forecast planning and analysis feature to simulate various scenarios. The forecast planning and analysis tools enable for the creation, saving, visualization, and comparison of multiple analyses, enabling better planning.
locale: en-US
release: yokohama
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Explore, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Forecasting planning and analysis

You can use the forecast planning and analysis feature to simulate various scenarios. The forecast planning and analysis tools enable for the creation, saving, visualization, and comparison of multiple analyses, enabling better planning.

You can install Forecast planning analysis from the ServiceNow Store. After installation, you can navigate to Forecast planning analysis by selecting the list icon ![List icon.](../../../reuse/icons/product-icons/list-fill-24.svg).

## Analysis contexts

An analysis context is used to group different analyses for a specific use case. This context enables you to organize and manage multiple analyses within a single, cohesive structure. Creating an analysis context involves selecting a metric definition or a metric that you want to simulate and specifying the number of periods to forecast and the number of previous periods of data to use. By setting up an analysis context, you can help confirm that all relevant analyses are considered and compared systematically, providing a comprehensive view of potential outcomes.

**Note:** You can choose a manual, automated, or calculated metric definition when creating analysis contexts. You must have at least 12 periods of historical data for forecast planning analysis. This provides the necessary foundation for simulating different analyses.

## Analysis creations

An analysis is a simulation that models different outcomes based on specific interventions or changes. After creating an analysis context record, you can create different analyses. You can create the analysis by selecting the forecast method and adjusting the formula parameters. These analyses can be used to compare the outcomes with other analyses and make informed decisions for future planning.

## Forecasts

After creating an analysis record, a standard forecast graph and adjustable parameters are generated. This standard forecast acts as a baseline, showing how the metric would likely perform if no external changes were made. The original values used for the forecast are displayed for each of the parameter fields. In the following example a calculated metric definition is used to display the forecast model.

The following example shows a generated standard forecast.

![IStandard forecast. For the text description, refer to the text that preceded this example.](../images/standard-forecast.png "Example of importing a template")

You can create forecast interventions, to explore different possible outcomes by updating input parameters. A graph is generated showing the standard forecast and the new adjusted forecast.

The following example shows a generated standard and adjusted forecast.

![Adjusted forecast. For the text description, refer to the text that preceded this example.](../images/adjusted-forecast.png "Example of importing a template")

After creating and publishing multiple analyses and forecasts, you can compare the analyses and view a graph that captures the data for each analysis you select.

**Note:** After publishing an analysis and forecast, you can't change the parameters.

By comparing these analyses, you can better understand the potential impacts of your decisions, aiding in more strategic and informed planning.

The following example shows a generated comparison graph for two different analyses.

![Comparison of two analysis as a forecast graph. For the text description, refer to the text that preceded this example.](../images/forecast-comparison.png "Example of a Comparison")

**Note:** You can select up to five analysis records for comparison. If the selected analysis have adjusted values, those are plotted in the comparison. Otherwise, the standard forecast values are plotted.

**Parent Topic:**[Exploring Operational Sustainability Management \(formerly ESG Management\)](esg-new-explore.md)

**Related topics**  


[Set up analysis contexts and analyses](set-up-scenarios.md)

[Create an analysis context](../task/create-an-analysis-context.md)

[Create an analysis](../task/create-a-scenario-analysis.md)

[Adjust parameters](../task/create-a-forecast-intervention.md)

[Create a forecast comparison graph](../task/create-forecast-comparison.md)

