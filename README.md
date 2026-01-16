# State-of-Health-SOH-battery-prediction
The State of Health (SOH) of a battery indicates how its current capacity compares to when it was new. For example, if a battery originally lasted 10 hours but lasts only 7 hours after two years of use, its SOH is 70%. In this project, researchers simulated battery usage over time, and machine learning models are used to predict SOH.

## State of Health (SOH) Derived Forumla 

In this project, the SOH formula is derived because the original researchers did not explicitly calculate the SOH values.

The SOH is calculated as:

**SOH** = (Cap(W) / Cap(i)) × 100%

Where:
- **Cap(W)**: Battery capacity at cycle *W* (after a certain number of charge and discharge cycles)
- **Cap(i)**: Initial battery capacity when the battery was new
- A **cycle** refers to one complete charge and discharge process of a battery. In other words, when a battery is used from 100% down to 0%, one full cycle is completed.
