---
title: Introduction to Documentation
type: docs
bookToc: true
---

# Introduction to Documentation
Documentation is a key part of any sowftware project, but it's often something that many engineers struggle with even when we recognize its importance. Writing well is just as difficult whether it is code or docs,  and both require deliberate effort in order to hone your skills.

Documentation has a positive feedbackloop -- if you have documentation that is well-written, provides real value, and is easy to find, you're much more likely to have people work to keep it acurate and upto date. In contrast, if you have documentation that is inaccurate, hard to read, and/or hard to find, then people will tend to discount the value of documentation entirely -- so they are much less likely to treat it as a key component of your project.

## Documentation Tips
### Make your documentation easy to find
Docs that no one knows about or can't find when they need them are essentially docs taht done exist.  If we want to encourage people to write good docs, we need to make sure we can model good behavior. Some specifics tips for accomplishing this goal:

- Establish strong norms(if not hard and fast rules) about where documentation belongs, preferably in no more then 2 places (eg, a Git repo for technical docs and a Google Drive for design docs).  If people have to look in too many places to find what they are looking for, they will eventually just giveup (and it makes it more likely you'll have many different inconsistent documents for the same thing).
 - Make it easy to find documents in those repos without needing to play a guessing game with keywords (especially since a search for something like "terraform" or "docker" is probably going to give you to many results to be useful).  Provide good tables of contents (they should not be long) and put related documents close to each other topologically.
 - Give documents descriptive, non-generic titles. Giving a document a title like "Docker" or "Alerts" becomes increasingly troublesome the larger your project gets -- if your're using Docker for three different applications and local development, what does the "docker" document refer to?
 - Keep in mind the specific restrictions of your repositories. If you are using a wiki with a table of contents in the left margin that only shows ~20 characters, keep your titles as close to that limit as possible. If you are a Git repo, Make sure the filenames for your markdown douments are also descriptive.

### Make Documents serve a single purpose
A doument that tries to do too manythings ends up doing none of them well. If you are writing a step-by-step how-to on a specific process, avoid going into a deep dive on the involved systems. in addition, keeping your documentation focused will mean individual documents will be kept shorter, which is important if you want people to be able to read easily and find the information they are looking for.

Consider breaking your documentation into a set of distict categories, and make sure the type of document has a very clear in the title (so you could title the document "Runbook: MongoDB Memory Alerts", for instance). Use an [ADR] to define what these types are -- such as:
- How-tos are step-by-step guides to common procedures intended for execution under normal operation. A reader should be able to execute these steps safely when following the document.
- Runbooks are documents intended to be used in concert with alerts that guide troubleshooting and mitigation responses and should include information on issues that users may expect with upstream and downstream services. A reader should be able to preform a quick diagnosis of an alert's underlying causes, or at least rule out any common issues, with the information provided in the document.
- Guides provide a deep dive into how a specific system or service works, woth references to ADRs that illustrate how technical decisions were made on the project. Readers should come away with a strong understanding of how the system works, as well as how to gather more information about the system and its state on their own.

These arent ment to be precriptive; define your categories in a way that works best for your project. However, whatever you decide, the categories should be clearly defined and focused; notice the "what the reader should get from this document" part of the description -- if you cannot adequately summarize what a reader is supposed to get from the document in a single sentance, it is probably too widely scoped.

### Keep your audience in mind always
The most important thing when writing documentation is to remember that you are writing this for someone. It may be new engineeers, it may be people on-call, it may be stakeholders in the c-suite, but whoever they are, you intendfor someone to be reading this at some point in the future.

If you aren't keeping this audience in mind throughout the process of writing your docs,then you are going to miss the mark. Writing a document intended for new engineers and assuming a ton of knowledge will severly limit its utility. Similarly, writing something intended for project leads and spending pages defining common terms they're already familiar with will probably cause them to lose patience and start to skim things over.

### Avoid going overboard with graphics or videos
Often we'll be tempted to add lots of screen shots, diagrams, or other graphics to documentation to try and make things more clear. a well-placed graphic can help -- but to many will make the upkeep of your documentation too difficult, it is much more difficult to edit a graphic (and videos even more so) that to edit text, so use them only when they're worth the added cost in maintainability.

in addition, adding lots of graphics will make it harder to read the text. If people cannot follow from one paragraph to the next (seeing them both on the screen at the same time), this is especially difficult. If you need to use large praphics, use thumbnails and link to the larger version to prevent them from being to distracting. Graphics can also make your docs less accessible, so captions and alt text are important.

### Keep individual documents short -- but not too short
Ther's nothing worse thatn trying to find the one paragraph you need from a 20 page document. In order to avoid this, we should keep individual documents short and focused. Generally, anything more then 4 "pages" (ie, you would need to scroll four full screens to see the whole thing) is going to feel "long" to most readers -- if you go over this length, be aware that a lot of people will resist reading this documentation in a single sitting. This might be acceptable for a thorough technical document, but it's not great for something you're expecting people to refer to regularly.

If your document is something people are going to have to refer to in a crisis, you should consider keepingit even shorter -- no more than two pages. Following the other tips on this page will help you keep your documents short and focused.

One Warning -- if you link to other documents in yours to keep your document shorter, try to avoid sending people down a wikipedia-esque link hole. If you can summarize the information you want people to get from the other document ina sentance or two, you should try to do that (in addition to providing the link for further exploration).

### Get Reviews for your documentation
You wouldn't want to put code in production without a though code review and testing -- you shouldn't expect people to use your documentation before it gets a though review either. SOme tips for reviewing docs:
- Junior Members of your team are great people to have review your docs, since they will likely be using them themost. They aren't usually the best people to write docs though, since they have the least context for them.
- For step-by-step guides, try running the commands. Do they work? Is it safe to runthem? They Should not use real people's usernames or other problems if someone just cut-and-pastes the command!
- Try reading paragraphs out loud. Does the language feel awkward or ambiguous?
- If you're the writer, have the reviewer tell you what they took away from the document -- is it what you wanted them to know? Did they come away with a good mental model of the system you described?

### Miscellaneous
- IF you use graphics, write the caption first then make sure the graphic represents what you want to convey.
- Lists and Tables can be a good way to present information people need in a hurry -- they are easier to digest than paragraphs of text (but may not be best for nuanced information).
- Use an active voice rather then a passive voice whenever possible ("do this thing" not "this thing must be done").
- Put conditionals before imperatives to prevent people from doing something without realizing when they shouldn't ("if not Y, do X",not "do x if not Y)