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

I will make a rather bold statement, but I believe that this is the most important step in test automation using BDD. Why?

The first reason is that one must have experience as a tester to design tests that bring value. We can have a volume of even 30,000 tests, but if they are not valuable, they become useless in terms of feedback regarding our application. It is worth spending more time here on careful test design. I also talked to the participants about what tests they understand as valuable and what value they see in conducting tests.

The second extremely important thing is to build story elements so that these elements are reusable. Here, a balance must be maintained between very precise steps and large abstractions.

By designing steps and remembering about balance, we allow them to be used multiple times, thus avoiding code duplication.

Designing reusable steps has another benefit. With a large volume of steps, automatic tests can be designed and built even by a manual tester who only knows BDD and Gherkin. In this case, building automatic tests will be nothing more than assembling existing steps into new tests. It may be necessary to add only a few steps, but it is faster than implementation from scratch, and colleagues can always help.

We also cannot forget about the productivity of code creation, and in this aspect, I include showing how to quickly generate methods corresponding to steps in our designed story using keyboard shortcuts and placing them in the appropriate classes.

This stage was crowned with the creation of methods placed in the appropriate classes that did nothing yet

## 12:30 PM Views - essential element

To automate UI tests, we need to work on elements. Most of the team had an idea of what they are and how to search for them (sometimes even after going through 10 lessons on finding elements).

So we moved on to practice, which is finding the elements needed to automate our user stories. At the beginning of the training, I said that I wanted it to be extremely practical.

We started by searching for elements together on a large TV screen and discussing how to extract them best. I showed my simple, clear, and fast way based on practice (the world is not ideal, not every element has an ID) on how to extract elements.

## The method has been shown, now it's time for practice!

We went through about 4-5 examples together. What do I mean by "together"? After showing testers my way of finding elements, I started giving them tasks to extract elements from a real project.

We started with the simplest div and then increased the difficulty. Two identical elements, an element from an endless loop, extraction by text.

We discussed each example with QA right after the entire team showed that they actually extracted the given element.

It turned out that extreme 5 examples with prior discussion are enough to cover 95% of cases. What about the remaining 5%? Let's be realistic, we'll use Google and find a solution then

## 2:00 PM What shoult the elements do?

After declaring the elements, it was time to further add page classes. Since most testers had knowledge of Java, creating methods with actions such as entering values in inputs, clicking on elements, and creating getters required for assertions went smoothly.

What was not so obvious were collections of elements. However, since we were using Selenide support, testers immediately understood how to implement and use them.

Collections were crucial in allowing for efficient checking of the number of elements in the collection, making assertions on them, and efficiently operating on a larger volume.

## 3:20 PM Filling empty steps

After creating the page classes, we were able to define specific steps. I showed the testers how to connect their tests so that they would run in containers and explained what happens before the test is executed in the @Before and @After methods (containerization in Selenoid).

It is worth noting that Selenide is very helpful for us. UI tests are the most expensive tests, so efficient writing at this layer counts. Automatic screenshot capture after a failing test or implemented waits allow us to save a huge amount of time compared to pure Selenium.

More about Selenide in the upcoming posts, as it is a topic for a completely new series of articles.

In the steps themselves, knowledge of Java came in handy once again. We used object creation and chaining methods to keep the code simple and readable.

## 4 PM Running our tests and best practices

The moment of the final launch of our tests has arrived. Everything went smoothly and the tests worked as they should - there was euphoria.

However, I asked the team if they were sure that was it?

What about the stability of the test? We ran the tests only once, how can we be sure they are stable?

What about the assertions, how do we know if they are working correctly? We may have broken our assertions by not providing real feedback on the conditions being checked.

The entire work was done on our training branch

## 5 PM End of training 

So the training has come to an end. I asked for feedback and it turned out that writing tests itself is not scary.

The problem often lies in the lack of a big picture of QA. What does Maven do? What do the XML files run? How does TestNG manage tests?

Although we did not have time to go into every aspect in great depth, the whole team created a test and learned the big picture. What I noticed is that they gained confidence in their behavior.

Originally, a complex issue was broken down into simpler elements that were easier to understand.

## Continuation: 10 days after the reaining

Are you curious about what happened 10 days after the training? Pride of the QA team who participated in the training.

Junior QA is quickly gaining knowledge about Java to be able to start writing valuable tests in their daily work. We are already preparing the first simple task to get familiar with the whole flow, handling Git, merge requests, and code review.

Mid QA, who wrote tests not implemented in the project, sent me their first merge request. Some cosmetic improvements were needed, and the first merge to the master branch is close. (Edit: it has already been merged.) Another system fragment for automation is waiting in the queue.

Mid QA, starting with individual automated tests, took the branch from the training and prepared all possible cases. Their work is already on the master branch.

Mid QA returned to backend testing, but the knowledge they gained allows them to maintain the tests in case any of the QA team members go on vacation.

## Observations

My first observation as a training instructor is that it's hard to maintain extreme focus for about 8 hours. After some time, you can feel that it's too much. If I were to conduct it again, I would divide it into a 2-day training. Then independent work for QA, followed by another meeting after (5-10 days) to discuss their problems. And a fourth meeting after (20-30 days), where progress would be visible, and we could summarize the whole transformation project into a team of automation testers who write tests efficiently and effectively.

An additional observation is that for such a project to succeed, changes will need to be introduced in the organization. Who is responsible for the environment in which the tests are run, locally or on a server, what do we write tests in? All these decisions must be made. You also need to prepare the infrastructure for it. Otherwise, it will end up again in just "tinkering".