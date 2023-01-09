---
title: "What is regression testing?"
date: 2022-01-09
draft: false
description: "What regression testing is, and why it's important"
summary: "What regression testing is, and why it's important"
slug: "regression-testing"
tags: ["regression", "testing", "test", "cases", "list"]
---

If you simply want the TL;DR, scroll to the bottom.

When I started working as a software tester at a logistics company, the team I was in had a platform of seven different apps, ranging from a year to ten years old in age. 

Ten years is a long time in software land, and so the older apps had become very complex to develop in, but also to test. In order to verify that the unchanged parts of the app still worked as intended after new code was added, we had to do regression testing.

In the team I started in (with multiple ops roles also doing acceptance testing), all regression testing was done manually, after release, in production, out of experience with what had failed before. We definitely functionally tested our user stories separately, but when it came to proper regression testing, everything was done by memory, based on previous experience.

The regression testing at that point was more of a one-time quality check after the fact than a preventative measure for the quality of the software. Granted, the suite of apps was low/medium-code, but this way of working left something to be desired. 

We ended up improving a lot of things about our development and testing process, which I will describe in other posts. But for now: regression testing.

One of the apps we worked on was a scanning & weighing app for parcels. This app had a lot of technical debt in the form of long delayed version migrations, and therefore had to be regression tested thoroughly. There were so many different process flows within this app that we couldn’t remember to test all of them. So simply out of necessity, we decided to create an excel with all the different flows that we needed to test. Thus, the list of test cases was born.

At first, this list this list contained test cases ordered by category: scans, type of labels being scanned. It took a while (as in: a few hours for every run) to get through the list. We then decided to assess the risk on every functionality being tested, and ended up with risk based test cases. This way we could choose to test only high risk functionalities if the developers had only touched certain low risk areas of the app, and we had less time than normal to do a full run. This too, is a necessity if your testing is al done manually.

After a while, I reordered the list to allow for easy succession of test cases based on the user/parcel journey: scans, return scans, undeliverable scans, and so on. Then I added a test data preparation section at the beginning, so I could do it all at once instead of having to register a parcel for scanning (through an API request) for every test case separately. 

The next step would be to automate the regression testing and implement it in the deployment pipeline so that it gets triggered when the developers deploy a new version of the app to a test environment. But this too is a tale for another time.

So, TL;DR for those who just want to know why and how to do regression testing:

- Regression tests are tests you do on unchanged parts of the system to verify it’s still working.
- The best way to start with this is to create a list of test cases that should be executed before every release (not after).
- It’s best to group the test cases in such a way that you can easily do one after the other; test cases are a continuation of other test cases.
- It’s best to group all the preparation you have to do for the test cases together as well, that too saves time.
- The ultimate goal is to automate most of your regression testing so all you have to do is maintain the automated tests, but this involves more technical knowledge and is a post for another time.
