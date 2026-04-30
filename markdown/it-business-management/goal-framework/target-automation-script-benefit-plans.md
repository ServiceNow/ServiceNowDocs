---
title: Target automation script for benefit plans
description: Use the predefined Benefit Plans script as a target source to automate the actual value of your targets from the benefit plans of relevant work items.
locale: en-US
release: zurich
product: Goal Framework
classification: goal-framework
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Goal Framework and Goal Framework for SPM, Strategic Portfolio Management]
---

# Target automation script for benefit plans

Use the predefined Benefit Plans script as a target source to automate the actual value of your targets from the benefit plans of relevant work items.

Use the following predefined benefit plans script to configure the target source for your targets. The script fetches the required data for monetary or non-monetary benefit plans and updates the actual value for the target. You can use this script as is or you can also modify it according to your requirement. You can also create context variables and configure them for this target source \(Benefit Plans\).

```
result = '';
var benefitPlans = new GlideRecord(sn_gfa.GFAdvancedConstants.BENEFIT_PLAN_TABLE);
benefitPlans.addQuery('sys_id', 'IN', benefit_plan);
benefitPlans.query();

var nonMonetaryBenefitSum = 0;
var monetaryBenefitSum = 0;
var hasMonetary = false;
var hasNonMonetary = false;
while (benefitPlans.next() && !(hasMonetary && hasNonMonetary)) {
    if (!gs.nil(benefitPlans.getValue('currency'))) {
        monetaryBenefitSum += parseInt(benefitPlans.getValue('actual_benefit'));
        hasMonetary = true;
    } else {
        nonMonetaryBenefitSum += parseInt(benefitPlans.getValue('nm_actual_benefit'));
        hasNonMonetary = true;
    }
}

if (hasMonetary && hasNonMonetary)
    gs.addErrorMessage(gs.getMessage('The Benefit Plan list can contain either monetary or non-monetary benefit plans.'));
else
    result = hasMonetary ? monetaryBenefitSum : nonMonetaryBenefitSum;
```

**Parent Topic:**[Goal Framework and Goal Framework for SPM reference](goal-framework-reference.md)

