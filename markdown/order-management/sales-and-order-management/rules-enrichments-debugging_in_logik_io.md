---
title: Debugging in CPQ
description: How to use the debugger to perfect your scripts before deployment.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Setting up enrichments and rules scripting, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Debugging in CPQ

How to use the debugger to perfect your scripts before deployment.

When you need to fix a script in CPQ, the debugging tool in Advanced Functions and Enrichment Scripts can help. This guide shows you how to write debug JSONs to isolate and test your scripts before deployment. By following these best practices for debugging faulty scripts, you can help ensure your blueprints run flawlessly.

## General guidelines for debugging

Using `console.log()`: When coding a complex behavior, you may have to check whether certain values are set or manipulated the correct way. Instead of seeing only what is returned by the rule, use the `console.log([variableName])` function in a script to show the value of the variable at that line when run in the debugger.

Comment out blocks of codes: When a script becomes long, it may be necessary to comment large sections of code to see where the behavior originates. This can usually be done by using `//` or `/* */` and then debugging.

Comment out debug JSON for future use: If you are continually updating a rule during implementation, itʼs a good idea to save your debugging JSON either at the top or bottom of the script inside a comment block. That way, when the script is saved, the JSON can also be saved for future reference.

For more tips on these features, see [Using comments and the console to debug scripts](rules-enrichments-comments-and-console_log.md).

## How to use the debugger

![Debugger screen](../images/cpq-scripting-debugging.png)

When in the script editor:

-   Toggle the dubugger options by clicking the bug icon \(a\).
-   Enter your JSON in the Debugger Inputs section \(b\), as it would appear when your rule runs during configuration.
-   Run your rule with the debugger inputs by clicking **Run Debugger** in the Debugger Output panel.

    **Note:** The script does not have to be saved in order to run the debugger. The state of the script when the button is clicked is used when testing.

-   Returned objects and console.log information appear in the Debugger Output panel \(d\).

The CPQ debugger uses JSON format, which is written using attribute-value pairs. The attributes are the variable names of the fields used in the rule, and the value is the fieldʼs data in its object format.

**Note:** As long as a field is referenced in the rule or enrichment, it must have a corresponding attribute in the JSON, or the script cannot be run in the debugger.

Also note:

-   The JSON package is wrapped using curly brackets \(\{ \}\)
-   Each field is separated by a comma \(,\).
-   Each attribute-value pair is separated by a colon \(:\).

The structure of the JSON you use depends on the object type of each field, as well as whether the script is being used for a rule or an enrichment.

## Field-specific JSON formatting

-   Text, numbers, Boolean values, and single-select picklists fields are the easiest fields to debug, as they correspond to simple, singular-value objects such as strings, numbers, and Boolean values.

    ```
    {
    	"cfg":{
    		"textField": "value",
    		"singleSelect picklist": "value",
    		"numberField": 123,
    		"booleanField": true
    	}
    } 
    ```

-   Date fields use the ISO-8601 international standard to hold date information. If a field inputs dates in the debugger, the data should be a string in the format `YYYY-MM-DDThh:mm:ss.sssZ`.

    ```
    {
    	"cfg":{
    		"dateField": "2024-01-01T00:00:00.000Z"
    	}
    } 
    ```

-   Multi-select picklists are in the form of an array that contains strings. Even with only one option selected, the strings should be in an array format when debugging, wrapped by square braces \(\[ \]\) and separated by commas \(,\).

    ```
    {
    	"cfg":{
    		"multiSelect picklist": [
    			"option 1",
    			"option 2"
    		]
    	}
    }
    ```

-   Product pickers are unique to reference in a rule or enrichment, since they have their own type of simple rules, bulk actions. They can be referenced only by their picklist option, treating them as a single-select or multi-select field. Or, the debugger can reference a product picker subfield or aggregate using the key `pkr`.

    ```
    {
    	"cfg": {
    		"productPickerSS": "selectedValue",
    		"productPickerMS": [
    			"selectedValue1",
    			"selectedValue2"
    		]
    	},
    	"pkr": {
    		"productPicker2": {
    			"value": "productPicker2_option1",
    			"select": true,
    			"quantity": 100,
    			"exampleSubfield": "Example Value",
    			"aggregates": {
    				"quantity_max": 100
    			}
    		}
    	}
    }
    ```

    Note that when you reference a product picker subfield in a rule, you need to use the `pkr` object and not `cfg`.

    ```
    let x = pkr.productPickerName.subFieldName
    ```

-   Sets cannot be referenced by advanced functions, but the fields contained in them can. Due to the nature of the set field, a setʼs rows can be determined and referenced only in the On Configure/Reconfigure enrichment. However, you can test for when a field such as optionValue is in a rule.

    ```
    {
    	"set": {
    		"exampleSet": {
    			"index": 1,
    			"optionValue": "product1",
    			"selectOption": true,
    			"size": 2,
    			"aggregateExample1": 1
    		}
    	}
    }
    ```

    To learn more about defaulting a setʼs fields, see [Scripting: How to populate set values](enrichments-on-configure-reconfigure-scripts-how-to-populate-set-values.md).


## Context-specific JSON formatting

Field inputs are entered in JSON format, using the field variable name as the key and the intended value as the value.

```
{
  "cfg": {
    "exampleField": "Example Value"
  }
}
```

On configuration and reconfiguration, inputs are entered in JSON format, using the field variable name as the key. The value is an object consisting of two properties: **value** and **userEdited**. **value** should be set to the intended field value. **userEdited** is a Boolean value.

## Context-specific JSON formatting: fields

```
{
	"cfgRequest": {
		"exampleField": {
			"value": "Example Value",
			"userEdited": false
		},
		"exampleMultiselect picklist": {
			"value": [
				"one",
				"two"
			],
			"userEdited": false
		}
	}
}
```

For more information about how to use the **userEdited** property, see [Scripting: Checking for first and subsequent configurations](enrichments_on_configurer_and_reconfigure_behavior.md)

## Context-specific JSON formatting: product pickers

```
"cfgRequest": {
	"pkr": {
		 "productPicker1": {
					"data": [
						{
							"value": {
								"value": "productPicker1_option1",
								"userEdited": false
							},
							"select": {
								"value": true,
								"userEdited": false
							},
							"quantity": {
								"value": 100,
								"userEdited": false
							},
							"exampleSubfield": {
								"value": "Example Value",
								"userEdited": false
							}
						}
					],
					"aggregates": {
						"quantity_max": {
						"value": 100
					}
				}
			}
		},
		"productPicker2": {
			"value": "productPicker2_option1",
			"userEdited": false
		}
	}
}
```

## Context-specific JSON formatting: sets

```
{
	"cfgRequest": {
		"set": {
			"exampleSet": {
				"data": [
					{
						"index": {
						"value": 1
						},
						"optionValue": {
							"value": "product1",
							"userEdited": false
						},
						"selectOption": {
							"value": true,
							"userEdited": false
						},
						"textField": {
							"value": "a",
							"userEdited": false
						}
					}
				],
				"size": {
					"value": 1,
					"userEdited": false
				},
				"aggregateExample1": {
					"value": 1
				}
			}
		}
	}
}
```

## Context-specific JSON formatting: product pickers in sets

```
	"cfgRequest": {
		"set": {
			"exampleSet": {
				"data": [
					{
						"index": {
							"value": 1
						},
						"optionValue": {
							"value": "product1",
							"userEdited": false
						},
						"selectOption": {
							"value": true,
							"userEdited": false
						},
						"productPicker1InSet": {
							"value": [
								"option1_Of_productPicker1InSet",
								"option2_Of_productPicker1InSet"
							],
						"userEdited": false
						},
						"pkr": {
							"productPicker2InSet": {
								"data": [
									{
										"value": {
											"value": "option1_Of_productPicker2InSet",
											"userEdited": false
										},
										"select": {
											"value": true,
											"userEdited": false
										},
										"quantity": {
											"value": 100,
											"userEdited": false
										}
									}
								],
								"aggregates": {
									"quantity_max": {
									"value": 100
									}
								}
							}
						}
					}
				],
				"size": {
					"value": 1,
					"userEdited": false
				},
				"aggregateExample1": {
					"value": 1
				}
			}
		}
	}
}
```

On BOM Response enrichment:

Product List: Inputs are entered as an array of objects in JSON format, using the property variable name as the key, and the intended value as the value.

```
[
	{
		"id": "test product",
		"quantity": 2
	},
	{
		"id": "test product2",
		"quantity": 5,
		"bomType": "MANUFACTURING"
	}
]
```

Picklist extension Pricing enrichment:

picklist extension Request: Inputs are entered as an array of objects in JSON format, using the property variable name as the key, and the intended value as the value. In the example, “set” and “index” are only needed if using a set.

```
[
	{
		"fieldVariableName": "myField1",
		"set": "mySetVariableName1",
		"index": 1,
		"optionValue": "Option 1",
		"productId": "myProduct1",
		"productUniqueIdentifier": "myId"
	}
]
```

## If the debuggerʼs behavior is different from runtime behavior

In almost every case, the debugging JSON needs to match exactly what would normally be entered during runtime as valid values for the fields. Make sure that you are using the correct data type or structures described above.

In other cases, similar rules may be acting on the same field. In this case, the debugger will not be helpful, as it can only show the behavior of one rule at a time. It might be necessary to inactivate entire rules and redeploy in order to rule out the undesired behavior.

If all else fails, please open a case with our support team, or email us at support@logik.io.

