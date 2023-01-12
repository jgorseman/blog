---
title: "Refining user stories"
date: 2022-01-12
draft: false
description: "What does a good user story contain?"
summary: "What does a good user story contain?"
slug: "user-stories"
tags: ["user", "stories", "gwt", "scenarios", "acceptance", "criteria"]
---

User stories are the easiest way to verify for a tester whether a new functionality is acceptable—if they contain the right information. 

User stories are taken from the agile way of working, and are essentially tasks bundled together in such a way that you get a cohesive piece of functionality for your software when it’s finished.

One part of a user story is the following sentence: *”As a … I want to … So that …”* and filling in the blanks for every story helps figuring out the who, what and why. For example: *As a person visiting the website to buy items, I want to be able to add items to a shopping cart, so that I can easily checkout all my items when I’m done shopping.*

The second part—or at least how we do it at my job as of writing this—is the *Acceptance Criteria*. These are one-line criteria that give a slightly more comprehensive overview of what actually needs to be done in order to consider the user story done. To follow on the example above, a criterium could be: *The shopping cart icon at the right top of the screen should show how many items are in it.*

The third part, and one that we only added when I worked there a while, are the Given-When-Then (GWT) scenarios. These are especially helpful for developers and testers to be able to specify, in advance, what results the user or system actions should have.

Having these scenarios often means the difference between a developer having to go to the user story creator to clarify how the user or system should behave, and the developer being able to pick it right up without having to ask further.

A GWT scenario works as follows: first comes the scenario title which gives a summary of the scenario, then we get the *given*, which is the prerequisite for the user or system to have in order to be able to perform the action. Then follows the *when*, which is the action that needs to be performed. Lastly follows the *then*, which is the result of the action performed. To give an example:

Scenario: Shopping cart icon displays number of items added

- Given: the user is on a webpage that contains shopping items
- And: the user has not added any items to cart yet
- When: the user clicks on “Add to cart” next to an item
- Then: the shopping cart logo in the top right corner of the webpage will display a “1”  in the top right corner of the logo

As you can see, the scenarios are very detailed. This makes it easier for the developer to know how the user story creator wants to see a functionality work. The developer is still allowed the freedom and creativity to implement it in their way, but there’s less confusion about what the functionality should do.

As you can also see, there’s an *And* in the scenario. “And” is used to display clearly the multiple prerequisites, actions or results in the scenario, if there are more than one.

That almost brings us to the end. One more part of user story templates that we use is to clarify any dependencies we have on other teams, internal or external to the organisation. Having these clearly in view, and making sure they do not block the user story’s completion in some way is important, to ensure the work does not get delayed too much.

That's what we use as a team in order to build good software. Having all components clearly filled out in a user story means the functionality can be built faster and more effectively.
