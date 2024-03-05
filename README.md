# Peoplebox_assignemnt

The provided Python code transforms the input CSV file containing employee data into a structured format representing historical records of employee compensation, engagement, and performance reviews.

1. Sorting: The data is sorted by Employee Code and Date of Joining to ensure chronological order, which is necessary for deriving effective and end dates.

2. Deriving Effective and End Dates: The effective date and end date for each historical record are derived. The end date is set as one day before the next effective date to avoid overlap. For the latest record of an employee, a far-future date (e.g., 2100-01-01) is assigned as the end date.

3. Transforming Columnar Data: Columnar data related to compensation, engagement, and review are transformed into a row-based format. Each row represents a specific period with consistent data, facilitating historical data analysis.

4. Handling Missing Data: Missing data are filled in by inheriting values from the most recent past record for the same employee, ensuring continuity and accuracy of the historical records.

5. Writing Output to CSV: The transformed data is written to a CSV file formatted for historical data analysis, including fields for employee identifiers, compensation, dates, performance ratings, and engagement scores.

Assumptions:
- Compensation, pay raise date, variable pay, performance rating, and engagement score remain constant until changed.
- Missing values are filled with the last known values.
