---
categories:
- bioinformatics
date: 2015-11-24T00:00:00Z
published: true
tags:
- learning
title: Software Carpentry Instructor Training
url: /bioinformatics/software-carpentry-instructor-training
---

This week I attended the [Software Carpentry](http://www.software-carpentry.org) instructor training workshop hosted by [Elixir UK](http://www.elixir-uk.org) at the [University of Manchester](http://www.manchester.ac.uk). I've been on one of their courses as part of the [Scientist Training Programme](http://www.nshcs.org.uk/nhs-scientist-training-programme) and learnt loads. The whole ethos of improving scientific computing for more productive science is something I want to get on board with, so becoming an instructor seemed like a good challenge, as well as a boost for the old CV.

Below is a collection of my notes from the two days and a short review about the process.

## Overall Ethos

Software carpentry is [marginal gains](http://lifehacker.com/the-value-of-marginal-gains-1514453003) for teaching. Repeatedly improving understanding by 1% with small simple changes, leads to significant progress over time.

>Progress = Novice -> Competent -> Expert

Learning is about making the right connections and avoiding misconceptions.

Think through the implications of a broken mental model caused by a pre-existing misconception in order to work out the correct understanding.

>Novice - don't have mental models.
>
>Competent - use the mental models of others.
>
>Expert - create their own mental models.

Build a mental model of your learner's mental model to help direct your teaching.

Identify the mistakes and misunderstandings you had and guess/determine what your learners may encounter.

#### Simple lesson workflow *that scales*

Think ; Pair ; Share

Learn to listen to your room. Look for the sound of engagement.

Never teach alone; management and feedback assimilation is much easier with more than one pair of eyes.

#### Setting Questions & Tests for Maximum Impact

Good questions have diagnostic power in right *and* wrong answers.

Peer instruction relies on a really good question.

Test the mental model **not** mental knowledge.

#### Soliciting and Using Feedback...

...is for students *and* teachers.

Improving outcomes demands a feedback loop.

Formative feedback is a good way to workout what to teach next.

#### Lesson Delivery

*Jugyō kenkyū* - [lesson study](https://en.wikipedia.org/wiki/Lesson_study)

>Collaborative teaching with shared resources and experiences in small groups. Lessons are reviewed by other teachers and feedback is shared across the group leading to improvements in teaching practice.

Content and delivery are almost independent processes. Good content != Good Delivery and *vice versa*.

Review both regularly to improve performance. The act of soliciting feedback ensures better feedback in future.

Video review is a good model to implement. Services like [Athena]() and [Smarter Cookie](http://www.beasmartercookie.com) look particularly useful. Share videos with peers for performance feedback.

Every teacher has a different stage presence/personality. Who are you on stage? Normally, slightly louder and faster version of self, but not always the case.

#### Concept Map

- What are the facts (nodes)?
- What processes (arrows) link the facts (nodes) together into a concept?

Reflection via [concept maps](http://cmap.ihmc.us/docs/theory-of-concept-maps) creates connections and promotes reinforcement of the mental model.

*Example of the concept map I drew for the patient pathway in clinical genetics*

![clinical-genetics-concept-map](/images/2015/12/2015-12-13 16.17.18.jpg)

Getting learners to produce a concept map for a given teaching point is useful for gauging whether everyone is on the same page. They are also good for summative assessment (does your concept map match mine?).

NB: Good practice for refreshing memory before teaching.

#### Cognitive load theory

For any activity there is a constant conflict of relative vs extraneous load. If applied appropriately [cognitive load theory](https://www.mindtools.com/pages/article/cognitive-load-theory.htm) means presenting information at a pace and at a level of complexity that the learner can fully understand.

The aim is to reduce/remove extraneous cognitive load. Extraneous cognitive loads are not relevant to the lesson and are therefore **distracting**.

#### Faded Examples

[Faded examples](http://www.learnlab.org/research/wiki/index.php/Does_learning_from_worked-out_examples_improve_tutored_problem_solving%3F) are a method of teaching a mental model using a fill in the gaps approach with repeated short problems. They are really good for programming tasks where the learner can work backwards from a complete example to writing the entire code themselves.

Simple steps for creating faded examples:

1. Show all the steps to solve a problem.
2. Present a similar problem with a single step removed.
3. Present a similar problem with multiple steps removed.
4. Repeat until the problem solver is effectively creating an answer from scratch.

Works best for well defined problems such as how to do something specific using code.

#### Reverse Instructional Design

1. Write summative assessment
  * This is the knowledge and skills you are aiming to each.
  * What should learners know and be able to do after this lesson.
2. Write formative assessments to gauge assimilation of knowledge and methods during the teaching.
  * Use these to direct the flow of your teaching.
  * Check you're hitting every part of that final assessment target and that learners are understanding each step.
3. Lessons should plug the gaps between the formative and summative assessments.
  * Spend more time on ideas/concepts identified as weak in formative assessments.
  * What points of the curriculum do your learners already know? These can be taught lightly leaving more time for less well known/understood areas.

## Mini Review

The two days were extremely intense. I was shattered at the end of it all! But I did gain a lot and will be completing the process after Christmas. The speakers were all very friendly and approachable. They demonstrated the Software Carpentry ethos fully and I found it extremely inspiring. The location was fine (flat teaching room), it had plenty of power points for laptops, and coffee and lunch were provided. I did the computer bits on my iPad, which personally proved very slow and the etherpad didn't play very nicely. This is possibly because the tablet itself is old and slow, but using a proper laptop is something I'd probably consider for future versions of the workshop.
