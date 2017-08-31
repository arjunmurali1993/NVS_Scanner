#NVS Strategy Evaluator

This is an Excel VBA based scanner, that scans all NSE stocks and outputs a list of the ones that are trending.

###Requirements
1. Excel (Any Version)
2. ta-lib Technical Analysis Add-in for Excel (file included)
3. Internet Access

###Instructions
1. Download and extract to C:\NVS Strategy
2. Install ta-lib Add-in
 a. Open Excel and then go to File->Options
 b. Under Add-in, select 'Excel Add-in' in Manage and then click 'Go'
 c. Then click 'Browse', locate the included 'ta-lib.xll' file and then click 'Ok'.
 d. ta-lib Add-in is now installed
3. Ensure your system time settings have the Short Date format as DD-MMM-YY.
4. Open 'Strategy Evaluator.xlsm' and then ensure all the locations are correct. If you've extracted to C:\NVS Strategy, then it should already be correct.
If you've used a different location, change all the locations so that Excel can locate the files properly.
5. Enter your Capital and the number of simultaneous trades. You can use this Simultaneous Trades field to control your risk.
For example, if you wish to use only 1/20th of your capital for each trade, then simply enter 20 in the simultaneous trades field. A value of 1 here will give
full size quantities that will use up your full capital to trade.
Note: Quantities are calculated based on Zerodha's BO/CO leverages. Please ignore if you are using other broker.
6. Column A contains the sample space of stocks to scan from. You can add your own list (Example: Nifty 50 stocks) by entering all the scrip symbols starting from 
column A1. Please ensure that there are no empty cells in between the list.
Note: The default list contains all stocks for which Zerodha BO/CO orders can be placed using the minimum of 20.8x leverage that they provide.
7. Column B contains the dates for which the new data has to be imported from NSE and scanning has to be performed. You can add any number of dates, but ensure 
that they were trading days and they are arranged oldest to newest. To see which dates need to be added, just open any of the .xlsx file from the 'Stocks' 
folder and see till which date (in column B) the data has been populated. Then enter all trading days from the last date to today. Ensure that there are no
gaps or any trading days are missed. This will corrupt the data and you will not get an accurate list.
8. Once everything is set, Click 'GO' and wait for the scanning to complete. This should take anywhere between 5-15 minutes and to ensure uninterrupted 
scanning, please do not do anything else on the system till it finishes. If you see it stopping at any stock, with one of the files from Stocks folder open, 
it has been interrupted. Close everything except 'Strategy Evaluator.xlsm' and then Click 'GO' to start again.
9. Once it has completely finished, you will get a list of stocks with coloured entry, targets, etc.

