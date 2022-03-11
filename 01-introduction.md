# Introduction

Welcome to the Liferay Poshi tutorial. What is Poshi and why do we use it at Liferay? These and other questions will be answered as you go through this tutorial.

# What is Poshi?

Poshi is a test automation framework that is simple, easy to understand, and does not require prior programming language to get started. It is an end-to-end testing tool that allows testers to write tests that simulate a user's behavior as they navigate through a site. It is not JavaScript, rather, Poshi uses a Groovy-like script syntax built on top of [Selenium WebDriver](https://www.seleniumhq.org/docs/03_webdriver.jsp), which is one of the most popular open source tools for browser automation.

## And what is Poshi Standalone?

Previously, Poshi scripts could only be ran by downloading and creating the testcases in the [Liferay source code](https://github.com/liferay/liferay-portal/). Poshi Standalone, which we will be using in this tutorial, is a Gradle project that foregoes the need to download Liferay source.

# Why do we need Poshi?

Say your team is upgrading your implementation of Liferay DXP. How long will it take to manually test for regressions? A few hours? Days? Weeks, maybe? By the time you're done testing it is possible that a new upgrade is available and ready for testing.

With a constantly evolving platform like Liferay DXP, manual test executions can quickly become unsustainable because of time and cost constraints. A more realistic means to continuously test your implementation is through automated testing.