---
description: >-
  This page describes what Property validations are and how they can be set when
  creating properties.
---

# Validations

In the `Modeling view` under the `Technical view`, when adding properties, you can also specify validations for these properties.

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-23 at 14.54.21.png" alt=""><figcaption></figcaption></figure>

### Property Validations

Property validations are crucial for various native object types to ensure data integrity and compliance with business rules. The types of validations include:

* **Integer & Float**:
  * Ensure numeric values fall within accepted thresholds (e.g., non-negative quantities).
  * Confirm inputs expected to be numeric truly are.
* **String**:
  * Enforce length constraints (minimum or maximum characters).
  * Validate content against specific formats or regex patterns (e.g., email addresses).
  * Limit content to permissible characters.
* **Date & Datetime**:
  * Check values are within an acceptable logical range.
  * Ensure chronological order for series of dates (start date comes before end date).
  * Verify correct formatting according to application standards.

To begin adding a validation, click the **property** of interest to access the sidebar, then navigate to the settings tab. It's important to note that only properties labeled with a Property Type of **`Native type`** can have validations set. Once this is confirmed, select the _**data type**_ that matches one of the previously listed validation types. The process is detailed below.

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-23 at 15.05.42.png" alt="" width="371"><figcaption></figcaption></figure>

### Validation Tab

With the validation tab visible, under the field restrictions, we do see a couple of extra options listed below as&#x20;

* No validation
* Forced validation
* Validation options

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-23 at 15.22.58 (1).png" alt="" width="373"><figcaption></figcaption></figure>

1. The first option is as self explanatory as we would expect. No validation would be applied to the property.&#x20;
2. The second option _**Forced validation**_ displays a restriction option with the ability to add a restriction based on the type of validation selected**.**

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-23 at 15.38.34.png" alt="" width="370"><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-23 at 15.41.48.png" alt=""><figcaption><p>This window is displayed when the add restriction button is clicked to add the "custom" validation.</p></figcaption></figure>

Once the changes have been saved, our validation is applied to the property going forward.&#x20;

The above example applies to the _**string**_ validation but the other validation types may defer on how they are presented when the **`Add+`** restriction button is clicked as shown below.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-23 at 15.45.42.png" alt=""><figcaption><p>Integer / Float validation shows option types Less than, Greater than or In between.</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-23 at 16.21.29.png" alt=""><figcaption><p>Date validation shows type options as Before date, After date &#x26; Between dates. </p></figcaption></figure>



3. The third a nd last option _**Validation options**_ adds a few extra options besides the Restriction option as seen in the second option. The extra options when selected are also applied to the property as seen below.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-23 at 15.55.20.png" alt="" width="371"><figcaption></figcaption></figure>

**Overall, property validations across these native object types are fundamental to ensuring that data stored and processed by applications meet defined constraints and business rules. Adding these validations can significantly reduce errors, enhance data quality, and provide a better user experience.**
