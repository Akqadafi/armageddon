
Main responsibilities

1. Retrieve and validate the finding

The EventBridge event should contain only routing information.

Agent should retrieve the complete record from: waf-correlation-findings using finding_id.

This ensures the agent operates on the full stored evidence rather than trusting a small event payload.

It should verify:

    the finding exists
    status is still OPEN
    it has not already been processed
    severity is valid
    required evidence is present

2. Select a playbook

The playbook selection should be deterministic.

Example:


| Severity | Playbook                                              |
| -------- | ----------------------------------------------------- |
| Low      | Record only                                           |
| Medium   | Notify analyst                                        |
| High     | Notify and create incident                            |
| Critical | Notify, create incident, request containment approval |


SOAR execution record

I would also either create a fourth table or store response history inside the incident table.

Required table: soar-executions

