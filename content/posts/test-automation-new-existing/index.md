---
title: "Risk-based testing and test automation"
date: 2023-08-06
draft: false
showSummary: true
slug: "autotest-new-versus-existing-apps"
tags: ["Test automation"]
summary: "Why automating testing in new apps takes a different strategy than automating the tests in existing apps."
showReadingTime: false
---

![roulette-painting](roulette-dalle.jpg "A painting of a roulette wheel in a casino, generated by DALL-E.")

When you're starting with test automation, it matters whether you are going to cover a new app or an existing app. With new apps, you can cover features with tests as the app gets built. It makes it a lot easier to cover the entire app comprehensively, and starts paying dividends immediately.

With an app that has existed for a while, maybe for many years, covering the entire app as you would with a new app might be impossible or undesirable, simply because there's no time to cover it, and some parts of the app are much higher risk than others.

So as you would with manual testing, test automation in existing apps can also be done through an assessment of the risk of its functionalities.

Test automation is also only viable when the cost of creating and maintaining an automated test is less than the repeated manual testing plus the feedback time between tester and developer. This means that high risk, oft-repeated regression tests are the best to automate.

### Assessing risk

So we need to assess risk. How do we do this? With the following formula:

{{< katex >}}

\\(\ risk = probability * impact \\)

The above means we will want to assess the parts (which can be part of any quality characteristic such as functionality, security or performance) of an app which have either a high chance of failing, a big (financial) impact on the business if it fails, or a combination of both.

Impact can be assessed by measuring what business operation a functionality supports. If a login functionality fails to work, and millions of people use it every day, the impact would be greater than if only the performance of the login page was degraded. Part of measuring the impact can also be how fast it can be fixed. If a functionality is easy to fix, the impact can be contained easier.

Probability of failure is the harder one to assess, but can be done through experience and by measuring the complexity of (parts of) the app, the amount of technical debt it has, and the integrations it has with other apps, databases, and systems. Is the functionality dependent on other high-risk functionalities? Is there a chance of cascading failure?

### Risk determines design

Determining risk of applications should not only inform what to test, but also how to design applications in such a way as to minimize risk. Build in fallbacks and failsafes to ensure that when a functionality crashes or gets overloaded, the system has a back up functionality to use instead.

It speaks for itself that we want to automate the tests that cover the highest risk functionalities first, because those will also be the tests that are going to be performed the most. Test automation, however, is limited to testing software, so it has to mock hardware. In many cases, test automation will speed up development and testing, but it will not replace it. This is because mocking (faking) a part of the software in order to be able to test an app introduces its own risk. So test automation is essential, but not sufficient for a great testing strategy.