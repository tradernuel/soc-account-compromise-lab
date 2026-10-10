Investigation 001: Repeated Failed Logon Attempts

Objective

Investigate failed Windows authentication events and determine whether repeated failures are visible in the Security event log.

Lab Environment

Operating system: Windows

Tool: Windows Event Viewer

Log source: Windows Security

Event ID: 4625 — Failed logon

Test Procedure

Opened Windows Security logs in Event Viewer.

Filtered the log for Event ID 4625.

Attempted to sign in with an intentionally incorrect password three times.

Refreshed the filtered log and examined the resulting events.

Observations

Three new failed-logon events appeared at approximately 16:02:27, 16:02:31, and 16:02:34.

An older failed-logon event was also present.

The inspected event reported an invalid username or password.

The three test attempts occurred within a short time window.

Analysis

The new events demonstrate that Windows records failed authentication attempts. Several failures close together can be a useful detection signal, but the known test activity explains these particular events.

Conclusion

Result: Expected test activity observed.

The controlled test generated observable failed-logon events. No evidence from this test alone establishes an actual account compromise.

Limitations

The test was performed locally on the analyst's own computer.

The events do not establish the identity or intent of an external attacker.

No automated alerting or detection rules have been configured yet.

## Evidence Screenshot

evidence/6a364c4e-ccdd-46b8-afa0-1465be2c74af.jpg
evidence/d3db718d-3aef-4efa-bc30-2db96705262a.jpg
evidence/ee3ab16a-8935-426e-9f0f-adf283df9b54.jpg


The screenshot shows three failed-logon events generated during the controlled authentication test.

