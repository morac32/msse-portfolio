MSSE601-ADR-risk-based-testing
Name: Carolann Mora 
Course: MSSE 601 – Software Engineering Fundamentals 
Term: Fall 2026 

1.	Context 

During Week 7, I drove and wrote the testing strategy for the Golden Bike Shop Software Quality & Test Plan. The team had limited time to verify an implementation that still lacked some functionality, including authentication and availability-by-period searches. Automated test coverage was also limited. The decision was how to allocate testing effort without overstating what the system could do or what had been verified.

2.	Options

Option 1: Test every requirement to the same depth. This would provide more uniform coverage but consume time on requirements with different levels of risk and potentially leave critical scenarios insufficiently tested.

Option 2: Test only basic successful workflows. This would be quicker, but would provide little evidence about concurrency conflicts, boundary conditions, or failure scenarios.

Option 3: Prioritize testing by risk. This would concentrate effort on requirements where failures could have the greatest operational impact, while explicitly recording what remained partially tested, unsupported, or untested.

3.	 Decision

I chose Option 3: risk-based testing, grouping non-functional requirements (NFRs) into three tiers:
•	Tier 1 - Deep testing: NFR-01 (data consistency), NFR-02 (concurrent transaction integrity), and NFR-03 (telemetry freshness).
•	Tier 2 - Targeted testing: NFR-04 (security), NFR-05 (pricing), and NFR-08 (usability).
•	Tier 3 - Limited testing: NFR-06 (recovery) and NFR-07 (operational reliability).

These tiers define the intended testing priorities; they do not mean that all planned tests were implemented or passed.

4.	Reasoning

I prioritized NFR-01, NFR-02, and NFR-03 because inconsistent records, duplicate reservations, and stale telemetry could lead to incorrect operational decisions. Given the team’s limited testing capacity, deeper checks of these risks offered more value than spreading effort equally across every requirement. Basic workflow testing alone would not expose important concurrency and boundary failures.

The incomplete implementation also limited what could be verified. For example, missing authentication meant the security gap could not be treated as a passing result, while unsupported availability-by-period functionality could not be fully tested. Recording these limitations was necessary to keep the test plan credible.

5.	Consequences

The decision focused effort on data integrity and reservation-related risks, but accepted less testing evidence for security, recovery, pricing, usability, and operational reliability. It also made the testing plan dependent on clear reporting: stakeholders must distinguish intended coverage from tests run, and a high-priority test that remains incomplete still represents unresolved risk.

With more time and a more complete implementation, I would first expand Tier 1 with boundary, repeated-execution, and concurrency tests, then increase security and recovery coverage. I would revisit the tier assignments if new defects, implementation changes, or production-readiness requirements showed that a lower-tier risk had become more significant.

Evidence
•	Week owned: Week 7 - Week 7 Software Quality & Test Plan
•	Where the decision shows up: Section 5, “Where We Stop, and the Risk We Accept,” and Section 7, “Team Decision Record.”
•	AI use: AI assisted with reviewing and editing the ADR for clarity and consistency. I revised the suggestions to reflect my decision and reasoning. This statement must match the team’s Week 7 AI Use Record.
<img width="468" height="637" alt="image" src="https://github.com/user-attachments/assets/6752cf3a-e131-418d-b2f0-55d9ac9dbb9a" />
