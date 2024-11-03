# upstox_option_chain
Upstox Options Chain Data and Margin Calculator
This project retrieves options chain data from Upstox for specific financial instruments and calculates margin requirements and premium earned for options trading. It uses the Upstox API to access options data, filter based on user input, and compute values required in options trading.  

  
Project Overview
This project is developed as part of a Python Development Internship assessment and focuses on:  
Retrieving the highest bid/ask prices for options contracts based on user inputs.  
Calculating the required margin and premium earned for options based on the retrieved data.  
The project is intended to showcase skills in data processing, API integration, and options trading data analysis.  
  

Features  
Retrieve Options Chain Data: Retrieve data for specific instruments, expiry dates, and options types (put/call).  
Calculate Margin and Premium: Calculate required margin and premium earned for selected options.  
User Interaction: Command-line interface allows users to input values for instrument selection, expiry date, and options side.  
  
Installation  

pip install requests pandas  
Set Up Upstox API Credentials:  

Obtain your API Key, Secret Key, and Redirect URI from the Upstox Developer Portal.  
Enter these values when prompted during script execution.  
  
Usage  
Run the Jupyter Notebook: Open the notebook in Jupyter and run each cell in order.  

Input API Details: When prompted, enter your api_key, secret_key, redirect_uri, and authorization code.  

Select Options: You will be prompted to select instrument_name, expiry_date, and side (put or call). The system will fetch and display relevant options data.  
  

View Results:  

Option Chain Data: Shows highest bid/ask prices.  
Margin and Premium Calculation: Displays required margin and premium earned for selected options.  
  
Project Structure  
Notebook Cells:  
Cell 1: Imports necessary libraries.  
Cell 2: Sets up user inputs and API authorization.  
Cell 3: Fetches and filters options chain and portfolio data.  
Cell 4: Defines main functions for retrieving and calculating options data.  
Cell 5: Runs a loop to allow user interaction and displays the results.  
  
Functions  
Function 1: get_option_chain_data  
Purpose: Retrieves options chain data for a given instrument, expiry date, and option type (put/call).  

  

Inputs:  
instrument_name: Name of the instrument (e.g., NIFTY).  
expiry_date: Expiration date in YYYY-MM-DD format.  
side: Option type - "PE" for put or "CE" for call.  
Output: A DataFrame containing instrument_name, strike_price, side, and bid/ask.  
Function 2: calculate_margin_and_premium  
Purpose: Calculates margin requirement and premium earned for each option contract.  

  
Inputs:  
data: DataFrame returned by get_option_chain_data.  
Output: DataFrame with margin_required and premium_earned columns added.  
  
Challenges  
API Integration: Handling multiple API requests, including managing authentication tokens.  
Data Filtering: Efficiently filtering and merging data from options and portfolio endpoints.  
Error Handling: Managing errors, such as missing data or invalid API responses, was essential for smooth execution.  

