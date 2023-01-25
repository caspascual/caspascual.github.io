---
layout: essay
type: essay
title: "See You Halfway There!"
# All dates must be YYYY-MM-DD format!
date: 2023-01-24
published: true
labels:
  - Smart Questions
  - StackOverflow
---
At some point in our lives, we’ll have a problem that leaves us with no choice but to ask someone else for help. The same applies to us programmers when we have an error in our code and can’t find a solution after reading through documentation and rewriting it entirely. With no other options, we turn to our best friends Google and StackOverflow. However, when we go on to ask our questions, there are certain guidelines, like Eric Raymond’s [“How To Ask Questions The Smart Way”](http://www.catb.org/esr/faqs/smart-questions.html), we should follow before posting.

## The Not Smart Way
Take [this](https://stackoverflow.com/questions/75228089/i-am-trying-to-find-the-problem-within-this-code) question asked on StackOverflow as an example. The question is titled “I am trying to find the problem within this code”. In the description, he says that he is getting  “NameError: name ‘home_team’ is not defined” on a snippet of his code. Numerous problems are apparent in this question when following Raymond’s guide. The first is his title. The only thing his title does is tell people they have a problem rather than giving a concise description as Raymond suggests. Another problem with this question is that it is easily googleable. Copying and pasting his error code brings up numerous links to very similar questions as his. Per the guidelines, questions should be searched on the web before asking.

Thankfully for the question author, no one has given him the “STFW” answer. The best answer in the replies gives steps on how to fix the problem (by initializing the undefined variable), reasons for the problem, and even the source code of their solution. The answer author even italicized words to put emphasis on the most important parts of the solution.
Here’s another [question](https://stackoverflow.com/questions/75224180/if-statement-trigger-please-assist) on StackOverflow. The question is “if statement trigger, please assist”. In their description, they provide the source code of 2 if statements and state that they want those if statements to trigger based on the conditional. The first problem with this question is again, the title; it doesn’t describe the problem. Another problem is within his description. The grammar is very hard to understand and the question author didn’t even describe their problem or what they did. All they stated was what the code should do.

## The Smart Way
Take a look at [this](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array) other question. The question is “Why is processing a sorted array faster than processing an unsorted array?” In his description, the author of the question provides source code made in C++ that processes through an array. When he sorts said array before processing through it, the run time is significantly faster. The author of this question is an exemplary example of Raymond's guidelines. Their title was clear and concise, they explained clearly what they did and what the problem is/does, and they explicitly said what they wanted at the end. To even show that their problem is not a fluke, the author of the question provided the source code of a Java version of their code to show that it’s not a problem with the language that they were writing in.

The question is also answered in a very smart way. The best answer gives a very detailed explanation of the question author’s problem. He provides an example of branch prediction, the part in their code that’s causing the problem (an if statement in their loop) with a visualization, and source code for a solution to the problem.

## Importance
Software engineers, at some point in their careers, will need to post a question about the problem they have while programming. Everything requires context to understand. You cannot expect someone to immediately understand what you are saying from only vague descriptions. In order for us to get a clear answer-back, we must provide a clear explanation. Asking smart questions is an important skill to have as a software engineer, otherwise, we’ll be stuck forever on a problem.

## Final Thoughts
Reading Eric Raymond’s guidelines reminded me of a quote my high school physics teacher once told me. “Learning requires both the student and the teacher to work together. You have to meet me halfway there.” Asking questions is a part of learning, and learning requires both sides, the student and the teacher, to meet each other halfway. In order for me to do that, I must ask smart questions.
