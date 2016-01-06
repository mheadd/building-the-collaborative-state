# Enabling the Enterprise

Its not often that I run across posts about enterprise architecture that get me excited. [This one](https://medium.com/@postenterprise/the-abuse-of-reuse-96b2e0af01a7#.60vib6z9f) – by Tariq Rashid – did. Very much so.

This issue interests me because its one that, as a former state IT executive and policy advisor, I have personal history with. I also believe its an issue that will have great impact on how successful governments are at redesigning services around users, and embracing civic technology and open data.

[The post](https://medium.com/@postenterprise/the-abuse-of-reuse-96b2e0af01a7#.60vib6z9f) presents a novel and compelling view of what an enterprise architecture can be by preaching against one of the central tenants of most enterprise architecture documents – mandated reuse of IT components:

>Reuse of a vaguely similar functions is encouraged or even mandated. These strategies go further and propose the pre-emptive building of big platforms for future reuse. The problem is, this kind of reuse is **wrong and damaging**.

In my experience, many enterprise architecture planning efforts are born out of a perceived need to prevent expensive (and possibly wasteful) investment in disparate IT platforms and systems. Asserting that reuse is bad in this context can be viewed by some as radical – almost heretical – thinking.

## What is Enterprise Architecture?

I don’t have a lot of detailed discussions about enterprise architecture with others in the civic technology community, but the issue is implicit in many of the discussions that open data and civic hacking advocates have.

Why do governments implement technology they way they do? What was the decision process that led to investment in a specific technology or acquisition of a specific system? How is the overall vision for technology investment and management by a government developed, and by who?

Every civic hacker has pondered these questions from time to time.

Before we go too deeply into this issue, it helps to have an understanding of what enterprise architecture is from the perspective of a government IT organization. Ideally, an Enterprise Architecture (EA) Plan – developed, not surprisingly, by an Enterprise Architect – will provide a series of recommendations that can help an organization invest wisely in technology. It should present a coherent vision for IT planning and investment that will guide an organization into the future. Good EA plans help enable the efficient adoption of valuable IT solutions by an organization, and help mitigate the negative impacts of potentially disruptive changes in technology the organization may face in the future.

In practice, many government EA plans are a set of rules that agencies are expected to abide by. Many agency IT staff view Enterprise Architects as hopelessly out of touch with the realities of implementing systems meant to provide front-line services to the public. (The words “Ivory Tower” and “Enterprise Architect” are often muttered closely together in front-line agency circles.) Many EA plans are out of date, in a perpetual state of being updated and are viewed with some level of derision by agency IT personnel and outside IT vendors.

## An Enterprise History

My own, admittedly limited, experience with helping to craft an EA plan stems from my time as a chief advisor to the CIO for the State of Delaware. I was tasked with helping to implement the Governor’s vision for e-government (that’s what we were calling it in those days), which involved work to provide Internet-based access to government information and services. This was a [key objective of the Governor](http://www.govtech.com/featured/Delawares-Dynamic-Minner.html) and an enormous amount of emphasis was placed on moving state services online.

One of the most acute challenges we faced was that some agencies had already started to implement online services before an overarching plan was in place – investing in new solutions to move services to the web, or engaging vendors to build new online applications. Because some of this activity had happened in the absence of a coherent strategy from the central IT organization (where I worked) there was concern that agencies would invest in very different technologies to do things that had significant overlap (e.g., identity management, payment processing, etc.). There was additional concern that at some point these different solutions would become the responsibility of the central IT agency to take care of.

In every government that I have worked for, people invariably tell stories of how agencies with political clout or dedicated funding sources acquire a new (usually non-standard) technology that gets implemented, gains usage or traction with stakeholders and then gets foisted onto the central IT agency for long-term maintenance and upkeep. As a result, most central IT agencies view an EA plan as a way to reign in “those rouge agencies.”

In a way, I took this view as well when I made recommendations for a set of common components to be used for all agency e-government projects. I argued that if we could identify a core set of components that could be used over and over again as new projects got rolled out to the public we would reduce complexity and save money. [This is a shot](https://civicio.files.wordpress.com/2015/03/title-slide.jpg) of the title slide from a presentation I made to state leaders on this subject in 2003 (I’ve had this presentation in a file in my office all these years).

## Prescriptive vs. Enabling Architectures

When I think about how I would design an enterprise architecture today, I think I would make it look and work a lot like [Heroku](https://www.heroku.com/), or [AWS](http://aws.amazon.com/). What I love about Heroku is that it is designed to enable the efficient deployment of apps – you build and deploy things in a way that feels easy and makes sense because the platform is engineered to support it. It enables desired behavior instead of outlawing undesired behavior. If you want to roll your own app monitoring or logging (or whatever else you need for your app) you can do that, but the cost and complexity of your bespoke approach are on you. Alternatively, you can quickly and easily leverage one of the [preexisting add-ons](https://addons.heroku.com/) to support your application and Heroku takes care of the hard stuff for you.

This kind of *enabling* architecture stands in stark contrast to the *prescriptive*, rule-based architectures we see so often in government. Looking back on my old e-government presentation with almost 12 years of additional experience, it’s easy to see the flaws in my approach, and the logic in the recommendations here. I think most people with any exposure to enterprise architecture would immediately see the benefits of what the author is saying, but then why do most EA plans not look like what the author is describing?

I think there are specific reasons why most EA plans look very different than the vision presented here. I also think that if we’re going to get closer to that vision – or another one that provides similar benefits – then we need to understand the reasons for these differences.

## Accounting for Differences

There is an interesting discussion in Rashid’s post about *developing with minimal commitment* and *avoiding sticky contracts*, and while I agree that doing those things would make for more sensible enabling architecture plans (and better IT implementation) the problem I see is that most government procurement processes don’t work this way at all. The procurement process is long, complex and costly – for both vendors and governments – so it promotes stickiness, if for no other reason than to try and provide a return on the investment in the process itself. This design is [not accidental](three-hard-truths-for-government-procurement-reform.md), and there are no easy routes to changing it.

Prescriptive architectures filled with **dos** and **don’ts** for agencies are usually a product of big up front investment in technology platforms and systems. If a state or local government has preemptively invested in a system then there are strong incentives for the adoption of requirements that agencies use this systems (to justify to cost of investment).

IT planning and spending – like everything else in state or local government – are a function of the budget process. Planning, adoption, executing and auditing of government expenditures is a multiyear process that (generally speaking) is a [lousy fit](bizzaro-budgeting-and-public-sector-innovation.md) for the way that we use and consume technology today. *Easy-on-easy-off pay-as-you-go* expenditures are not easily engineered into this process. The current budget process used by almost every state and local government is engineered to support larger, up front expenditures for technology which tend to favor prescriptive architectures filled with rules about what agencies can use (the stuff that’s already been bought and paid for) and what they can’t (everything else).

The public budgeting process generally discourages smaller, iterative funding approaches to IT projects. From a pure self interest standpoint, there are strong incentives pushing project advocates to get as much funding allocated for their project as possible, lest their request get crowded out by competing initiatives. Better to get the biggest allocation possible and, ideally, get it encumbered so that there are assurances it is there if things get tight in the next budget cycle.

In addition, There are a number of actors in the budget process at all levels of government (i.e., legislators) who equate the size of a budget allocation for a project with its importance. This can provide another strong incentive for project advocates to think big – in many cities and states, funding for IT projects is going to compete with things like funding for schools, pension funding, tax relief and a bunch of other stuff that’s probably going to resonate with some pretty vocal constituencies. This can put a lot of pressure on project advocates to push for as much funding as they can. There’s just too much uncertainty about what will happen in the next budget cycle.

This tends to result in the pre-emptive building of big platforms (those for which funding is obtained during the budget process) for future reuse, and the adoption of prescriptive architectures to ensure agencies use them.

An Enterprise Architecture that supports smart investment in technology is critical for governments to reap all of the benefits of service redesign, open data and civic innovation . But the reason that most governments rely on overly prescriptive EA plans and large upfront investment in (ostensibly) reusable components is because state and local government procurement and budgeting processes favor them.

If we’re going to craft EA plans to support innovation, we have to find ways to [reengineer these fundamental processes of government first](built-to-fail).

### Originally published:
March 16, 2015