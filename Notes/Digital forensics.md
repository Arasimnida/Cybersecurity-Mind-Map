## Introduction

Digital forensics (aka: cyber forensics) is a branch of forensic science and [[Cyber security]] concerned with the proper acquisition, preservation and analysis of [[Digital evidence]], typically after an unauthorised access or use has taken place.

![[forensics-timeline.png]]


The **goal of digital forensics** is to explain the current state of a *digital artefact*. 

A famous forensics case is [[The BTK Killer]] who occurred in 1991.

**Forensic analysis use their wits and tools to reveal facts.** if we try to prove the case one way or the other we will find only what we expect. Determine the guiltiness or not of someone is not our job. We always have to look deep because some adversaries may use [[Anti-forensics tools]] or try to hide data. During a forensics investigation some [[Forensics tools]] are used and *should be used*. 
## Legal Framework

**The court decides** whether or not a [[Crime]] is committed. The court need to follow **rigorous methodology** in handling [[Digital evidence]]. It is really important to respect the law, because we don't want the court to reject ours [[Digital evidence]]. 

Our evidences must respect the guidelines for [[Admissibility]]. 

A forensic analysts operate within a legal framework.

![[forensic-LegalFramework.png]]

In traditional forensics the [[Locard's Exchange Principle]] is a guiding principle.

Evidence must be **admissible**, which is determined by the judge according to a set of exclusionary rules: [[Relevance]], [[Authenticity]], [[Credibility]], and proper search and seizure.

To reduce the chance of producing inadmissible evidence, digital investigators must follow a strict [[Methodology]].

## Digital Investigation Process

Predefined pattern of activities when performing an investigation to generate **admissible evidence**. Serve as useful **points of reference** for reflecting on the state and nature of the field. *Independent of a particular technology* in corporate, military, and law enforcement environments. One famous and important model is the [[Kruse & Heiser model]], because it's linear and easy to remember. Beyond Kruse, many more models are proposed but in general they end up being complex, subtle and hard to follow by the investigators.
#### Some limitations of digital investigation models:
- **Complexity:** Define many steps and cumbersome inter-relations
- **Rigidness:** In practice, most digital investigations do not proceed in linear fashion
- **Incompleteness:** Don't help digital investigators with some of the most important steps of each step of an investigation, including the completeness and repeatability of each step

In practice, digital investigators need to complement investigative models with a methodology that:
1. **guides** them in the right direction, while
2. allows them to maintain the **flexibility** to handle diverse situations
3. and preserves the **rigors** of forensic science

[[The scientific method]] provides such methodology.

## Data decoding

In digital forensics we need to interpret and analyse digital artefacts **correctly**. In [[Computer Systems]], data is always encoded in [[Binary]] To correctly interpret it we need to determine what **[[Data encoding schemes]]** was the artefact encoded as ?

In digital forensics we face 3 challenges related to data encoding:
1. We don't know how the data was encoded.
2. The data is corrupted (intentionally or accidentally).
3. The data is encrypted or steganogaphically encoded.

In order to face those challenges we are going to use [[Text editors]].

The way the raw data is represented and how it is rendered by applications can differ. Most editors allow to select the encoding scheme of a file to be loaded or saved. **The raw bytes contain the ground truth**. Therefore, in forensics, we usually need to inspect the raw bytes, for which we use a [[Hexadecimal editor]].

Knowing which [[Endianness]] is important in digital forensics because we have to be **correct**.

The challenge a forensics analyst is facing is to decode the data without knowing the correct [[Structured data type]]. The idea is to look for **[[Magic numbers]]** or [[Byte Order Mark (BOM)]]. We have to be aware that **magic number can be changed**. The footer of the file can also contains precious information for a forensics investigation.

If a file is **corrupted** and we try to repair it, we need to check if file [[Metadata]] is consistent with the file format spec. Excellent resource: http://www.garykessler.net/library/file_sigs.html. It is then possible to open the file using an [[Hexadecimal editor]] and apply fix.

If we are facing [[Encryption]] we have to use [[Cracking techniques]]. 

If we are facing [[Steganography]] we have to use [[Steganography techniques]] to read correctly all relevant information.

Three effects make **detection of [[Watermarking]] useless**:
1. Watermark cannot be detected
2. False watermarks are detected
3. Unauthorised detection of watermark

Example of a common investigation involving watermarks:
![[common-watermark-example.png]]

## Different branches of digital forensics

Digital forensics can be split in different branches: 
- [[Computer forensics]]
- [[Network forensics]]
- [[Mobile device forensics]]
- [[Cloud forensics]]


#cybersecurity #forensics





