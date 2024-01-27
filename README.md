# Monetary-Policy-Analiysis

**Euro Area Conventional Monetary Policy Analysis on Inflation** (2016-2021) - University Group Project

*Is the transmission of ECB conventional monetary policy effective on banks’ volumes and banks’ rates since 2014? Is there a time lag?*

## 01. INTRODUCTION

**DATA SOURCE**

The *datasets* used for the project have been taken from the official website of **ECB Statistical Data Warehouse**. In particular:
* the **MRO dataset** with all dates to be able to perform a proper analysis regarding the *main refinancing operations* set by the Governing Council of the ECB and providing the bulk of *liquidity* to the banking system;
* the **MIR dataset** used for the analysis of monetary *developments* and the monetary *transmission* mechanism as well as for the monitoring of *financial* **stability**;
* the **BSI statistics** based on either the *aggregated* or the *consolidated* balance sheet of the monetary financial institutions (MFIs) sector.


**MIR dataset**

The majority of MIR dataset consists of continuous attributes (about 95.65%), representing the monthly interest rates collected from 2014-01 to 2023-02. The remaining features (about 4.35%) refer to:
*   **Country** in the Euro Area, where company is domiciled;
*   **Type of Loans**, describing the different financial instruments composition; 
*   **Maturity**, the date on which the term of the loan expires;
*   **BS Counterpart Sector**, revealing the sector in which the institutions are involved in;
*   **IR Business Coverage**, reflecting the extent to which services and other resources have been used during the financial year, based on loan volume.

Regarding the financial instruments composition of the MIR dataset, let's include four different types of Loans:
1.   **Loans**, holdings of financial assets created when creditors lend funds to debtors;
2.   **Lending for House Purchases**, loans granted for the purposes of investing in housing for own use or rental, or for the purchase of land;
3.   **Credit for Consumption Other Lending**,  loans for consumption or granted to households for business, debt consolidation, education purposes;
4.   **Extended Credit**, the amount of convenience credit left outstanding on the account after the relevant billing date.


**BSI dataset**

The majority of BSI dataset consists of continuous attributes (about 95.65%), representing the monthly stock data collected from 2014-01 to 2023-02. The remaining features (about 4.35%) refer to:
*   **Country** in the Euro Area, where company is domiciled;
*   **Type of Loans**, describing the different financial instruments composition; 
*   **Maturity**, the date on which the term of the loan expires;
*   **Data Type**, making a distintion between the Outstanding amounts at the end of the period (stocks) and the Financial transactions (flows);
*   **BS Counterpart Sector**, revealing the sector in which the institutions are involved in.

Regarding the financial instruments composition of the BSI dataset, let's include the same types of Loans collected in the previous one. 

## 02. MRO ANALYSIS

We utilized the main refinancing operations data from 2014 to 2023, considering the MRO Normal Value. Analysing the MRO for the **2014-2022** period, it is evident that the interest rate remained *consistently* at or near **0%**, aligning with the **low** *inflation* prevalent during this period. The ECB attributes this low inflation to various factors, including economic slack and the aftermath of the 2009-2012 twin recession. Additionally, digitalization, globalization, and demographic changes, such as the widespread adoption of e-commerce, intensified market competition and necessitated greater price transparency, reducing profit margins.

A combination of these interconnected factors explains the persistently **low** *inflation* from 2013 to 2019. While reduced demand and economic slack exerted downward pressure on inflation during 2014-2020, a *recovery* in demand in **2021**, following the initial pandemic wave, led to constrained labor supply, resulting in wage and *price* **increases**. In **2022**, the Russian invasion of Ukraine raised concerns about an imminent energy supply shock, contributing to increased *energy prices*. Despite this, swift government interventions and strategic responses by companies helped mitigate the potential crisis.

By **2023**, energy prices *decreased* compared to 2022, and transitory inflation shocks, particularly in food, everyday goods, and some services, emerged. Our analysis indicates that the ECB's conventional *monetary policy* effectively addressed the **decrease** in inflation. While this doesn't imply a halt in MRO increases, it signals the **effectiveness** of the policy in managing and reducing inflation.

## 03. MIR ANALYSIS

Examining the period from February 2014 to February 2023, we observe **consistent** behavior in the average interest rates (%) for *Loans* and *Lending for House Purchases*. A slight divergence begins around August 2022, where interest rates for Loans grow from about 2.8% to 3.8%, while rates for Lending for House Purchases increase to 3.3%. The average interest rate (%) for *Credit for Consumption* and *Other Lending* is **higher**, maintaining stability until April 2019, with a subsequent slight increase to 7.60%. The blue line, representing the average interest rate (%) of *Extended Credit*, remains the **highest**, exhibiting stability around 15%.

Analyzing the impact of *loan* **maturity**, we focus on the period's end for objectivity. We consider the average interest rates of Loans across Euro Area *countries*, specifically for Lending for House Purchases, Credit for Consumption, and Extended Credit. Additionally, we explore the **increase** in interest *rates* since the beginning of the MRO (Main Refinancing Operations) rise, noting impacts on households, non-profit institutions, and non-financial corporations.

## 04. BSI ANALYSIS

BSI (Banking Sector Indicator) and MIR (Monetary Interest Rates) Correlation Analysis: In **2022**, the MRO (Main Refinancing Operation) experienced a gradual *increase* after a prolonged period of MRO=0%. The first interest rate change occurred on 2022-07-27. To visualize the transmission of this monetary policy change, a correlation analysis was conducted using the **Outstanding** amount of loans from the balance sheet of MFIs and the changes in interest rates set by the MFIs (Monetary Financial Insitutions). The analysis aimed to determine if the **increase** in *MIR* led to a **decrease** in the *Outstanding* amount at the end of the period.

Utilizing the BSI dataset and MIR dataset with Type of Loan=Loan and Maturity=Total, the analysis covered the period from September 2022 to February 2023. The *Spearman's rank* correlation revealed a statistically significant **negative** correlation, indicating that an *increase* in interest rates for loans led to a *decrease* in the Outstanding amount. This suggests that the *loans* on the asset side of the MFIs **decreased** as a consequence of the monetary policy (MRO increase).

To ensure objectivity, the maturity of loans was considered up to the end of the period. The analysis extended to the average interest rate of loans across Euro Area *countries* where companies are domiciled and across *BS counterpart* sectors from 2014 to 2023. The same analysis was performed for Lending for House Purchases and Extended Credit.

## 05. REGRESSION ANALYSIS
To capture additional insights regarding the **effectiveness** of the *monetary policies* applied through the value of the MRO in the period 2014-2023 and 2022-2023, we turn to **regression** models. In particular: 

**Interest Rate Analysis:**
*  An increase in MFIs' interest rates was observed since July-August 2022.
*  Regression for the 2014-2023 period showed low R^2 when MRO was close to 0%.
*  A separate regression for the 2022-2023 period demonstrated a strong correlation between the increase in MRO and interest rates, indicating its explanatory power.
  
**Volume Analysis:**
*  Negative correlation between the outstanding amount of loans and interest rates was observed.
*  Regression assessing the direct impact of MRO increase on outstanding loans at the end of the period revealed a time lag.
*  Notably, the outstanding amount increased with MRO till November 2022, after which it decreased, aligning with correlation and regression results.

**Focused Regression:**
*  A specific regression for September 2022 to February 2023 reaffirms the negative slope, suggesting a decrease in outstanding loans for MFIs at the end of the period.
*  Adjusted R squared indicates a low explanatory power, emphasizing the complexity of drawing definitive conclusions.
*  In essence, the regressions highlight the nuanced impact of MRO increases on interest rates and loan volumes for MFIs, revealing time lags and varying trends during different periods.

## 06. CONCLUSION
Despite the **lag** in the *effectiveness* of monetary policy through MRO increases, it is noteworthy that inflation is anticipated to decrease in certain parts and sectors of the euro area for March 2023. This, however, does **not** imply an *immediate* reduction in the MRO by the ECB.

The fear of an energy supply shock due to the Russian invasion in Ukraine in 2022 led to increased energy prices. Governments responded with price caps, and companies developed data-driven software to manage shortages. In 2023, energy prices have *decreased* compared to 2022, but transitory inflation shocks *persist* in food, everyday goods, and some services.

The positive news of expected *inflation* **decrease** in March does not mark the end of the 'too high inflation period' but suggests the conventional *monetary policy* of the ECB may be taking **effect**.
