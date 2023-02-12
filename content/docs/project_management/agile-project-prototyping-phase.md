# How the Prototyping Phase Works

Prototyping is where you [try out different solutions to the problems](https://dwpdigital.blog.gov.uk/2016/02/19/learning-through-prototyping-tools-for-universal-credit-claimants/) you learned about during discovery. Prototyping is done using the [steel cable](/docs/project_management/the-steel-cable) work as a foundation.

Spend this phase building prototypes and testing different ideas. And do not be afraid to challenge the way things are done at the moment: this is a chance to explore new approaches.

You do not have to prototype the user’s entire wider journey.

You might not even want to prototype all of the transaction or element you’re working on: often it makes sense just to focus on the areas you think will be most challenging. This lets you do the minimum you need to test your riskiest assumptions.

With any idea or prototype you try out, build things that are just complex enough to let you test different ideas, not production quality code. Expect to throw away any code - and lots of the ideas you test - at the end of alpha.

By the end of prototyping, you should be in a position to decide which of the ideas you’ve tested are worth taking forward to beta.

The prototyping phase tend to last between 6 and 8 weeks. At the end of this, you should do an assessment to determine if the effort was successful enough to move on to the beta phase.

It’s okay to decide at the end of your discovery that you do not think it’s worth moving head into prototyping.

## Focus on testing your riskiest assumptions

A crucial part of prototyping is [identifying your riskiest assumptions and testing them](https://hackernoon.com/the-mvp-is-dead-long-live-the-rat-233d5d16ab02). What these are will depend on the service you’re building. For instance, on SABER, we needed to test our methods of talking to third parties for identity verification, because we wanted to use step functions, an AWS product we hadn’t used before. We prototyped this by rigging up a step function to ping a simple API (in this case, a weather API) just to make sure we understood how this worked.

If you are constrained by legislation, you will need to find out if there are feasible ways of accomplishing your goals within the current legal framework, or if you will have to reduce the functionality to work within the limits of legislation. You could also articulate what would be possible if there were legislative changes.

## Things to pay attention to at alpha

There are a couple of points in the [Service Standard](https://www.gov.uk/service-manual/service-standard) you’ll want to pay particularly close attention to at this phase.

## Solving a whole problem for users

One of our goals for any feature is to solve a whole problem for a user.

In prototyping, this could mean showing:

- how you know that you’ve got the scope of your part of the journey right
- you’ve looked at the wider user journey your service is part of
- you have a sense of what would need to happen to make the journey as a whole work as well as possible (in particular, you’re able to talk about other services that are part of the same journey, and the opportunities and challenges involved in making changes to those services)
- you’re working in the open, and are collaborating with stakeholders and other contractors working on related projects that are part of the journey where it makes sense to do so
- you understand any constraints with legislation, contracts or technology that impact on your service
- you’re planning to minimize the number of times a user has to submit the same information into the system

## Getting the scope of your part of the journey right

Getting the scope of a transaction right is probably the most important part of making it simple to use. Use prototyping to explore [what scope makes sense from the user’s point of view](todo).

### Joining up with the user’s wider journey

Not all transactions are part of a wider journey for the user. But if yours is, you should have explored that wider journey as part of discovery.

You could bring a rough journey map (or similar artifact) to your prototyping assessment, showing [where your service sits in the user’s journey](todo), the different organizations involved and the different channels people use to access them.

If one of your riskiest assumptions is that it’s possible to make changes to other services in order to provide the user with a simple, intuitive journey, use the prototyping phase to test that assumption by talking to the people responsible for those other services. By the end of prototyping, make sure you’re clear what can be changed and how difficult or costly it would be to make those changes.

If you face any blockers collaborating within the client organization or elsewhere, you need to show how you’re addressing them, for example by building relationships with potential collaborators.

Either way, you should be talking and building relationships with your client and other stakeholders, as well as other people working in the same space, such as the [Digital Service Coalition](https://digitalservicescoalition.org/#/).

### Dealing with constraints

Use the prototyping phase to explore any immovable constraints in legislation, contracts or legacy technology that affect the service you’re planning to build. By the end of prototyping, you should be able to explain:

- how you’ll create a service that meets user needs while working within these constraints.
- where they’re the type of constraints that can be removed over the long term and the organization’s plan for doing this. For example, by changing a technology platform or contracting with suppliers in a different way.

### Working in the open

During prototyping, you should continue to talk with your team, your project, and your practice about the prototypes you’re building and what you’re learning from them. This could be done in a weekly demo, a shared document, or even a Slack thread. Consider if it’s worthwhile to distribute this wider in a more formal environment, like an OTT.

### Reusing users’ information where possible

It’s often the case that, when interacting with related services, user data might already be available in some format within the service.

Use the prototyping phase to investigate whether you can reuse that data, so that users do not have to provide the same information multiple times as they move from task to task. Unless there are public policy, trust or legal reasons not to share data, you’ll be expected to show how you’re working towards sharing it.

## Providing a joined up experience across different channels
Your feature or service will need to work well across all the channels a user might use to access it.

This involves understanding how the online and offline parts of your service link together and any pain points users experience as a result of this.

You could work towards this in prototyping by:

- including offline elements like letters in your prototyping experiments and user research, especially where this relates to a risky assumption (for example, that you’ll be able to change the content of letters)
- considering user journeys that start within a third party organization, like referrals
- inviting feedback from other members of your practice during the prototyping – they’ll have a really useful perspective on what the riskiest assumptions are

## Making sure everyone can use your service

With an online prototype, you cannot apply the full range of technical accessibility tests you’d use for production code. But you should be able to show that you:

- understand the [WCAG accessibility principles]() – this will help you identify and test any specific accessibility challenges you’re likely to face with your service
- are including disabled people in your user research

By the end of prototyping you should have a plan for how you’re going to tackle accessibility at beta.

You should also be able to show that you’ve considered inclusion in the wider sense, where applicable to your target audience. For example, this may mean:

- you’ve thought about whether there are likely to be pain points for particular groups of people when accessing the service (for example, if you’re asking for someone’s permanent address and your users include homeless people, you’ll need to show that you’ve got a plan to stop them being excluded)
- including people with low levels of digital confidence in your user research

## Deciding whether to move on to beta

Prototyping is finished when you’ve got a prototype that’s substantial enough to help you make a decision about whether to move on to the [beta phase]() or not.

To move on to beta you’ll need to be confident that:

- you can create something that meets users’ needs and is cost-effective
- you’ll have the budget and people necessary to deliver what you need to

You should be able to explain how you came to this decision using the success metrics you identified at the end of discovery.

If you get to the end of your prototyping and you’re not confident you could do these things, you could stop altogether or decide to repeat discovery or continue prototyping.

## Other things to consider at prototyping

When you’re confident you want to move on to beta, your project team and client should start working on a product brief. This should include an assessment of whether your team has the right people for success.

There are a few other things that you’ll need to consider in this phase. You’ll need to show that you’ve started to think about:

- the sorts of programming tools you’d like to choose for beta and why you’d get value for money
- how you’ll identify threats to your service, how you’ll deal with them and how you’ll stay up to date with threats
- whether or not you’ll open source your code; SHOC has a preference for doing this where possible, but it may depend on the client
- whether or not you’re going to be using common platforms
- how your users would be affected if your service had technical problems

You should also continue to refine the metrics you’ll use to [measure how successful your service is](https://www.gov.uk/service-manual/measuring-success).

If you’ve created any new design patterns - or learned anything useful about an existing design pattern - you should share what you’ve learned in the SHOC playbooks.

Related guides
You may find these guides useful:

How the discovery phase works
How the beta phase works
How the live phase works
Retiring your service
Source Credit: This content is an edited reprint from the GOV.UK Service Manual under the terms of the Open Government Licence v3.0.