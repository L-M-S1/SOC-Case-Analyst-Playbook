Certain steps for a SOC analysis include finding an anomaly, checking it against known data, testing what could be going on with the data, and escalating the issue if it is a known malicious attack. 

The tools I would use for this depends on the OS, assuming Windows, they would be Windows proprietary event logs. If they were Linux, I would use an ELK stack (ElasticSearch, LogStash, and Kibana) 

Ai can be used to assist in sorting through data, determining if escalation should be done, with confirming its beliefs. Any information provided to an AI assistant will be combed over to remove any sensitive information prior to prompting.
