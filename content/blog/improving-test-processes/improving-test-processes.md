---
title: "Improving the software QA process within your team"
date: 2023-03-30
draft: false
showSummary: true
slug: "improving-test-processes"
tags: ["software testing"]
summary: "Going from no software testing, to automated test automation."
showReadingTime: false
feature: "improving-test-processes/feature-improving-qa-process.jpg"
---

You might be surprised that there are IT software development teams out there that do not have a structured QA process, or even any testing process at all.

But then software gets released that doesn't work, or doesn't work in the way the business intended.

### Start testing

Say you're in a team like that, the first thing you might do is test your user stories before they get released. This is a start. If it's the only thing you do, however, the chance that new code will break old functionalities as the system becomes more complex is big.

You'll have to start testing the existing functionalities as well (called regression testing). When the system becomes complex enough over years of software development, trying to remember what old functionalities work in what way in order to test them before new code gets released is going to become impossible.

### Document your tests

In order to remember all the functionalities, you have to figure out what they are. Time to create a spreadsheet with all the apps in it and catalog all the old and new functionalities.

At a certain point, however, you'll have so many functionalities that testing them all is impossible anyway. So you start doing risk-based testing, where you test only the highest risk functionalities before a release.

Now you're starting to set up a proper QA process. Figuring out how to get scenarios from new user stories into the spreadsheet effectively can be done by telling your team to write Given-When-Then scenarios that can be used in development and testing, and those will make it easier to implement test cases in your spreadsheet.

Even with risk-based testing there's still a lot to test, and testing everything you need to test manually before every release is time-consuming and because you have to test the same things over and over again, it's frankly boring as hell.

### Automate your tests

Here comes test automation. You get a tool that allows you to automate testing the existing functionalities, so there you go, you're now building automated tests. You've got a lot of catching up to do, it seems.

Now the challenge is to automate tests covering functionalities faster than they are added. In other words, you gotta make sure new functionalities are covered with automated tests before they are released, else you will have always have a backlog to catch up to.

Say you have your automated tests, but you as a tester are the only one running them, only after developers have built and peer reviewed their functionality, and the tests catch bugs. Now you have to go back to the developers after they have moved on to building other functionalities.

### Make your automated tests run automatically

So you're gonna want to tighten that feedback loop. Developers deploy their code to a dev/test environment, and what if the tests automatically run when that happens, and they give the developers results right after?

Now you have continuous testing, and the developers will have fast feedback, so that when the user story reaches you it's already been through a filter and it will be higher quality than without the continuous testing.

If all your existing functionalities are covered with automated tests, and new functionalities are tested through CI/CD, and they get covered with automated tests before they get released, congratulations, you now have a pretty mature QA process.

All this will take time and it will require changes in the process with which software gets released, and changing for the better won't always be easy, because people don't like to change.

It will also require people to realise that you can't just build super fast without creating problems later on with bugs and incidents in production. Hence the adage: *slow is smooth, and smooth is fast.*
