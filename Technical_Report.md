## 1. Executive Summary
The Stage 3 workflow processes medical delivery requests by collecting delivery details, validating requests and checking driver availability. Available drivers receive a priority route and dispatch through the electric fleet. If no driver is available, the system notifies the customer of a delay and returns the request to validation.

## System Prompt Architecture
- **Structure:** C-P-T-C (Persona, Context, Task, Constraints)
- **Data Isolation:** XML tags (`<flowchart_data>`)
- **Reasoning & Verification:** Chain-of-Thought `<thinking>` block + `INSUFFICIENT_DATA` anti-hallucination rule
