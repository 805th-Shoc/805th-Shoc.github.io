# The Steel Cable
a.k.a. spanning cable, guide wire, tracer bullet

Imagine you are standing on one side of a canyon looking over at the other. We need to eventually move a lot of things across that gap, and we’re tempted to start thinking about the grand bridge that will move passenger cars, freight trucks… or maybe even a train! But first, we want to figure out how to string one solitary steel cable across the canyon. That steel cable will help us answer a lot of important questions. How long is it? Where do we anchor these first attachments? Is this the right spot in the canyon?

Sometimes the cable becomes a key part of the eventual bridge, sometimes we keep just one anchor, and sometimes we end up moving the whole thing. It’s better to build the cable and adjust it than wait until you know the perfect location. Furthermore, we ensure that we can always get something across. Once it’s up, we’re never totally cut off from our end goal.

## So, What is a Steel Cable?
The steel cable is generally what the team builds first. It allows the engineering team to start doing valuable work while the details of user value are still being determined. It reduces the risk in the basic project infrastructure. It is a foundational component for the later work of building the minimal user journey or MVP.

A more general way to describe this is: If you draw the architecture diagram, you should have something real that works in every block, even if it doesn’t do anything useful other than accepting a write and returning a read.

While the steel cable is centered around an engineering outcome, other practices (ie. design, product) can get a better sense of what their interest in the steel cable might be from the sections below.

## What Isn’t a Steel Cable?
Features. The whole point of the cable is that you don’t need to know exactly what the user experience is or what they need yet, but you have the basic idea of architecture, so you should set that up first.

Overall, the steel cable analogy doesn’t imply that you need to have everything in place up front; if you aren’t sure you need the cache, you shouldn’t add it. It is expected that the team will have some discussion about what is and is not included.

## Example of a Steel Cable
The steel cable is an exercise in determining technical (ie. infrastructure, tooling) scope and reducing risk. In the [GROWS “tracer bullet” definition](), it says:

“It doesn’t have to do anything more than a “Hello, World” level program, but it needs to have all the pieces working together, from front end to back end.”

The steel cable means that you have data flow set up between all components of the application at an infrastructure level (where infrastructure explicitly includes front end frameworks).

So, for example, you’re building a web application. Based on your initial understanding of the problem space, you believe you will need one load balancer talking to a tier of application servers, talking to a Postgres database AND data in an S3 bucket AND a caching system.

In this case, SHOC defines the steel cable as the minimal infrastructure for:

- a load balancer that is configured to talk to…
- your application servers, which can receive a HTTP request
- S3, which app servers can connect to
- Postgres database, with managed migrations, which app servers can connect to
- your caching system (redis, etc)
- the delivery pipeline (CI) needed to build and deploy the above
- automated deployments to dev and prod

If your application is supposed to write data into those systems, the steel cable means that your application writes 1 record into each system, and reads it back for display to confirm that it works.

Note, this is just one example of a steel cable (in this case, a web app). If you know your application will need a frontend framework, it may involve rending “Hello World” on a React page with a build pipeline for the assets. Or, if you have a mobile app as part of your system, then you’ll want to see the same in an iOS build. Further, if 3rd party integrations are crucial to your application, the steel cable includes creating those connections. What infrastructure is included in your application will be specific to your project and needs.

## What’s the Value?
The primary value of the steel cable is a massive reduction in project risk. It forces you to confront access control, deployment, automation, CI, test infrastructure at the beginning of the project. All of those feel “easy” but in practice are fraught with peril. Plus, once you have something working, it’s much easier to edit it. Your application engineering flow is much smoother if the workflow is

```
“code, test, confirm, commit, watch the robot deploy and validate, repeat”
```

than

```
“code, test, realize you need a DB, swear, try to figure out how to add that in your feature PR, swear some more, shave the yak, look up, it’s 2 weeks later”
```

It’s a form of the “go slow to go fast” heuristic.

## When Do You Build One?
Assuming you have access to the environment, your goal is to complete this by the end of the first sprint. If you think you can’t get it done in the first sprint, then consider whether you’ve over-scoped the cable. Alternatively, it could be a sign of a problem:

- the team lacks training on the selected tools
- lack of access to required systems
- improper team sizing

These issues should be identified and discussed within the team immediately.

This proposed time frame is a guard rail so that teams aren’t spending months building something they think is the steel cable. Realistically, there might be circumstances in which you need more time–but the steel cable should be as simple as possible.

In terms of project timeline, this can often (not always) be parallelized with early discovery phases.

## How Do We Use It?
Once you have the steel cable established, all future changes are iterative: you’re always migrating from a working state to a new working state. A working steel cable web app could be verified by going to https://my-system-steel-cable.foo.bar and having that return an HTML page that looked like:

```
<html>
<head>Hello, world</head>
<body>
<p>I wrote "It worked!" into the database.</p>
<p>I read this value from the database: "It worked!"</p>
<p>I wrote "It worked again!" into S3 at /my-bucket/foo.txt</p>
<p>I read this value from /my-bucket/foo.txt: "It worked again!"</p>
</body>
</html>
```

…the minimal amount to show that it worked: no styling, no extraneous javascript libraries, and renders a simple string component. If you break something, you fix it immediately. No breaks once the cable is built, all future iterations of the application are built from this.

## In Closing
The goal of the steel cable is simplicity – you are just trying to make sure the F/E, B/E, and infrastructure (including deployments) can connect. Nothing more. The value of the steel cable is primarily for the internal team, so that they can make sure the F/E and B/E connect.

By working through the problem space from end to end with small piece of code, we can discover all the as-yet-unknown unknowns. In turn, that will help us ensure we properly scope the MVP. This is incredibly useful when hooking up infrastructure systems in the government space because it is common for the most technical unknowns are in how to hook the systems together/move data from point A to point B.

## FAQ
### What About a COTS Project?
The steel cable is explicitly for building a new application from scratch. Sometimes, however, we are working with COTS or GOTS (Commercial or Government-Off-The-Shelf), like ServiceNow. In those cases, COTS is a box on the architecture diagram. You’re still going to need to figure out the deployment pipeline and, in theory, your COTS solution will need to talk to other services.

### What About Delays in Gaining Infrastructure Access?
We often face delays in gaining access with our clients. We expect the granting of access to be a primary focus of the teams’ stakeholder. The team should implement what is possible given the access available, and find creative solutions to the remaining challenges. For example, if you do not have a GitHub account, maybe it would be possible to use a private GitHub repo and switch when the official one becomes available.