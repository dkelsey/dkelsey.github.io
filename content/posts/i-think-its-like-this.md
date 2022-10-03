---
title: "I Think Its Like This"
date: 2022-10-02T19:22:24-07:00
draft: true
---

My musings on the state of affairs at DataBC.

## Historically
* They followed the Gov's higherarchical command and controll organization.
* They have technical people manage projects and pay vendors to do the work.
* Projects are deliverred to the spec defined by the stakeholder.
* They, like everyone else, is excited and eager to adopt new technology.  

## When I joined
I joined as the two senior systems people, Operations people, parted.   
The culture valued technical solutioning, building, solving challenges quickly.

When I started I became accoutable for the successfull operation of: 
* 27 production critial line of business Tomcat applications, 
* The Kong API Gateway, which was both an experiment, and a critical line of business application - GDX's analytics team ran the Corporate Enterprise Analytics platform through the Gateway.

These services were unsupportable.
Not a single piece of documentation existed containing required information necessary for a skilled technician to operate any of these servers.

* No synopsys of what each service did; no context.
* No definition of the criticality of the service.
* No list of key contacts, stakeholders, clients.
* No pointers to sources of documentation.
* No description of where the service ran, nor how to successfully stop or start the service.
* No list of test cases or test data that can be used to assess the successfull operation of these service.
* No description required skills or privileges necessary to manage or exercise the service.

I would say it was even worse than this as, there were a number of undocumented, unfinished, "creative solutions" pepperred throughout the infrastructure, taking advantage of, at the time, bleeding edge technology.  All untouched by anyone for a few years; Unknown by anyone.

## I realized a few things
1. No one was left who was around when these things were built and deployed.
2. I was left holding the bag.
3. Any colleagues, and anyone after me, would be in the same situation.
4. I had do to something.

# I think it's like this

I'm drawing from "uncle Bob's Clean Code" talk.

He describes how, with a green field project programmers can move like lighning and acheive amazing things quickly.
As time progresses and the code base grows, it becomes harder and harder for the programmers to add features and fix bugs.

Whey?

Bob describes the senario:

How many of you have experience this:

you work on a hard problem and you try a bunch of things and eventually you get it to work.  
You yell "no body tough it! Quick check it in!"

You congratulate eachother, and move on.

Fixing the problem is not finishing.  
Your next task is to "clean" the code.  Re-write, refactor, so that the code makes sense, does what it's supposed to do, is maintainable.

Long digression but...

What we had at dataBC was a whole bunch of systems that were wrestled into working order, and never cleaned.

Where is the supporting documentation?

## My solution

I have been reading about Site Reliability Engineering.   I have a track record of working at places and finding that nothing is written down.   Every aspect of the software development work is ad hoc, who's success is dependant on heroic effort of individuals.  

1. I started Operational Playbooks.
2. I started to record every incident in JIRA tickets.
3. I started Blame-Free Post Incident Reviews
4. I started regular "sharing sessions" where I explained my understanding of how things worked - and reviewed docmentation.
5. I made initiating and continuously revising documentation part of my job.

I did this for 3 years, not just in the last two weeks as I was heading out the door, as our directory of technology stated.

# My Point

## I see a recurring pattern in organizations

1. One hero, with skills and tallent, tackels the hard problems.
2. They are successfull at first, for a while.
3. The continue to get more and more thrown at them.
4. Eventually, they max out; they can't do more, they are spending all their time "servicing interrupts".

Management, sort of wakes up, scratches their head, and tries to figure out "why is this person so slow?"

I guess we need to hire more people. 

Management wants to Scale the services; they want to ...

Is' a bit of the capability maturity model.

### Initial 
* The software process is characterizes as _ad hoc_, and occasionally even chaotic.  Few processes are defined, and success is dependant on individual effort and heros.

They are all stuck in the Initiation stage of the CMM.