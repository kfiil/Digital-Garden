# Strategy and Roadmap Uncertainty

## Content
1. [[Strategy and Roadmap Uncertainty#Strategy|Strategy]]
2. [[Strategy and Roadmap Uncertainty#Domain|Domain]]
4. [[Strategy and Roadmap Uncertainty#Roadmap|Roadmap]]
5. [[Strategy and Roadmap Uncertainty#High-performing Team|High-performing Team]]
6. [[Strategy and Roadmap Uncertainty#Concerns|Concerns]]
7. [[Strategy and Roadmap Uncertainty#Notes|Notes]]

## Strategy
1. Mapping out domain landscape ([[Turning Domain Discovery into Product and Organizational Improvements with a DDD Exemplar|Domain Discovery & Core Domain Chart]])
2. Make an investment decision - *which of the proposed improvements to increasing differentiation or removing complexity should you choose?*

## Domain
- Domain Discovery - *A primary purpose of domain discovery techniques, like big picture event storming, is to map out the current state of the landscape, capturing concepts like business processes, socio-technical structures, and roles like customers and colleagues.*
- [Core Domain Chart](https://github.com/ddd-crew/core-domain-charts) - *exploring possible evolutions. The purpose of this activity is to visualize options, moving from discovery towards action*
- Business processes / Journey Overview (exisiting and know future ones)

## Roadmap
### Setting Expectations and Delivering on Schedule
Notes [[Strategy and Roadmap Uncertainty#Setting Expectations and Delivering on Schedule|here]]

### Strategies for Handling Roadmap Uncertainty
> Think about how to break down big projects into a series of smaller deliverables so that you can achieve some of the results, even if you don’t necessarily complete the grand vision.

Notes [[Strategy and Roadmap Uncertainty#Strategies for Handling Roadmap Uncertainty|here]]

### Solution Approach
- Building the right thing, building the thing right
- Solution design(user story mapping, event storms)
	- Risk assesment of new initiatives 
- The Software Delivery Mantra
	- Don’t confuse motion with progress
	- Don’t confuse progress with the ability to deliver on time
	- Don’t confuse delivering on time with delivery of the right outcome

### Guiding critical projects
[[Guiding Critical Projects Without Micromanaging]]
- Being outcomes-driven (is the work getting done, with good quality, in reasonable time, without burning out the people involved) is the only way I know how to work.
- I trusted every person individually who was working on it, but I didn’t feel like I understood the details and I was worried that we weren’t asking ourselves the hard prioritization questions often enough. So I started a monthly update meeting.
- [Manage Colony Leadership Team](https://docs.google.com/presentation/d/1eEXQUkkxLC8HUbRRxbek1Xc4xOW__rk5p5ZBwfm0FXc/edit?usp=sharing) The colony leadership team and the squads follow up on the objectives in biweekly meetings

## High-performing Team
- [[Durable teams - The Managers Path, Camille Fournier]]
- [[Debugging Teams - Groundhog Day by Camille Fournier]]
- Questions
	- _How do you know you are doing a good job?_
	- _How do you know you are doing the right thing?_
	- _How do you know whether your colleagues need your help?_


## Notes
### Setting Expectations and Delivering on Schedule 
One of the most frustrating questions that engineering managers get asked regularly is why something is taking so long. We’ve all been asked this question before. We’ve been asked it as hands-on engineers, as tech leads, and as managers of small teams, but the question takes on a whole new level of intensity when you’re managing team managers, because answering it is significantly harder when you aren’t embedded deeply in the details. 
First things first: hopefully you’re being asked this question because something is running over plan by a significant margin. That is the time when it makes the most sense to ask, and when you should do your best to understand the scenario and answer. 
Sadly, we are often asked this question in times when things are not taking any longer than the estimate. We are often asked this question when our leadership, for whatever reason, either didn’t like the original estimate or didn’t ask for it at all, and now they’re upset, despite nothing going wrong. 
==Therefore, you must always be aggressive about sharing estimates and updates to estimates, even when people don’t ask, especially if you believe that the project is critical or likely to take longer than a few weeks. This means you must be aggressive about getting estimates, and as we all know, software estimation is a very difficult process. Negotiating the process that your team uses to estimate, on what timescale, for what projects, may be part of your job at this level.==
Source [[4.  Resources/Books/The Manager's Path]]

### Strategies for Handling Roadmap Uncertainty 
There are few strategies I’ve learned about building a roadmap: 
- **Be realistic about the likelihood of changing plans given the size and stage of the company you work for.** If your startup has a history of changing the year’s plans every summer to account for the business results from the first half of the year, be prepared for a change in the summer, and try not to promise things to your team that would require continuity beyond that point.
- **Think about how to break down big projects into a series of smaller deliverables so that you can achieve some of the results, even if you don’t necessarily complete the grand vision.** Breaking down the technical work will require you to work closely with the product or business managers to figure out how the details should be prioritized. All of you should be aware by now that things will change quickly, so everything must be repeatedly reexamined with an eye toward what’s most valuable right now.
- **Don’t overpromise a future of technical projects.** Don’t promise your team exciting technical projects “later,” because the product roadmap for later hasn’t been written yet. This kind of thinking will get hopes up and then disappoint. If the project is important, get it scheduled now — or as close to now as possible. If the project is not urgently important, you can put it on the backlog, but you should be realistic that once “later” rolls around, there will be a long list of competing priorities from other parts of the business. If you haven’t taken the time to articulate the value of this work, it will get pushed aside in favor of projects that are more clearly valuable.
- **Dedicate 20% of your team’s schedule to “sustaining engineering.”** This means allowing time for refactoring, fixing outstanding bugs, improving engineering processes, doing minor cleanup, and providing ongoing support. Take this into account in every planning session. Unfortunately, 20% is not enough to do big projects, so additional planning will be needed to get major technical rewrites or other big technical improvements. But without that 20% time, there will be negative consequences with missed delivery goals and unplanned and unpleasant cleanup work.
- **Understand how important various engineering projects really are.** Product and business projects usually have some kind of value proposition to justify them. However, the same rigor isn’t always applied when it comes to technical projects. When an engineer comes to you with an engineering project that she wants to do, think about framing the project by answering these questions:  
  
  How big is that project? 
  How important is it? 
  Can you articulate the value of that project to anyone who asks? 
  What would successful completion of the project mean for the team? 
  
  The value of these questions is that you start to treat big technical projects the same way as product initiatives. These projects have advocates and goals, they have schedules, and they are managed like other big initiatives. This is a scary process because there are times when you “know” something is important, but you don’t know how to articulate it in a way that the business will value. Especially given the complex nature of technical projects and the challenge of measuring things like engineering efficiency, you’re sometimes stuck trying to explain technical details to a nontechnical partner who may not totally understand where you’re going or why. My advice is to do your best to gather data to support yourself, and talk about what will be possible when the work is done. If you look at a technical project and realize that you’re proposing a bunch of work for a system that is rarely changed and won’t enable core improvements to your technology or business, it probably isn’t worth the effort. Unfortunately, there is never enough time for all the exploratory engineering, legacy code cleanup, and technical quality improvements your team will want to do, and this process will help you pick your battles.

Source [[4.  Resources/Books/The Manager's Path]]

### The Software Delivery Mantra
#### Navigating Complex Delivery
Developing software with complex requirements or environments with ambiguity can make a team lose their heading. It requires structure to ensure accurate, timely delivery and everyone to be on the same page. In this article, I illustrate the steps I have cultivated in my career to make sure the course of the team is headed in the right direction when they veer off course.

![](https://miro.medium.com/max/1400/1*4skQhSqZ83Xae73EtXu_vw.jpeg)

Credit: Dreamstime.com

#### The Mantra
> — Don’t confuse motion with progress  
> — Don’t confuse progress with the ability to deliver on time  
> — Don’t confuse delivering on time with delivery of the right outcome

#### Motion is not always progress
You could be treading water. The first area of inspection is generally looking to see if the activities of the team align to some direction. Things I look out for:
- lack of clarity on the end goal
- lack of smaller, near term milestones
- a singular focus on activities in the absence of a plan

#### Progress is great, how are we pacing?
If the activities are driving incremental progress in the project, the next area is to see if the pace of work will result in delivery in a timely fashion. The pitfalls to watch out for here are:
- lack of a [work-back plan](https://datou-tech.medium.com/back-stop-buck-stop-timely-software-delivery-9783a1f98dce?source=user_profile---------1----------------------------) or an agile technique to estimate delivery (ie, story point heuristics)
- lack of debate on tradeoffs on all sides of scope, quality and time
- absence of communication and action taken on blockers (ie, clearly calling out dependencies)

#### We are going to make it! Wait… where are we?
This last one is most suited as a first step but when building software in an agile environment, there should be constant evaluation if the goals have changed since development started. Especially long lived initiatives or teams building out large platforms. Things to look out for:
- lack of structured documentation outlining the goals
- lack of community understanding of what the goal is (and explicitly what the goal is not)
- absence of qualitative success metrics

#### Summary
While this article focused primarily on things to avoid, I hope it provides some cautionary signs to help you prevent your projects from heading to the wrong destination or never arriving.

I have heard this phenomena termed “Swirl” also. Here is a bonus doodle:

![](https://miro.medium.com/max/1400/1*ARCbmNisjmJWhLTwGVI1xg.jpeg)