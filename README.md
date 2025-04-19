## Project Title:
**Lottery Number Frequency Analyzer & Predictor**

## Description:
This code processes historical lottery draw data from a text file, cleans and converts it into a structured CSV format, analyzes number frequencies, and predicts the most probable numbers to appear in future draws. It supports both all-time and recent (e.g., last 90 days) analysis.

Updating the data text file with new draws will improve the accuracy of the predictions. However, keep in mind that this analysis only provides the probability of the winning numbers based on historical trends, and does not guarantee 100% accuracy.

---

## How It Works:

1. **convert_txt_to_csv**  
   Converts a raw `.txt` file with tab-separated values and full month names into a structured `.csv` file with proper date formatting (`DD-MM-YYYY`).

2. **clean_csv**  
   Cleans the converted CSV file by:
   - Removing rows where all values are missing (`-` or `–`)
   - Ensuring all values are 2-digit numbers (e.g., `5` → `05`)

3. **analyze_all_time**  
   Loads the cleaned CSV, analyzes number frequency across all draws, and prints:
   - Top 5 predicted numbers
   - Top 10 most frequent numbers with percentage appearances

4. **analyze_last_90_days**  
   Similar to the all-time script, but filters data from the last 90 days and predicts the most likely numbers based on recent trends.

---

## How to Use:

1. Place your raw data file (e.g., `data.txt`) in the project folder.
2. Run the jupyter scripts in the following order:
   ```bash
convert_txt_to_csv
clean_csv
analyze_all_time
analyze_last_90_days