# Course 6 Module 4 - Detection and Response

## Practices for Log Collection

- Log: record of eventys occurring within organizations system

# Log Types to Record:

- Network: devices like firewall, routers, switches
- System: operating systems
- Application: software application
- Security: systems like antivirus or IDS
- Authentication: login attempts

## Log File Formats

# JSON File Formats

- Format: lightweight, easy to read/write
- Syntax Components:
	• Key-value Pairs: "key" : "value"
	• Commas: used to separate data items
	• Double Quotes: enclose text data
	• Curly Brackets: enclose object
	• Square Bracket: enclose an array

# Syslog

- Standard: standard for logging/formatting data
- Format Components: native language format for Unix systems
	1. Header: contains timestamps, hostname, application name, and message ID
	2. Structured Data: optional additional information enclosed in square brackegts
	3. Message: detailed log message about the event
- Priority: the urgency of the event, enclosed in angle brackets, typically lower numbers indicate higher urgency
- Transport: uses port 514 for plaintext and 6514 for encrypted logs

# XML (eXtensible Markup Language)

- Format: native to windows system )
- Syntax Components:
	• Tags: paired start (<tag>) and end (</tag>) tags that store and identify data
	• Elements: data and its surrounding tags
	• Attributes: provide additional info about an element

# CSV (Comma Seperated Format)

- Format: uses commas to separate data values

# CEF (Common Event Format)

- Format: uses pipe character (|) to separate core fields
- Structure: defined by syntax ( Versoion | Device Vendor | Device Product | Device Version | Signature ID | Name | Severity | Extension )

## Detection Tools and Techniques

# IDS Technologies

- Hist-based IDS (HIDS)
	• app installed on individual host to monitor activity
	• installed on all endpoints
	• monitors inbound/outbound traffic, file systems, system resource usage, and user activity
- Network-based IDS (NIDS)
	• app that collects/monitors network traffic and data
	• installed on devices at specific points in network
	• detects malicious network traffic between devices
- Combined Use
	• using both HIDS and NIDS
	• provides multi-layered approach and comprehensive view of activity

# Detection Techniques

1. Signature-based Analysis
- Definition: detects threats by comparing current activities against database of knwn patterns linked to malicious activity
- Advantages: low rate of false positives
- Disadvantages: signatures can be evaded, requires constant update, inability to detect unknown threats
2. Anomaly-based Analysis:
- Definition: flags any behaviors that deviates from predefined baseline of normal or expected system activity
- Phases:
	• Training Phase: data collected to establish baseline of normal system behaviours
	• Detection Phase: current system activity compared against baseline
- Advantages: ability to detect new/evolving threats
- Disadvantages: high rate of false positives, pre-existing compromise

## Suricata
- open-source tool functioning as an IDS, IPS, and network analysis tool

# Rules (signatures)

- Purpose: identify specific patterns, behaviour, and conditions of network traffic that indicate malicious activity
- Detection Method: uses signature analysis
- Three Components of Signature:
	1. Action: action to take if signature matches network activity (alert, pass, drop, reject)
	2. Header: includes network traffic details (IP, ports, protocol, traffic direction)
	3. Rule Options: used to customize signatures, ordering is important
- Rule Ordering Processing: prossesses rules in default order (pass, drop, reject, alert). Order affects final verdict for a packet, especially ith conflicting rules
- Custom Rules: customizing helps minimize false positive alerts

# Configuration and Logs

- Configuration File: suricata.yaml, which uses YAML file format to configure srttings and customize how IDs interact with environment
- Log Files Generated:
	• eve.json: standard log file storing detailed info/meta data in JSON format. Contains unique identifiers called flow_id to correlate between logs
	• fast.log: legacy file format that records minimal alert info, used for basic logging/alerting

## Log Sources and Log Ingestion

# SIEM Process Refresher

1. Collect and aggregate data: gather event data from various sources
2. Normalize data: convert collected data into standard, consistent format
3. Analyze data: correlate data to find patterns indicating unusual/malicious activity

# Log Ingestion

- Definition: process of collecting/importing data from log sources into SIEM tool
- Purpose: provides data for SIEM to work effectively
- Data Handling: SIEM creates copy of event data it receives and stores it
- Data Types: authentication attempts, network activity, etc

# Log Forwarders

- Function: software that automates process of collecting/sending log data from sources to SIEM
- Necessity: manual upload of logs is inefficient for networks with thousands of systems
- Tooling: many SIEM tools use their own proprietary log forwarders or integrate with open-source forwarders

## SIEM Search Methods

# Splunk Searches
- Language: uses Search Processing Language (SPL) to search/retrieve events from indexes
- Basic Search: index=main fail
	• index=main: tells Splunk to retrieve events from index named main
	• fail: search term, returns any event containing this term
- Pipes [|]: separates/chains commands. The output of proceeding command becomes the input for the next command
	• (eg: index=main fail | chart count by host)
- Wildcards (*): special characters that substitute for any character, useful for finding similar but not identical data
	• (eg: index=main fail* [searches for "fail", "failure", "failed", etc])












