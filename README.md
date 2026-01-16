# State-of-Health-SOH-battery-prediction
The State of Health (SOH) of a battery indicates how its current capacity compares to when it was new. For example, if a battery originally lasted 10 hours but lasts only 7 hours after two years of use, its SOH is 70%. In this project, researchers simulated battery usage of time, and machine learning models are used to predict SOH.

## State of Health (SOH) Forumla 

The **State of Health (SOH)** of a battery measures how much usable capacity remains compared to its initial condition.

A **cycle** refers to one complete charge–discharge process of a battery. In other words, when a battery is used from 100% charge down to 0%, one full cycle is completed.

The SOH is calculated as:

\[
\text{SOH} = \left( \frac{\text{Cap}(W)}{\text{Cap}(i)} \right) \times 100\%
\]

Where:
- **Cap(W)**: Battery capacity at cycle *W* (after a certain number of charge–discharge cycles)
- **Cap(i)**: Initial battery capacity when the battery was new
