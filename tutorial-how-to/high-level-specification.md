# High level specification

Before kick-starting your Uniscale journey you should have:

1. [Create an account](https://help.uniscale.com/account-and-preferences/create-an-account)
2. [Create a workspace](https://help.uniscale.com/workspace-administration/manage-workspaces/create-a-workspace)
3. [Invite to a workspace](https://help.uniscale.com/workspace-administration/manage-workspaces/invite-to-a-workspace)

When this is done, you are ready to follow the guide below on how to build better software!



## Introduction to high level specification

* What
  * Abstract specification
  * Purpose and motivation
  * High level requirements
  * High level end user behavior
* Why
* Who
  * Founder, visionary, product owner, program manager, ...
* How



## Describe your high level specification

Screenshot of solution description with the high level specification written.

Inspiration for things to include in your solution description:

* What - Describe what you're building
  * Try to explain in a few sentences what your product is doing?
  * Try to explain your solution so that a 6 year old can understand it. How would you explain what you are doing to a relative?
  * What are the overall functionalities and features of your solution?
  * What are the main requirements from your actors?
    * Try to write in a few sentences how you will solve this problem without going into details
    * Try come up with 3-5 bullets that explains overall what your solution will be doing
* Why are you building this solution?
  * What is the purpose and the value of it?
    * What is your motivation for building this solution?
    * What are the struggles and challenges that you see in the market?
    * What are the problems or needs that people have?
    * What is your desired outcome with making this product? What will people get out of using it?
    * Why am I/we the right person to solve this problem compared to others?&#x20;
* Who - Roles that will be using our solution
  * List all the actors that will be involved in your solution.
    * Think of internal and external people who are involved in your solution using/interacting with it or maintaining it.
* Find data sources (where does your data come from)
  * List here where the different types of data will come from. For example from manually inputting data, integration with systems, service providers, or elsewhere? Does the customer have to provide their details or personal information?
* Group actors
  * Can you group the listed actors based on for example their type and interactions with each functionality? This is to identify patterns of your actors, like roles and people that interact with the solution, fx the end-users (customers), and stakeholders like system administrators, suppliers, third-party contributors etc.&#x20;
* Functionality grouped (the what) by actors/groups (the who)
  * Of the high-level functionality, what actors will be using each part? This will help you break down your solution into modules.



## Create your first modules

Link to article: Learn about module



### Best practices for creating modules

Module as an isolated part of functionality ( = it can perform a task independently - the component can operate, be tested, and be modified without affecting or being affected by other components). “What changes together sticks together”

* Ideally it has a distinct ownership often leading to 1 team managing 1 specific module
* Examples of modules: Account; Payments; Inventory



### Module description

* Intended functionality for the specific module:
* What is the exact action that this module intends to achieve
* Detailed explanation of what this module is supposed to do and how it proposes to achieve it
* Actors
  * Who is going to interact with this module?

Notes:

* The modules will be the services at one point
* The modules define the departments of the company, and where and how the company will be scaling
* Modules are the different scenes in which different actors interact with the solution (one scene that you probably have always is an ‘account scene’ so an internal handling of things, other scenes describe then how different actor groups interact with the solution: one that faces the customer(s), one that focusses provider)
* Behaviors
  * Use cases are also concrete. They describe the scenes (actors + functions) that are the basis of the modules

### Pages

* Pages are an element for structure, where you can organize and group your functional use cases. Often used (if needed) when you have locked in the first revision.&#x20;

### Functional use cases - high level definition & user story&#x20;

* This is the high-level behavior: a clear description of the high-level functionality intended for the user (this usually entails an action/ taking the user from point A to point B
* A good logic to follow is that you should describe the functional use case with: 1) define the actor, 2) define their need, 3) define the what (they want to achieve) and 4) define the outcome (result that they hope to achieve)
* Examples: (House cleaning app: As a house owner, when my house is dirty, I want to book a cleaner, so that my house is cleaned)
* Who? This is where you bring in your UX and UI people - they will be the ones to start to break down the high-level user behavior and have a clear understanding of how to do this the best way possible to achieve what is described in your high-level functional specifications

#### Acceptance criteria

* Describe what this is and how it will work
* Note; Our Generative AI can help write suggestions for what acceptance criteria to include.&#x20;
* Definition: a list of qualifications that the functional use case (UX flow if detailed specification?) needs to fulfill



## Next steps

* Module revision?
* Generate SDK?
* Detailed specification
* Invite in relevant people













