# Monetary-Policy-Analiysis

**Conventional Monetary Policy on Inflation Analysis** considering the Euro Area (2014-2023).

*Is the transmission of ECB conventional monetary policy effective on banks’ volumes and banks’ rates since 2014? Is there a time lag?-*

The *dataset* is downloaded from the official website of **ECB Statistical Data Warehouse**. 
Then, it could be usefull to create:
* the **MRO dataset** with all dates to be able to perform a proper analysis regarding the main refinancing operations set by the Governing Council of the ECB and providing the bulk of liquidity to the banking system;
* the **MIR dataset** used for the analysis of monetary *developments* and the monetary *transmission* mechanism as well as for the monitoring of *financial* **stability**;
* the **BSI statistics** based on either the *aggregated* or the *consolidated* balance sheet of the monetary financial institutions (MFIs) sector.


**MIR dataset**

The majority of MIR dataset consists of continuous attributes (about 95.65%), representing the monthly interest rates collected from 2014-01 to 2023-02. The remaining features (about 4.35%) refer to:
*   ***Country*** in the Euro Area, where company is domiciled;
*   ***Type of Loans***, describing the different financial instruments composition; 
*   ***Maturity***, the date on which the term of the loan expires;
*   ***BS Counterpart Sector***, revealing the sector in which the institutions are involved in;
*   ***IR Business Coverage***, reflecting the extent to which services and other resources have been used during the financial year, based on loan volume.

Regarding the financial instruments composition of the MIR dataset, let's include four different types of Loans:
1.   ***Loans***, holdings of financial assets created when creditors lend funds to debtors;
2.   ***Lending for House Purchases***, loans granted for the purposes of investing in housing for own use or rental, or for the purchase of land;
3.   ***Credit for Consumption Other Lending***,  loans for consumption or granted to households for business, debt consolidation, education purposes;
4.   ***Extended Credit***, the amount of convenience credit left outstanding on the account after the relevant billing date.


**BSI dataset**

The majority of BSI dataset consists of continuous attributes (about 95.65%), representing the monthly stock data collected from 2014-01 to 2023-02. The remaining features (about 4.35%) refer to:
*   ***Country*** in the Euro Area, where company is domiciled;
*   ***Type of Loans***, describing the different financial instruments composition; 
*   ***Maturity***, the date on which the term of the loan expires;
*   ***Data Type***, making a distintion between the Outstanding amounts at the end of the period (stocks) and the Financial transactions (flows);
*   ***BS Counterpart Sector***, revealing the sector in which the institutions are involved in.

Regarding the financial instruments composition of the BSI dataset, let's include the same types of Loans collected in the previous one. 

In conclusion, it could be usefull to recap the findings of the analysis by observing some **regression** models which could give some additional information regarding the *effectiveness* of the monetary policies applied through the value of the MRO in the period 2014-2023 and especially in the period 2022-2023.
