---
title: Authorization to Operate
type: docs
bookToc: true
---

# Authorization to Operate (ATO)
The Official management decision given by a senior organizational official to authorize operation of an information systems and to explicitly accept the risk to organizational operations (including mission, functions, image, or reputation), organizational assets, individuals, other organizations, and the Nation based on the implementation of an agreed-upon set of security controls.

## ATO Overview
Every federal information system must go through NIST's [Risk Management Framework (RMF)](https://csrc.nist.gov/projects/risk-management/risk-management-framework-(RMF)-Overview) before it can be used to process federal information. This process culinates in a signed Authority to Operate (ATO) being issued. Because the ATO process is a complex, multi-step process which will constrain the design and implementation of your systems, you should start thinking about how it applies to your system before you begin designing and implementing it.

### Definitions
- Assessment: The step of the ATO process (and RMF) where the system and package are reviewed by a third party.
- ATO package: The SSP and other documentation needed to get an ATO.
- Authority to Operate (ATO): The approval for the government system to be run in production, and the compliance process for getting there.
- Compliance: Ensuring that a system meets minimum security requirements.
- Information system: a discrete set of information resources organized for the collection, processing, maintenance, use, sharing,dissemination, or disposition of information ([44 U.S.C. 3502](https://www.law.cornell.edu/uscode/text/44/3502#8)).
- POAM: Plan of Action and Milestones. They are the TODOs following and assessment, which are usually low-risk security findings that need to be addressed.
- RMF: The [NIST Risk Management Framework (RMF)](https://csrc.nist.gov/projects/risk-management/risk-management-framework-(RMF)-Overview), which is what most ATO processes are based on.
- Security: The sum of processes and features safeguarding systems and data.
- Systems Security Plan (SSP): The primary document in an ATO package, the bulk of which contians the [NIST 800-53 security controls](https://nvd.nist.gov/800-53/Rev4). "The purpose...is to provide and overview of the security requirements of the system and describe the controls in place or planned for meeting those requirements." ([NIST SP 800-18](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-18r1.pdf#page=7))

### Roles
Roles in ATO process typically include:

- Assessor: Responsible for checking the compliance of systems; sit in an agency's Security team. Validates and verifies that the documented controls (see [Step 3]())actually work, using assessment cases (see [Step 4]()).
- Authorizing Official (AO): Responsible for overall impact categorization and risk acceptance. The AO is ultimately responsoble for determining if the risk of operating the system is acceptable, and if so, issuing an Authority to Operate (ATO) for that system. They often Designate this responsibility to one or more people.
- Information System Security Officer (ISSO): Supports the information security team, consults on control selection, organizes scanning process. Reports to the Information System Security Manager (ISSM).
- Penetration tester(s): Conducts the penetration test after terms are agrees to as a documented in the Rules of Engagement (RoE).
- Program team: Those who are trying to build/launch the system.
- System Owner: The system owner is usually the product lean or tech lead of the project team. They will be named in the ATO documents and are the main contact during the evaluation process that leads up to an ATO.

### FISMA
in the Federal government, the principle law governing the security of information systems is the Federal Information Security Management Act (FISMA). For more information of FISMA, check out the [FISMA Ready introduction](https://github.com/fisma-ready/introduction).

One of the goals of the Federal Information Security Management Act of 2002 (FISMA) is to “provide a comprehensive framework for ensuring the effectiveness of information security controls over information resources that support Federal operations and assets.” The National Institute of Standards and Technology (NIST) was tasked with designing and implementing this framework: the result is NIST’s Risk Management Framework (RMF). All federal information and information systems (except classified information and national security systems) are subject to NIST’s RMF. There’s [an introduction to the RMF on NIST’s website](http://csrc.nist.gov/groups/SMA/fisma/framework.html). A more comprehensive guide, including how to apply the framework, references to the various relevant publications, and definitions of roles and responsibilities, is found in NIST’s [Special Publication 800-37](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-37r1.pdf).

### Re-authorization
Your system may need to be reassessed and re-authorized if your application team is planning to make substantive changes, such as changes to:

- Encryption methodologies
- Administrative functionality within the application
- The kinds of information you store (for example, personally identifiable information (PII))
- The external services used or how/what data flows to/from them
- Anything that will requires an update to the System Security Plan, system diagram, etc.

Example changes that do not require re-authorization, as long as they don’t include the above:

- Features
- Bug fixes
- Interface changes
- Documentation updates

The Authorizing Official determines whether a system needs re-authorization. If you’re planning a change that you think may require re-authorization, contact them.

If it needs re-authorization, follow the usual steps for getting an ATO. You should be able to reuse most of your existing ATO materials, assuming they have been kept up-to-date.

### ATO renewal
Many ATOs are issued with a time limit, often this expiration is between one and three years. When an ATO nears expiration, you’ll need the ATO to be renewed. Follow the usual steps for getting an ATO. You should be able to reuse most of your existing ATO materials, assuming they have been kept up-to-date.

## Types of ATOs
For all federal agencies, the [Risk Management Framework (RMF)](https://csrc.nist.gov/projects/risk-management/risk-management-framework-(RMF)-Overview) describes the process that must be followed to secure, authorize, and manage information systems. The RMF defines a process cycle that is used for initially securing the protection of systems through an ATO and integrating ongoing monitoring.

Authorization to Operate (ATO) - This is the end goal for every system. These ATOs are typically issued for 3 years, at which point they must be recertificed.

Conditional ATO (cATO) - This is usually issued to a system where too many outstanding issues were found. This allows the system to operate while the problems are corrected. These problems are tracked and become conditions that must be met at specific time intervals. cATOs are usually issued for less than a year.

Interim Authority to Test (IATT) - An IATT provides provisional authority to operate during system development. During this time period, teams should be working towards implementing controls and documenting the system for their ATO assessment.

## Steps of the ATO Process
“The ATO process”, as it’s commonly called, is formally defined in the National Institute of Standards & Technology (NIST)’s [Risk Management Framework (RMF)](https://csrc.nist.gov/projects/risk-management/risk-management-framework-(RMF)-Overview):
![OrgRMF](/images/orgrmf.png)
The steps in the process are as follows:

### Step 1: Categorize Information System
The information systems’ owner, working with the AO, categorizes the system based on the potential impact on the organization if the information system, or the information within it, is jeopardized. The system will end up with a category of low, moderate or high, based on criteria described here.

If your system will be providing novel or risky functions, or handling extremely sensitive data, do this as early as possible.

### Step 2: Select Security Controls
“Controls” are individual security requirements laid out by the National Institute of Standards and Technology (NIST). NIST’s encyclopedic [Special Publication 800-53](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r4.pdf) (currently on revision 4) is the definitive guide to security and privacy controls for federal information systems.

Your AO determines which controls need to be implemented. This is generally based on the following:

- The impact level of the system (low, moderate or high). SP 800-53 provides a “baseline” set of controls for each level. The higher the level, the more controls or control enhancements are in scope. For systems running on cloud infrastructure, you should consult [FedRAMP’s security control documentation](https://www.fedramp.gov/resources/documents-2016/).
- Which controls are already taken care of by your infrastructure. If you’re running in the cloud, many controls are taken care of at the infrastructure or platform layer. If your provider has received a FedRAMP P-ATO, it will provide a document called a customer responsibility matrix (CRM) or control implementation summary (CIS) listing the residual or hybrid controls that are the responsibility (or partial responsibility) of the applications running on the infrastructure or platform.
- What type of ATO you want to receive. The options will be specific to the organization doing the authorizing.
- Tailoring. The information system owner, working with the AO and the agency’s information security team, can then add, remove or modify controls to achieve cost-effective, risk-based security, based on the agency’s mission or business need.

This step should happen as an integral part of any system design activities. The team should also develop a monitoring strategy to ensure that security controls continue to be effective once the system receives its authority to operate.

### Step 3: Implement Security Controls
As part of system development work, controls are implemented. The implementation is documented in the SSP.

This step is essentially “state how your system meets each of the regulations”. Using established web frameworks (Rails, Django, etc.) and hosting in a platform takes care of a lot of the lower-level controls and security best practices for you, so you only need to be concerned with your application’s custom code and configuration. This custom code and configuration is known as the “attack surface”. The final version of this document is called the System Security Plan.

Fill out the documentation. The full list of data and functions in and of the system (in government parlance “mission based information types” and “delivery mechanisms”) must be itemized in structured data. While the data types are obviously arbitrary and custom to each system we produce, the government has a formalized data set of mission functions that should be mapped to the system via [NIST 800-60](https://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-60v1r1.pdf). For a Rails app, for example, this can simply be a link to the ```db/schema.rb``` file on GitHub.

### Step 4: Assess Security Controls
In other words, “verify that your system is secure”.

Before your system can go live with government information, your contol implementation must be tested. Testing is often performed by the development team and infrastructure team working together with the agency’s information security team, based on a security assessment plan. The security assessment plan will depend upon the type of ATO. FedRAMP has a [Security Assessment Framework](https://www.fedramp.gov/resources/documents-2016/) for FedRAMP ATOs.

There will usually be a penetration test conducted on the system. Any penetration test findings deemed serious enough to prevent an ATO will need to be fixed right away to unblock the ATO process. They will also review the SSP document and test the control narratives. This testing and review process will take 1-2 weeks and should be the top priority for the project team at the time.

The results of the assessment are documented in a security assessment report (SAR). Depending on the findings of the security assessment, remediation work may have to take place before the system receives its ATO. Other problems that are less critical can be remediated at a later date: these are listed in a document called a plan of action and milestones (POAM or POA&M).

### Step 5: Authorize Information System
The SSP, SAR and POAM together form a security authorization package (FedRAMP requires a further document: a continuous monitoring strategy). The Authorizing Official will make a risk-based decision whether to grant an ATO based on the information in this package. This decision, made in consultation with other key stakeholders such as the CISO, balances security considerations with the mission and operational needs of the agency.

Once all of the materials are prepared and testing is done and the system is considered “ready” by the Authorizing Official, they will sign the ATO memo. If an ATO is granted, an authorization decision document is issued and signed by the AO which lists the conditions under which the ATO will remain valid, including the ATO’s expiry date.

### Step 6: Monitor Security Controls
Once a system receives an ATO, it must be assessed at regular intervals to ensure the effectiveness of the control implementation. Any changes to the system’s security boundary or its environment should also be assessed to determine their impact.

There are several ways to ensure that your system remains compliant:

- Perform regular, automated security scans on your system, and act on the findings in a timely manner.
- Keep your System Security Plan (and any other architecture/security-related documentation) up-to-date.

## Security Categorization

### Overview
The impact level of your project is very important, and affects the process you’ll follow to launch your project. At first you’ll be making a prediction of your project impact level. As you enter the ATO assessment process the impact level will be determined with the help of your AO.

The impact level is determined by the functionality of the system and the data it contains. The methodology defines three security objectives of the system: ```confidentiality```, ```integrity```, and ```availability```. These security objectives are assigned one of three impact levels: ```low```, ```moderate```, or ```high```. This process is described in [NIST’s FIPS 199](http://csrc.nist.gov/publications/fips/fips199/FIPS-PUB-199-final.pdf) publication.

Once the potential impact on these three objectives is determined, the overall impact level of the system is determined based on the “high water mark” principle. This process is described in [NIST’s FIPS 200](http://csrc.nist.gov/publications/fips/fips200/FIPS-200-final-march.pdf) publication.

Determining the impact levels is ultimately subjective; the AO makes the final determination.

### Categorize using the 3 security objectives
Go through each of the security objectives and determine the impact on the organization or individuals if the system is compromised. The framework we usually use is to ask ourselves (and the agency we are creating the system with) three worst case scenario questions:

- What is the worst possible outcome if all of the confidentiality of the system is lost? i.e.
  - What if all of the data in the system is exposed to the public?
- What is the worst possible outcome if all of the integrity of the system is lost? i.e.
  - What if an error makes it into the data?
  - What if an update to the data is lost?
- What is the worst possible outcome if all of the availability of the system is lost? i.e.
  - What if the system has downtime?

If the potential impact is a limited adverse effect on organizational operations, organizational assets, or individuals, we select “low”. If the potential adverse impact is serious, we select “moderate”. If the potential adverse impact is severe or catastrophic, we choose “high”.

The answer to each question should then be interpreted in terms of impact to either the public or the government. The higher value for either impacted party is be used.

### Considerations

The canonical or singular nature of a function being provided by the system must be taken into consideration in the categorization. The more singular and canonical the system under evaluation is, the higher the impact level.

For example, if we re-post data from weather.gov, it is less impactful for us to lose availability than it is for weather.gov itself. Conversely, GSA is the only source of FedBizOpps data - therefore our availability is much more important for that data and function, and we should select a higher impact level for availability.

If there is any authorization or authentication being done, it is likely at the moderate level for all metrics.

Just because we need availability: high, doesn’t mean it needs confidentiality: high or integrity: high. These determinations are important for later tailoring of system controls.

### PII

Privacy risk is partially assessed based on to the degree to which a program or information system collects and makes use of personally identifiable information (PII). Per [OMB Circular A-130](https://obamawhitehouse.archives.gov/sites/default/files/omb/assets/OMB/circulars/a130/a130revised.pdf), PII is “information that can be used to distinguish or trace an individual’s identity, either alone or when combined with other information that is linked or linkable to a specific individual.”

Storing PII always raises the level to at least moderate for the confidentiality and integrity objectives.

## Selecting the overall impact level

Once you have decided on the impact level (```low```, ```moderate```, ```high```) for each of three objectives (```confidentiality```, ```integrity```, and ```availability```), you must then determine the overall impact level of the system. A low impact system is one in which all three of the security objectives are ```low```. A moderate impact system is one in which at least one of the objectives is ```moderate```, and none are high. A high impact system is one in which at least one objective is ```high```.

For more information, see [NIST 800-18](http://csrc.nist.gov/publications/nistpubs/800-18-Rev1/sp800-18-Rev1-final.pdf):

- [Table 1](http://nvlpubs.nist.gov/nistpubs/Legacy/SP/nistspecialpublication800-18r1.pdf#page=27) for FIPS categorization
- [Section 3.13](http://csrc.nist.gov/publications/nistpubs/800-18-Rev1/sp800-18-Rev1-final.pdf#page=31) for security controls


## General Tips

- As soon as you have a stable server that isn’t changing its security boundary (talk to the project developers about this, but it can be very early on), you should start this process. As long as there aren’t those significant changes, the tests will run periodically on any updates you make. At the very latest, start this process at least two months before launch. Do not commit to a launch date without coordinating with your AO on this first.
- One thing that will help the process is great documentation, which can mitigate some problems from occurring during the ATO process. Documentation, and specifically your README, should reflect a high level narrative of the architecture and data flows of the application. Questions to consider include:
  - What does it do?
  - How does it move information around?
  - What does it accomplish by doing it?
- The DigitalGov team at GSA has collected a list of [Requirements for Federal Websites and Digital Services](http://www.digitalgov.gov/resources/checklist-of-requirements-for-federal-digital-services/) that you should familiarize yourself with.
- Exactly how big of a splashy launch are you planning? Is POTUS announcing it? Have you figured out what level of traffic you need to support? This should be coordinated between the engineers on your team, your client, and the Infrastructure Team.

### System Security Plans (SSPs)
- Remember that the reviewer knows nothing about your system, and likely doesn’t have software development background. The purpose of the SSP is to get the entire system and everything security-related around it into the brain of the reviewer.
- Filling out the SSP is hard, and will likely be the most time-consuming part of the ATO process.
- Sections 9, 10, and 13 are the hard/important ones to fill out. Focus on these first.
- It will be easiest to fill out your SSP while going through side-by-side with a recent SSP, ideally for a similar system.
  - Looking at another SSP will help you understand the language/detail required.
  - Reuse/adapt content from previous SSP(s) whenever possible.
- When filling out the SSP, try taking a rough first pass, and flesh it out later.
- Don’t Repeat Yourself.
  - Lots of controls and sections have overlap - you will be tempted to restate the same thing multiple times. If this seems to be the case, reread the question carefully to be sure. The SSP template authors choose their words carefully.
  - Rather than repeating the same thing across multiple controls/sections, give a brief summary with the core details of who’s responsible and how the control is fulfilled, and then cross-reference the more detailed explanation in the other place.
- Maintain consistency.
  - Inconsistency can confuse the reviewers, forcing them to come back and say “well, which is it?” which slows down the process.
  - Be especially careful to be consistent with terminology, using the exact names from the following tables throughout your ATO materials:
    - User Roles
    - Software Components
- Refer to specific User Roles and Software Components in Title Case.
- Only include information about your [soon-to-be] production system. Other environments (development/staging) are out of scope.

### System/network diagrams
One of the requirements for an SSP (and the Rules of Engagement) is to include a network diagram for your system. Some tips:

- The diagram should be as detailed as possible.
- The boxes in the diagram should roughly correspond to the rows in the ```Software Components``` tables.
  - Include all external services, such as:
    - The Digital Analytics Program
    - New Relic
- The arrows should correspond to rows in the ```Ports, Protocols, and Services``` table(s), with labels of the format ```<protocol><port>(<T(CP) or U(DP)>) - <Purpose>```.
  - Example: ```HTTPS 443(T) - uploading files```
- Include a visual “ATO Boundary.”
  - A dotted line box is a nice way to do this.
  - The system diagram includes things outside of the ATO boundary for context. Delineating the parts of the diagram being ATOd versus the parts that exist for context (such as the cloud.gov router) is helpful for reviewers.
