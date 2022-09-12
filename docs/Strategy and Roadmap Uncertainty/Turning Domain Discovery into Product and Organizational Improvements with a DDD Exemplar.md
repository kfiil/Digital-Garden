---
read: 2022-09-09
source: https://medium.com/nick-tune-tech-strategy-blog/turning-domain-discovery-into-product-and-organizational-improvements-with-a-ddd-exemplar-9e759c365a9e
---
# Turning Domain Discovery into Product and Organizational Improvements with a DDD Exemplar
One of the challenges I see regularly is inertia following domain discovery workshops. Techniques like big picture [event storming](https://github.com/ddd-crew/eventstorming-glossary-cheat-sheet) are great for mapping out the business and visualising problems and opportunities, but that’s where progress can easily get stuck. How do you go from event storm to product and organizational improvements?

I recommend mapping out your domains on a [core domain chart](https://github.com/ddd-crew/core-domain-charts), exploring how you could evolve each domain, and creating a [scorecard](https://medium.com/nick-tune-tech-strategy-blog/sequencing-architecture-modernization-risk-averse-vs-risk-tolerant-e74191e39c34) to decide which you should invest in.

Often, companies want to combine improvements to their products with improvements to their operating model and ways of working. In my work, people usually want to introduce DDD practices into their ways of working. I recommend running a DDD Exemplar project.

A DDD Exemplar is a project, ideally achievable within a quarter, that results in improvements in a domain(s) and improvements in how teams build products. The goal of an exemplar is to show how DDD can be applied within a specific organization. It lays the foundations for other teams to copy and adapt. It’s a proof-of-concept for how teams build products.

> You don’t have to call it a “DDD Exemplar” in your organization, you’re welcome to use any name you prefer.

Why Things Get Stuck After Discovery?
-------------------------------------

In companies with many teams and many millions of lines of code, including a lot of legacy, there are endless things that can be improved in the product, software, and organization. Choosing what to focus on is a big decision and the wrong choice can have major implications for the business and the individual.

People also worry about making the wrong decisions and having to abandon them. It’s extremely frustrating as an engineer to work on something which is cancelled and to switch focus to something else. You expect the new project to be cancelled and it’s hard to become motivated.

Some technology leaders feel like they don’t have the experience and skills to confidently lead major technology and organizational modernizations. They are used to managing on a smaller scale but the company has grown and they’re outside their comfort zone.

Another hurdle to decision making is when technology leaders feel that the skills needed to deliver big changes don’t exist within the organization like the lack of DDD, architecture, or cloud skills.

Choosing where to focus is a balancing act: delivering new products, fixing legacy software, and improving engineering culture. Different stakeholders usually assign different levels of importance to each of those needs, creating a conflict which also blocks progress on making a decision.

If you are facing any of these challenges, I hope that the following suggestions can help you make progress.

Evolving the Domain Landscape
-----------------------------

A primary purpose of domain discovery techniques, like big picture event storming, is to map out the current state of the landscape, capturing concepts like business processes, socio-technical structures, and roles like customers and colleagues.

Any change you want to make to your product portfolio, internal or external- facing, is going to change your domain landscape. You’re going to invest in one or more domains to make them more differentiating or reduce operating costs.

After domain discovery, I recommend mapping out your domain landscape using a [core domain chart](https://github.com/ddd-crew/core-domain-charts), and exploring possible evolutions. The purpose of this activity is to visualize options, moving from discovery towards action.

To create a core domain chart, start by placing each domain where you believe it currently lives on the chart. There are a few [patterns](https://medium.com/nick-tune-tech-strategy-blog/core-domain-patterns-941f89446af5) which can help you. Measuring the differentiation and complexity of each domain is not trivial, so it’s good to seek feedback from product and engineering people in each domain.
![[1 ZivHZQT9f4GCHJDIMIL6Jg.jpeg]]

Start by mapping out the current state of your domains

> If you’re not sure what your domains are, I have created a [Strategic DDD Kata](https://medium.com/nick-tune-tech-strategy-blog/strategic-domain-driven-design-kata-delivericious-b114ca77163) which provides a scenario for you to practice designing domain boundaries. You can apply the same techniques to your own landscape.

Exploring Options
-----------------

When your domains are laid out on the core domain chart, you can begin to generate delivery options. For each domain chart on the chart, explore how you could evolve it by adding an arrow(s).

Domains can be evolved generally in two directions. You can move them to the right of the chart to make them more differentiating. Usually, this is correlated with an increase in complexity, because to make a domain more differentiating you need to develop greater expertise and capabilities in that area.

Domains can also be evolved downwards. This signifies removing complexity. The goal of removing complexity is usually to reduce the operating costs of a domain or improve the reliability.
![[Turning Domain Discovery into Product and Organizational Improvements with a DDD Exemplar 1.jpeg]]

Creating options: exploring possible evolutions of your domain landscape

In some domains, the existing software may be overly-complex and hard to evolve. You may want to show an arrow going down, and then an arrow moving to the right. This implies that you need to clean up the existing solution before you can add differentiating new capabilities.

![[Turning Domain Discovery into Product and Organizational Improvements with a DDD Exemplar 2.jpeg]]

Sometimes you need to reduce unnecessary complexity before exploiting new complexity

Complexity
----------

As you can see, there are different types of complexity. Some complexity we embrace because there is an opportunity to differentiate, whereas some complexity is providing little or no value and is simply making our systems more complex and expensive to maintain.

It’s also possible to exchange complexity. The example I see most often is complex manual processes (_Operational Complexity_) involving multiple people, excel spreadsheets, and a variety of tools. By automating these processes with software, the software gets more complex, but the manual processes become less complex.

It can be tricky to capture the nuance of exchanging complexity on a core domain chart. It all depends on how you define the y-axis. I use _Model Complexity_, which means the effort required to learn the domain, model it in software, and maintain the software. This doesn’t include the complexity of manual processes so I would show an arrow going up with a small note.

![[Turning Domain Discovery into Product and Organizational Improvements with a DDD Exemplar 3.jpeg]]

Adding complexity to the software domain model to reduce operational complexity (e.g. manual processes)

DDD Exemplar
------------

Mapping out your domain landscape provides options. The next step is to make an investment decision: which of the proposed improvements to increasing differentiation or removing complexity should you choose?

I recommend creating a scorecard which scores each option against criteria that are most important to you. I have a [separate post](https://medium.com/nick-tune-tech-strategy-blog/sequencing-architecture-modernization-risk-averse-vs-risk-tolerant-e74191e39c34) on this topic.

One of the common scenarios I deal with is organizations who not only want to evolve their landscape but also improve their ways of working and DDD expertise. In these situations, I usually recommend a DDD exemplar.

A DDD Exemplar is a project which will evolve the domain landscape in a meaningful way, while also upskilling a team with DDD techniques. The most important aspect of a DDD Exemplar is that it will provide the foundations of an organizational model that can be applied to other teams if successful.

Choosing a DDD Exemplar
-----------------------

When looking at the domain landscape for options that would be suitable as a DDD Exemplar, there is no specific rule on which to choose. It could be adding differentiation to a core domain or reducing complexity in a supporting domain.

Here’s one example of a domain evolution which was a good fit for a DDD Exemplar. There is a good balance of business, technology, and organizational improvements.

*   Current process is highly manual involving 20+ people scattered across different teams. Big picture event storming can be used to map out the current process, and help to build a lasting collaborative approach between product, engineering, and other disciplines.
*   The future automated process needs to be carefully designed, not just a a copy of the existing manual process. Another chance to use collaborative DDD techniques, this time for designing new processes.
*   The domain has a number of intricate challenges which will provide the team with a great opportunity to practice and improve their software domain modelling skills.
*   The domain is a supporting domain but is a key enabler of existing and future core domains. Removing the operational complexity would make it easier to support future changes in core domains.
*   A meaningful outcome can be delivered within a quarter which would be satisfying for business stakeholders — the new process will free up a lot of time and result in less support cases.

One piece of advice: choosing the right people for an exemplar is key. It’s not a place for sceptical senior engineers who think they know everything, it is a place for people who like learning and working collaboratively, and sharing what they’ve learned with other teams.

If you like concepts in DDD but you’re not sure how it all fits together, the [DDD Starter Modelling Process](https://github.com/ddd-crew/ddd-starter-modelling-process) is my recommended place to get started. It can guide you through your first few cycles of discovery, strategy, and implementation and then you’ll be in a good place to guide yourself.

Building the Narrative
----------------------

Building a narrative is important for at-least two reasons. The first reason is to sense-check your plans: does your proposal for a DDD exemplar make business sense, or is it driven by personal interest in the domains you are personally most interested in evolving?

The second reason is that you may need to sell the idea to get buy-in and investment to run with it. I’ve seen a lot of good ideas fail to get off the ground because they weren’t pitched in the right way.

My advice is to use Simon Wardley’s Strategy Cycle as the basis for your narrative. You don’t need to reference the cycle in your narrative, but I recommend loosely following the structure.

![[Turning Domain Discovery into Product and Organizational Improvements with a DDD Exemplar 4.jpg]]
The Strategy Cycle. Credit: Simon Wardley

Starting with purpose, what is your organization trying to achieve? What are the most important challenges or opportunities your company is facing?

Two companies I recently spoken to were facing a similar challenge: they had made a major pivot in their business model and were forging a new industry. They had validated the concept and taken on a large amount of funding. While exploiting the new business models they also needed to scale their organizations. This is the type of business context I would use to begin the narrative.

The second part of the narrative is the landscape. For this, you can use the core domain chart you created of the current state. You’ll need to add details around the core domain chart but the diagram can summarize the current and possible future states.

The third part of the narrative is the climate. How is your landscape evolving based on external pressures? Your core domain might be moving left because your competitor’s have launched a new innovation that renders yours obsolete.

The fourth part of the narrative is doctrine. This focuses on how your organization is operating. In your narrative for a DDD exemplar, you may want to highlight weaknesses in certain DDD practices, like collaborative design, that the organization must improve if it wants to achieve its purpose.

When organizations scale, the costs of inefficiencies in how they work are amplified. I include this type of information to stress the importance of doctrine.

The final part is leadership. This is the possible evolutions on your core domain chart and your proposal which may be a DDD exemplar or something else.

I recommend that a good proposal outlines the why and talks a little bit about the how. How are you going to approach the problem? How are you going to put the right people in place? How are you going to measure success?

I try to make it as easy as possible for management to realise it’s a good idea, that has been well planned out so they can just say “yes”.

In Reality…
-----------

I’m not advocating that you follow every step in this article in order and propose a DDD exemplar. Every company has a unique context of challenges, goals, and people that there is never simple a recipe for making good strategic decisions.

What I wanted to emphasise in this article is that I see a lot of teams getting stuck after domain discovery and not knowing what to do next. I’ve outlined the general approach I use: map out the domain landscape, identify possible evolutions, build a narrative, and use a DDD Exemplar if you’re trying to introduce a DDD approach into your organization.

I hope this approach can give you inspiration to help you break the post-discovery inertia. Please feel free to leave a comment or contact me directly if you have any questions or want to add to the discussion.