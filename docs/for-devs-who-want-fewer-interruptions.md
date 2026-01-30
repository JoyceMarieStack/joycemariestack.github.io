# For Developers Who Want Fewer Interruptions — Write Docs That Deflect Slack Questions

It’s every developer’s favorite topic: documentation.

YaY!

I can hear the collective groan from across engineering Slack channels. “Nobody reads the docs anyway!” you say. You’re not entirely wrong but that’s exactly the problem we need to fix.

## The Problem: The Colleague Test

Ask yourself this: is finding and reading the docs faster and easier than asking a colleague?

Let’s do the quick math:

- Reading the docs — 20 minutes of focused effort to find the right stuff and extract what you need.
- Slack to Tom — 3 minutes for a direct answer, zero cognitive load.

Tom is just too good.

The thing is that there is [good science showing](https://dl.acm.org/doi/10.1145/1357054.1357072) that when people are constantly interrupted, they develop a mode of working faster to compensate for the time they know they will lose by being interrupted.

Poor Tom.  

If you want fewer pings, fewer hand-raises, and more time to focus  you need docs that answer questions before they reach you.

This is the “Docs Feedback Loop of Doom”. We skip the docs because it’s easier to ask. Then the docs don’t get updated because nobody uses them. So we keep asking. Tom keeps answering. Tom burns out. Everyone loses.

## The Solution: Docs as Code

A little while back, I co-wrote an Architecture Standard for adopting Docs as Code alongside a Developer Documentation Best Practice.

There are very real pain points developers kept voicing on the topic of documentation:

    “I don’t know what to write.”

    “I don’t have time.”

    “It doesn’t get recognized.”

I am preparing presentations on Docs As Code but in the meantime I wanted to provide frameworks and formulas to help folks get into a good mindset.  

## How to Make Writing Effortless: The 2-Year Test

Let’s tackle the first big blocker: I don’t know what to write.

Here’s the easiest fix — use The 2-Year Test.

Ask yourself:

    *“What are all the problems I’ve solved and lessons I’ve learned over the last two years?”*

Brain dump everything down onto a page:-

- Python and zScaler
- Kafka topic partitioning
- Onboarding a new NeoID client
- Grant privileges to Kafka topic
- Publishing to Backstage
- Data leakage in model training

You don’t need to be an expert. You just need to be a few steps ahead of the next person. People don’t learn best from experts, they learn from peers a little further along the path.

## Add specificity – write for a person in your exact context  

Writing for everyone is challenging so don’t start there.  

There are lots of others in the organization having the same problems that you are having.  

A little while back I was having zScaler issues when working with Python locally.  I searched for zScaler in Confluence and got:

- Certificate issues with zScaler
- zScaler
- zScaler problems
- Dealing with zScaler
- zScaler Issues
- zScaler Linux Issues

The pages that I wish I could have found were:  

- How to set up a Python environment behind zScaler when pip can’t reach PyPi
- How to set up a Python environment behind zScaler when pip can’t be reached as a non Python programmer

And if you can’t think of something from the past, write for your future self instead.

Imagine yourself two years from now, trying to remember how you set up that Python environment behind zScaler when pip couldn’t reach PyPI.  Write that doc today. Future you (and everyone else) will thank you.

## Every Piece of Writing is a List

Great writing is a stack of ideas, easy to capture in lists. Think of a Jenga tower made of “ideas” blocks

    Tech docs, runbooks, or release notes = listing processes, steps, or features

    Incident reports = listing causes, impacts, and solutions

    Knowledge sharing = listing lessons learned and best practices

## Curate, Don’t Preach

You don’t have to teach as an expert. You can simply curate:

    Share tips that made something click.

    Note mistakes you’ll avoid next time.

    Summarize decisions you respect and why.

    Capture lessons you’re still testing.

That’s how we all learn especially in fast-moving fields like AI. Everyone’s figuring it out together.

So don’t write to impress. Write to express what you’ve learned.

Because when you write docs that answer real questions, you won’t just save time —
you’ll save Tom from another Slack ping.
