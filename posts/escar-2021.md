---
author: Kevin Gomez Buquerin
title: "Structured methodology and survey to evaluate data completeness in automotive digital forensics"
date: 2021-10-11T09:31:07+02:00
description: "Publication for 19th escar Europe"
draft: false 
---

# Structured methodology and survey to evaluate data completeness in automotive digital forensics

## Abstract

The collection and analysis of potential evidence in digital forensic investigations is a challenging task that made its arrival in the automotive domain. It is accompanied by increasingly complex in-vehicle components with high diversity in used technologies and a wide range of external interconnections — which raises the question of what sources of information in which formats are even available for any analysis. The main contribution of this paper is an answer to this question as well as a cross-domain methodology to validate the completeness of the results in a structured way. We introduce a three-step process. It starts with a brainstorming session to create an initial basis of knowledge in a specific area of research. In a second step, system archaeology analyses are employed to establish an advanced knowledge base stemming from design documents and similar resources. The second step widens and deepens the knowledge and provides means to evaluate the quality of the brainstorming session results. The third step establishes expert analyses. Relevant automotive digital forensics stakeholders (e.g., OEMs, suppliers, etc.) were interviewed to collect information from expert groups and evaluate both initial phases. Based on this analytical, syntactic, inductive, and systematic research method, we offer a complete perspective for a specific area of research. The presented methodology is implemented to identify a complete set of data formats in automotive digital forensics. We conducted an online survey to evaluate data formats and tools in digital forensics with 56 experts participating and identified a total of 60 different data formats used in this domain.

## Conference

[19th escar Europe](https://www.escar.info/escar-europe.html)

## Links

- [Paper URL](https://hss-opus.ub.rub.de/opus4/frontdoor/index/index/docId/8351)
- [DOI](https://doi.org/10.13154/294-8351)
- [Survey Data](https://github.com/k-gomez/adf-survey-2021)

## Survey results

The survey results can be found on my [corresponding Github repository](https://github.com/k-gomez/adf-survey-2021). There are all results to reproduce results shown in the [paper](https://hss-opus.ub.rub.de/opus4/frontdoor/index/index/docId/8351).

However, here are some findings of the survey. Category referes to the survey section:

| Data format | Category | Description |
| ----------- | -------- | ----------- |
| .dd | Free mentions (uncathegorized) | raw dd file |
| .raw | Free mentions (uncathegorized) | raw memory dump |
| .l01 | Free mentions (uncathegorized) | EnCase forensics software |
| .dmg | Free mentions (uncathegorized) | Apple Disk Image file |
| .ivs | Free mentions (uncathegorized) | files contain initial vectors for stream analytic |
| .vdr | Free mentions (uncathegorized) | Example: [https://www.haleproducts.com/vehicle-data-recorder-vdr-system](https://www.haleproducts.com/vehicle-data-recorder-vdr-system) |
| .ewf | Free mentions (uncathegorized) | Expert witness file: [https://www.youtube.com/watch?v=3S-joLMbDGo](https://www.youtube.com/watch?v=3S-joLMbDGo) |
| .aff | Free mentions (uncathegorized) | advance forensics file format |
| MIB-Traces | Free mentions (uncathegorized) | Java Logs |
| .mem | Free mentions (uncathegorized) | memory dump |
| .vmem | Free mentions (uncathegorized) | virtual memory dump |
| .img | Free mentions (uncathegorized) | image file |
| .aff4 | Free mentions (uncathegorized) | advance forensics file format new version |
| .a01 | Free mentions (uncathegorized) | ALZip by ESTsoft. But could be a typo for e01 files that are "Expert Witness compression Format" disk image file |
| Capture from CAN-bus | Free mentions (uncathegorized) | usually .pcap or .pcappng |
| .sqlite | Free mentions (uncathegorized) | .sqlite files from SQL databases |
| .mp4 | Free mentions (uncathegorized) |  files from onboard camera |
| .lef | Free mentions (uncathegorized) | EnCase Logical Evidence Data** |**
| .odx | Free mentions (uncathegorized) | BizTalk Server Orchestration File which was developed by Microsoft |
| .pdx | Free mentions (uncathegorized) | Index file created by Adobe Acrobat, a document creator and viewer program; contains an index of documents and directories |
| .bin | Free mentions (uncathegorized) | binary data |
| .no | Free mentions (uncathegorized) | unknown |

| Data format / Tool / Source | Automotive component |
| --------------------------- | -------------------- |
| OEM Diagnostic tool read-out report or printscreens | Battery related systems |
| V2GTP used for charge control between car and charge point | Battery related systems |
| RTM data format used in China | Battery related systems |
| Memory dumps created by using debugging interfaces, such as JTAG, on the hardware component | Battery related systems |
| Diagnostic Trouble Code Readings | Battery related systems |
| WLAN | End-point devices |
| 5G | End-point devices |
| obd dongle | End-point devices |
| BLE | End-point devices |
| backend | End-point devices |
| PDX | End-point devices |
| ODX | End-point devices |
| lime/avml memdumps | End-point devices |
| mobile | End-point devices |
| ProtoBuf | End-point devices |
| NAND flash dump | Telematics control unit |
| HTTP RESTfull | Telematics control unit |
| MQTT | Telematics control unit |
| 802.11p | Telematics control unit |
| HTTP(S) HTML based | Telematics control unit |
| XML | Telematics control unit |
| ProtoBuf | Telematics control unit |
| tcu | Telematics control unit |
| wave | Telematics control unit |
| PTP gPTP SyncE | Telematics control unit |
| Text Logs | Telematics control unit |
| NOR flash dump (for example Audi MMI and BMW CIC) | Infotainment |
| BT4, BT5, BTLE | Infotainment |
| MMC | Infotainment |
| USB | Infotainment |
| Franca IDL | Infotainment |
| A2B | Infotainment |
| SOME/IP | Infotainment |
| if linux-based: memdumps as above | Infotainment |
| any media files and their metadata | Infotainment |
| Sync Gen 3 | Infotainment |
| info 3.5 GM | Infotainment |
| binary images | Infotainment |
| Text Logs | Infotainment |
| TomTology extraction | External navigation system |
| becker | External navigation system |
| wayteq | External navigation system |
| Last Destinations Database | External navigation system |
| POI Database | External navigation system |
| OEM Diagnostic tool read-out report or printscreens | Comfort system |
| NPDU | Comfort system |
| OEM Diagnostic tool read-out report or printscreens | Immobilizer system |
| BTLE | Immobilizer system |
| NFC | Immobilizer system |
| Mobile Device Key Message Format defined by Car Connectivity Consortium | Immobilizer system |
| CCC Key protocols | Immobilizer system |
| No. of registered keys | Immobilizer system |
| OEM Diagnostic tool read-out report or printscreens | Gateway |
| Autosar Routing Spec | Gateway |
| L2 Ethernet Gateways | Gateway |
| Communication Logs (Tesla) | Gateway |
| Lane assist | Safety monitoring system |
| Automatic braking | Safety monitoring system |
| NAND flash dump | eCall |
| eCall report from dispatcher (court order) | eCall |
| GPS "Perlenschnur" | eCall |
| eCall SMS | eCall |
| Gen 11 GM | Airbag |
| Crashdata (EEPROM) | Airbag |
| DTCs | Airbag |
