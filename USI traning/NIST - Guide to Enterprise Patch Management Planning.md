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

   1. automatically

   1. manually

        When directed to do so by a user, administrator, vendor, or tool.

        As a result of other software being installed or updated.

        Through the replacement of removable media used by an asset.

    Some installations require administrator privileges, such as installing firmware patches for a BIOS. Some patch installations require user participation or cooperation.

* **Change software configuration and state**

    In some cases, making a patch take effect necessitates implementing changes. (Including restarting patched software, rebooting the operating system or platform on which the patched software runs, redeploying the applications, or altering software configuration settings)

    In other cases, no such changes are needed.

---

## References

1. [NIST - Guide to Enterprise Patch Management Planning:Preventive Maintenance for Technology](https://nvlpubs.nist.gov/nistpubs/specialpublications/nist.sp.800-40r4.pdf)

1. [What is Security Controls](https://ibm.com/topics/security-controls)

1. [FedRAMP and FIPS-Defined Impact Levels](https://linkedin.com/pulse/fedramp-fips-defined-impact-levels-continuum-grc)

1. [What Is An Attack Surface?](https://fortinet.com/resources/cyberglossary/attack-surface)
