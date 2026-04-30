---
title: Step execution scripts
description: In a step configuration record, the step execution script field determines what a step with this configuration does when it runs.
locale: en-US
release: yokohama
product: Automated Test Framework \(ATF\)
classification: automated-test-framework-atf
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Step configurations, Administration, Automated Test Framework \(ATF\) reference, Automated Test Framework \(ATF\), Testing and debugging applications, Building applications]
---

# Step execution scripts

In a step configuration record, the step execution script field determines what a step with this configuration does when it runs.

## Step inputs

The input variables to a step are determined by the inputs related list in the step configuration record. The **inputs** parameter to `executeScript()` gives the script access to these variables. For example, if the inputs related list contains two records, *var1* and *var2*, the script can reference *var1* with the expression `inputs.var1` and can reference *var2* with `inputs.var2`.

## Step outputs

The output variables to a step are determined by the outputs related list in the step configuration record. The **outputs** parameter to `executeScript()` gives the script access to these variables. For example, if the outputs related list contains two records, *out1* and *out2*, the script can reference *out1* with the expression `outputs.out1` and can reference *out2* with `outputs.out2`.

## Step result

The **stepResult** parameter provides access to an API that controls whether the step passes or fails. It also determines the message the step writes to the log.

The method `stepResult.setSuccess()` causes the step to succeed. The method `stepResult.setFailed()` causes the step to fail.

The method `stepResult.setOutputMessage()` sets the message to write to the log when the step succeeds or fails. It takes one parameter: the string to write to the log. If the script calls `stepResult.setOutputMessage()` more than once, the most recent value set overwrites any previous value.

## Record Query step execution script

```

    (function executeStep(inputs, outputs, stepResult) {
         if (gs.nil(inputs.table)) {
            stepResult.setOutputMessage(gs.getMessage("The '{0}' input variable was not specified",
               'table'));
         stepResult.setFailed();
          return;
    }
    var query = new GlideRecord(inputs.table);
    query.addEncodedQuery(inputs.field_values);
    query.query();
    if (!query.next()) {
         stepResult.setOutputMessage(gs.getMessage("No records matching query:\n{0}",
             inputs.field_values));
          stepResult.setFailed();
    } else {
         stepResult.setSuccess();
         outputs.table = inputs.table;
         outputs.first_record = query.getUniqueValue();
         stepResult.setOutputMessage(gs.getMessage("Found {0} {1} records matching query:\n{2}",
                                                  [query.getRowCount(),
                                                   inputs.table,
                                                   inputs.field_values]));
    }
    }(inputs, outputs, stepResult));
    
   
```

## Custom scripted step configs

```

    ((function executeStep(inputs, outputs, stepResult, timeout) {
	// Waits up to the timeout for some asynchronous logic to finish
	// This script checks for completion once a second for up to 60 seconds
	var counter = 1;
	// Try for up to 60 seconds
	while (counter <= timeout) {
		// If the asynchronous logic is finished, return "true" to pass the step
		// isMyAsyncLogicFinished() can be replaced with any asynchronous event that needs to be tested
		if (isMyAsyncLogicFinished()) {
			stepResult.setOutputMessage("Success!");
			stepResult.setSuccess();
			return;
		}
		// Wait one second, and log the total number of seconds waited
		gs.info("Waited " + counter + " seconds for asynchronous logic to finish");
		sn_atf.AutomatedTestingFramework.waitOneSecond();
		counter++;
	}
	// If this point is reached, the retry loop ran out of tries; return false to fail the step
	stepResult.setOutputMessage("FAILURE: Timed out after waiting for " + timeout + " seconds");
	stepResult.setFailed();
}(inputs, outputs, stepResult, timeout));
    
   
```

**Note:** The above example can also be used for Run Server Side script by replacing `stepResult.setSuccess()`” and `stepResult.setFailed()` with `return true` and `return false`.

**Parent Topic:**[Step configurations](step-configurations-module.md)

