---
layout: post
title: From zero to pro - learning ui test automation in 8 hours. is it possible?
date: 2023-04-26 11:59:00-0400
description: I have decided to teach manual QA test automation in 8 hours
categories: automation
giscus_comments: false
related_posts: false
---

I decided to conduct an experiment. To teach QA professionals how to automate UI tests to the extent that they provide value to the project, all in 8 hours.

I wasn't interested in just tinkering with tests on the side, only to end up in a drawer. I wanted each QA professional to write automation scripts that would be merged into the master branch with the tests. Do you think it was successful? Let's move on to the next paragraphs and find out
<br>

## Introduction to the whole story

Often, when QA professionals start their work, usually as manual testers, the word 'test automation' appears in their minds. They test manually, test manually, test manually, but tasks (especially in regression testing) start to repeat themselves. Due to the monotonous task, the tester wants to start automating application tests.

They learn how to search for elements on the page (xpath or css), they learn Selenium, waiting for elements, and various tricks to make the tests stable. They continue to learn, time passes, but it does not bring value to the project. The problem arises of how to move from basic tests to tests that will be valuable, stable, and quick to implement.

When writing the first tests, the tester still needs to think about how to integrate them into the process, pipeline, and find time to test manually. These tests, as individual tests, eventually end up in the drawer.

The value of learning and automation is zero!

I decided to conduct a small experiment. Is it possible to break free from this state and learn UI testing that adds value to the project in 8 hours? The value for me was writing a test that would be merged into the master and executed together with the tests already written

## Heroes

In order for you to have a reference in this story, I need to introduce the levels of participants in my experimental workshop.

Junior QA - about a month of testing internship in projects, junior, junior, knowledge of Java (saw Java code for the first time) : )

Mid QA - manual testing, basic knowledge of Java + basic Selenium - writing basic tests that were not used in the project.

Mid QA - manual testing, stronger level of Java + some automated tests also not used in the project.

Mid QA - manual testing, stronger knowledge of Java + QA who is deeply involved in Postman and backend.

## Start time 9:00

We started our training by explaining our goal and then moved on to discussing tests.

Firstly, I explained the environment we would be working in. I discussed the role of Cucumber and Gherkin in our code, what steps, runners, page classes, and test containerization are.

The first two hours of explaining the big picture were crucial because they allowed testers to understand the flow between the different layers. The discussion of examples was done on a ready-made test package, which each QA ran on their own machine.

This also allowed us to check at the beginning of the training whether anyone had any configuration problems. We actually put together many elements into one working mechanism. After such an introduction, there was nothing left but to move on to implementing the tests.

## 11:00AM feature file - given, when, and, then and empty steps