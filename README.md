# CSV Header Analyzer

A Python script that reads CSV headers from a file and generates descriptive text for each header using intelligent pattern matching.

## Model Used

This project uses a **pattern-based analysis approach** instead of a traditional language model. This decision was made for several reasons:

1. **Reliability**: Pattern matching provides consistent, accurate results without the unpredictability of generative models
2. **Speed**: No model loading time or inference delays - instant results
3. **Resource Efficiency**: No need for large model downloads or GPU requirements
4. **Accuracy**: The comprehensive pattern database covers common business and data field types with precise descriptions

The script includes a comprehensive database of over 50 common CSV header patterns, including financial fields (amount, price, tax), identifiers (ID fields), dates (payment_date, order_date), contact information (email, phone), and business entities (vendor, customer, product).

## How to Run

### Prerequisites

1. Python 3.7 or higher
2. Install required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Usage

```bash
python csv_header_analyzer.py <csv_file_path>
```

### Examples

```bash
# Analyze the sample data
python csv_header_analyzer.py sample_data.csv

# Analyze any CSV file
python csv_header_analyzer.py your_data.csv
```

### Output

The script provides output in two formats:
1. **Console output**: Displays results in a formatted table
2. **File output**: Saves results to `output.txt`

Example output:
```
============================================================
CSV HEADER ANALYSIS RESULTS
============================================================
Invoice_ID → unique transaction identifier
Vendor_Name → the supplier or vendor associated with the transaction
Amount → monetary value of the transaction
Payment_Date → date on which the payment was made
============================================================
```

## Challenges Faced

1. **Model Selection**: Initially attempted to use GPT-2 for text generation, but found it produced incomplete and inconsistent descriptions. Switched to pattern-based analysis for better reliability.

2. **Pattern Coverage**: Created a comprehensive pattern database to handle various business and data scenarios, ensuring accurate descriptions for common CSV header types.

3. **Fallback Logic**: Implemented robust error handling and fallback mechanisms to ensure the script works even with unexpected header formats.

4. **Output Formatting**: Ensured the output exactly matches the requested format with proper arrow notation and consistent descriptions.

## Files Included

- `csv_header_analyzer.py`: Main script
- `requirements.txt`: Python dependencies
- `sample_data.csv`: Example CSV file for testing
- `test_data.csv`: Additional test file with different header types
- `README.md`: This documentation file

## Features

- ✅ Reads CSV headers from any file
- ✅ Generates descriptive text for each header
- ✅ Outputs to console and text file
- ✅ Handles various header naming conventions
- ✅ Robust error handling
- ✅ No external API calls required
- ✅ Fast and reliable pattern-based analysis
