---
layout: essay
type: essay
title: "Ask Smarter"
# All dates must be YYYY-MM-DD format!
date: 2023-01-24
published: true
labels:
  - Smart Questions
  - StackOverflow
---
At some point in our lives, we’ll have a problem that leaves us with no choice but to ask someone else for help. The same applies to us programmers when we have an error in our code and can’t find a solution after reading through documentation and rewriting it entirely. With no other options, we turn to our best friends Google and StackOverflow. However, when we go on to ask our questions, there are certain guidelines, like Eric Raymond’s [“How To Ask Questions The Smart Way”](http://www.catb.org/esr/faqs/smart-questions.html), we should follow before posting.

## The Not Smart Way
Take [this](https://stackoverflow.com/questions/75228089/i-am-trying-to-find-the-problem-within-this-code) question asked on StackOverflow as an example. 
```
I was trying to run the code below when scraping data from a website:

for match in match_data:
    home_team.append(match.find('th', class_='fhome').get_text())
    score.append(match.find('th', class_='fscore').get_text())
    away_team.append(match.find('th', class_='faway').get_text())
then I got the error message below:

NameError: name 'home_team' is not defined

I tried to USE the code below:

for match in match_data:
    hometeam = home_team.append(match.find('th', class_='fhome').get_text())
    tscore = score.append(match.find('th', class_='fscore').get_text())
    awayteam = away_team.append(match.find('th', class_='faway').get_text())
But the error message is still the same as above
```
The question is titled “I am trying to find the problem within this code”. In the description, they say that they are getting  “NameError: name ‘home_team’ is not defined” on a snippet of their code. Numerous problems are apparent in this question when following Raymond’s guide. The first is their title. The only thing their title does is tell people they have a problem rather than giving a concise description as Raymond suggests. Another problem with this question is that it is easily googleable. Copying and pasting the error code brings up numerous links to very similar questions. Per the guidelines, questions should be searched on the web before asking.

Thankfully for the question author, no one has given them the “STFW” answer. The best answer in the replies gives steps on how to fix the problem (by initializing the undefined variable), reasons for the problem, and even the source code of their solution. The author of the answer even italicized words to put emphasis on the most important parts of the solution.


Here’s another [question](https://stackoverflow.com/questions/75224180/if-statement-trigger-please-assist) on StackOverflow.
```
margaretscript = c://.....margaret.py

maryscript = c://......mary.py

James is getting it's value from an interface which then sends the value of james to the script. James can be either margaret or mary meaning james = "margaret" or james = "mary"

print(james)

if (james == 'margaret'):

    runpy.run_path(path_name=margaretscript)

if (james == 'mary'):

    runpy.run_path(path_name=maryscript)

else:

     exit()
if not mary or margaret, exit or break or stop script. I want james' result to trigger the if statements. If james == margaret then the runpy should run in margaret and not mary. PLEASE HELP
```
The question is “if statement trigger, please assist”. In their description, they provide the source code of two if statements and state that they want those if statements to trigger based on the conditional. The first problem with this question is again, the title; it doesn’t describe the problem. Another problem is within their description. The grammar is very hard to understand and the question author didn’t even describe their problem or what they did. All they stated was what the code should do.

## The Smart Way
Take a look at [this](https://stackoverflow.com/questions/11227809/why-is-processing-a-sorted-array-faster-than-processing-an-unsorted-array) other question. 
```
Here is a piece of C++ code that shows some very peculiar behavior.

For some reason, sorting the data (before the timed region) miraculously makes the primary loop almost six times faster:

#include <algorithm>
#include <ctime>
#include <iostream>

int main()
{
    // Generate data
    const unsigned arraySize = 32768;
    int data[arraySize];

    for (unsigned c = 0; c < arraySize; ++c)
        data[c] = std::rand() % 256;

    // !!! With this, the next loop runs faster.
    std::sort(data, data + arraySize);

    // Test
    clock_t start = clock();
    long long sum = 0;
    for (unsigned i = 0; i < 100000; ++i)
    {
        for (unsigned c = 0; c < arraySize; ++c)
        {   // Primary loop.
            if (data[c] >= 128)
                sum += data[c];
        }
    }

    double elapsedTime = static_cast<double>(clock()-start) / CLOCKS_PER_SEC;

    std::cout << elapsedTime << '\n';
    std::cout << "sum = " << sum << '\n';
}
Without std::sort(data, data + arraySize);, the code runs in 11.54 seconds.
With the sorted data, the code runs in 1.93 seconds.
(Sorting itself takes more time than this one pass over the array, so it's not actually worth doing if we needed to calculate this for an unknown array.)

Initially, I thought this might be just a language or compiler anomaly, so I tried Java:

import java.util.Arrays;
import java.util.Random;

public class Main
{
    public static void main(String[] args)
    {
        // Generate data
        int arraySize = 32768;
        int data[] = new int[arraySize];

        Random rnd = new Random(0);
        for (int c = 0; c < arraySize; ++c)
            data[c] = rnd.nextInt() % 256;

        // !!! With this, the next loop runs faster
        Arrays.sort(data);

        // Test
        long start = System.nanoTime();
        long sum = 0;
        for (int i = 0; i < 100000; ++i)
        {
            for (int c = 0; c < arraySize; ++c)
            {   // Primary loop.
                if (data[c] >= 128)
                    sum += data[c];
            }
        }

        System.out.println((System.nanoTime() - start) / 1000000000.0);
        System.out.println("sum = " + sum);
    }
}
With a similar but less extreme result.

My first thought was that sorting brings the data into the cache, but that's silly because the array was just generated.

What is going on?
Why is processing a sorted array faster than processing an unsorted array?
The code is summing up some independent terms, so the order should not matter.
```
The question is “Why is processing a sorted array faster than processing an unsorted array?” In their description, the author of the question provides source code made in C++ that processes through an array. When they sort through said array before processing through it, the run time is significantly faster. The author of this question is an exemplary example of a question that follows Raymond's guidelines. Their title was clear and concise, they explained clearly what they did and what the problem is/does, and they explicitly said what they wanted at the end. To even show that their problem is not a fluke, the author of the question provided the source code of a Java version of their code to show that it’s not a problem with the language that they were writing in.

The question is also answered in a very smart way. The best answer gives a very detailed explanation of the question author’s problem. They provide an example of branch prediction, the part in the questioner's code that’s causing the problem (an if statement in their loop) with a visualization, and source code for a solution to the problem.

## Importance
Software engineers, at some point in their careers, will need to post a question about the problem they have while programming. Everything requires context to understand. You cannot expect someone to immediately understand what you are saying from only vague descriptions. In order for us to get a clear answer-back, we must provide a clear explanation. Asking smart questions is an important skill to have as a software engineer, otherwise, we’ll be stuck forever on a problem.

## Final Thoughts
Reading Eric Raymond’s guidelines reminded me of a quote my high school physics teacher once told me. “Learning requires both the student and the teacher to work together. You have to meet me halfway there.” Asking questions is a part of learning, and learning requires both sides, the student and the teacher, to meet each other halfway. In order for me to do that, I must ask smart questions.
