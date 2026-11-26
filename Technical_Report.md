
## 1. Executive Summary
The Stage 3 workflow processes medical delivery requests by collecting delivery details, validating requests and checking driver availability. Available drivers receive a priority route and dispatch through the electric fleet. If no driver is available, the system notifies the customer of a delay and returns the request to validation.

## System Prompt Architecture
- **Structure:** C-P-T-C (Persona, Context, Task, Constraints)
- **Data Isolation:** XML tags (`<flowchart_data>`)
- **Reasoning & Verification:** Chain-of-Thought `<thinking>` block + `INSUFFICIENT_DATA` anti-hallucination rule

## 3. Risk & Error Handling

The EcoRoute workflow may face risks such as missing delivery data, unavailable drivers, incorrect AI-generated routes, and malicious external instructions.

To manage these risks, the system validates delivery information, checks driver availability, and verifies AI-generated recommendations before dispatching vehicles.

If required information is missing, the system requests validation. If no driver is available, the customer is notified and the request returns to the validation stage.

### Red Teaming & Audit Logs

- **Prompt Injection:** External data is treated as untrusted information using XML tags.
- **AI Hallucinations:** Missing information is flagged as `INSUFFICIENT_DATA` instead of generating unsupported answers.
- **Data Validation:** Incorrect or incomplete delivery information must be detected before route assignment.
- **Error Logging:** Failed operations and security incidents are recorded for review.

### Red Teaming Audit Log

| Test | Expected Result | Status |
|---|---|---|
| Malicious instructions in external data | Ignore unauthorized commands | Pending |
| Missing delivery information | Request data validation | Pending |
| No driver available | Notify customer | Pending |
| Incorrect AI-generated route | Flag for verification | Pending |
