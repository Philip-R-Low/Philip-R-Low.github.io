---
layout: essay
type: essay
title: "Coding Standards suck, actually."
# All dates must be YYYY-MM-DD format!
date: 2026-02-12
published: true
labels:
---
## The not so bad
Like any good clickbait title, the title of this essay is an overexaduration of my opinion on coding standards. There are some parts of coding standards that are reasonable asks of users. For example, when style guides for Typescript and Javascript say to avoid using var, I agree. When they say they prefer defing new objects with {} and new arrays with [] instead of using new, I agree. Not using " when defining class or object parameters not only makes them easier to identify but takes less effort anyway.

## Who the \*\*\*\* cares?
One of the thing that bothers me most about coding standards, are when they become needlessly picky. For example, the afformentioned style guides insist on using single quotations for string characters. While some languages do actually care about having either single or double quotes, Javascript and Typescript are not among those languages. Why then, should I care which someone uses? As far as I can tell, rules like this exist for the sake of existing. I do not believe it is best practice to make pointless rules.

## Why am I tying my hands behind my back again?
The other big gripe I have with coding standards is that sometimes they force inefficient solutions, or ones that take longer to write. For a smaller example, I point again to the afformentioned Typescript and Javascript style guides. Some (specificlly eslinter) require dot notation for getting the parameter of an object. To be perfectly honest, I actually prefer bracket notation, as I feel I somehow hit fewer errors on the same code written with it instead of dot notation. 

A bigger, more significant example, Typescript style guides will (typically) heavily restrict usage of any or unknown typings. This is understandable in the sense that the point of typing is to avoid typing errors, and the unknown and any types are far more prone to these errors. However there are times when you can easily write a perfectly correct function with an any or unknown type, but sticking strictly to a style guide eats up a long time or in extreme cases forces a different approach to a solution.

I will liken these types of issues to another type of problem that I find plagues the tech industry. Would you use a chatbot to solve a math problem? If you answered with an unqualified yes, I assume you either do not know what a neural network is, or you've already sold your soul (and brain) to Roko's Basilisk. (If you don't know what Roko's Basilisk is, don't bother looking it up. You would be better served looking up Pascal's wager and then getting a concussion.) I claim reasonable people would instead use a calculator. Why would you pick a tool that is ill-suited for a job (more complex and in the AI case, more prone to error) when you have a simpler tool that is more effective and efficient at completing the job at hand?

<img width="400px" class="rounded float-start pe-4" src="../img/codingStandards/lint-roller.jpg">
## -fix is my friend
I want to conclude on a more positive note. There is some unqualified good to come out of playing with coding standards and linters: the smaller problems I have with these tools are fixed with... well adding -fix to the linting. Small insignificant violations like using the wrong quote marker can be fixed automaticly. It allows me to use bracket notation to my heart's desire knowing I can just have the computer do the inferior syntaxing for me. Over all it makes stupid rules just a little less stupid.