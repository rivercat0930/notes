# NIST Special Publication - Guide to Enterprise Patch Management Planning:Preventive Maintenance for Technology

## Executive Summary

*Enterprise patch management* is the process of identifying, prioritizing, acquiring, installing and verifying the installation of patches, updates, and upgrades throughout an organization.

In past perimeter-based security architectures, most software was operated on internal networks protected by several layers of network security controls.
While patching was generally considered important for reducing the likelihood of compromise and was a common compliance requirement, **patching was not always considered a priority.**

**In today's environments, patching has become more important, often rising to the level of mission criticality.**

As a part of a zero trust approach to security, it is now recognized that the perimeter largely does not exist anymore, and most technologies are directly exposed to the internet, putting systems at significantly greater risk of compromise.

There is often a divide between business/mission owners and security/technology management.
***Leadership and business/mission owners should reconsider the priority of enterprise patch management in light of today's risks.***
**Patching should be considered a standard cost of doing business and should be rigorously followed and tracked.**

---

## Introduction

### Purpose and Scope

The purpose of this publication is to ***help organizations imporove their enterprise patch management planning*** so that they can strengthen their management of risk.

This publication is intended to apply to all types of computing technology assets, including IT, operational technology (OT), Internet of Things (IoT), mobile devices, and cloud computing, and to all types of patchable software, including applications, operating systems, and firmware.

[**Additional Information**]

* IT includes desktop and laptop computers, on-premises servers, networking equipment, printers, and other types of assets typically found in an organization's own offices or data centers.

* OT refers to programmable systems or devices that interact with the physical environment (or manage devices that interact with the physical environment)

---

## Risk Response Approaches for Software Vulnerabilities

This section outlines possible risk response approaches for software vulnerabilities, provides an overview of the software vulnerability management life cycle, and takes a closer look at parts of that life cycle with respect to patching.

### Risk Responses

Patching is one of several ways to respond to risks from software vulnerabilities.

This publication references four types of *risk responses*:

1. **Accept**

    Accept the risk from vulnerable software as is, such as by relying on existing security controls to prevent vulnerability exploitation or by determining that the potential impact is low enough that no additional action is needed.

    [**Additional Information**]

    * What is security controls?

        Security controls are parameters implemented to protect various forms of data and infrastructure important to an organization.

        Security controls refers to any type of safeguard or countermeasure used to avoid, detect, counteract or minimize security risks to physical property, information, computer systems or other assets.

        * Physical security controls

            Such things as data center perimeter fencing, locks, guards, access control cards, biometric access control systems, surveillance cameras and intrusion detection sensors.

        * Digital security controls

            Such as usernames and passwords, two-factor authentication, antivirus software and firewalls.

        * Cybersecurity controls

            Include anything specifically designed to prevent attacks on data, including DDoS mitigation and intrusion prevention systems.

        * Cloud security controls

            Include measures that you take in cooperation with a cloud services provider to offer the necessary protection for data and workloads.

    * Waht is potential impact is low enough?

        A system falls under a low impact level if the loss of confidentiality, integrity, or availability will have a *limited impact* on the agency or constituents.

1. **Mitigate**

    Reduce the risk by eliminating the vulnerabilities (patching the vulnerable software, disabling a vulnerable feature, or upgrading to a newer software version without the vulnerabilities) and/or deploying additional security controls to reduce vulnerability exploitation (using firewalls and network segmentation to isolate vulnerable assets)

1. **Transfer**

    Reduce the risk by sharing some of the consequences with another party, such as by purchasing **cybersecurity insurance** or by replacing conventional software installations with software-as-a-service (SaaS) usage where the SaaS vendor/managed service provider takes care of patching.

1. **Avoid**

    Ensure that the risk does not occur by eliminating the attack surface, such as by uninstalling the vulnerable software, decommissioning assets with the vulnerabilities, or disabling computing capabilities in assets that can function without them.

    [**Additional Information**]

    * Attack surface

        The attack surface is the number of all possible points, or attack vectors, where an unauthorized user can access a system and extract data.

By default, an organization accepts the risk posed by using its software. Software could have vulnerabilities in it at any time that the organization does not know about, and sometimes previously unknown vulnerabilities are exploited - a zero-day attack.

Once a new vulnerability becomes publicly known, risk usually increases because attackers are more likely to develop exploits that target the vulnerable software.

**Installing a patch or update or upgrading software to a newer version without the vulnerabilities are the only forms of risk response that can completely eliminate the vulnerabilities without removing functionality.** However, immediately patching, updating, or upgrading vulnerable software is sometimes not viable. Examples of why include the following:

* A patch may not be available yet.

    A vulnerability may be announced before a patch is ready. (it could be days, weeks, or months before the patch is released)

* The vendor may no longer support the vulnerable software. (Meaning that a patch for it will never be released because the software is at end-of-life)

* The organization may need to wait for a scheduled outage window, perform testing first, update other software that interacts with the software to be patched, or train exployees on new features or interfaces.

* Some patches may be considered a higher priority, so other patches are delayed due to limited resources.

* The manufacturer may require customers to update the software on a delayed schedule.

    Such as for assets with human safety implications in a highly regulated sector, because of the extensive testing and certification that must be performed first.

    ***In these cases, organizations that choose to implement updates on their own may be voiding the product warranty and preventing future support from the manufacturer.***

* The organization may need to comply with specific legal, regulatory, or business requirements.

    For example, an organization may need to use Federal Information Processing Standards (FIPS)-validated cryptographic modules for protecting data, but the cryptographic modules in the upgraded software are not yet FIPS-validated.

***Even when patching, updating, or upgrading vulnerable software is viable, organizations can choose to respond to the risk from the vulnerabilities in a different way, such as any of the other risk response examples at the beginning of this section.***

### Software Vulnerability Management Life Cycle

1. **Know when new software vulnerabilities affect your organization's assets, including applications, operating systems, and firmware.**

    This involves knowing what assets your organization uses and which software and software versions those assets run down to the level of packages and libraries, as well as keeping track of new vulnerabilities in that software.

    For example, your organization might subscribe to vulnerability feeds from software vendors, security researchers, and the National Vulnerability Database(NVD).

1. **Plan the risk response**

    This involves assessing the risk the vulnerability poses to your organization, choosing which form of risk response (or combination of forms) to use, and deciding how to implement the risk response.

    For example, you might determine that risk is elevated because the vulnerability is present in many organization assets and is being exploited in the wild, then choose mitigation as the risk response and mitigate the vulnerability by upgrading the vulnerable software and altering the software's configuration settings.

1. **Execute the risk response**

    This will vary depending on the nature of the selected risk response, but common phases include the following:

    1. **Prepare the risk response**

        This encompasses any preparatory activities, such as acquiring, validating, and testing patches for the vulnerable software; deploying additional security controls to safeguard the vulnerable software; or acquiring a replacement for a legacy asset that cannot be patched. It might also include scheduling the risk response and coordinating deployment plans with enterprise change management, business units, and others.

    1. **Implement the risk response**

        Examples of this include distributing and installing a patch, purchasing cybersecurity insurance, deploying additional security controls, and changing asset configurations and state (software reset, platform reboot).

        ***Any issues that occur during implementation should be resolved.***

    1. **Verify the risk response**

        This step involves ensuring that the implementation has been completed successfully.

        * For patching, this means confirming that the patch is installed and has taken effect.

        * For deploying additional security controls, ensure they are functioning as intended.

        * For risk avoidance, verify that vulnerable assets were decommissioned or replaced.

    1. **Continuously monitor the risk response**

        Make sure that the risk response continues to be in plcae. (no one uninstalls the patch, deactivates the additional security controls, lets the cybersecurity insurance lapse, or restarts the decommissioned asset)

### Risk Response Execution

This section takes a closer look at the common phases of executing a risk response, as described in the previous subsection, specifically within the context of patching.

#### Prepare to Deploy the Patch

Examples of common steps for preparing to deploy a patch include the following.

* **Prioritize the patch**

    A patch may be a higher priority to deploy than others because its deployment would reduce cybersecurity risk more than other patches would. Another patch may be a lower priority because it addrersses a low-risk vulnerability on a small number of low-importance assets.

* **Schedule patch deployment**

    Many organizations schedule patch deployments as part of their enterprise change management activities.

* **Acquire the patch**

    Patches may be downloaded from the internet, built internally by developers or system administrators, or provided through removable media.

* **Validate the patch**

    A patch's authenticity and integrity should be confirmed, preferably by automated means, before the patch is tested or installed. The patch could have been acquired from a rogue source or tampered with in transit or after acquisition.

* **Test the patch**

    A patch may be tested before deployment. This is intended to reduce operational risk by identifying problems with a patch before placing it into production.

    Testing may be performed manually or through automated methods.

#### Deploy the Patch

Patch deployment varies widely based on several factors

* The type of software being updated. (firmware, OS, application)

* The asset platform type. (IT, OT, IoT, mobile, cloud, VM, containers)

* Platform traits. (managed/unmanaged asset, on-premises or not, virtualized or not, and containerized or not)

* Environmental limitations. (network connectivity and bandwidth)

**Many aspects of patch deployment are dependent on patch management technologies.**

At a high level, example of common steps for deploying a patch include:

* **Distribute the patch**

    Distributing the patch to the assets that need to have it installed can be organization-controlled (and occur automatically, manually, or as scheduled) or vendor-controlled, such as delivered from the cloud.

* **Validate the patch**

    A patch's authenticity and integrity should be confirmed before installation, preferably through automated means.

* **Install the patch**

    Installation can occur in numerous ways.

  * automatically

  * manually

    When directed to do so by a user, administrator, vendor, or tool.

    As a result of other software being installed or updated.

    Through the replacement of removable media used by an asset.

    Some installations require administrator privileges, such as installing firmware patches for a BIOS. Some patch installations require user participation or cooperation.

* **Change software configuration and state**

    In some cases, making a patch take effect necessitates implementing changes. (Including restarting patched software, rebooting the operating system or platform on which the patched software runs, redeploying the applications, or altering software configuration settings)

    In other cases, no such changes are needed.

* **Resolve any issue**

    Installing a patch may cause side effects to occur, like inadvertently altering existing security configuration settings or adding new settings, and these side effects can inadvertently create a new security problem while fixing the original one.

    Patch installation can also cause operational issues that may necessitate uninstalling the patch, reverting to the previous version of the software, or restoring the software or asset from backups.

* **Verify Deployment**

    A patch’s deployment can be verified to ensure that it has been installed successfully and taken effect.

    The robustness of verification can vary a great deal and is largely dependent on an organization’s needs, but automated means are generally needed to achieve verification at scale.

* **Monitor the Deployed Patches**

    the patch’s deployment can be monitored using automation to confirm that the patch is still installed.

  * monitoring could confirm that the patch has not been uninstalled by a user or an attacker

  * an unpatched version of the software has not been restored from a backup
  
  * the device has not been reset to a vulnerable factory-default state

    Another reason for monitoring the deployed patches is to see if the patched software’s behavior changes after patching.

    As part of a layered security approach to mitigating supply chain risk, this might be helpful at detecting, responding to, and recovering from situations where the installed patch was itself compromised.

---

## Recommendations for Enterprise Patch Management Planning

* Enterprise patch management has been a contentious issue for decades, with personnel from the security and business/mission side of organization often having conflicting opinions

    For example, many organizations have struggled with balancing the trade-offs between earlier deployment and more testing.

    Deploying patches more quickly reduces the window of opportunity for attackers, but increases the risk of operational disruption because of lack of testing.

    Testing patches before deployment decreases the risk of operational disruption but increases the window of oportunity for attackers.

    Testing can also consume considerable staff resources, and it still might miss problems.

* The reason that made enterprise patch management more difficult is **dynamic and dispersed computing assets**, as well as the sheer number of installed software components to patch

  Patch management processes and technology take different forms depending on the type of assets.

  The result is that ***many organizations are unable to keep up with patching***.

  ***Patching often becomes primarily reactive versus proactive.***

  * Proactive

    Means doing more work now to reduce the likelihood of incidents in the future.

    It also means that if a patch fails, that disruption can be managed and remediated on the organization's schedule.

  * Reactive

    Means if a compromise of an unpatched vulnerability occurs, the organization will have to perform incident response, their reputation may be danaged, and/or they may potentially be fined or sued.

    **As part of incident response efforts, the missing patch will probably need to be installed anyway in addition to installing all the preceding patches it is dependent upon, as well as performing other prerequisite recovery actions such as reverting to a good known state or rebuilding the environment from scratch.**

* Disruptions from **patching** are **largely controllable**, while disruptions from **incidents** are largely **uncontrollable**.

* **Disruptions from patching are also a necessary part of maintaining nearly all types of technology in order to avoid larger disruptions from incidents.**

**Security and technology personnel can take steps to reduce the likelihood of patching causing disruptions, as well as direct patching efforts to prioritize the vulnerabilities that are causing the most risk to the organization.**

### The recommendations support the following principle

Organizations should strive to adopt in their enterprise patch management practices.

* **Problems are inevitable; be prepared for them**

    Risk responses, including patching, will nerver be perfect. Some may inadvertently cause operational problems.

    For example, to improve enterprise patch management, organizations need to change their culture so that instead of fearing problems and thus delaying risk responses, personnel are prepared to address problems when they occur. The organization needs to become more *resilient*, and everyone in the organization needs to understand that problems caused by patching are a necessary inconvenience that helps prevent major compromises.

* **Simplify decision making**

    Conducting a risk assessment of each new vulnerability in order to plan the optimal risk response for it is simply **not feasible**.

    Organizations do not have the time, resources, expertise, or tools to do so. Planning needs to be done in advance so that when a new vulnerability becomes known, a decision can quickly be made about how to respond to it.

* **Rely on automation**

    Automation is also needed for emergency situations, like patching a severe vulnerability that attackers are actively exploiting. Having automation in place gives an organization agility and scalability when it comes to its risk responses.

* **Start improvements now**

    Some of the changes that an organization may need to make might take years to put in place, but that does not mean that other practices cannot be improved in the meantime.

### Reduce Patching-Related Disruptions

***Organizations should strive to decrease the number of vulnerabilities introduced into their environments.***

Possible methods for decreasing the number of vulnerabilities:

1. Harden software

    Such as enforcing the principles of least privilege and least functionality (deactivating or uninstalling software services, features, and other components that are not needed)

1. Acquire software that is likely to have fewer vulnerabilities over time compared to other software.

1. Work with software development partners that are likely to introduce fewer vulnerabilities into software over time

    taking into consideration factors such as how rigorous their secure software development practices are, how quickly they address issues and release patches, how often problems are associated with their patches, and how transparent they are in their security-related communications.

1. Use managed services instead of software when feasible

    Before: You have an SQL server that you're responsible for maintaining. This includes ensuring its security, applying patches and updates, managing backups, and handling any scalability or performance issues.

    After: You transition to using Amazon Web Services (AWS) Relational Database Service (RDS). AWS RDS is a managed service that automates much of the maintenance work associated with running a relational database, such as setup, patching, backups, and scaling.

1. Select stacks or platforms that are likely to have fewer vulnerabilities over time compared to other stacks or platforms

    running software within a small container instead of a larger operating system.

***Organizations should consider deploying applications in ways that make patching less likely to disrupt operations.***

Traditional Approach: Previously, ABCD Corp would schedule maintenance windows during off-peak hours to apply patches, resulting in downtime. Customers in different time zones were still affected, leading to frustration and complaints.

Improved Strategy:

1. Microservices Architecture: ABCD Corp redesigned their application using microservices, allowing individual services to be updated without taking down the entire application.

1. Blue-Green Deployment: For major updates, they implemented a blue-green deployment strategy. They applied patches to the "green" environment while the "blue" environment served live traffic. After testing the updates in green, they switched traffic to it, achieving near-zero downtime.

1. Canary Releases: For less critical updates, they used canary releases, gradually rolling out the change to a small percentage of users before making it available to everyone. This allowed them to monitor the impact of the patch on system stability and user experience without widespread disruption.

### Inventory Software and Assets

***Organizations should establish and constantly maintain up-to-date software in inventories for their physical and virtual computing assets, including OT, IoT, and container assets***

A realistic goal is to maintain a close-to-comprehensive inventory by relying on automation to constantly discover new assets and collect up-to-date information on all assets.

When conducting software patching (updates), attention should be given to the specific details of each asset, such as servers and computers. In compiling a software inventory, one should record not only the software and its versions running on the asset but also include the technical and business characteristics of the asset. When assessing risks and determining the priorities for addressing issues, one should not only consider the software running on the asset itself but should take into account all the characteristics of the asset. This is because these characteristics provide the necessary context for understanding the potential security vulnerabilities of the asset.

The characteristics that an organization should inventory will vary, but the following are examples of possible characteristics to track:

* The asset’s platform type (e.g., IT, OT, IoT, mobile, cloud, VM)

* The party who administrates the asset (e.g., IT department, third party, end user, vendor/manufacturer, shared responsibility model)

* The applications, services, or other mechanisms used to manage the asset (e.g., endpoint management software, virtual machine manager, container management software)

* The asset’s network connectivity in terms of protocols, frequency/duration, and bandwidth

* The technical security controls already in place to safeguard the asset

* The asset’s primary user(s) or interconnected services and their privileges

Examples of mission/business characteristics that an organization should track include:

* The asset’s role and importance to the organization, which are contextual and may be hard to define or determine

* Laws, regulations, or policies that specify how soon a new vulnerability in the asset must be addressed

* Contractual restrictions on patching (e.g., a highly regulated asset can only be patched by its manufacturer after testing and certification)

* Mission/business restrictions on risk responses for that asset (e.g., an asset can only berebooted during a monthly maintenance outage)

### Define Risk Response Scenarios

***Organizations should define the software vulnerability risk response scenarios they need to be prepared to handle.*** Example of such scenarios include:

* Routine patching

  * This is the standard procedure for patches that are on a regular release cycle and have not been elevated to emergency status.

  * Because routine patching does not have the urgency of emergency scenarios, and routine patch installation can interrupt operations (e.g., device reboots), it is often postponed and neglected.

  * Provides many additional windows of opportunity for attackers.
  
  * Delaying routine patching also makes emergency patching more difficult, time-consuming, and disruptive because of the need to first install previous patches that new patches depend upon.

* Emergency patching

  * This is the procedure to address patching emergencies in a crisis situation, such as a severe vulnerability or a vulnerability being actively exploited.

  * Emergency patching may be part of incident response efforts.

  * Emergency patching needs to be handled as efficiently as possible to prevent the imminent exploitation of vulnerable assets.

* Emergency mitigation

  * This is the emergency procedure in a crisis situation, like those described above for the emergency patching scenario, to temporarily mitigate vulnerabilities before a patch is available.

  * The mitigation can vary and may or may not need to be rolled back afterward. A patch might be flawed and not actually correct a vulnerability, or a patch might inadvertently disrupt the operation of other software or systems.

  * Temporary stop using the software until patch is ready.

* Unpatchable assets

  * This is the implementation of isolation or other methods to mitigate the risk of systems that cannot be easily patched.

  * Unpatchable assets need to be included in risk response planning because a new vulnerability in an asset might necessitate a change in the methods needed to mitigate its risk.

### Assign Each Asset to a Maintenance Group

***Organizations should use the software inventories, technical and business/mission characteristics, and risk response scenarios to assign each asset to a maintenance group.***

Maintenance needs include not only patching (e.g., patch schedule, patch testing needs, outage restrictions, level of impact if vulnerable software is compromised) but also any other appropriate forms of mitigation and risk response, such as temporary mitigations used when patches are not yet available.

Example:

* On-premises datacenter (including servers, network equipment, storage, etc.)
  
  * Software to patch: Firmware, operating systems, and applications for server platforms

  * Outage restrictions: Must adhere to scheduled outage windows for all nonemergency situations

  * Existing mitigations: Network-based security controls restricting access to the assets and security controls running on the assets themselves

  * Level of impact to the organization if compromised: High

### Define Maintenance Plans for Each Maintenance Group

Organizations should define a maintenance plan for each maintenance group for each applicable risk response scenario.

* Maintenance Plans for Routine Patching

    Organizations should consider adopting phased deployments for routine patching in which a small subset of the assets to be patched receive the patch first.

    Organizations should offer flexibility with how soon routine patches are to be installed, while also forcing installation after a grace period has ended.

* Maintenance Plans for Emergency Patching

    Organizations should consider using the same general approach for emergency patching as for routine patching, except with a highly accelerated schedule.

* Maintenance Plans for Emergency Mitigation

    Organizations should plan for the quick implementation of multiple types of emergency mitigations to protect vulnerable assets.

    Organizations should plan to replace emergency mitigations with permanent fixes.

* Maintenance Plans for Unpatchable Assets

    Organizations should plan to implement multiple types of long-term risk mitigation methods besides patching to protect vulnerable assets.

    Organizations should plan to implement multiple types of mitigations to protect vulnerable unpatchable assets.

    Organizations should plan on periodically reevaluating their alternatives to patching.

### Choose Actionable Enterprise-Level Patching Metrics

* Take advantage of low-level metrics that they already collect when developing enterprise-level metrics to capture patching performance

* Utilize their existing low-level metrics to develop enterprise-level metrics that reflect the relative importance of each vulnerability and patch.

* Frequently update their low-level metrics and strive for them to be as accurate as possible in order to improve the enterprise-level metrics based on them.

1. Vulnerability Response Time

1. Patch Deployment Time

1. Patch Coverage Rate

1. Patch Failure Rate

1. Re-patching Rate

1. Vulnerability Exposure Time

1. Risk Exposure Index

1. Patch Dependencies

1. Patch Testing Success Rate

### Consider Software Maintenance in Procurement

Organizations should take software maintenance into consideration when procuring software.

1. Will you be releasing updates for this software to address vulnerabilities?

1. Approximately how many patches, updates, and upgrades do you expect to release each year for this software? On average, how quickly do you expect to address each vulnerability and release a patch? Do you bundle patches together or is each patch separate? How often do you anticipate releasing emergency updates?

1. For how many years are you committed to correcting vulnerabilities in the software?

1. Will you release updates on a regular schedule, as needed, or both? If a schedule will be followed, what is that schedule (weekly, monthly, quarterly, etc.)?

1. Do you have a vulnerability disclosure and incident response program for your software? How transparent are you in your security-related communications to your customers?

1. When a vulnerability in your software becomes public but a patch, update, or upgrade is not available, how do you recommend that customers protect their computing assets
running your software? Will you provide an emergency mitigation to prevent vulnerability exploitation while maintaining most or all software functionality?

1. When your software is patched or updated, how disruptive will that be to the operating software? For instance, will it require restarting the software, rebooting the asset on which the software is running, etc.?

1. How do you test your patches before release? How often do customers experience significant issues with your patches? Do you provide rollback capabilities for uninstalling patches?

---

## References

1. [NIST - Guide to Enterprise Patch Management Planning:Preventive Maintenance for Technology](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-40r4.pdf)

1. [What is Security Controls](https://ibm.com/topics/security-controls)

1. [FedRAMP and FIPS-Defined Impact Levels](https://linkedin.com/pulse/fedramp-fips-defined-impact-levels-continuum-grc)

1. [What Is An Attack Surface?](https://fortinet.com/resources/cyberglossary/attack-surface)
