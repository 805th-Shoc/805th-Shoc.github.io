---
title: Risk Management Framework
type: docs
bookToc: false
---

# Risk Management Framework (RMF)

For all federal agencies, the Risk Management Framework (RMF) describes the process that must be followed to se
cure, authorize, and manage information systems. The RMF defines a process cycle that is used for initially securing the protection of systems through an Authorization to Operate (ATO) and integrating ongoing monitoring.

## Adopting the Risk Management Framework
The risk management framework is a framework, not a policy. Frameworks have to be implemented. The way we implement needs to overcome issues with point-in-time ATO documentation while maintaining its strengths.

### Goals
The solution an agency adopts should:

- Address the shortcomings of assessment and accreditation.
- Get to ATO efficiently.
- Allow data and tools to flow between organization policy-setting and information systems.

### Continuous monitoring
OMB has directed agencies to adopt [Information Security Continuous Monitoring (ISCM)](https://obamawhitehouse.archives.gov/sites/default/files/omb/memoranda/2014/m-14-03.pdf). Continuous monitoring requires ongoing awareness of vulnerabilities and threats. These cannot be assessed at a single point in time in order to produce an ATO and then trusted until the next ATO review or reauthorization. NIST’s [Special Publication 800-137](http://csrc.nist.gov/publications/nistpubs/800-137/SP800-137-Final.pdf) describes implementation of ISCM.

### An organization-wide approach

Among the requirements is whole-organization involvement:

Maintaining an up-to-date view of information security risks across an organization is a complex, multifaceted undertaking. It requires the involvement of the entire organization, from senior leaders providing governance and strategic vision to individuals developing, implementing, and operating individual information systems in support of the organization’s core missions and business functions.

NIST uses three tiers to describe how the organization should integrate monitoring into their systems. In Tier 1, the agency should set its risk tolerance, governance, policies, and strategies. In Tier 2, the agency should set business processes that can support these organizational goals. In Tier 3, the agency needs information systems that provide the data for these processes. Data moves from the systems into the processes into the organization. Tools and capabilities flow from the organization into the processes into the systems.

### Structured data
A modern implementation of the risk management framework needs to support this movement of information. To do this, agencies need to integrate the development of secure systems with how that security is documented. To keep data moving from systems to the organization, the agency needs to produce consistently up-to-date documentation that is reliable. To make tools available to systems at the right time, the agency needs to restrict pace of development as little as possible.

## Risk Management Framework Stages
Government information systems must follow a risk management framework described by the National Institute of Standards and Technology (NIST). The framework is a cycle of activities that an agency needs to perform on all information security systems:

- Categorize: Define the level of risk the system presents — low, moderate, or high — based on a worst case scenario
- Select: Choose baseline security controls and any guidance or supplement controls based on the categories
Implement Put the controls in place using appropriate engineering practices. See SP 800-70
- Assess: Determine how effective the controls are. See SP 800-53A
- Authorize: Review the risks to the system and, if they are acceptable, authorize the system
- Monitor: Track changes that affect security controls and reassess how effective they are
Continuous monitoring leads the agency back into the cycle, reviewing whether new information requires new categories, controls, or assessment criteria.

The risk management framework describes specific categories or levels of risk that a system can pose to the government, and it recommends specific baseline controls based on a system’s risk level. Agencies determine much of the process for themselves, including how to analyze risk, how to demonstrate selected controls, and whether and how to exceed the baseline recommendations. One of the key components of the framework is that the final step, monitoring, is continuous.

OMB and NIST have directed agencies to change how they approach risk management frameworks from point-in-time accreditation and authorization reviews to continuous monitoring of information system security. Here we provide a high-level overview of why this has changed and how to make continuous review work for your systems, your development teams, and your information security teams.

## Categorize
Categorization is based on an impact analysis and is performed to determine the types of information included within the authorization boundary, security requirements for the information type, and potential impact resulting from a security compromise. Agencies are required to categorize their information systems as low-impact, moderate-impact, or high-impact for the security objectives of confidentiality, integrity, and availability and to select appropriate security controls.

### Objectives
Information systems have three security objectives defined by the Federal Information Security Management Act (FISMA).

- Confidentiality: Prevent unauthorized disclosure of information.
- Integrity: Prevent unauthorized modification or destruction of information.
- Availability: Prevent disruption of access to information or use of the system.

### Categorizing
To categorize the information system, you need to establish two things. First, what are the data types in the system? Second, for each of those data types, would the failure of each of the three security objectives pose a low, moderate, or high risk to the agency? Decide how damaging the loss of confidentiality, integrity, or availability would be to both the agency’s ability to work and its money, property, or people.

#### Risks and risk categories

| Area of risk | Low risk | Moderate risk | High risk |

| Ability to work | Minor but noticeable | Significant but does not affect agency’s primary functions | Harms ability to perform primary functions |

| Money, property, or people | Minor | Significant | Catastrophic |



### Expressing the results
For each information type, state the risk for confidentiality, integrity, and availability. Structure it in this way:

```SC information type = {(confidentiality, impact), (integrity, impact), (availability, impact)}```

Use low, medium, or high for the impact. Then take the maximum impact category against each objective and use that for the information system as a whole. Structure it the same way:

```SC information system = {(confidentiality, impact), (integrity, impact), (availability, impact)}```

An individual data type’s impact can be n/a if there is no risk at all, but for the whole system, the minimum risk level on any objective is Low.

### Categorization under continuous monitoring
You should begin categorizing information systems as close to the beginning of the system development life cycle as possible. Each time you identify an information type the system will handle, give it an initial categorization. As you assemble a larger set of them, review the initial categories and update if needed. You might find that relationships among categories raise the risk of one or more of them. You might find that the use of the system is going to change, which could change the risks. The full set of information types will produce system categories that are unsurprising. You are more likely to be prepared to select, implement, assess, and document the correct controls.

Building knowledge of risk as you build the system is best done by having the developers participate. As they identify system risks, they can think about good controls rather than reacting after the fact to categorization received from information security. And the flexibility this builds into the development life cycle will make it much easier to react to issues raised by continuous monitoring.

### More detailed reading from NIST
- [FIPS 199](http://csrc.nist.gov/publications/fips/fips199/FIPS-PUB-199-final.pdf) describes the objectives, categories, and how to structure your categories.
- [SP 800-60](http://csrc.nist.gov/publications/nistpubs/800-60-rev1/SP800-60_Vol1-Rev1.pdf) recommends an specific approach to categorization.

## Select
Controls are the management, operational, and technical safeguards or countermeasures employed within an organizational information system that protect the confidentiality, integrity, and availability of the system and its information. The specific controls required to protect the system are based on the categorization of the system.

Security and privacy control baselines serve as a starting point for the protection of information, information systems, and individuals’ privacy. NIST SP 800-53B defines these security and privacy control baselines. The three defined control baselines contain sets of security controls and control enhancements that offer protection for information and information systems that have been categorized as low-impact, moderate-impact, or high-impact.

These are the security and privacy control families for information systems in NIST SP 800-53 rev. 5. Specific controls and control enhancements are found within each control family.

ID	Control Family

AC	Access Control

AT	Awareness and Training

AU	Audit and Accountability

CA	Security Assessment and Authorization

CM	Configuration Management

CP	Contingency Planning

IA	Identification and Authentication

IR	Incident Response

MA	Maintenance

MP	Media Protection

PS	Personnel Security

PT	PII Processing and Transparency

PE	Physical and Environmental Protection

PL	Planning

PM	Program Management

RA	Risk Assessment

SA	System and Services Acquisition

SC	System and Communications Protection

SI	System and Information Integrity

SR	Supply Chain Risk Management

## More detailed reading from NIST
- [FIPS 200](http://csrc.nist.gov/publications/fips/fips200/FIPS-200-final-march.pdf) lists the minimum security requirements for controls in seventeen areas of information security.
- [SP 800-53](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53r5.pdf) provides a full list of controls and augmentations to those controls that an agency can adopt.
- [SP 800-53B](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53B.pdf) provides a full list of controls and augmentations to those controls that an agency can adopt.

## Implement
Controls specified in the System Security Plan (SSP) are implemented by taking into account NIST SP 800-53 Security and Privacy Controls for Federal Information Systems and Organizations and the minimum organization requirements (i.e., organizationally defined parameters).

A team must implement the selected security controls and document all the processes and procedures they need to maintain their operation. This includes implementing the security controls and documenting the security control implementation details, as appropriate, in the security plan.

There are three types of control implementation:

System Specific Controls - System-specific controls are security controls that provide a security capability for a particular information system only and are the primary responsibility of information system owners and their AO.

Common Controls - Common controls are security controls that can support multiple information systems efficiently and effectively as a common capability. When these controls are used to support a specific information system, they are referenced by that specific system as inherited controls.

Hybrid Controls - Hybrid controls are security controls where one part of the control is deemed to be common and another part of the control is deemed to be system-specific.

### Assess
The purpose of assessing security controls is to ensure they were implemented correctly, operate as intended, and successfully meet the security requirements for the information system. Assessments are required prior to system authorization and annually to ensure that the security measures are working effectively.

A full scope assessment of all security controls must be performed prior to the initial ATO, and the ATO must be renewed every three years. Each year, 1/3 of the controls are tested so that by the end of the third year, all controls have been tested for the ATO renewal. A full scope assessment of the controls can be required if significant changes to the information system are made at any time throughout the lifecycle.

There are currently two approaches for completing assessments:

A Security Control Assessment (SCA) is a systematic, manual procedure for evaluating, describing, testing, and examining information system security controls.

Adaptive Capabilities Testing (ACT) is an agency-specific, next-generation assessment based on NISTIR 8011 that relies heavily on automation and focusing on capabilities rather than individual controls.

[NIST SP 800-53A](https://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53Ar5.pdf), Guide for Assessing the Security Controls in Federal Information Systems and Organizations, has more detailed information about assessing security controls.

[NISTIR 8011](https://nvlpubs.nist.gov/nistpubs/ir/2017/NIST.IR.8011-1.pdf), Automation Support for Security Control Assessments, has more detailed information about automated assessments and capabilities.

## Authorize
While agencies have a lot of flexibility in how they implement the risk management framework, all of them need to include formal authorization of the system before it is operational. This is as true for continuous monitoring as it was for point-in-time documentation.

### What is Authority to Operate?
Authority to Operate (ATO) is the usual name for the result of this step. It is the last step in the risk management framework before a system is operational. (Monitoring happens during operation.) ATOs usually take the form of a document describing the risks to the government of that system, the controls that are in place to safeguard it, and the acceptance of the risks it presents.

In authorizing an information system to operate, NIST requires a senior official to explicitly accept the risks of the system and its controls. Although the term “Authority to Operate” is not described in law, the ATO is the term applied to how the official accepts those risks.

### Defining the ATO process
The Chief Information Security Officer (CISO) at each agency and the head of that agency define the processes by which the agency will review information system security. How this is structured depends on a number of things, such as the agency’s willingness to take on risk and what kind of demonstration they expect for controls. To receive an ATO, the developers of a system must show how the system meets the controls that apply to it. (How they demonstrate that is also part of this defined process.)

Traditionally, the way to demonstrate controls is in a single document. It describes each risk and the controls in place for that risk. These documents can be dozens or hundreds of pages, and they usually describe how each control is implemented. Auditors can review these documents quickly and easily against the requirements and recommended controls from NIST, but they can be difficult to assemble from the broader systems developers have created.

### More detailed reading from NIST
[SP 800-37](http://csrc.nist.gov/publications/nistpubs/800-37-rev1/sp800-37-rev1-final.pdf)

## Monitor
Risk management is a continuous process. Information systems are in a constant state of change with upgrades to hardware, software, or firmware and modifications to the surrounding environments where the systems reside and operate. A structured approach to managing, controlling, and documenting changes to an information system or its environment of operation is an essential element of an effective monitoring program. Strict configuration management and control processes are established by the agency to support such monitoring activities.

Security Impact Analysis (SIA) determines the extent to which proposed or actual changes to the information system or its environment of operation can affect or have affected the security state of the system. Changes to the information system or its environment of operation may affect the security controls currently in place, produce new vulnerabilities in the system, or generate requirements for new security controls that were not needed previously. If the results of the SIA indicate that the proposed or actual changes can affect or have affected the security state of the system, corrective actions are initiated and appropriate documents are revised and updated.

### More detailed reading from NIST
- [SP 800-37](http://csrc.nist.gov/publications/nistpubs/800-37-rev1/sp800-37-rev1-final.pdf) provides guidance for applying the risk management framework, start to end.
- [SP 800-53A](http://nvlpubs.nist.gov/nistpubs/SpecialPublications/NIST.SP.800-53Ar5.pdf) describes customizable procedures to assess how the framework, as applied, works with the agency’s risk tolerance. How you assess the framework is a key input to your ongoing monitoring processes.

## Authorization package
In order to satisfy an agency’s requirements for a completed ATO, a team must complete a set of documents called the “authorization package” that fully describe the security controls that are in place to protect the information system. NIST SP 800-37 defines the authorization package as:

The essential information that an authorizing official uses to determine whether to authorize the operation of an information system or the provision of a designated set of common controls. At a minimum, the authorization package includes an executive summary, system security plan, privacy plan, security control assessment, privacy control assessment, and any relevant plans of action and milestones.

The exact process and document titles vary from agency to agency, but in general the most common required document names are:

System Security Plan (SSP) - A formal document that provides an overview of the security security controls, whether in place or planned, and implementation details for meeting those requirements. This document summarizes the overall approach taken to address each of the control families. Sometimes the SSP document includes the NIST SP 800-53 security and privacy controls; other agencies prefer to break the details of those out into a supplemental document.

Privacy Impact Assessment (PIA) - An analysis of how information is handled that ensures handling conforms to applicable legal, regulatory, and policy requirements regarding privacy. Determines the risks and effects of collecting, maintaining, and disseminating information in an identifiable form in an electronic information system. Examines and evaluates protections and alternative processes for handling information to mitigate potential privacy risks. Defined and required by Office of Management and Budget OMB M-03-22.

Privacy Threshold Assessment (PTA) - A questionnaire used to determine if a system contains personally identifiable information (PII), whether a PIA is required, whether a System of Records Notice (SORN) is required, and if any other privacy requirements apply to the information system. A PTA should be completed when proposing a new information technology system through the budget process that will collect, store, or process identifiable information, when starting to develop or significantly modify such a system, or when a new electronic collection of identifiable information is being proposed. A PTA will determine if a PIA is required.

Risk Assessment (RA) - A document that identifies risks to organizational operations (including mission, functions, image, reputation), organizational assets, individuals, other organizations, and the nation resulting from the operation of an information system. Part of risk management, an RA incorporates threat and vulnerability analyses and considers mitigations provided by security controls or privacy controls planned or in place. Synonymous with risk analysis.

Incident Response Plan (IRP) - The documentation of a predetermined set of instructions or procedures to detect, respond to, and limit consequences of malicious cyber attacks against an organization’s information system(s).

Disaster Recovery Plan (DRP) - A written plan for recovering one or more information systems at an alternate facility in response to a major hardware or software failure or destruction of facilities.

ATO Boundary Diagram - A visual layout of the information system that clearly describes the authorization boundary. This diagram shows which technology resources are included within the ATO boundary and all external connections.

Interconnection Systems Agreements / Memoranda of Understanding / Memoranda of Agreement (ISA/MOU/MOA) - Agreements between the federal agency operating an information system with an ATO and outside organizations. These agreements include details of sensitive information being shared and how it is being secured. These are generally included in ATO processes in order to clearly document how Personal Identifying Information (PII) is being shared between the federal agency and other agencies or third parties.

Plan of Action and Milestones (POA&M or POAM) - A document that identifies tasks needing to be accomplished. It details resources required to accomplish the elements of the plan, any milestones in meeting the tasks, and scheduled completion dates for the milestones.

Security Assessment Report (SAR) - Assesses the findings of the assessor and the recommendations for correcting any identified vulnerabilities in the security controls.

Risk Assessment Report (RAR) - Assesses and documents the use of resources and controls to eliminate and/or manage vulnerabilities that are exploitable by internal and external threats.

## Problems of the Assessment and Authorization
Many agencies have created strong processes for creating an ATO document, which describes a system and its controls at a single point in time. This is useful as a compliance check, but point-in-time documentation is insufficient to modern information security needs.

### Out-of-date controls
An ATO can be a very large document that takes a long time to write, often longer than it takes new threats to evolve or new capabilities that might require new controls. The point-in-time ATO cannot describe new controls and new risks.

### Lagging security reviews
ATOs define a point at which they must be reviewed or renewed, even if controls have not changed. This requires review of the whole management framework. But traditional implementation of information security did not require review more frequently. Developers might work on security improvements, but they are not included in the documents that inform compliance.

### Lagging product improvements
One way to prevent out-of-date controls is to slow down the adoption of enhancements. But slowing adoption can create other problems. Issues that could have been discovered and addressed earlier are instead discovered late in development. Because so many other decisions or assumptions have already been made, they are more expensive to address and the organization has fewer choices to solve them.

Slowing work can also leave systems lagging behind the skills of good developers. This has knock-on effects, reducing the pool of developers who want to join government, and reducing opportunities for government developers to build on their own skills.

### Reduced contributions to compliance from developers
The people who develop systems think about the security of a system in terms of how the system works and what modules serve as security controls. Compliance reviews work from the opposite direction: starting from the controls and identifying which modules implement them. Information security teams can ask which module implements each control repeatedly until they satisfy a list of controls.

If information security teams could ask instead what security controls a particular module implements, a development team could provide the full range at once. This allows developers to think more proactively about how each module they develop functions as a security feature.