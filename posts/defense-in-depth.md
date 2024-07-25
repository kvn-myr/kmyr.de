---
author: Kevin Gomez Buquerin
title: "Defense in depth through combination of MITRE ATT&CK™, MITRE D3FEND™, and NIST SP 800-53"
date: 2022-06-02T10:06:20Z
draft: false
---

# Defense and detection in depth

I have given a presentation at the [Ninth EU MITRE ATT&CK® Community Workshop June 2, 2022](https://www.attack-community.org/event/) on this topic. Recordings are not available. However, you can find the presentation on the [workshop website](https://www.attack-community.org/event/).

The [MITRE ATT&CK](https://attack.mitre.org)™ framework is used by SOCs (Security Operation Center), CERTs (Computer Emergency Response Team), and various other security teams in different organizations. It enables the description of tactics and techniques of various threats. The framework gives organizations the ability to determine an attacker's current position in their attack and predict possible future moves. In addition, several tools use [MITRE ATT&CK](https://attack.mitre.org/)™ to provide a common vocabulary and naming of tactics and techniques.

However, one quickly realizes that pure knowledge of the most important and relevant tactics/techniques is not very helpful if the knowledge gained is not used. Many teams create detection rules based on the techniques identified. An example is the [SIGMA](https://github.com/SigmaHQ/sigma) format, which allows you to add the relevant techniques detected by the rule. In this way, security teams can identify coverage of adversaries relevant to their organization.

## What does MITRE D3FEND™ and NIST SP 800-53 have to with it?

*Good* detection and sometimes prevention is enough for most companies. But you can go further! Some time ago, [MITRE D3FEND](https://d3fend.mitre.org)™ was released. I would argue that it is similar to [NIST SP 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final), which describes various security controls. Using [MITRE D3FEND](https://d3fend.mitre.org/)™, you can search for [MITRE ATT&CK](https://attack.mitre.org)™ techniques and find the appropriate defenses within the 5 defense tactics (harden, detect, isolate, deceive, and evict).

[NIST SP 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) is a *comprehensive standard* that describes various security controls for different *families* (no, not malware families :)), such as access control, awareness and training, audit and accountability, configuration management, media protection, and more. A mapping between [MITRE ATT&CK](https://attack.mitre.org) and [NIST SP 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final) is available through [the MITRE CTID project](https://ctid.mitre-engenuity.org/our-work/nist-800-53-control-mappings/).

## Combining all three

To combine all three frameworks, you need one prerequisite: a list of relevant adversaries to focus on. This information can come from a variety of sources. The following list gives you some examples (the list is definitely not exhaustive):

- TI (Threat Intelligence) team / tools / vendors.
- OSINT (Open-Source Intelligence), i.e., Googling for relevant threats to your business/industry
- Risk Department: describe what your key risks are. You can determine how an attacker might exploit them

If you use the [MITRE ATT&CK](https://attack.mitre.org)™ matrix, you can select some attackers and malware families that are relevant to you. At the end, you can export the matrix in `.json` format. The file contains a list of defined threats and their corresponding techniques. These techniques can be prioritized. For example, if several of your adversaries use the same technique, you can consider prioritizing them. The resulting `.json` file allows you to prioritize the techniques based on their score (number of times the technique has been used by the adversary). The top techniques can be used in content engineering to figure out what to focus on and what techniques to identify. You can also determine the coverage of your top techniques. This can be useful for your management and other reports.

The prioritized or even the full list of techniques is used in combination with [MITRE D3FEND](https://d3fend.mitre.org)™ to gather defenses. Again, you can create a scoring. The more techniques that lead to a particular defense, the higher that mitigation should be prioritized. The same is true for [NIST SP 800-53](https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final), where the most important techniques can be broken down to specific systems and services. You can use this information to determine the appropriate security controls. And these top N lists are also very useful for reporting and strategic decision-making. 

### Benefits 

As mentioned earlier, this methodology allows you to prioritize your organization's techniques and defenses. It also allows you to make strategic decisions that are statistically sound and not just based on your gut feeling or your boss's. Which IDS do you want to buy? Now, evaluate which top techniques and defenses the IDS can cover.

In addition, the lists you create can be converted into top 10 or top 5 lists. This allows you to create reports specific to your organization, which can be helpful in discussions with other teams and management.

One major benefit I see is the ability to determine coverage of detection, prevention and defense. You may find that you have 80% coverage for a particular technique. If you have more protocols, that coverage increases to 90%.

### Problems and shortcomings

Well, all that glitters is not gold with this methodology. You are completely dependent on the *correctness* of all frameworks. If the techniques used by a particular threat actor are not covered, the relevant techniques will not be prioritized.

In addition, you are highly dependent on a strong focus on TI and *complete* lists of your adversaries, including their tactics and techniques.
