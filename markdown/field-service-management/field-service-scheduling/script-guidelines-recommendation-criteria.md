---
title: Providing a script for custom task recommendation criteria
description: Guidelines for creating scripts in recommendation criteria for an Intelligent Task Recommendation policy.
locale: en-US
release: xanadu
product: Field Service Scheduling
classification: field-service-scheduling
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Setting up Intelligent Task Recommendations, Setting up a Field Service scheduling method, Configuring Field Service Management, Field Service Management]
---

# Providing a script for custom task recommendation criteria

Guidelines for creating scripts in recommendation criteria for an Intelligent Task Recommendation policy.

## Customization script return object

Your script should return a JavaScript object in a minimum form as follows:

```
{ 
  "<task sys_id1>": 
    {
      "rating": <rating1>
    },
  "<task sys_id2>”:
    {
      "rating": <rating2>
    },
  …
}
```

For filter constraints, set the return objects rating to one to unify the filter constraint result of the recommendation criteria by using the sn\_task\_recommend.TaskRecommendationUtil.setRatingToOne\(your object\); method.

To normalize the rating result of ranking criteria, the return JavaScript object should include normalization information.

```
{           
    "<task <sys_id1>":     
        {
            "rating": <rating1>, 
            "normalizationData": 
                {
                    "numerator": <numerator value1>,
                    "denominator": <denominator value1> 
                }
        },    
    "<task <sys_id2>":     
        {
            "rating": <rating2>, 
            "normalizationData": 
                {
                    "numerator": <numerator value2>,
                    "denominator": <denominator value2> 
                }
        },
    ...
}
```

For ranking criteria, the return object can contain data for final normalization.

**Note:** If your scripts include normalization data, you can refer to the default script includes in the predefined recommendation criteria:

-   The filtering constraint Exclude tasks agent cannot travel to: sn\_fsm\_task\_rec.TaskRecommendationDistanceRuleProcessor
-   The ranking criteria Distance from task: rankTaskOnDistance\(\)

## Customized script in recommendation criteria

The following example shows how to write a script for the recommendation criteria.

```
var customizedScript = <your-script>; 
var customizedResult = customizedScript.<your-method>(); 
ruleResult = TaskRecommendationFSMUtil.parseRuleResult(customizedResult, "<customized-rule>");
```

The following sample configuration provides a "distance from task" filter constraint.

```
var distanceRule = new TaskRecommendationDistanceRuleProcessor(args); 
var ruleProcessResult = distanceRule.processRule(user, tasks, timeStart, timeEnd, 'ranking'); 
ruleResult = TaskRecommendationFSMUtil.parseRuleResult(ruleProcessResult, "Distance from task");
```

**Note:** Do not replace the task recommendation application keyword `ruleResult` in the script with any other words. Otherwise, the application will not be able to process the rule execution result.

**Parent Topic:**[Setting up Intelligent Task Recommendations](../concept/administer-task-recommendations.md)

