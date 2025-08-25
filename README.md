Dress Attribute Analysis Project

Overview

This project analyzes dress attributes from an Excel file containing dress data. It extracts attributes such as Length, Silhouette, Sleeve Type, Neckline, and Waistline from image URLs and filenames using pattern matching techniques. The script then analyzes the distribution of these attributes, generates visualizations, and creates a detailed summary report.


Files in this Project
• `unified_dress_analysis.py`: The main script that combines all functionality into a single comprehensive program
• `dress_analysis_code_explanation.md`: A detailed explanation of the code structure and key components
• `Best_Seller_Tags_Completed.xlsx`: The output Excel file containing the dress data with extracted attributes
• `dress_silhouette_analysis.png`: A pie chart visualization of the silhouette distribution
• `vendor_dress_distribution.png`: A stacked bar chart visualization of vendor distribution by silhouette
• `Dress_Analysis_Summary.txt`: A detailed summary report of the analysis findings


Requirements
• Python 3.6+
• pandas
• numpy
• plotly
• openpyxl (for Excel file handling)


How to Use

Running the Unified Analysis Script

To run the complete analysis:


from unified_dress_analysis import DressAnalyzer

# Create an instance of the DressAnalyzer
analyzer = DressAnalyzer()

# Run the full analysis
analyzer.run_full_analysis()


This will:
1. Load and clean the dress data from the Excel file
2. Extract attributes for all dresses
3. Create visualizations of the attribute distributions
4. Find interesting examples from the analysis
5. Save the results to an Excel file
6. Generate a summary report





Key Components

DressAnalyzer Class

The main class that encapsulates all functionality:

• `__init__(self, excel_file='Best_Seller_Tags.xlsx')`: Initialize the DressAnalyzer with the Excel file
• `load_data(self)`: Load and clean the dress data
• `load_filters(self)`: Load filter values from the Filters sheet
• `extract_attributes_from_url(self, style, vendor, image_url)`: Extract dress attributes from image URLs
• `analyze_all_dresses(self)`: Extract attributes for all dresses
• `show_attribute_summary(self)`: Show summary statistics for the extracted attributes
• `create_visualizations(self)`: Create visualizations of the attribute distributions
• `create_silhouette_chart(self)`: Create a pie chart of the silhouette distribution
• `create_vendor_chart(self)`: Create a bar chart of the vendor distribution by silhouette
• `save_results(self)`: Save the results to an Excel file
• `create_summary_report(self)`: Create a summary report of the analysis
• `find_interesting_examples(self)`: Find interesting examples from the analysis
• `run_full_analysis(self)`: Run the full analysis pipeline


Attribute Extraction Algorithm

The core of the analysis is the attribute extraction algorithm, which uses pattern matching to identify dress attributes from image URLs and filenames. The algorithm:

1. Starts with default values for each attribute based on the most common values in formal wear
2. Extracts the filename from the URL for analysis
3. Uses pattern matching to identify keywords in the filename that indicate specific attributes
4. Updates the attribute values based on the identified keywords
5. Applies logical relationships between attributes (e.g., if a dress is strapless, it likely has a sweetheart neckline)


Visualizations

The script generates two visualizations:

1. **Silhouette Distribution Pie Chart**: Shows the distribution of dress silhouettes (A-Line, Mermaid, Jumpsuit, Ball Gowns, Two Piece Set)
2. **Vendor Distribution Stacked Bar Chart**: Shows the distribution of dress silhouettes by vendor for the top 10 vendors


Summary Report

The script generates a detailed summary report with:

1. Dataset overview (total dresses, vendors represented, extraction success rate)
2. Extraction method description
3. Key findings for each attribute (Length, Silhouette, Sleeve Type, Neckline)
4. Vendor insights
5. Accuracy and limitations of the analysis
6. Recommendations for further analysis and use of the data


Project Structure

dress-analysis/
\u251c\u2500\u2500 unified_dress_analysis.py      # Main script with all functionality
\u251c\u2500\u2500 dress_analysis_code_explanation.md  # Detailed code explanation
\u251c\u2500\u2500 README.md                      # This file
\u251c\u2500\u2500 Best_Seller_Tags.xlsx          # Input data file
\u251c\u2500\u2500 Best_Seller_Tags_Completed.xlsx  # Output data file with extracted attributes
\u251c\u2500\u2500 dress_silhouette_analysis.png  # Visualization of silhouette distribution
\u251c\u2500\u2500 vendor_dress_distribution.png  # Visualization of vendor distribution
\u2514\u2500\u2500 Dress_Analysis_Summary.txt     # Summary report of the analysis


Conclusion

This project demonstrates how to extract and analyze dress attributes from image URLs and filenames using pattern matching techniques. The unified script combines all functionality from individual scripts into a single comprehensive program, making it easy to run the entire analysis with a single command.