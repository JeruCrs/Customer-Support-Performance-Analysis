## 📉 LinkUp Broadband | Sales Performance and Revenue Decline Analysis

### 🏢 Company Background
LinkUp Broadband is a **fictional internet service provider** in the Philippines that provide services across different regions such as NCR, Luzon, Visayas, and Mindanao.

**Business Situation:** the Customer Support Manager, has been hearing more complaints about slow support. She needs to find out where the support delays are coming from and whether slow resolution is actually hurting customer satisfaction, before she presents to her director in two weeks.

**Purpose of the Analysis Breakdown:**
1. Measure how fast the team responds to and resolves tickets, and how that compares against the company's own 4-hour and 24-hour targets.
2. Identify which issue category and which part of the process are slowest.
3. Verify whether longer resolution times are linked to lower customer satisfaction scores.
4. Provide actionable-insights evidence-based that the Manager can present to the director meeting, rather than presenting raw numbers alone 
---
### 📝 Processes
1. First, I understood the business situation the manager was facing. She had been hearing complaints about slow support and had a raw ticket export, but no real analysis. I asked questions to break her concern into something I could actually analyze.
2. I clarified how she defined "slow." She confirmed LinkUp's own internal targets: a 4-hour first response and a 24-hour resolution, so I had a clear benchmark instead of guessing what "slow" meant.
3. Since she wanted to know if slow support was hurting satisfaction, I asked what would count as evidence of that. We agreed CSAT scores tied to resolution time would answer it, since that was the closest measure of customer sentiment she had.
4. After clarifying the situation, I broke the main question ("where are delays coming from, and is it hurting satisfaction?") into six smaller, answerable questions covering ticket volume, common issues, response/resolution speed, target performance, the slowest category, and the CSAT relationship.
5. I received the dataset and a data dictionary describing each column, its expected values, and known data quality issues, so I understood the data before touching it.
6. In the cleaning process, I used Power BI's Power Query to clean and standardize the data. I fixed inconsistent capitalization, spacing, and spelling in the text columns, standardized mixed date formats, removed exact duplicate rows, and followed the client's rules for null or invalid values instead of guessing. For example, leaving blanks as null rather than replacing them with 0 or an average, and never deleting a whole row over one bad field. I kept the raw import as a separate, untouched query and did all cleaning in a second query built on top of it.
7. After cleaning, I built helper columns like resolution_bucket and month to group the data, then created DAX measures for the averages, medians, and the two target percentages, being careful to exclude blanks from those calculations rather than treating them as zero or as "met."
8. I built visuals to explore each of the six questions. Ticket volume by month, issue category counts, response/resolution averages and medians, target percentage cards, resolution time by category, and CSAT by resolution-time bucket.
9. Through those charts and cards, I identified draft findings for each question, and where a result looked unclear or contradicted the underlying numbers, I went back to verify it against the raw data rather than accepting it at face value.
10. To give the findings context for a non-technical audience, I used Power BI visuals (cards, bar and column charts) and wrote plain-language chart titles that state what each visual shows, rather than just labeling the axes.
11. Once the findings were confirmed, I planned to build a set of recommendations tied to the evidence, to put on the Findings and Recommendations page for the Manager to bring to her director.
---
### ‼️Findings
- March recorded the highest ticket volume at 110 tickets, a 31% increase from February. The increase was driven primarily by Slow Internet and Billing tickets, which together accounted for the entire month-over-month increase. Luzon recorded the largest regional increase, with ticket volume rising 72% from February.
- Slow Internet was the most common issue category over the year period, concentrated mainly in the NCR and Luzon regions. Together, these two regions accounted for 59% of Slow Internet tickets.
- Average first-response time was 1.92 hours, with a median of 0.50 hours. Average resolution time was 31.12 hours, compared with a median of 22.65 hours, indicating that a smaller number of longer-running tickets are pulling the average upward.
- 85% of tickets met the 4-hour first-response target, while 53% met the 24-hour resolution target.
- Installation had the longest average resolution time at 68.7 hours, with a median of 53 hours. Within Installation tickets, Low- and Medium-priority tickets also had substantially longer average resolution times than High- and Urgent-priority tickets.
- Tickets resolved within 24 hours received an average CSAT of 4.34, compared with 3.17 for tickets taking longer than 24 hours, indicating that longer resolution times are associated with lower customer satisfaction.
---
### 💡 Recommendations
- Monitor unresolved tickets approaching the 24-hour target and establish an escalation process for tickets at risk of breaching the target.
- Review Installation workflows, handoffs, scheduling, and escalation points, with particular attention to Low- and Medium-priority tickets.
- Prioritize tickets exceeding 24 hours for review, as these tickets were associated with lower average CSAT.
- Continue monitoring Slow Internet tickets due to their high volume, while addressing Installation separately as the largest resolution-time concern.
---
### 🛠️ Tools and Technologies
- Application: Microsoft PowerBI
- Data Cleaning: Power Query
- Exploratory Data Analysis and Visualization: Microsoft PowerBI Charts and Graphs
