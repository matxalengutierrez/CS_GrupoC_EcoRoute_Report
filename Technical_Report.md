
## 2.Process Logic Breakdown

**- Start: Customer Requests Medical Delivery:** Initiates the delivery process. Source: ‘Start: Customer Requests Medical Delivery’.

**- Data Input: Delivery Address & Urgency Level:** Collects the delivery address and urgency level. Source: ‘Data Input: Delivery Address & Urgency Level’.

**- Action 1: Validate Request Details:** Validates the submitted request details. Source: ‘Action 1: Validate Request Details’.
  
**- Decision: Is Driver Available?:** Checks driver availability and determines the next process path. Source: ‘Decision: Is Driver Available?’.
  
**- YES branch – Assign Priority Route:** Assigns a priority route when a driver is available. Source: ‘Assign Priority Route’.
  
**- Dispatch Electric Fleet Driver:** Dispatches an electric fleet driver along the assigned priority route. Source: ‘Dispatch Electric Fleet Driver’.
  
**- End: Medical Package Delivered:** Ends the workflow when the medical package is delivered. Source: ‘End: Medical Package Delivered’.
  
**- NO branch – Notify Customer Delay:** Notifies the customer when no driver is available. Source: ‘Notify Customer Delay’.
  
**- Loop – Return to Validation:** Returns the process to request validation after notifying the customer of a delay. Source: ‘Validate Request Details’.
