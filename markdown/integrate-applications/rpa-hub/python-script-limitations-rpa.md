---
title: Limitations of Python script in Python connector
description: The limitations of the Python script in the Python connector are as follows.
locale: en-US
release: zurich
product: RPA Hub
classification: rpa-hub
topic_type: reference
last_updated: "2025-08-21"
reading_time_minutes: 1
breadcrumb: [Python connector, Connectors, Automation components, RPA Desktop Design Studio, Robotic Process Automation \(RPA\) Hub, Workflow Data Fabric]
---

# Limitations of Python script in Python connector

The limitations of the Python script in the Python connector are as follows.

## SecureString data type

Python does not recognize `SecureString` since it is specific to .NET. Therefore, do not use `SecureString` data type. If you need to use a secure string, ensure you convert it to a plain string before passing it as input to a Python method.

## user\_input

If the code contains `user_input` \(for prompting to enter input\), it runs indefinitely and the RPA Desktop Design Studio must be restarted. Avoid including this in the script, especially when writing in the configuration window.

Interactive calls such as input\(\)/user\_input\(\) \(or any user prompt\) cause the script to wait indefinitely for console input. Since the RPA Desktop Design Studio runs the script in a non-interactive execution environment \(where there is no console to capture user input\), the script gets stuck and never completes. This issue often requires a restart of the RPA Desktop Design Studio.

## Output printing twice

In the following code, the output is printed twice.

```
class Called1:
def greet(self, name):
return "Hello, " + name

class Calling1:
def call_method(self, input_name):
        # Create an object of Called1
        obj = Called1()
        # Call Called1's method with parameter
        result = obj.greet(input_name)
return result

caller = Calling1()
output = caller.call_method("Abel")
print(output)
```

When the code is changed as follows, the output is printed once.

```
class Called1:
    def greet(self, name):
        return "Hello, " + name
 
 
class Calling1:
    def call_method(self, input_name):
        # Create an object of Called1
        obj = Called1()
        # Call Called1's method with parameter
        result = obj.greet(input_name)
        return result
        
        
if __name__ == "__main__":
    caller = Calling1()
    output = caller.call_method("Abel")
    print(output)
```

Mention the top level code within the script. For example, `if __name__ == "__main__":`. This is known as a `__name__` guard.

The method or function is imported from the module into the internal script. When importing, it's necessary to guard the top-level execution with `__name__` to ensure it understands whether the execution is from an import or a direct run. For more information, see [\_\_main\_\_ — Top-level code environment](https://docs.python.org/3/library/__main__.html).

**Parent Topic:**[Python connector](../concept/python-connector-rpa.md)

