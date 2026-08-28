# Project-Title---Data-Visualization
1. Data Integrity and Preprocessing Insights
Missing Value Impact: Missing data was confined to spatial location columns (pickup_zone, dropoff_zone, pickup_borough, dropoff_borough) and the payment column. Imputing payment with the mode and dropping unrecorded spatial points reduced the dataset from 6,433 to 6,383 rows (a negligible ~0.78% data loss), ensuring strict spatial integrity for borough-level aggregations.
Duplicate Records: Zero duplicate rows were found, confirming high initial recording fidelity.
2. Geographic and Demand Distribution
Manhattan Dominance:
oThe Count Plot reveals that Manhattan accounts for the vast majority of taxi pickups, followed by Queens, Brooklyn, and negligible traffic from the Bronx.
oThe Bar Chart demonstrates that Manhattan generates the highest cumulative fare revenue by a substantial margin, driven primarily by trip volume rather than individual trip distance.
Tipping Patterns Across Boroughs:
oThe Box Plot shows that while Manhattan has a consistent tipping behavior around the median, high-value tip outliers occur across Manhattan and Queens (often tied to longer transit journeys such as airport routes).
3. Financial and Transactional Dynamics
Payment Method Preferences:
oThe Pie Chart highlights that electronic payments (credit card) represent the dominant share of transactions compared to cash.
Fare Distributions Across Payment Channels:
oThe Violin Plot shows that credit card transactions have a longer, wider upper tail for fare amounts. Cash transactions are heavily concentrated in lower fare brackets, indicating that riders prefer card payments for expensive or long-distance rides.
Temporal Trend (Fare Over Time):
oThe Line Chart demonstrates that mean daily fare fluctuates within a stable bounded band across the recorded timeline, with isolated spikes likely reflecting weekend travel patterns or adverse weather/demand shifts.
4. Trip Characteristics and Correlations
Distance Distribution:
oThe Histogram shows a sharp right-skewed distribution. The majority of trips are short-distance (under 3–5 miles), typical of dense urban commuting.
Distance vs. Fare Dynamics:
oThe Scatter Plot shows a strong positive linear relationship between trip distance and fare. Borough clustering highlights that intra-Manhattan trips cluster at the lower end (low distance, lower fare), whereas trips originating in Queens often span longer distances with higher baseline fares (e.g., JFK/LaGuardia airport runs).
Correlation Analysis:
oThe Heatmap and Pair Plot confirm extremely strong positive correlations (r>0.90) between distance, fare, and total.
otolls correlate moderately with higher distances and totals (primarily associated with inter-borough bridge and tunnel crossings).
Key Takeaways
1.Core Business Driver: NYC taxi operations in this dataset are predominantly short-distance, credit-card-funded trips concentrated in Manhattan.
2.High-Margin Segments: Longer-distance routes originating in outer boroughs (notably Queens) yield significantly higher individual fares, tips, and toll revenues.
3.Data Quality Note: Future iterations should ensure the df_cleaned DataFrame is passed to downstream visualization calls rather than the original df to avoid unhandled spatial NaN artifacts.
