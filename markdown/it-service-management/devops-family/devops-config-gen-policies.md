---
title: Generic policies in DevOps Config
description: By default, the DevOps Config Policy content pack contains a set of generic policies to validate your configuration data.
locale: en-US
release: xanadu
product: DevOps \(Family\)
classification: devops-family
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 24
keywords: [PaCE content, PaCE policies, PaCE content policies, DevOps Config policies, Default DevOps Config policies, PaCE default policies, DevOps Config Policy content pack]
breadcrumb: [Default DevOps Config policies, Reference, DevOps Config, IT Service Management]
---

# Generic policies in DevOps Config

By default, the DevOps Config Policy content pack contains a set of generic policies to validate your configuration data.

**Important:** DevOps Config is now deprecated and no longer supported or available for new activation.

You can use or customize these default DevOps Config policies to validate that your configuration data content is conformable, or [administrate the full life cycle of PaCE policies](https://www.servicenow.com/docs/access?context=pace-managing-policies&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US).

**Note:** You can’t modify the default policies. However, you can make a copy of the policy and customize your copy.

<table id="table_gsp_4vm_nzb"><tbody><tr><td>

[A](devops-config-gen-policies.md#a) \| [C](devops-config-gen-policies.md#c) \| [D](devops-config-gen-policies.md#d) \| [F](devops-config-gen-policies.md#f) \| [G](devops-config-gen-policies.md#g) \| [K](devops-config-gen-policies.md#k) \| [L](devops-config-gen-policies.md#l) \| [M](devops-config-gen-policies.md#m) \| [N](devops-config-gen-policies.md#n) \| [S](devops-config-gen-policies.md#s) \| [U](devops-config-gen-policies.md#u)

</td></tr></tbody>
</table>## All Key-Value Comparator \(allKeysValuesComparator\)

Checks whether all the key-value combinations of any additional deployables are the same as the main deployable.

Results into a non-compliant status for the following conditions:

-   When a key is present in the main deployable but not in the additional deployables.
-   When a key is present in the additional deployables but not in the main deployable.
-   When a key is present in both the main and additional deployables but with different values

Use case: Detect any configuration drifts between staging and production environments.

-   **Input arguments**
    -   additionalDeployablesInput
        -   A list of additional deployables to be compared with the main deployable.
        -   Type: List
        -   Mandatory: True
    -   includeNodes
        -   A boolean value to indicate whether to include nodes other than the config data items \(CDI\) for the validation.
        -   Default: `False`
        -   Type: True \| False
        -   Mandatory: False
    -   exceptionList
        -   A comma-separated list of key names that should be ignored during comparison.
        -   Type: String
        -   Mandatory: False

## Authorized Email Domains \(authorizedEmailDomains\)

Checks whether an email domain value that is identified based on a regular expression are included in the authorized email domain list.

Results into a non-compliant status when an email domain isn’t an authorized domain.

Use case: Prevent \(sensitive\) data from leaving a trusted company email domain.

-   **Input arguments**
    -   authorizedDomains
        -   A comma-separated list of authorized email domains.
        -   Example:

            ```
            gmail.com,servicenow.com
            ```

        -   Type: String
        -   Mandatory: True
    -   exceptionList
        -   A comma-separated list of key names that are ignored by the policy.
        -   Type: String
        -   Mandatory: False

## Authorized Hosts in URLs \(authorisedHostsInURLS\)

Checks whether the format of the host component of the URL values in a snapshot are authorized.

Results into a non-compliant status when the URL values in a snapshot aren’t according to the format specified for the host component.

Use case: Prevent exposure of \(sensitive\) data through unauthorized URLs.

-   **Input arguments**
    -   authorizedHostsRegex
        -   A comma-separated list of regular expressions used for validating the host component in URLs.
        -   Example:

            ```
            notpresent$,code.devsnc+,mydomain.com
            ```

        -   Type: String
        -   Mandatory: True
    -   exceptionList
        -   A comma-separated list of key names that are ignored by the policy.
        -   Type: String
        -   Mandatory: False

## Authorized Key-Value Combinations \(authorisedKVCombinations\)

Checks whether the input key values found in a snapshot are authorized.

Results into a non-complaint status when a key has an unauthorized value.

-   **Input arguments**
    -   authorisedList
        -   A JSON list of keys with a list of authorized string values for each key.
        -   Example:

            ```
            {
              "image":"k8s.example.io,gke.example.io,docker.example.com:8444", 
              "domain":"example.service-now.com"
            }
            ```

        -   Type: JSON
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the authorized keys and their key values used for the validation are case-sensitive.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False

## Authorized Ports Range \(authorisedPortsRange\)

Checks whether the input port values found in a snapshot are authorized.

Results into a non-complaint status when a port value is not in the acceptable range.

Use case: Check that port names are within the acceptable range for the environment in which they’re used. The policy can be used for any range value check, not just port numbers. For example, to check that all the parameters defining a heap size are within the appropriate range.

-   **Input arguments**
    -   keysRegexWithRange
        -   A JSON list of port keys and port range with the minimum and maximum values. A key is identified as a port when the key matches the regular expressions specified in the input.
        -   Example:

            ```
            { 
              "^web_port$": "5000-5003",
              "env.db.port": "10000-65535"
            }
            ```

        -   Type: JSON
        -   Mandatory: True
    -   exceptionList
        -   A comma-separated list of key names that are ignored by the policy.
        -   Type: String
        -   Mandatory: False

## Certificate Validator \(certificateValidator\)

Checks whether certificates exist in a snapshot and whether the certificates have expired or are going to expire within the expiration period.

Results into a non-compliant status when the `expiration-date` key or the `certificate` key with the PEM-encoded format value in a snapshot has expired or will expire within the expiration period. The expiration period is calculated from the date on which the policy is executed plus the expiration days.

-   **Input arguments**
    -   certificatesNode
        -   The name of the node that contains the certificates.
        -   Default value: `certificates`
        -   Type: String
        -   Mandatory: True
    -   expirationDays
        -   The number of days to calculate the expiration period for the certificates. The expiration period is calculated from the date on which the policy is executed plus the expiration days.
        -   Type: Integer
        -   Mandatory: False
    -   exceptionList
        -   A comma-separated list of certificate names that are ignored by the policy.
        -   Type: String
        -   Mandatory: False

## Consistent Nodes Comparator \(consistentNodesComparator\)

Checks whether all the key-value combinations are the same for every first-level node in a snapshot.

Results into a non-complaint status when any two first-level nodes in a snapshot have different key-value combinations.

Use case: When all the nodes in a snapshot are a group of devices or virtual machines \(VMs\), they have the same configuration.

-   **Input argument**

    exceptionList

    -   A comma-separated list of nodes or key-value combinations to be excluded from the validation.
    -   Type: String
    -   Mandatory: False

## Correct Host Regex \(correctHostRegex\)

Checks the format for host-related keys to ensure that a host name is authorized to use.

Results into a non-complaint status when a key with a URL value in a snapshot doesn't match the regular expression provided for the authorized hosts.

-   **Input arguments**
    -   authorizedHostRegex
        -   A regular expression used for validating the host component in the URLs.
        -   Example:

            ```
            mydomain.com
            ```

        -   Type: String
        -   Mandatory: True
    -   exceptionList
        -   A comma-separated list of keys with the URL values to be excluded from the comparison.
        -   Type: String
        -   Mandatory: False

## Detect Unused Variables \(detectUnusedVariables\)

Checks whether the `vars` folder of a deployable or a collection includes variables that are not used in a snapshot.

Results into a warning when a variable is declared but not used in a snapshot.

## Different Key Names Same Values \(differentKeyNamesSameValues\)

Checks whether the values are the same for key pairs.

Results into a non-compliant status when the specified key pairs do not have the same value.

Use case: Obtain a finer grained control of conditions by checking that the values are the same for different keys.

-   **Input argument**

    keyPairs

    -   An array of key pairs that should have the same values. A key pair should have different keys and should not consist of a single key \(`[key1`\) or more than two keys \(`[key1=key2=key3]`\).
    -   Example:

        ```
        ["key1=key3","key2=key4"]
        ```

    -   Type: Array of strings
    -   Mandatory: True

## Different Values Nodes Comparator \(differentValuesNodesComparator\)

Checks whether the key value is different across all components when a key exists in multiple components of a snapshot.

Results into a non-compliant status when a key has the same value in multiple components.

**Note:** If a key has multiple occurrences inside the same component, use the [Unique Key Value \(uniqueKeyValue\)](devops-config-gen-policies.md#u) policy.

-   **Input argument**

    keynameList

    -   A comma-separated list of key names that should have different values for first-level nodes.
    -   Example:

        ```
        key1,key2
        ```

    -   Type: String
    -   Mandatory: True

## Docker Image Format Validator \(dockerImageFormatValidator\)

Checks whether the docker image of a service follows the regex as specified in the input. For example, provide a regex value to ensure the tagging and versioning of docker images follow best practices.

Results into a non-compliant status when the image value does not match the regex input value in the `imageExpectedRegex` input argument.

-   **Input arguments**
    -   imageExpectedRegex
        -   A regex value for a docker image.

            Example input value to ensure that the tag of an image is an alphanumeric value:

            ```
             ^.*:([0-9]+.?)+([-_]{1}[A-Za-z0-9.]+)?$
            ```

        -   Type: String
        -   Mandatory: True
    -   serviceExceptionList
        -   A comma-separated list of services that are exempted from the validation.
        -   Type: String
        -   Mandatory: False

## Docker Image Registry Validator \(dockerImageRegistryValidator\)

Checks whether the registry of a docker image is included in the authorized list of registries.

Parses the docker image for each service, fetches the value of a registry in an image, and then checks whether the fetched registry value is included in the **authorizedRegistryList** input.

Results into a non-compliant status when the image registry is not in the **authorizedRegistryList** input.

-   **Input argument**

    authorizedRegistryList

    -   A comma-separated list of registries.

        Example:

        ```
        k8s.example.io,gke.example.io,docker.example.com:8444
        ```

    -   Type: String
    -   Mandatory: True

## Docker Network Validator \(dockerNetworkValidator\)

Checks whether the network for a docker service is defined in the network sections.

Results into a non-compliant status when the network for a service is not defined in the top-level network section or the network for a service configured in the **labels/com.docker.lb.network** property is not defined in the service-level section and the top-level network section.

## Duplicate Values \(duplicateValues\)

Checks for duplicate values within a snapshot.

Results into a non-compliant status when there are duplicate key values in a snapshot except for the values defined in the exception list.

Use case: Obtain a finer-grained control of conditions by checking that snapshot values are different.

-   **Input arguments**
    -   includePath
        -   A boolean value to indicate whether to include the full path of the node in the output.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: True
    -   pathSeparator
        -   A string to indicate the path separator for nodes.
        -   Default value: `/`
        -   Type: String
        -   Mandatory: True
    -   exceptionList
        -   An array of strings to be excluded from the validation.
        -   Default value: `["true", "false", "yes", "no", "enabled", "disabled"]`
        -   Type: Array of strings
        -   Mandatory: False

## Forbidden Key-Value Combinations \(forbiddenKVcombinations\)

Checks whether there are any forbidden key-value combinations in a snapshot.

Results into a non-complaint status when any key found in a snapshot has a forbidden value as specified in the input list.

-   **Input argument**

    forbiddenKV

    -   A JSON list of keys with a list of forbidden values for each key.
    -   Example:

        ```
        {
          "username":"root,admin",
           "password":"qwerty123"
        }
        ```

    -   Type: JSON
    -   Mandatory: True

## Generic List Validator \(genericListValidator\)

Compares the key values of a snapshot with the list of values provided in the input. The key value might be a string, a list of comma-separated strings, an array of strings, or an object. When the key value is an object, the keys of the object are used in the comparison.

Note the following points for the policy compliance:

-   When the operator is `IN`, the policy is compliant when all the strings in the key value are included in the input list.
-   When the operator is `EQUALS`, the policy is compliant when all the strings in the key value match all the strings, listed in any order, in the input list.
-   When the operator is `CONTAINS`, the policy is compliant when the key value contains all the strings in the input list.
-   When the operator is `NOT CONTAINS`, the policy is compliant when none of the strings in the key value exist in the input list.

-   **Input arguments**
    -   keysToValidateObject
        -   An array of objects where each object contains a key path, an operator, and a reference list.
        -   Allowed operators are `IN`, `CONTAINS`, `NOT CONTAINS`, and `EQUALS`.
        -   Example input value to enforce that a user defined in the system `/root/user path` is either `user1` or `user2`:

            ```
            [ 
                { 
                  keyPath: ["system", “root”, "user"]  
            
                  operator: "IN" 
            
                  referenceList: [user1, user2] 
            
                 } 
            ]
            ```

        -   Default value: `[]`
        -   Type: Array of objects
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the list comparison should be case-sensitive.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: False

## Generic Validator \(genericValidator\)

Checks whether the value of a key is valid based on the operator and reference input value.

Note the following points for the policy compliance:

-   When the operator is `=` or `==`, the policy is compliant when the key value matches with the reference input value.
-   When the operator is `<`, the policy is compliant when the key value is less than the reference input value.
-   When the operator is `>`, the policy is compliant when the key value is greater than the reference input value.
-   When the operator is `<=`, the policy is compliant when the key value is less than or equal to the reference input value.
-   When the operator is `>=`, the policy is compliant when the key value is greater than or equal to the reference input value.
-   When the operator is `!=` or `<>`, the policy is compliant when the key value does not match the reference input value.
-   When the operator is `IN`, the policy is compliant when the key value is included in the reference input list.
-   When the operator is `NOT IN`, the policy is compliant when the key value is not included in the reference input list.
-   When the operator is `CONTAINS`, the policy is compliant when the key value contains the reference input value.
-   When the operator is `NOT CONTAINS`, the policy is compliant when the key value does not contain the reference input value.
-   When the operator is `REGEX`, the policy is compliant when the key value matches the regular expression pattern as specified in the reference input value.

-   **Input arguments**
    -   keysToValidate
        -   An array of objects where each object contains a key, an operator, and a reference value.
        -   Allowed operators are `<`, `<=`, `>`, `>=`, `=` or `==`, `<>` or `!=`, `RANGE`, `CONTAINS`, `NOT CONTAINS`, `IN`, `NOT IN`, and `REGEX`.
        -   Example:

            ```
            [
                  {
                    "key": "webport-KO",
                    "operator": "RANGE",
                    "refValue": "8000-9000"
                  },
                  {
                    "key": "webport-OK",
                    "operator": ">=",
                    "refValue": 8000
                  },
                  {
                    "key": "fqdn-OK",
                    "operator": "REGEX",
                    "refValue": ".francecentral.cloudapp.azure.com$"
                  },
                  {
                    "key": "trace_level-KO",
                    "operator": "IN",
                    "refValue": "INFO,ERROR,FATAL"
                  },
                  {
                    "key": "trace_level-KO",
                    "operator": "NOT IN",
                    "refValue": "DEBUG,VERBOSE"
                  },
                  {
                    "key": "trace-KO-ifcasesensitive",
                    "operator": "CONTAINS",
                    "refValue": "ERROR"
                  }
                ]
            ```

        -   Type: String
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the list comparison should be case-sensitive.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: False

## Key Existence Comparator \(keyExistenceComparator\)

Checks whether all the keys from a main deployable also exist in the additional deployables provided in the input.

Results into a non-compliant status if a key is present in the main deployable but not in the additional deployables.

Use case: Compare your environment variables and check that they’re consistent.

-   **Input arguments**
    -   additionalDeployablesInput
        -   A list of additional deployables to be compared with the main deployable.
        -   Type: List
        -   Mandatory: True
    -   includeNodes
        -   A boolean value to indicate whether to include child nodes of deployables during comparison.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False
    -   caseSensitive
        -   A boolean value to indicate whether the key comparison is case-sensitive.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False
    -   exceptionList
        -   A comma-separated list of key names that should be ignored during comparison.
        -   Type: String
        -   Mandatory: False

## Key Naming Convention \(keyNamingConvention\)

Checks whether key names follow a given naming pattern.

Results into a non-complaint status when keys don't follow the prefix-suffix naming pattern as specified in the input arguments.

-   **Input arguments**
    -   maxLength
        -   An integer value indicating the maximum length for a key name.
        -   Type: Integer
        -   Mandatory: False
    -   approvedPrefixArray
        -   An array of strings that indicate approved prefixes for a key name.
        -   Type: Array of strings
        -   Mandatory: False
    -   includePath
        -   A boolean value to indicate whether to include the full path of the node in the output.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: True
    -   approvedSuffixArray
        -   An array of strings that indicate approved suffixes for a key name.
        -   Type: Array of strings
        -   Mandatory: False
    -   exceptionList
        -   A comma-separated list of keys to be excluded from validation.
        -   Type: String
        -   Mandatory: False

## Key Path Validator \(keyPathValidator\)

Checks whether a key for the specified key path is found in a snapshot, and if found, the value of the key is valid based on the operator value and reference input value.

Results into a non-complaint status when the key for the specified key path has an invalid value. In addition, if the `ignoreIfNotFound` input argument is `False`, results into a non-complaint status when the key path specified in the input argument is not found in a snapshot.

-   **Input arguments**
    -   pathAndDesiredValues
        -   A JSON object that contains a set of keys and a mapping of condition and value the keys must have.
        -   Example:

            ```
            {
                "release-1.0/paymentService-V1.0/integerValues": ["<","3"],
                "release-1.0/paymentService-V1.0/database/dbPort": [">","8000"]
            }
            ```

        -   Type: JSON
        -   Mandatory: True
    -   pathSeparator
        -   A string to indicate the path separator for nodes.
        -   Default value: `/`
        -   Type: String
        -   Mandatory: True
    -   ignoreIfNotFound
        -   A boolean value to indicate whether the key for the specified key path should exist in a snapshot.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: False

## Key Value Substring Check \(keyValueSubstringCheck\)

Checks for the specified substring in a snapshot value for a specified key name.

Results into a non-complaint status when the value of a key name does not contain the substring as specified in the input argument.

-   **Input argument**

    keyNameWithKeyValues

    -   A JSON object that contains a required substring set including key name substring, and key value substring pairs.
    -   Example:

        ```
        {
          "live": "2022"
          "environment": "aws"
        }
        ```

    -   Type: JSON
    -   Mandatory: True

## List Comparator \(listComparator\)

Checks whether any two keys have the same values by comparing the list of values between the two keys. The comparison is case insensitive.

Results into a non-compliant status when all the list of values in the first key match all the values, listed in any order, in the second key.

-   **Input arguments**
    -   list1Node
        -   The key name of the primary node.
        -   Type: String
        -   Mandatory: True
    -   list2Node
        -   A key name of the node to be compared with the primary node.
        -   Type: String
        -   Mandatory: True

## Mandatory Keys \(mandatoryKeys\)

Checks whether the list of key names specified in the input are present in a snapshot.

Results into a non-compliant status when the specified key name is not present in a snapshot.

-   **Input arguments**
    -   mandatoryKeys
        -   A comma-separated list of key names.
        -   Type: String
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the key comparison is case-sensitive.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False

## Memory Limit Validator \(memoryLimitValidator\)

Checks whether the memory resources assigned to a key value are within the specified limits of a memory unit.  Compares case-insensitive key values of metric units \(including KB, MB, and GB\) and binary units \(including KiB, MiB, and GiB\). Converts a key value and its input values to bytes before comparing.

Results into a non-compliant status when a key value is not within the specified limits or is not a memory unit.

-   **Input argument**

    pathAndLimitsArray 

    -   An array of key paths and the minimum and maximum values for memory unit limits as min and max.
    -   Type: Array of objects
    -   Mandatory: True
    Example:

    ```
    [ 
        { 
        keyPath: ["deploy", "resources", "limits", "cpu"], 
        min: "250m", 
        max: "500m" 
        }, 
        { 
        keyPath: ["deploy", "resources", "limits", "cpu"], 
        min: "1GB", 
        max: "8GB" 
        } 
    ]
    ```


## Mandatory Tags List \(mandatoryTagsList\)

Checks whether the tag nodes found in a snapshot have authorized values.

Results into a non-complaint status when a tag node has a value not included in the authorized tag list.

-   **Input arguments**
    -   tagsNodeName
        -   A comma-separated list of key names.
        -   Type: String
        -   Mandatory: True
    -   tagsList
        -   A comma-separated list of authorized tag values.
        -   Type: String
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the key comparison is case-sensitive.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False

## Mandatory Value \(mandatoryValue\)

Checks whether all the keys provided as input have a non-empty value.

Results into a non-compliant status when the value of a key is null or empty, or results into a warning when the key name specified in the input is not found in a snapshot.

-   **Input arguments**
    -   keysList

        -   A comma-separated list of key names.
        -   Type: String
        -   Mandatory: True
    -   stopAtFirstFound
        -   A boolean value to indicate whether to check only the first occurrence of the key value in a snapshot.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: True
    -   trimValue
        -   A boolean value to indicate whether to remove any leading or trailing spaces from the key value before comparison.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the key comparison is case-sensitive.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False

## Mandatory Value By Type \(mandatoryValueByType\)

Checks whether all the keys provided as input have a non-empty value.

Results into a non-compliant status for the following conditions:

-   When the value of a key specified in the `keyNamesString` input argument is not a string value or is empty.
-   When the value of a key specified in the `keyNamesInteger` input argument is not an integer value or is empty.
-   When the value of a key specified in the `keyNamesBoolean` input argument is not a boolean value or is empty.

-   **Input arguments**
    -   keyNamesString
        -   A comma-separated list of key names that must have a string value.
        -   Type: String
        -   Mandatory: False
    -   keyNamesInteger
        -   A comma-separated list of key names that must have an integer value.
        -   Type: String
        -   Mandatory: False
    -   keyNamesBoolean
        -   A comma-separated list of key names that must have a boolean value.
        -   Type: String
        -   Mandatory: False

## No Clear Sensitive Data \(noClearSensitiveData\)

Checks whether the values are encrypted for the key names containing the specified keywords.

Results into a non-compliant status when the key name containing the specified keywords is not encrypted.

Use case: DevOps Config is used by organizations to manage and govern sensitive data \(passwords, API keys, and tokens\) through its permission-based access controls.

-   **Input arguments**
    -   keyWords
        -   A comma-separated list of strings used for identifying sensitive keys in a snapshot. The policy uses the case insensitive comparison.
        -   Default value: `pass,pwd,secret`
        -   Type: String
        -   Mandatory: True
    -   exceptionList
        -   A comma-separated list of keys to be excluded from validation.
        -   Type: String
        -   Mandatory: False

## No Duplicate Keys \(noDuplicateKeys\)

Checks whether there are no duplicate key names in a snapshot.

Results into a non-compliant status if a key name has multiple occurrences in a snapshot.

Use case: Deployment automation tools can handle multiple occurrences of settings badly resulting into downtime of services.

-   **Input argument**

    keyNames

    -   A comma-separated list of key names.
    -   Default value:  `dbConnectionString,dbUserName`
    -   Type: String
    -   Mandatory: False

## No Empty Values \(noEmptyValues\)

Checks whether all the keys have a non-empty value.

Results into a non-compliant status when the value of a key not included in the exception list is null or empty.

-   **Input arguments**
    -   trimValue
        -   A boolean value to indicate whether to remove any leading or trailing spaces from the key value before comparison.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the key comparison is case-sensitive.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False
    -   exceptionList
        -   A comma-separated list of keys to be excluded from validation.
        -   Type: String
        -   Mandatory: False

## No Forbidden Values \(noForbiddenValues\)

Checks whether there are any key names with forbidden values in a snapshot.

Results into a non-complaint status when any key found in a snapshot has a forbidden value as specified in the input list.

-   **Input arguments**
    -   forbiddenValues
        -   A comma-separated list of forbidden values.
        -   Default value: `root`
        -   Type: String
        -   Mandatory: False
    -   excludedKeyNames
        -   A comma-separated list of keys to be excluded from validation.
        -   Default value: `name,*desc*`
        -   Type: String
        -   Mandatory: False

## No FTP \(noFTP\)

Checks whether all the URLs in a snapshot use the FTPS protocol.

Results into a non-compliant status when a URL contains FTP in a snapshot.

-   **Input arguments**
    -   searchValue
        -   A search term that should not be present in the key value.
        -   Default value: `FTTP:/`
        -   Type: String
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the key comparison is case-sensitive.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False
    -   exceptionList
        -   A comma-separated list of keys to be excluded from validation.
        -   Type: String
        -   Mandatory: False

## No HTTP \(noHTTP\)

Checks whether all the URLs in a snapshot use the HTTPS protocol.

Results into a non-compliant status when a URL contains HTTP in a snapshot.

-   **Input arguments**
    -   searchValue
        -   A search term that should not be present in the key value.
        -   Default value: `HTTP:/`
        -   Type: String
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the key comparison is case-sensitive.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False
    -   exceptionList
        -   A comma-separated list of keys to be excluded from validation.
        -   Type: String
        -   Mandatory: False

## Node Keys Comparator \(nodeKeysComparator\)

Checks whether all the keys from the primary node are the same in the secondary node.

Results into a non-compliant status if a key is present in the primary node but not in the secondary node or vice versa.

-   **Input arguments**
    -   fromNode
        -   An array of strings indicating the path of the primary node in a snapshot.
        -   Default value: `[]`
        -   Type: Array of strings
        -   Mandatory: True
    -   toNode
        -   An array of strings indicating the path of the secondary node in a snapshot.
        -   Default value: `[]`
        -   Type: Array of strings
        -   Mandatory: True
    -   includePath
        -   A boolean value to indicate whether to include the full path of the node in the output.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: False

## No LDAP \(noLDAP\)

Checks whether all the URLs in a snapshot use the LDAPS protocol.

Results into a non-compliant status when a URL contains LDAP in a snapshot.

-   **Input arguments**
    -   searchValue
        -   A search term that should not be present in the key value.
        -   Default value: `LDAP:/`
        -   Type: String
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the key comparison is case-sensitive.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False
    -   exceptionList
        -   A comma-separated list of keys to be excluded from validation.
        -   Type: String
        -   Mandatory: False

## Nodes Value Comparator \(nodesValueComparator\)

Compares all key-value combinations between two nodes in a snapshot.

Results into a non-compliant status for the following conditions:

-   When a key specified in the `sameValueKeys` input argument has a different value in two nodes.
-   When a key specified in the `diffValueKeys` input argument has the same value in two nodes.
-   When the `allowMissingKeys` input argument is set to `False` and if a key is present in the primary node but not in the secondary node or vice versa.

Use case: Ensure consistency between nodes by comparing the values for keys between two nodes.

-   **Input arguments**
    -   fromNode
        -   An array of strings indicating the path of the primary node in a snapshot.
        -   Default value: `[]`
        -   Type: Array of strings
        -   Mandatory: True
    -   toNode
        -   An array of strings indicating the path of the secondary node in a snapshot.
        -   Default value: `[]`
        -   Type: Array of strings
        -   Mandatory: True
    -   includePath
        -   A boolean value to indicate whether to include the full path of the node in the output.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: False
    -   sameValueKeys
        -   A comma-separated list of key names with the same values.
        -   Type: String
        -   Mandatory: False
    -   diffValueKeys
        -   A comma-separated list of key names with different values.
        -   Type: String
        -   Mandatory: False
    -   allowMissingKeys
        -   A boolean value indicating whether to check all the keys from the primary node are the same in the secondary node.
        -   Default value: `False`
        -   Type: True \| False
        -   Mandatory: False

## No White-Space Characters Allowed \(noWhiteSpaceAllowed\)

Checks whether the key values do not contain white-space characters including leading and trailing spaces.

Result into a non-compliant status when a key value includes a white-space character.

Use case: Prevent white-space characters from causing issues for tools or applications when settings are applied.

-   **Input argument**

    excludedKeyNames

    -   A comma-separated list of keys to be excluded from validation.
    -   Default value: `description`
    -   Type: String
    -   Mandatory: False

## Same Key Value \(sameKeyValue\)

Checks whether the values of a key if included in multiple components of a snapshot are the same across all components.

Results into a non-compliant status when a key has different values in multiple components.

-   **Input argument**

    keyList

    -   A comma-separated list of key names
    -   Mandatory: True
    -   Type: String

## Same Values Comparator \(sameValuesComparator\)

Checks whether all the keys provided as the `keyList` input argument have the same value across the deployables.

Results into a non-compliant status when the value of a key is different in multiple deployables, or results into a warning when the key name specified in the input is not found in any of the deployables.

Use case: Detect any configuration drifts between staging and production environments.

-   **Input arguments**
    -   additionalDeployablesInput
        -   A list of additional deployables to be compared with the main deployable.
        -   Type: List
        -   Mandatory: True
    -   keysList
        -   A comma-separated list of key names.
        -   Type: String
        -   Mandatory: True
    -   stopAtFirstFound
        -   A boolean value to indicate whether to check only the first occurrence of the key value in a snapshot.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: True
    -   caseSensitive
        -   A boolean value to indicate whether the key comparison is case-sensitive.
        -   Default value: `True`
        -   Type: True \| False
        -   Mandatory: False

## Unique Key Value \(uniqueKeyValue\)

Checks whether the key value is different for a key when the key has multiple occurrences in a snapshot.

Results into a non-compliant status when a key has the same value in more than one occurrence.

-   **Input argument**

    keyList

    -   A comma-separated list of key names.
    -   Mandatory: True
    -   Type: String

## Unique Values Across Deployables \(checkUniqueKeyValue\_crossDeployables\)

Checks whether all the keys provided as the `keyName` input argument have different values across the deployables.

Results into a non-compliant status when the value of a key is the same in multiple deployables, or results into a warning when the key name specified in the input is not found in any of the deployables.

Use case: Detect any configuration drifts between staging and production environments.

-   **Input arguments**
    -   additionalDeployablesInput
        -   A list of additional deployables to be compared with the main deployable.
        -   Type: List
        -   Mandatory: True
    -   keyName
        -   A comma-separated list of key names.
        -   Type: String
        -   Mandatory: True

## Unresolved Variables \(unresolvedVariables\)

Checks whether there are any unresolved variables in a snapshot.

Results into a non-compliant status when a variable used in a key value cannot be resolved.

Use case: Ensure all the variables used in the configuration data settings are replaced with a value because any unresolved variables can break the deployment operation.

