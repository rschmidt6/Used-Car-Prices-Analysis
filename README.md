# Used Car Depreciation Analysis

## Summary

This analysis tests conventional wisdom about car value retention using 50,000 real-world car sales records. Key findings debunk the "luxury holds value" myth and reveal smaller/efficiency focused vehicles (hybrids, small engines, mass market brands) retain value better on a percentage basis.

**Key Insights:**
- Mass market brands retain value better than luxury brands (67-68% depreciation vs 70-73%)
- Peak depreciation occurs at 10-15 years across all categories due to warranty expiration and major maintenance issues
- Efficiency retains better value: hybrids, small engines, and practical brands show superior percentage retention
- Optimal buying strategy: Purchase 5-9 year old vehicles, sell before 10-year value drop

## Dataset

**Source:** [Kaggle Car Sales Dataset](https://www.kaggle.com/datasets/minahilfatima12328/car-sales-info/data)

**Analysis:** [Google Sheets Workbook](https://docs.google.com/spreadsheets/d/1Ftvm0MkiBCBfI_4wmqv2-oJbIKng2kGXirLZrQGYkRU/edit?gid=1066987514#gid=1066987514)

**Scope:** 50,000 car sales records spanning multiple brands, fuel types, and engine sizes

## Data Overview

- **Price Range:** $78 - $168,081
- **Mileage Range:** 630 - 453,537 miles
- **Brands:** BMW, Ford, Porsche, Toyota, Volkswagen
- **Engine Sizes:** 1.0L - 5.0L
- **Fuel Types:** Petrol, Diesel, Hybrid
- **Time Period:** Cars manufactured 1980-2022

## Methodology

**Data Cleaning:**
- Removed outlier vehicles priced under $500 (likely salvage/some kind of data error)
- Filtered out vehicles with >300,000 miles (fleet vehicle outliers)
  - These two filters removed about 300 rows
- Added calculated fields: Car Age (2023 - Manufacturing Year)

**Analysis Approach:**
- Grouped cars into 5-year age brackets
- Calculated depreciation rates between consecutive age groups
- Formula: `(Previous Period Price - Current Period Price) / Previous Period Price × 100`

## Analysis Results

### Brand Value Retention

<img src="https://github.com/rschmidt6/Used-Car-Prices-Analysis/blob/main/charts/manu_prices.png" alt="manufacturer prices" width="80%"/>
<img src="https://github.com/rschmidt6/Used-Car-Prices-Analysis/blob/main/charts/manu_depr.png" alt="manufacturer depr" width="80%"/>

**Total Percentage Depreciation (0-35+ years):**
- BMW: 73% total depreciation
- Porsche: 70% total depreciation  
- Toyota: 68% total depreciation
- Ford: 67% total depreciation
- Volkswagen: 67% total depreciation

**Key Finding:** Luxury brands lose more value percentage-wise despite higher absolute dollar retention.

### Fuel Type Performance

<img src="https://github.com/rschmidt6/Used-Car-Prices-Analysis/blob/main/charts/fuel_prices.png" alt="fuel prices" width="80%"/>
<img src="https://github.com/rschmidt6/Used-Car-Prices-Analysis/blob/main/charts/fuel_depr.png" alt="fuel depr" width="80%"/>

**Insights:**
- **Hybrids** maintain value best initially (35.5% first-period depreciation) but face steeper declines after 15 years
- **Petrol** shows highest initial depreciation (40%) but stabilizes in middle years
- **Diesel** provides most consistent, predictable depreciation pattern

### Engine Size Impact

<img src="https://github.com/rschmidt6/Used-Car-Prices-Analysis/blob/main/charts/engine_prices.png" alt="engine prices" width="80%"/>
<img src="https://github.com/rschmidt6/Used-Car-Prices-Analysis/blob/main/charts/engine_depr.png" alt="engine depr" width="80%"/>

**Findings:**
- Small engines (1.0-1.4L) consistently outperform larger engines in value retention
- Large engines (4.4L+) face accelerating depreciation after 15 years
- Sweet spot: 2.0-2.4L engines balance performance with depreciation resistance

## Business Recommendations

### For Consumers
- **Buy In Best Value Window:** Purchase 5-9 year old vehicles for best price/depreciation balance
- **Avoid buying 10-15 Year Range:** High depreciation period, likely due to warranty expiration and major maintenance needs
- **Efficiency Strategy:** Choose hybrids under 10 years, likely even newer, and small engines for long-term ownership

### For Dealers
- **Inventory Management:** Avoid buying 10-15 year old luxury vehicles due to peak depreciation
- **Pricing Strategy:** Luxury brands may have high margins but face steeper percentage losses (though absolute value depreciation also highest)
- **Fleet Useage:** Diesel vehicles offer predictable depreciation for fleet use

### For Fleet Use
- **Replacement Timing:** Sell vehicles before 10 year mark to avoid depreciation hike
- **Vehicle Selection:** Smaller engine, mass-market brands optimize value
- **Technology Considerations:** Hybrid benefits diminish after 15 years due to maintenance complexity

## Technical Implementation

**Tools Used:**
- Google Sheets for data analysis and visualization
- Pivot tables for data aggregation
- Statistical analysis of depreciation patterns

**Key Formulas:**
```
Car Age = 2023 - Year of Manufacture
Depreciation Rate = (Previous Price - Current Price) / Previous Price × 100
```

## Limitations

- Missing original MSRP data limits comprehensive depreciation analysis
- Dataset may not represent all geographic markets
- Sample sizes vary across fuel types and engine categories
- Analysis assumes 2023 baseline for age calculations

## About This Analysis

This project demonstrates end-to-end data analysis skills including data cleaning, statistical analysis, and business insight generation. The analysis challenges common assumptions about vehicle value retention and provides actionable recommendations for multiple stakeholder groups.

**Skills Demonstrated:**
- Data cleaning and quality assessment
- Pivot table analysis and statistical calculations
- Data visualization and pattern recognition
- Business insight generation and recommendation development
- Technical documentation and presentation
