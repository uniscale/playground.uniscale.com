---
description: Learn more about the building blocks of a service
---

# PORTED- Service basics

## Overall structure

<figure><img src="../../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

## Service Composition: Understanding the Key Elements

Services are multifaceted, incorporating various elements that work cohesively to deliver functionality. This article delves into the primary components involved in service design, their application, objectives, and underlying principles. By dissecting these elements, we aim to provide a clearer understanding of what goes into creating a robust service.



```
// Example of a service with various levels of namespaces 
// and functionality
Service 
├─ Namespace
|   └─ Endpoint A
|   └─ Endpoint B
|   └─ Technical Usecase 
|      └─ Technical Usecase Flow 
└─ Empty namespace
└─ Namespace
   ├─ Aggregate A
   ├─ Aggregate B
   └─ Value object
   └─ Namespace
      └─ Property group
```

<figure><img src="../../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

## Namespaces

#### Understanding Namespaces in Your Service Architecture

Namespaces play a crucial role in the hierarchical organization of your service. Initially, they function to provide a structured framework. However, as your library evolves, namespaces become pivotal for identification purposes.

> As an analogy, consider a system of naming of people where each person has a given name, as well as a family name shared with their relatives. If the first names of family members are unique only within each family, then each person can be uniquely identified by the combination of first name and family name; there is only one Jane Doe, though there may be many Janes.&#x20;

#### Examples of namespace structure for a service:

```
Account (root level)
├─ Users
|   └─ Actions
└─ Sessions
   ├─ Activity
   └─ Backlog sessions
```

#### Revision cycle & update cycle

Namespaces are subject to the [locking/unlocking/readying](service-revisions.md) process within a revision. This means that editors of a service can manage the content via each of those statuses as needed.&#x20;

Since Namespaces reside at the root or top levels of most of the functionality of a service, they are quite crucial so in their status at any time.

***

## Use cases

Use cases ( UC) come in two forms: <mark style="color:purple;background-color:purple;">**`business`**</mark> and <mark style="color:purple;">**`system`**</mark>. <mark style="color:purple;background-color:purple;">**`Functional`**</mark> and <mark style="color:purple;background-color:purple;">**`technical`**</mark>.&#x20;

Functional UCs paint a more general picture of how a user might interact with your business to reach their goals. Instead of focusing on technical detail, it’s a cause-and-effect description of different inputs.&#x20;

{% hint style="info" %}
This type of UC is encountered and created from inside the [specification](../ported-specification/ported-solution-basics.md).&#x20;
{% endhint %}



In Uniscale, the main differentiation factor for the UCs is their technical intention.

Functional UCs have an [<mark style="color:purple;">**`service-to-module`**</mark>](service-basics.md#technical-intentions) intention. While technical UCs have an [<mark style="color:purple;">**`service-to-service`**</mark>](service-basics.md#technical-intentions) intention. For a full breakdown of these intentions, read more [here](service-basics.md#technical-intentions)

### Technical use cases&#x20;

&#x20;A technical UC is a detailed look at how users interact with each part of a system. It highlights how unique inputs and contexts cause the system to reach different outcomes. This level of detail highlights how a system’s functions work in any scenario.

#### Revision cycle & update cycle

UCs are subject to the [locking/unlocking/readying](service-revisions.md) process within a revision. This means that editors of a service can manage the content via each of those statuses as needed.&#x20;

## Use case flows&#x20;

### Standalone use case flow

Use case flows represent (UCF), as the name suggests an individual flow of a certain use case. These UCFs are created in the solution modules, and exported via service linking in the service.  Their technical intention is <mark style="color:purple;">**`service-to-module.`**</mark>

This process is described in detail bellow [here.](service-linking.md)

A functional UCF contains&#x20;

* a title
* a Rich Text description
* Possible functional Acceptance criteria
* and a list of linked endpoints

### Technical use case flows

As mentioned above, technical UCFs have the <mark style="color:purple;">**`service-to-service`**</mark> or <mark style="color:purple;">**`service-to-infrastructure`**</mark>

A  technical UCF contains&#x20;

* a title
* a Rich Text description
* possible Technical Acceptance criteria
* and a list of linked endpoints

#### Revision cycle & update cycle

UCFs are subject to the [locking/unlocking/readying](service-revisions.md) process within a revision. This means that editors of a service can manage the content via each of those statuses as needed.&#x20;



<figure><img src="../../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>

## End points

In Uniscale, we follow the same understanding and concept around endpoints as the industry.&#x20;

We must first distinguish between APIs and Endpoints as those can be quite familiar terms, with slight differences tho.

### **Endpoint vs. API**

It’s important to note that **endpoints** and **APIs** are different.&#x20;

An endpoint is a component of an API, while an API is a set of rules that allow two applications to share resources.&#x20;

Endpoints are the locations of the resources, and the API uses endpoint URLs to retrieve the requested resources.

***

As such, coming back to the definition of endpoints, they represent the **configuration of the expected behaviour of the API**, together with the expected **payloads** for the possible request and response. Quite a bit to take in so let's break that down.

### **Configuration of the expected behaviour of the API**

An endpoint will be defined by

* type: message or Request response
* owning namespace
* behaviour ( create, read, etc)
* name ( predefined based on behaviour or custom )&#x20;
* description optional

### Payloads

Depending on the type, and endpoint can contain **one** ( Message)  or **two** payloads (Request - Response)

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-09 at 16.18.09.png" alt=""><figcaption></figcaption></figure>

## Error codes

Once your endpoints are configured and set up with their payloads, they can be enriched with more configuration on how they will interact with outside systems or requests.

Initially, every endpoint assumes a happy scenario where no complications or bad scenarios can occur. The reality is different of course and for various reasons, your frontend can present various scenarios where the data is wrong, or missing, or the backend cannot process the requested information.

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-12 at 14.13.06.png" alt=""><figcaption></figcaption></figure>

In Uniscale you can enrich each endoints with direct Error codes to cover those exact scenarios. For each error code, you can provide&#x20;

* a system code
* a user message

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-12 at 14.12.52.png" alt=""><figcaption></figcaption></figure>

***

## Data contracts

Structuring your data can be done in multiple ways in Uniscale, and as such we have provided various top-level "containers" or "contracts" to manage their scope, and bounded context, in this way facilitating easier management of their Single source of truth.

#### Revision cycle & update cycle

Data contracts are subject to the [completion](service-revisions.md) process within a revision. This means that editors of a service can manage the content via each of those statuses as needed.&#x20;

<figure><img src="../../.gitbook/assets/image (54).png" alt=""><figcaption></figcaption></figure>

### Aggregates

Within DDD, aggregates represent the main data containers for your properties and data modeling. They are mainly characterized by a Single source of truth for individual properties and act as an umbrella for all the values within the same concept.

Aggregates are placed under a namespace which acts as its owner.

**Example  of aggregates**

* User
* Person
* Order
* Address

In Uniscale, aggregates have by default an aggregate identifier created automatically which follows the aggregate name. Afterward, an aggregate can be expanded with a flat or nested structure of properties.&#x20;

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-09 at 15.10.49.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (55).png" alt=""><figcaption></figcaption></figure>

### Value objects&#x20;

Value objects represent data contracts that are meant to be reused across your other data contracts. Their nature is to be reused, and as such, they can be quite simple in structure or even standalone.&#x20;

Value objects are placed under a namespace which acts as its owner.

**Example  of value objects**

* Gender
* SearchPayload

Value objects can be referred to as other aggregates, value objects and property groups. Editing them anywhere in the interface will also update the source of truth at its origin.

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-09 at 15.16.11.png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (56).png" alt=""><figcaption></figcaption></figure>

### Property groups

Once further into your modeling, you will reuse certain properties from across various aggregates and value objects, also with different cardinalities in mind. Exploring such scenarios, we can have:&#x20;

An **Order Summary**

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-09 at 15.23.19 (1).png" alt=""><figcaption></figcaption></figure>

We can see that the **UserIdentifier** is coming from an aggregate called **User.** The same goes for the **InvoiceIndentifier.** They are managed and owned by their respective aggregates, and aditionally we have a **created-at property**, followed by a list of Product Ids.&#x20;

This is mostly and mainly used as a payload for various endpoints, being in a **Message** or in a **Request-response** situation.

***

## Native type system



A **native data type** is a classification of data that tells the library generator how the library intends to use the data. In Uniscale we provide all the most commonly used data types. They are:&#x20;

<table><thead><tr><th width="164">Native type</th><th>Represents</th><th>Example</th></tr></thead><tbody><tr><td>GUID </td><td>a uniquely generated identifier</td><td>1234-a123-a4ag-432k</td></tr><tr><td>terminology</td><td>Collection of terms</td><td>female, male, other</td></tr><tr><td>date </td><td>Day-month-year</td><td>2024-01-01</td></tr><tr><td>datetime</td><td>Date with timestamp</td><td>2024 -01-01 12:34:20</td></tr><tr><td>boolean </td><td>logical true or false</td><td>true- 1, false- 0</td></tr><tr><td>float </td><td>fractional numbers</td><td>34.67, 56.99, -78.09</td></tr><tr><td>integer </td><td>whole number</td><td>300, 0 , -300</td></tr><tr><td>string </td><td>A sequence of characters</td><td>"hello world"</td></tr></tbody></table>

## Technical intentions&#x20;

At its baseline, every functionality in a service should exist for a purpose and intent. That intent can be internal or external. Towards functionality (solution or module), or towards another system ( service or infrastructure)

<figure><img src="../../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

<mark style="color:purple;">**`Service to module`**</mark>

All the functionality a service provides means to be exposed to a Frontend, a module, or a solution.

<mark style="color:purple;">**`Service to service`**</mark>

All the functionality a service provides means to be exposed to a system, in the shape of another service. Can sometimes be referred to as Backend communicating with another backend.

<mark style="color:purple;">**`Service to infrastructure`**</mark>

All the functionality a service provides means to expose an infrastructure as a whole, usually Storage, Networking, or any other IaaS scenarios.

