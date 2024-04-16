# Service linking

This article assumes that you have covered knowledge around [specification](../wip-specification/) and concepts in [service basics](service-basics.md).  If not, it is recommended to follow those first to better understand this article.

Having a look at the following illustration, we recognize the specification elements, and individually the Services on the side of it.&#x20;

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-12 at 09.06.55.png" alt=""><figcaption></figcaption></figure>

Within the solution, there are UX flows that require functionality from the service and as such, it will be provided via Use case flows from the service.&#x20;

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-12 at 09.08.40.png" alt=""><figcaption></figcaption></figure>

The process is more detailed than this so let's break it down with interface examples.&#x20;



### Dependencies Process&#x20;

As a process, this is where you will invite your Developers on your solution to collaborate with you in aiding you to break down the functionality required and properly connect it to the right services.

***

In essence, creating your dependencies in your application. This is where most of the time, many companies and projects end up going the complicated route and create what we call a "dependency spider web" or "a ball of mud". This is done due to a lack of an overview of the dependencies and also conscious decisions behind each of them.&#x20;

### Linking to services from solution specification

As your specification grows in complexity, you will end up adding [UX flows](../ported-specification/ported-solution-basics.md#ux-flow) within your [functional use cases](../ported-specification/ported-solution-basics.md#functional-use-case). They act as "requirements" or "needs" of functionality towards the services.&#x20;

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-12 at 09.40.51@2x.png" alt=""><figcaption></figcaption></figure>

After being linked, the UX flow will show under the linked Service flow

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-12 at 16.01.47.png" alt=""><figcaption></figcaption></figure>

Once a Service flow is linked (and this process is repeated from many other UX flows), from within the Service linking tab, you can now export all changes, service by service

<figure><img src="../../.gitbook/assets/CleanShot 2024-04-12 at 15.56.17 (2).png" alt=""><figcaption></figcaption></figure>

This will :

* create new Use case flows if they never existed prior
* move existing Use case flows to their targeted service
* link existing Use case flows to the UX flows in the specification.&#x20;

{% hint style="warning" %}
This change is irreversible so make sure you do this once all your specification breakdown has happened.
{% endhint %}



## Service editor functional view

Inside the service editor of a solution-owned service, the tab called Functional View will now be active.

Inside, a filtered representation of the solution specification is shown with only the items that link to the service. In essence, acting as an overview of all the dependencies the service has towards the solution.



