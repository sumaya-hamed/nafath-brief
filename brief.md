Version: NAFATH-V2
Your track: Networking

Overview

The NAFATH-V2 project uses six IT fields to keep a 5G service working well for emergency workers.

Software engineering helps the system handle requests safely, even when the connection fails.

Artificial Intelligence (AI) helps predict network problems before they happen.

Mobile applications allow emergency workers to use important information without internet access.

Networking uses 5G network slicing to give important communications special network resources.

Cybersecurity protects the system from attacks and helps restore the service after problems.

Data engineering organizes information into reports to help managers understand network usage.

Together, these six fields help make the service reliable, safe, and easy to manage.

This brief focuses on 5G network slicing and how it can help emergency workers communicate during network congestion.

Software

HTTP methods have two important properties: safety and idempotency.

Safe methods, such as GET and HEAD, allow users to get information without changing the server’s data.

Idempotent methods include GET, HEAD, PUT, and DELETE. Repeating the same request has the same intended result as doing it once.

This is important when the internet connection fails. Some requests can be repeated safely, but POST requests need extra protection to avoid doing the same action twice.

Resource: RFC 9110 – HTTP Semantics
https://www.rfc-editor.org/rfc/rfc9110.html

AI

Overfitting happens when an AI model learns the training data too well but cannot make good predictions using new data.

Cross-validation helps test how well the model works. The data is divided into smaller groups, and the model is trained and tested using different groups.

This helps the team check if the model can predict network congestion correctly.

Before using the model, the operator should also test it with new and realistic network data.

Resource: Scikit-learn – Cross-validation
https://scikit-learn.org/stable/modules/cross_validation.html

Mobile

The mobile app should work even when there is no internet connection.

It should show saved information and allow emergency workers to save new updates on their devices.

The app should tell users when information may be old or when updates have not been sent.

When the internet returns, the app should send saved updates to the server and download new information.

It should also prevent duplicate updates and protect private information using encryption and secure connections.

Resource: Android Developers – Build an offline-first app
https://developer.android.com/topic/architecture/data-layer/offline-first


Networking

5G network slicing creates different logical networks using the same physical network infrastructure.

The operator can create a special network slice for emergency workers.

This slice can be designed to provide fast communication, reliable connections, and enough network capacity.

During busy times, network rules can give important emergency communications higher priority.

However, a dedicated slice cannot prevent every outage or cyberattack. The operator still needs strong security, backup systems, and continuous monitoring.

Resource: ETSI – 5G Management and Orchestration
https://www.etsi.org/deliver/etsi_ts/128500_128599/128530/16.06.00_60/ts_128530v160600p.pdf

Cybersecurity

The incident response process has six main steps:

1. Preparation: Prepare security plans, trained teams, backups, and monitoring tools.
2. Detection and Analysis: Find suspicious activity and understand the problem.
3. Containment: Limit the damage and stop the attack from spreading.
4. Eradication: Remove the threat from the system.
5. Recovery: Restore the service and check that it works safely.
6. Lessons Learned: Learn from the incident and improve security.

The team must work together to protect emergency communications and reduce service interruptions.

Resource: NIST – Computer Security Incident Handling Guide
https://csrc.nist.gov/pubs/sp/800/61/r2/final

Data

A star schema has one main fact table connected to dimension tables.

A snowflake schema has dimension tables connected to other related tables. It can reduce repeated information, but it is more complex.

For daily reports about network usage in different regions, a star schema is usually easier to use.

The fact table can store network usage information. The date and region tables can help organize the data.

This makes it easier for managers to compare network usage by date and region.

Resource: Microsoft Learn – Star Schema in Power BI
https://learn.microsoft.com/en-us/power-bi/guidance/star-schema
