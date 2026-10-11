MSSE601-ADR-risk-based-testing
Name: Carolann Mora 
Course: MSSE 601 – Software Engineering Fundamentals 
Term: Fall 2026 

1.	Context 

During Week 7, I worked on the Golden Bike Shop Software Quality & Test Plan. The team had limited time to test an incomplete implementation. Important gaps included missing authentication, unsupported availability-by-period functionality, and limited automated test coverage. I needed to determine how to prioritize testing without treating unverified functionality as successful.

2.	Options

Option 1: Test every requirement to the same depth. This would give the team a more uniform testing approach but would spread limited effort across requirements with different levels of risk.

Option 2: Test only successful, basic workflows. This would be faster and easier to complete, but would provide little evidence about concurrency problems, boundary conditions, or failure scenarios.

Option 3: Prioritize testing by risk. This would concentrate effort on the requirements where defects could have the greatest operational impact, while explicitly documenting areas receiving limited or no testing.

3.	 Decision

I chose risk-based tiers that groups nonfunctional requirements (NFRs) into three testing tiers (Option 3): 
•	Tier 1 - Deep testing: NFR-01 (data consistency), NFR-02 (concurrent transaction integrity), and NFR-03 (telemetry freshness).
•	Tier 2 - Targeted testing: NFR-04 (security), NFR-05 (pricing), and NFR-08 (usability).
•	Tier 3 - Limited testing: NFR-06 (recovery) and NFR-07 (operational reliability).

These tiers define the intended testing priorities; they do not mean every planned test has been completed or passed.

4.	Reasoning

Inconsistent records, duplicate reservations, and stale telemetry could directly disrupt shop operations, making NFR-01, NFR-02, and NFR-03 the highest priorities. Equal-depth testing could consume limited time on lower-risk checks, while happy-path testing would not adequately examine concurrency and boundary conditions. Missing functionality also limited what could be verified. A risk-based approach allowed the team to prioritize consequential failures while distinguishing unsupported or unexecuted tests from successful results.

5.	Consequences

This choice focused limited effort on data integrity and reservation-related risks but left less evidence about security, recovery, pricing, usability, and operational reliability. Tier 1 coverage also remained incomplete. With more time and a more complete implementation, I would add boundary, repeated-execution, and concurrency tests, then expand security and recovery testing. I would reassess the accepted gaps before any production deployment.

Evidence
•	Week owned: Week 7 - Week 7 Software Quality & Test Plan
•	Where the decision shows up: Section 5, “Where We Stop, and the Risk We Accept,” and Section 7, “Team Decision Record.”
•	AI use: AI assisted with reviewing and editing wording. I revised the suggestions to reflect my decision, reasoning and evidence. 
<img width="468" height="637" alt="image" src="https://github.com/user-attachments/assets/b5f64556-d4e7-4750-b0a9-b8d9e3aa3bda" />
