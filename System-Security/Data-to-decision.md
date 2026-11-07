### 1: Who is this document for?

This document is for students and junior level analysts for the purposes of identifying a simple, standard list of first things to check when identifying an issue.

### 2: Examples of places to check.

|Source| Useful Information| Limitation|
|-----|----|---|
|Windows Event Log| Windows event log can allow you to view login events, application logs, system logs, and more with severity scores allowing for faster reaction to severe events.| Event logs don't necessarily tell you if an event is malicious.|
|Windows Defender| Windows defender shows file activity, device behavior, and can help detect malware| It does not show, nessesarily, what is going on throughout the entire network.|
|Windows Defender Firewall| Shows allowed and blocked traffic and can be configured to permit or restrict notifications depending on event type| It does not however result in immedient suspicion of malicious activity.|

### 3: Step-by-step procedure

|Step| Example|
|--|--|
|Ask the question| What makes me suspect there is malicious activity going on?|
|Identify a timeframe| Just before normal business hours, UTC 12:00-13:00|
|Identify the data| Login attempts from one or multiple devices|
|Inspect the data| number of attempts, frequency, brute force or spraying|
|Apply filters| once you know more about your data, hone in on the suspicious traffic|
|Record| Document everything in neat fashion according to your businesses procedures|
|Next steps| determine if the traffic truly is malicious or not and escalate the ticket if need be.|

### 4: Illustrative example

THIS DATA IS FICTITIOUS AND NOT TO BE ASSUMED TO BE BASED ON REAL DATA

|Time| User| Event ID| IP|
|--|--|--|--|
|7:00| Admin| 4655| 192.168.10.1|
|8:00| User1| 4656| 192.168.10.10|
|8:05| User1| 4655| 192.168.10.10|
|10:00| guest| 4655| 192.168.20.1|
|10:30| User1| 4656| 162.198.30.12|

(where 4655 is a successful login and 4656 is a failed login)

A broad scope could look like "all events from 11/7/2026" which would produce exactly what is listed in the table, or maybe even "show events between 7:00-10:00" which would show all but the third attempt at User1's login."

A narrow scope would be something like "List failed logins for User1 on 11/7/2026" which would produce this table

|Time| User| Event ID| IP|
|--|--|--|--|
|8:00| User1| 4656| 192.168.10.10|
|10:30|User1| 4656| 162.198.30.12|

Which allows you to see that at 10:30, there was a failed login attempt from a completely different IP address than the one currently connected to User1. 

### 5: Vender Learning

|Information Source| what was learned|
|---|---|
|Netacad| I learned most of what the different log sources were, what they provided and what their downfalls were via Netacad's Cyber Threat Management's second module and Data and Tools for Defense Analysis|
|Microsoft| I read up on windows specific tools through Microsoft's "windows security" pages|

### 6: Reflection

While I already had a fair understanding of Windows proprietary log tools before, I learned more about Linux tools and Splunk through these courses. I have completed the entirety of Netacad's Data and Tools for Defense Analysis, scoring roughly 93% on the final exam provided by the course and am currently working through finishing the Cyber Threat Management course. I have had AI assist me with drafting examples which I proceeded to fine tune with my own experiences and examples that I created. I believe that the skills I obtained during this class and learning from these modules will assist me in exceling in a field where log analysis is a mandatory as I will now be more comfortable identifying scope, reading data, and being able to use tools to help automate processes.
