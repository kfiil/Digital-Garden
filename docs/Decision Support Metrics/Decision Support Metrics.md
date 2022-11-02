# Decision Support Metrics
Defining metrics, we need to ensure they are actionable and it is clear what kind of leadership decision we would make based on the metric. If the metric is not actionable and a change in it will not trigger a leadership decision, they are likely vanity metrics that provide little useful information.

For each Decision Support Metrics we consider establishing, we should be able to answer: What action(s) would we take based on this metric?

- [[Project Health]]
- **Throughput / productivity** (Nr of deploys, nr of releases, WIP(open pull requests, tasks in doing etc), code review turnaround time, time to open pr, pr size, pr age, lines changed Distribution of Run, improve, Change, )
- **Software delivery performance** (fx deployment frequency, lead time for changes, time to restore, change failure rate)
- **Project / service / domain health** (support tickets, log errors, CVE, availability, latency, throughput, error budgets)
- **Squad / Lunar tech health** (reviews, reviews across, eNPS)

# “When a measure becomes a target, it ceases to be a good measure.”
Peter Drucker said “if you can’t measure it you can’t improve it,” but he didn’t mention the second-order effects of that statement. What changes after people get used to the measurements? What if we measure things that are only partly relevant to what we’re trying to improve?

Tracking metrics can tell us something new, but can also create problems. 

> When a measure becomes a target, it ceases to be a good measure.
> “Any observed statistical regularity will tend to collapse once pressure is placed upon it for control purposes.”

## Sources
- Podcast [Complex systems & second-order effects The Changelog: Software Development, Open Source](https://changelog.com/podcast/474) 
-   [A New Morality of Attainment (Goodhart’s Law)](https://unintendedconsequenc.es/new-morality-of-attainment-goodharts-law/)
-   [The Cobra Effect Redesigned (Examples & Antidotes)](https://unintendedconsequenc.es/the-cobra-effect-redesigned/)
-   [The Cobra Effect (Part 2)](https://unintendedconsequenc.es/the-cobra-effect-part-2)
-   [Uncertainty Saves Lives – the Peltzman Effect](https://unintendedconsequenc.es/uncertainty-saves-lives-peltzman-effect/)

## Four and More Types of Goodhart

One of the best papers digging into variations of the metric and goal problem is [Categorizing Variants of Goodhart’s Law](https://arxiv.org/abs/1803.04585 "Categorizing Variants of Goodhart’s Law"), by David Manheim and Scott Garrabrant. Their paper outlines four types of Goodhart’s Law and why they happen.

**Regressional**. When selecting a metric also selects a lot of noise. Example: choosing to do whatever the winners of “person of the year” or “best company” awards did. You might not see that the person was chosen to send a political message or that the company was manipulating numbers and will fall next year.

**Extremal**. This comes from out-of-sample projections. When our initial information is within a specific boundary we may still want to project what could happen out of the boundary. In those extreme cases, the relationship between the metric and the goal may break down.

**Casual**. Where the regulator (the intermediary between the proxy metric and the goal) causes the problem. For example, when pain became a 5th vital sign doctors were measured by their ability to make their patients more comfortable. If doctors start to prescribe pain medication too often or too easily they may increase addiction.

**Adversarial**. Where agents have different goals from the regulator and find a loophole that harms the goal. For example, colonial powers wanting to decrease the number of cobras in India or rats in Vietnam and paying a bounty for dead cobras or rat tails. People discovered that they could raise their own cobras to kill or cut off rat tails and release the rats. This is known as the [Cobra Effect](https://unintendedconsequenc.es/the-cobra-effect-redesigned/ "Cobra Effect").


# Types of metrics (DevOps Handbook)

### Business level

Examples include the number of sales transactions, revenue of sales transactions, user signups, churn rate, A/B testing results, etc.

> Our goal is to have every business metric be actionable—these top metrics should help inform how to change our product and be amenable to experimentation and A/B testing. When metrics aren’t actionable, they are likely vanity metrics that provide little useful information—these we want to store, but likely not display, let alone alert on.
> 

### Application level

Examples include transaction times, user response times, application faults, etc. Infrastructure level (e.g., database, operating system, networking, storage): Examples include web server traffic, CPU load, disk usage, etc.

### Client software level (e.g., JavaScript on the client browser, mobile application)

Examples include application errors and crashes, user measured transaction times, etc.

### Deployment pipeline level

Examples include build pipeline status (e.g., red or green for our various automated test suites), change deployment lead times, deployment frequencies, test environment promotions, and environment status.

### APPLICATION AND BUSINESS METRICS

At the application level, our goal is to ensure that we are generating telemetry not only around application health (e.g., memory usage, transaction counts, etc.), but also to measure to what extent we are achieving our organizational goals (e.g., number of new users, user login events, user session lengths, percent of users active, how often certain features are being used, and so forth). For example, if we have a service that is supporting e-commerce, we want to ensure that we have telemetry around all of the user events that lead up to a successful transaction that generates revenue. We can then instrument all the user actions that are required for our desired customer outcomes. These metrics will vary according to different domains and organizational goals. For instance, for e-commerce sites, we may want to maximize the time spent on the site; however, for search engines, we may want to reduce the time spent on the site, since long sessions may indicate that users are having difficulty finding what they’re looking for.

In general, business metrics will be part of a customer acquisition funnel, which is the theoretical steps a potential customer will take to make a purchase. For instance, in an e-commerce site, the measurable journey events include total time on site, product link clicks, shopping cart adds, and completed orders.

**Our goal is to have every business metric be actionable—these top metrics should help inform how to change our product and be amenable to experimentation and A/B testing.** When metrics aren’t actionable, they are likely vanity metrics that provide little useful information—these we want to store, but likely not display, let alone alert on.

Ideally, anyone viewing our information radiators will be able to make sense of the information we are showing in the context of desired organizational outcomes, such as goals around revenue, user attainment, conversion rates, etc. We should define and link each metric to a business outcome metric at the earliest stages of feature definition and development, and measure the outcomes after we deploy them in production. Furthermore, doing this helps product owners describe the business context of each feature for everyone in the value stream.

By radiating how customers interact with what we build in the context of our goals, we enable fast feedback to feature teams so they can see whether the capabilities we are building are actually being used and to what extent they are achieving business goals. As a result, we reinforce the cultural expectations that instrumenting and analyzing customer usage is also a part of our daily work, so we better understand how our work contributes to our organizational goals.

# Forming Your Error Budget

In order to base these decisions on objective data, the two teams jointly define a quarterly error budget based on the service’s service level objective, or SLO (see [Service Level Objectives](https://sre.google/sre-book/service-level-objectives/)). The error budget provides a clear, objective metric that determines how unreliable the service is allowed to be within a single quarter. This metric removes the politics from negotiations between the SREs and the product developers when deciding how much risk to allow.Our practice is then as follows:

- Product Management defines an SLO, which sets an expectation of how much uptime the service should have per quarter.
- The actual uptime is measured by a neutral third party: our monitoring system.
- The difference between these two numbers is the “budget” of how much “unreliability” is remaining for the quarter.
- As long as the uptime measured is above the SLO—in other words, as long as there is error budget remaining—new releases can be pushed.

For example, imagine that a service’s SLO is to successfully serve 99.999% of all queries per quarter. This means that the service’s error budget is a failure rate of 0.001% for a given quarter. If a problem causes us to fail 0.0002% of the expected queries for the quarter, the problem spends 20% of the service’s quarterly error budget.

# Measure Productivity

## CannotMeasureProductivity

[https://martinfowler.com/bliki/CannotMeasureProductivity.html](https://martinfowler.com/bliki/CannotMeasureProductivity.html)

## Code diff a day

The “Code diff a day” idea is that you on average should have created and landed a diff per day. This is a rule of thumb, so some days you might have less and some days you might have more. Thus the average part is important.

Handling a diff a day carries a bunch of benefits:

1. Cadence By aiming for a diff a day you get into a good rhythm of creating diffs, get them reviewed and landed every day. This also means that incrementally Uber will benefit from your code faster, as with a diff a day you make smaller steps and these get faster into production.
2. Reviews With a diff a day you also ensure that your reviewers are happy, as a day worth of code tends to be fairly quickly reviewable (e.g., compared with a week’s worth of code). When code changes are relatively small they tend to be faster reviewed, thus you are not blocked on code review for a long time. All in all, a win-win for you and your code reviewers.**
3. Planning No matter if the feature I work on is big or small, the “a code diff a day” idea forces me to break it into pieces that I can do in a day. And these pieces also include tests and proper test coverage, thus when planning I include the time for testing and verification.

Obviously, this idea can be misused. You could keep changing your favourite log statement to keep a high diff count, but such changes do not matter to Uber’s perspective. Thus don’t apply this idea naively. On the other hand, if you’re in doubt, I would much rather get two smaller diffs to review (e.g., 50 - 100 lines), than one big (e.g., 100-200 lines). Note that these line counts include tests, though tests are typically easier to read and thus I would rather read 100 lines of test code, than 100 lines of logic.

I tend to feel bad working on a diff where I have put more than a day’s worth of coding into, as I know it will be harder (read: take longer) to review. Thus I try to plan such that every diff I send out, is for a single feature that takes at most a day to code. If it turns out I overestimated and that the diff only took e.g. half a day, then I’ll still send out this diff for review. It also means that if I underestimated the effort I try to remove features/branches, to ensure that I stay within a day’s worth of code in each diff.

- Small CLs: [https://google.github.io/eng-practices/review/developer/small-cls.html](https://google.github.io/eng-practices/review/developer/small-cls.html)
- How to do a code review: [https://google.github.io/eng-practices/review/reviewer](https://google.github.io/eng-practices/review/reviewer)/
- Joakims test rant: [https://github.com/recht/rants/blob/master/testing.md](https://github.com/recht/rants/blob/master/testing.md)