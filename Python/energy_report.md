# The Road to Net Zero:
## *Analysing Australia’s Energy Transition & Emissions Pathway (1990-2023)*

### Background and Overview

This report explores Australia's energy and emissions trajectory from 1990 to 2023, with the goal of assessing progress towards the 2050 net zero target. Using publicly available datasets from the Department of Climate Change, Energy, the Environment and Water (DCCEEW), trends in greenhouse gas (GHG) emissions, economic growth, electricity generation mix transformation, and the influence of major policies are analysed. Data visualisations, key policy annotations, and basic forecasting models are used to explore and evaluate whether Australia is on track to meet its targets, offering insights for energy analytics and climate-aligned decision-making.

### Table of Contents
- [Executive Summary](#executive-summary)
- [Introduction](#introduction)
- [Datasets and Methodology](#datasets-and-methodology)
    - [Datasets](#datasets)
    - [Focus Period](#focus-period)
    - [Methods](#methods)
    - [Tools and Libraries](#tools-and-libraries)
- [Analysis and Key Findings](#analysis-and-key-findings)
    - [Policies Timeline](#policies-timeline)
    - [Emissions Trajectory](#emissions-trajectory)
    - [Energy Transition Progress](#energy-transition-progress)
    - [Economic Growth vs Emissions](#economic-growth-vs-emissions)
    - [Net Zero Alignment](#net-zero-alignment)
- [Conclusion](#conclusion)
- [Appendix](#appendix)
- [References](#references)

### Executive Summary
<p align = "center">
<img src = imgs/net_zero_alignment.png alt = "Net Zero Alignment">
</p>
<p align = "center"><small><em>Figure 1: Australia's emissions trajectory, targets, and safeguard mechanism 1990-2060</em></small></p>

Australia faces the challenge of sustaining economic growth while meeting its climate commitments.  This report examines historical emissions trends, economic performance, energy transition progress, and forecasts against Australia’s legislated 2050 net zero target.

**Key Findings:**
- **Budget Pressure:** Australia has consumed **54.3%** (**5.48 Gt CO<SUB>2</SUB>-e**) of its recommended fair share global emissions budget for the **2013-2050** period within the first **11 years**, leaving only **4.62 Gt CO<SUB>2</SUB>-e** for the remaining **2024 to 2050** period.
- **Budget Overshoot:** Both the legislated net zero pathways, and Business as usual (BAU) linear forecast indicate that the remaining budget would be exceeded by **2037**.
    - Overshoot by 2050:
        - Net Zero Pathway: **+1.44 Gt CO<SUB>2</SUB>-e** (**14.2%**)
        - BAU Linear Forecast: **+2.42 Gt CO<SUB>2</SUB>-e** (**24%**)
- **Decoupling Evidence:** Australia’s GDP has **more than doubled since 1990**, whilst emissions intensity fell by **72.4%**, indicating signs of **partial decoupling**.
- **Renewables Expansion:** Renewable electricity share grew from **10.1%** in 1990 to **33.9%** in 2023, through support of policies like the RET and SRES. 
- **Net Zero Alignment:** If no further measures are adopted, Australia is projected to **overshoot its 2050 goal by ~98.1 Mt CO<SUB>2</SUB>-e**, delaying net zero until **2058.**


### Introduction

To support Australia in meeting its national emissions targets, and to ensure the country’s ongoing competitiveness in an increasing decarbonised global economy, the Safeguard Mechanism was established. Introduced in 2016 under the National Greenhouse and Energy Reporting act 2007 (NGER Act), the Safeguard Mechanism forms a key component of Australia’s climate policy framework. This policy requires Australia’s highest greenhouse gas emitting facilities (*facilities emitting >100,000 tonnes of carbon dioxide equivalent in a year*) to reduce their emissions in alignment of national targets of **43% below 2005 levels by 2030**, and **net zero by 2050**.


### Datasets and Methodology

#### Datasets

|Dataset|Source|Period|Key Variables|Use case|
|:--|:--|:--|:--|:--|
|Emissions|DCCEEW - *Australia's Emissions Projections 2024*|1990-2023|Total & sectoral GHG (CO<SUB>2</SUB>-e)|Historical emissions and forecasting|
|Energy Mix|DCCEEW - *Australian Energy Statistics 2024* (Table O FY, machine-readable)|1990-2023|Generation by source|Renewable penetration analysis|
|Economics|ABS (primary) - retrieved via *DCCEEW Australian Energy Update 2024*, Table B|1990-2023|Chain Volume GDP & Population|Decoupling analysis|
|Policies|Analyst compiled (Excel)|1990-2023|Major climate & energy policies|Used for annotations|
|NDC Carbon Budget|Australian Government - *Australia's Nationally Determined Contribution 2022*|2021-2030|National carbon budget|Budget analysis|
|CCA Carbon Budget|Climate Change Authority - *Targets and Progress Review 2014* (Ch.8)|2013-2050|Global fair share carbon budget|Budget analysis|

#### Focus Period
- **Observed:** 1990 to 2023
- **Forecast:** 2024 to 2060
<br>

#### Methods
- **Exploratory data analysis**
- **Data visualisation**
- **Time-series trends analysis:** emissions, GDP, energy mix
- **Forecasting:** linear regression for emissions; interpolated pathway for legislated net zero
- **Budget analysis:** cumulative emissions vs. 10.1 Gt CO<SUB>2</SUB>-e allowance, 2013 to 2050
- **Policy overlay and interpretation**
<br>

#### Tools and Libraries
- **Python**: jupyter notebook, pandas, matplotlib, seaborn, sklearn for linear regression forecasts 
- **Excel**: compilation of policy timelines
<br>

### Analysis and Key Findings

#### Policies Timeline

<p align = "center">
<img src = imgs/policies_timeline.png alt = "Policies Timeline">
</p>
<p align = "center"><small><em>Figure 2: Key climate policy milestones 1990-2023</em></small></p>
<br>

#### Emissions Trajectory
How have Australia’s total and sectoral greenhouse gas emissions changed since 1990?


##### Historical Greenhouse Gas Emissions



<p align = "center">
<img src = imgs/historical_emissions.png alt = "alt text">
</p>
<p align = "center"><small><em>Figure 3: Historical greenhouse gas emissions and key climate policy milestones 1990-2023</em></small></p>



Figure 3 illustrates Australia’s total greenhouse gas emissions over a 33-year period with key national and international climate and energy policies annotated to provide contextual insight.

- Emissions **peaked at 649.79 Mt CO<SUB>2</SUB>-e in 2006** reflecting a culmination of a rising trend from 1995 onwards due to an increase in industrial activity and limited emissions constraints.
- Following the 2006 peak, there has been an ongoing downward trend in emissions with **emission falling to 443.57 Mt CO<SUB>2</SUB>-e in 2023** which represents a **31.7% reduction** from the 2006 emissions peak. This trend suggests that Australia has been making progress towards achieving its reduction targets. 
- Key factors that have influenced the decrease in emissions between 2006 to 2023:
    - **Policies**
        - The gradual decline of emissions from **619.33 Mt CO<SUB>2</SUB>-e to 559.5 Mt CO<SUB>2</SUB>-e** (**9.7%**) between 2008 to 2012 coincides with the **ratification of the Kyoto protocol in 2007** where Australia committed to emissions reduction targets of **108% of 1990 emissions levels** within this time period.
        - This decline further coincides with the introduction of **Renewable Energy Target (RET) in 2009** which has significantly transformed the renewable energy landscape in Australia. The policy aims to reduce greenhouse gas emissions in the electricity sector and increase renewable electricity generation.
        - The Safeguard mechanism, introduced in 2016 and reformed in 2023, set out major reduction targets of **43% below 2005 levels by 2030, and net zero by 2050**. With the exception of the increase in emissions in 2017, the stabilisation of industrial emissions under this act contributed positively to the reduction of greenhouse gas emissions between 2018 and 2023.
<br>
    - **Land use, Land-Use Change and Forestry (LULUCF)**
    <br> 
        <p align = "center">
        <img src = imgs/lulucf_analysis.png alt = "LULUCF analysis">
        </p>
        <p align = "center"><small><em>Figure 4: LULUCF's role in net GHG emissions</em></small></p> <br>
 
        - **Between 2015 to 2023, LULUCF has acted as a major carbon sink** for Australia’s emissions, reducing emissions by **~547.92 Mt CO<SUB>2</SUB>-e** over this time period. Visually represented by the red shading in Figure 4 above, this highlights LULUCF’s role in offsetting emissions from other sectors. 
        - Whilst Net GHG Emissions trend suggest gradual progress, further analysis indicates that a substantial share of emissions reduction is attributed to LULUCF offsets, rather than reductions from other sectors.
        - When LULUCF is excluded from emissions accounting, the trajectory of emissions tells a different story from that of the Net GHG Emissions; that emissions from other sectors **increased slightly between 2015 to 2018 from 548.21 Mt CO<SUB>2</SUB>-e to 565.8 Mt CO<SUB>2</SUB>-e** followed by a minimal **reduction to 531.94 Mt CO<SUB>2</SUB>-e in 2023**.
        - This deviation highlights the importance of LULUCF in meeting Australia’s reductions targets whilst revealing the structural risk that **Australia’s progress relies heavily on LULUCF offsets** rather than systemic decarbonisation across key emitting sectors.
<br>

##### Sectoral Emissions 

<p align = "center">
<img src = imgs/sectoral_emissions.png alt = "Sectoral emissions">
</p>
<p align = "center"><small><em>Figure 5: Sectoral and cumulative GHG emissions 1990-2023</em></small></p>

Figures 5(a) and 5(b) above illustrate the evolution of Australia’s sectoral emissions between 1990 to 2023 excluding LULUCF, and the sum of cumulative emissions contributions between this time period respectively.

- Across the 33-year period, the **Electricity sector has been the largest contributor** to Australia’s greenhouse gas emissions, emitting **~5945 Mt CO<SUB>2</SUB>-e** cumulatively. 
    - Emissions from this sector increased from **129.53 Mt CO<SUB>2</SUB>-e in 1990** to a peak of **211.63 Mt CO<SUB>2</SUB>-e in 2009**, before falling to **153.34 Mt CO<SUB>2</SUB>-e in 2023**; a **reduction of 27.5% from peak levels.** 
    - This reduction in emissions aligns with the expansion of renewable electricity generation following the introduction of the Renewable Energy Target (RET) in 2009.

<p align = "center">
<img src = imgs/sectoral_index_sectoral_emissions_2023.png alt = "Sectoral emissions indexed">
</p>
<p align = "center"><small><em>Figure 6: Indexed sectoral emissions and sectoral emissions share breakdown 2023</em></small></p> 

Whilst net carbon emissions seem to be on a downward trajectory, Figures 6(a) and 6(b) above provide a more nuanced view by showing how each sector’s emissions have evolved relative to 1990 levels, and their respective contributions to 2023 emissions.

- According to Figure 5(b) and Figure 6(a), Agriculture, Stationary Energy and Transport have each individually contributed over **2700 Mt CO<SUB>2</SUB>-e**, with varied emission trajectories since 1990. 
    - Transport, the third largest emissions sector in 2023, accounting for **18.2% of Australia’s emissions**, saw an increase of **57.5% during the 1990-2023** analysis period. This increase **reflects continued reliance on fossil fuel-based mobility and slow transition to electrification.** 
    - Stationary energy emissions rose steadily, reaching **154.2% of 1990 levels by 2023**, placing the Stationary Energy sector as the 2nd largest emitting sector in 2023, responsible for **19.2% of total emissions**. This growth highlights Australia’s over reliance on fossil fuels and high per capita energy consumption.
    - In contrast, Agriculture emissions remained relatively stable with emissions ranging between **77.37 Mt CO<SUB>2</SUB>-e** and **94.96 Mt CO<SUB>2</SUB>-e**.
- Despite having differing emissions trajectories, Fugitives, Industrial Processes, LULUCF and Waste have each contributed small shares of cumulative emissions during the analysis period. 
    - Fugitives and Industrial processes show increased emission trends with increases of **18.5% and 30.4% between 1990 to 2023** respectively.
    - Emissions from the Waste sector have been gently declining with 2023 emission levels representing **59.1% of 1990 emission levels**.
    - As discussed previously, LULUCF emissions have significantly decreased to the point where **LULUCF has transitioned from a source to a net sink**.

These contrasting sectoral emission trends indicate that while national net emissions seem to be declining, this progress has masked **underlying stagnation or growth in several key sectors**. They highlight uneven progress in decarbonisation across the economy and **underscore the need for targeted sector-specific interventions** to drive genuine emissions reduction.
<br>

#### Energy Transition Progress
How has Australia’s electricity generation mix evolved, and what is the share of renewables today?
##### Renewables vs Fossils (1990 vs 2023)

<p align = "center">
<img src = imgs/renewable_fossil_generation_share.png alt = "Renewable fossil overview">
</p>
<p align = "center"><small><em>Figure 7: Renewable and fossil electricity generation trends 1990-2023</em></small></p>

Figures 7(a) and 7(b) provide a high-level view of Australia’s electricity generation landscape from 1990 to 2023, highlighting the shift from a fossil fuel dominant system towards increased renewable integration.

- Between 1990 and 2023, Australia’s total electricity generation increased by **77.4%**, rising from **154,708 GWh** to **274,475 GWh**. Over this period:
    - There was a **23.8%** increase in renewable generation share from **10.1% of total generation (15,630 GWh)** to **33.9% in 2023 (93,112 GWh)**, and an **absolute growth of 77,482 GWh**. 
    - Fossil fuel generation saw absolute growth of **42,285 GWh from 139,078 GWh in 1990 to 181,363 GWh in 2023**, but its share declined from **89.9% to 66.1%**. 

- These findings reflect the accelerating contribution of renewables, particularly wind and solar through the introduction of policies such as the Renewable Energy Target and the establishment of governing bodies such as the Australian Renewable Energy Agency (ARENA) and the Clean Energy Finance Corporation (CEFC).

##### Evolution of Australia’s Electricity Generation

<p align = "center">
<img src = imgs/gen_mix_evolution.png alt = "Sectoral emissions indexed">
</p>
<p align = "center"><small><em>Figure 8: Evolution of Australia's electricity generation mix and source shares 1990-2023</em></small></p>

Figures 8(a) and 8(b) show the evolution of Australia’s generation mix and sources share between the 1990-2023 analysis time period respectively. It highlights Australia’s increasing energy demand, the decline in Coal’s share of the generation mix, and the uptake of renewable sources like Solar and Wind.

<p align = "center">
<img src = imgs/generation_mix_2023.png alt = "Sectoral emissions indexed">
</p>
<p align = "center"><small><em>Figure 9: Australia's electricity generation mix and source shares 2023</em></small></p>

Figures 9(a) and 9(b) show the state of Australia's Energy Generation mix in 2023. It highlights Coal as the dominant generation source and the position of Solar as the 3rd largest source of Australian energy and the largest renewable energy source.

##### Fossil Fuels’ role in the Generation Mix
- Historically, Coal has dominated Australia’s energy generation landscape, responsible for ~**70.4% of electricity generated between the 1990-2023** period *(Table 1)*. Figures 8(a) and 8(b) show that coal generation **peaked in 2007 at 186,744 GWh**, then declined to **127,633 GWh in 2023**; a **reduction of 31.7%**. Additionally, its share in the generation mix, has been steadily declining during the 33-year analysis period from **78.3% in 1990** to **46.5% in 2023**; a **reduction of 40.6%**. This decline in share and generation correlates with the introduction of policies such as RET, which incentivises the generation and use of renewable energy alternatives. 
- Natural Gas’s electricity generation saw a major increase (**284.5%**) between 1990 to its peak in 2020 from **14,359 GWh to 55,216 GWh** respectively. Following its 2020 peak, generation **fell by 11.5% to 48,865 GWh in 2023**. During the 1990 to 2023 period, natural gas’ generation share **increased from 9.3% to 17.8%**, making it Australia’s 2nd largest source of electricity.
- Oil products, only accounting for **1.5% of Australia’s total generation** within the 33-year period, has historically played a minor role in Australia’s electricity mix, and continues to decline in relevance from **2.3% in 1990** to **1.8% in 2023**.
<p align = "center">
<img src = imgs/electricity_generation_summary_table.png alt = "Sectoral emissions indexed">
</p>
<p align = "center"><small><em>Table 1: Australia's electricity generation mix statistics</em></small></p>

Table 1 summarises Australia’s electricity generation mix by source, reporting total electricity generation output and each sources share of the total electricity generated between 1990 to 2023, along with their ranks according to individual contributions.
##### The role of Renewables in the Generation Mix and the expansion of Wind and Solar
###### Hydropower
- Historically, hydropower has served as a consistent renewable electricity generation source, with generation ranging between **14,880 GWh to 16,933 GWh** throughout the 1990 to 2006 period. Despite its position as the third largest electricity generation source during the 33-year analysis period, post 2006 saw a decline in generation output, reaching a low of **11,869 GWh in 2009**, which coincides with a prolonged period of drought that impacted water availability.

- Since then, generation has gradually recovered, reaching **16,666 GWh in 2023**, despite fluctuations in trends which can be tied to rainfall variability. Notably, **2013 and 2014 were peak years**, where generation surpassed **18,200 GWh**, reflecting temporary recovery during wetter periods.

- Hydropower’s share of electricity generation, however, has followed a **decreasing trend from 9.6% in 1990 to 6.1% in 2023**, with its lowest share of **4.5% being recorded in 2009**. This **3.5% decrease in share** coupled with the decline in its absolute generation, reflects the **relative stagnation of hydropower** amidst the rapid growth of newer technologies such as wind and solar.

- The decline in hydropower’s share reflects both the physical limitations imposed by rainfall fluctuations, and the increased cost-competitiveness and scalability of newer technologies, particularly, solar. Whilst the future of hydropower seems constrained, it will always remain a valuable renewable energy source due to its flexibility and storage capacity.
<br>

###### Wind Energy Growth
- Wind electricity generation has experienced exponential growth in both its output and generation share during the 33-year analysis period. **In 2023, wind energy generated 31,385 GWh**, which accounted for **11.4% of the generation mix**, cementing it as the 2nd largest renewable generation source for that year.<br>
- Despite its position behind solar in 2023, wind power has cumulatively generated **~225 TWh** of electricity between 1990 to 2023, **surpassing solar in cumulative output, and placing it as the second largest historical renewable energy source, behind hydropower**.<br>
- Wind power’s expansion has been facilitated by:
    - Geographical advantages such as strong wind corridors along Australia’s southern coastlines, and elevated inland regions, which provide ideal conditions for commercial scale wind farms.
    - State based feed in tariffs (FiTs) and long-term Power Purchase Agreements (PPAs) that ensure market stability and investor confidence.

<p align = "center">
<img src = imgs/wind_solar_1990_2023.png alt = "Growth of wind and solar">
</p>
<p align = "center"><small><em>Figure 10: Growth of wind and solar electricity generation in Australia 1990-2023</em></small></p>

<p align = "center">
<img src = imgs/wind_solar_2000_2023.png alt = "Wind and solar yoy growth">
</p>
<p align = "center"><small><em>Figure 11: Annual growth of wind and solar electricity generation 2000-2023</em></small></p>

Figures 10 and 11 emphasise the growth of wind and solar in the 2000’s and the year-on-year growth in these sources within this period. These figures highlight the impact of the RET and solar credits scheme.
<br>

###### Solar Power Expansion
- Solar power has experienced **significantly steeper exponential growth in both its absolute generation and share**, from **near zero in 1990** to a generation output and share of **41,969 GWh and 15.3% in 2023** respectively. This rapid expansion placed solar power as **Australia’s third largest electricity source, and the leading renewable generator**. Its numerous benefits include its abundance, cost-effectiveness, and environmentally friendly nature.
<br>
<p align = "center">
<img src = imgs/large_vs_small_scale_solar.png alt = "Sectoral emissions indexed">
</p>
<p align = "center"><small><em>Figure 12: Large-scale versus small-scale solar electricity generation (2005-2023)</em></small></p>

- The exponential growth in solar electricity generation post 2010 has been facilitated by the introduction of the Large-scale Renewable Energy Target (LRET) and Small-scale Renewable Energy Scheme (SRES) under the Renewable Energy Target (RET).

    -  **Small-scale Renewable Energy Scheme (SRES)**
        -   Small-scale solar has functioned as the dominant source of solar electricity during the analysis period, accounting for **~72.1% of the total solar electricity generated**, with a generation output of **25,909 GWh in 2023**. 
        -   These findings are the result of the rapid uptake in rooftop solar following the introduction of the Solar Credits Scheme under the SRES. This scheme, incentivised renewable energy adoption through the use of Small-Scale Technology Certificates (STCs) which made the uptake of renewable energy more affordable for households and businesses.

    -  **Large-scale Renewable Energy Target (LRET)**
        - Large-scale solar has only accounted for **27.9% of the total solar electricity generated** during the 1990-2023 analysis period, producing **16,060 GWh in 2023**.
        - This scheme incentivizes renewable energy investment and development through the use of large-scale generation certificates (LGCs).

###### Bioenergy
- Bioenergy, a broad term used to encompass biogas and biomass such as bagasse and wood, despite achieving growth of **312.4% from 1990 generation levels**, continues to function as a niche contributor relative to wind and solar, accounting for only **1.1% of Australia’s generation mix in 2023**.

Australia’s electricity sector has undergone significant transformation over the past three decades. The implementation of major policies such as the RET have given rise to increased renewable electricity penetration, namely, wind and solar. While fossil fuels still dominate, their share of the generation mix has **decreased from 89.9% to 66.1%**. Renewables now account for **33.9% of total electricity generation**, and continued policy and infrastructure investments will be essential to maintain momentum toward net zero.


### Economic Growth vs Emissions

Is there evidence of decoupling between economic growth and emissions?

<p align = "center">
<img src = imgs/economic_emissions.png alt = "economic indicators">
</p>
<p align = "center"><small><em>Figure 13: Relationship between Australia's economic growth and greenhouse gas emissions 1990-2023</em></small></p>


Figure 13 explores the relationship between Australia’s economic growth and greenhouse gas emissions between 1990 to 2023, with the aim of assessing whether decoupling has occurred.

#### Economic Growth
-  Australia has experienced steady economic growth (**159.6%**) between the 1990 to 2023 period with its GDP increasing from **\$926 billion in 1990** to **\$2,403 billion or \$2.4 trillion in 2023**.
-  Despite linear growth in its population from **17 million to 26.7 million** *(Figure A3)*, its GDP per capita **increased by 66.2%** from **\$54,260 to \$90,162**.

#### Emissions Trajectory
-  Over the 33-year period, total greenhouse gas emissions **declined by 28.4%**, from **619.18 Mt CO<SUB>2</SUB>-e to 443.57 Mt CO<SUB>2</SUB>-e**.
-  Emissions per capita **fell by 54.1%** from **36.3 tonnes per person to 16.6 tonnes per person**.

These trends suggest that reductions in emissions have been sustained despite growth in both population and the economy.

#### Economic and Emissions Indicator Summary

<p align = "center">
<img src = imgs/economics_summary.png alt = "Economic indicators summary">
</p>
<p align = "center"><small><em>Figure 14: Percentage change in economic and emissions indicators 1990-2023</em></small></p>

Figure 14 summarises the percentage change in the four-core economic and emissions growth indicators: GDP, Emissions, GDP per capita and Emissions per capita. It visually highlights a **decoupling trend** between Australia’s economic growth and greenhouse gas emissions.

#### Decoupling Indicators and Emissions Intensity

<p align = "center">
<img src = imgs/index_emissions_intensity.png alt = "Decoupling indicators">
</p>
<p align = "center"><small><em>Figure 15: Indexed GDP vs emissions and emissions intensity 1990-2023</em></small></p>


Figure 15(a) and 15(b) highlight decoupling trends between Australia’s economic growth and emissions and decreasing emissions intensity respectively.
-  Between 1990 to 2023, there has been a clear **divergence between Australia’s GDP and emissions**. While GDP increased to **259.6% of its 1990 value**, emissions declined to **71.6%**. This decline in emissions despite continued economic growth highlights the **presence of absolute decoupling**.
-  Australia’s emissions intensity **fell by 72.4%** from **0.67 kgCO₂-e per dollar AUD in 1990** to **0.18 kgCO₂-e per dollar AUD in 2023**. This reduction implies increased resource use efficiency, and the adoption of cleaner, more sustainable energy sources and industrial practices.



### Net Zero Alignment

Based on current trends, is Australia on track to meet its 2050 net zero target?

- Under the Climate Change act of 2022, Australia has committed to reduction targets of **43% below 2005 levels by 2030 and net zero by 2050**. To assess progress towards these targets, emissions budgets, projected pathways, and alignment with global carbon budgets are examined.

<p align = "center">
<img src = imgs/net_zero_alignment.png alt = "Net Zero Alignment">
</p>
<p align = "center"><small><em>Figure 1: Australia's emssions trajectory, targets, and safeguard mechanism 1990-2060</em></small></p>

As depicted previously, Figure 1 demonstrates how Australia is tracking towards its emissions targets, in addition to forecasting based on current trajectories. It contextualises whether current reductions sufficiently align with legislated emissions targets.

#### The 2021-2030 Emissions Budget
Australia’s 43% below 2005 levels by 2030 legislated commitment corresponds to a cumulative emissions budget of **4,381 Mt CO<SUB>2</SUB>-e for the 2021 to 2030 period**.
-  Between 2021 to 2023, Australia emitted approximately **1,326.49 Mt CO<SUB>2</SUB>-e**, consuming **30.3% of its emissions budget**. This leaves Australia with a budget of approximately **3,054.51 Mt CO<SUB>2</SUB>-e (69.7%)** for the 2024-2030 period.
-  Based on current emissions trajectory, Australia is projected to **achieve its 2030 reduction target** of 43% below 2005 levels by 2030. Projected cumulative emissions to 2030 are expected to remain within the 2021 to 2030 budget, with approximately **353.76 Mt or 8.1% of the budget remaining**.

#### Net Zero Alignment
-  Current projections indicate that if no additional measures are implemented, **Australia would not achieve its target of net zero by 2050**. 
-  They indicate that Australia would **overshoot its 2050 goal by approximately 98.1 Mt CO<SUB>2</SUB>-e, achieving net zero by the year 2058**, nearly a decade later than planned.
-  This highlights a gap between present policy measures and the level of decarbonisation required to achieve alignment with Australia’s long term climate commitments.

#### Cumulative Budget and Alignment with Global Climate Commitments

<p align = "center">
<img src = imgs/cumulative_budget.png alt = "Budget analysis">
</p>
<p align = "center"><small><em>Figure 16: Australia's cumulative emissions trajectory and remaining carbon budget 2024-2050</em></small></p>

Figure 16 plots Australia’s cumulative emissions against its long-term global emissions commitment. It explores the legislated net zero path alongside forecasted emission trends, showing that Australia’s commitment to net zero by 2050 would **not cover its 10.1 Gt emissions allowance**, and the **remaining 2024 to 2050 emissions budget would be exceeded by 2037**.

- **Paris Agreement Commitments (2016)**
    -  Under the Paris Agreement, all participating countries agreed to ensuring that average global temperature increases are kept well below **2°C above pre-industrial levels** whilst pursuing efforts to **limit temperature increases to 1.5°C**. 
    <br>
- **Australia’s Recommended Carbon Budget (2013-2050)**
    - According to the Climate Change Authority, in order to cover its fair share of the global emissions budget, Australia has a recommended budget of approximately **10.1 Gt CO<SUB>2</SUB>-e** to cover the 2013 to 2050 period. This recommendation has been calculated using a modified contraction and convergence approach. 
    <br>
- **Budget Consumption to Date (2013-2023)**
    -  Australia has already consumed **54.3% (5,484.69 Mt CO<SUB>2</SUB>-e**) of its entire recommended 2013-2050 budget.
    -  This leaves only **4,615.31 Mt CO<SUB>2</SUB>-e or 45.7%** for the 2024-2050 period. 
    <br>
- **Forecasting Overshoot (2037-2050)**
    -  Both the legislated net zero pathway and the linear forecast pathway indicate that **by 2037, Australia would have exceeded its recommended carbon budget**.
        - The Net Zero pathway overshoots the budget by **1,435.67 Mt CO<SUB>2</SUB>-e or 14.2%** by 2050.
        - The BAU linear forecast path overshoots the budget by **2,424.09 Mt CO<SUB>2</SUB>-e or 24%** by 2050.


### Conclusion
Australia has successfully initiated decoupling of emissions from economic growth and significantly increased renewable energy adoption. Despite this, current trends indicate that without enhanced policy measures and targeted interventions, **the country is unlikely to meet its legislated net zero target and is likely to exceed its fair-share carbon budget**. Without accelerated action:
- **The carbon budget will be exhausted by 2037**, leaving no remaining allowance for 2040's emissions.
- The legislated net zero policy pathway **overshoots the budget by 14.2%** by 2050.
- Delayed reductions mean **net zero is not achieved until 2058**, eight years beyond target.

**Recommendations:**<br>
1. **Accelerate renewable deployment** specifically in the Electricity and Stationary Energy sectors.
2. **Accelerate electrification** of the transport industry.
3. **Strengthen safeguards** – enforce steeper declines in facility-level baselines.

**Next Steps:**
- Update analysis with introduction of new policies and most recent data.
- Build interactive dashboards using Tableau and Power BI.
- Apply more advanced forecasting methods (ARIMA/Prophet).
- Test scenario analysis with different policy assumptions.

### Appendix

#### Supplementary Figures

The following figures provide extended visualisations supporting the analyses in this report. They offer additional perspectives on sectoral emissions, energy generation share and economic indicators.

<p align = "center">
<img src = imgs\appendix_sectoral_emissions_inlulucf.png alt = "sectoral emissions including lulucf">
</p>
<p align = "center"><small><em>Figure A1: Sectoral emissions including LULUCF 1990-2023</em></small></p>

Figure A1 above depicts total sectoral emission trends including LULUCF, highlighting the offsetting role of LULUCF in recent decades.

<p align = "center">
<img src = imgs\appendix_sectoral_share_exlulucf.png alt = "sectoral share of GHG emissions">
</p>
<p align = "center"><small><em>Figure A2: Sectoral share of GHG emissions 1990-2023</em></small></p>

Figure A2 illustrates the proportional contribution of each sector to total greenhouse gas emissions, highlighting electricity's continued dominance.

<p align = "center">
<img src = imgs\appendix_population_growth.png alt = "emissions versus GDP">
</p>
<p align = "center"><small><em>Figure A3: Total emissions vs GDP</em></small></p>

Figure A3 highlights Australia's linear population growth between 1990 to 2023.

<p align = "center">
<img src = imgs\appendix_emissions_vs_gdp.png alt = "emissions versus GDP">
</p>
<p align = "center"><small><em>Figure A4: Total emissions vs GDP</em></small></p>

Figure A4 further highlights the presence of decoupling between GDP and greenhouse gas emissions

### References
- ABC News. (2007, December 3). *Rudd signs Kyoto ratification document*. https://www.abc.net.au/news/2007-12-03/rudd-signs-kyoto-ratification-document/976234
- ABC News. (2014, July 10). *Carbon tax: A timeline of its tortuous history in Australia*. https://www.abc.net.au/news/2014-07-10/carbon-tax-timeline/5569118
- Clean Energy Finance Corporation. (Miller, M., 2018). *Climate finance and financial markets in Australia: The CEFC and ARENA*. 
https://www.cefc.com.au/media/402005/mmiller_alj_v92_pt10.pdf
- Clean Energy Regulator. (2025, August 1). *Safeguard Mechanism*. https://cer.gov.au/schemes/safeguard-mechanism
- Clean Energy Regulator. (2025, June 30). *Small-scale Renewable Energy Scheme*. https://cer.gov.au/schemes/renewable-energy-target/small-scale-renewable-energy-scheme
- Climate Change Authority. (2014). *Targets and Progress Review: Final Report* - Chapter 8 (Australia’s emissions budget to 2050). https://www.climatechangeauthority.gov.au/sites/default/files/Targets%20and%20Progress%20Review%20Final%20Report_Chapter%208.pdf
- Climate Change Authority. (2017, December). *Review of the Emissions Reduction Fund*. https://www.climatechangeauthority.gov.au/sites/default/files/ERF%20Review%20Report.pdf
- Department of Climate Change, Energy, the Environment and Water (DCCEEW). (2024). *Australia’s Emissions Projections 2024* (chart data). https://www.dcceew.gov.au/climate-change/publications/australias-emissions-projections-2024
- Department of Climate Change, Energy, the Environment and Water (DCCEEW). (2024). *Australian Energy Update 2024* (Australian Energy Statistics; Table O FY; Table B). https://www.energy.gov.au/publications/australian-energy-update-2024
- Department of Climate Change, Energy, the Environment and Water. (2025, October 7). *Rewiring the Nation*. 
https://www.dcceew.gov.au/energy/renewable/rewiring-the-nation
- Department of Climate Change, Energy, the Environment and Water. (2025, June 18). *Safeguard Mechanism*. 
https://www.dcceew.gov.au/climate-change/emissions-reporting/national-greenhouse-energy-reporting-scheme/safeguard-mechanism
- Department of Climate Change, Energy, the Environment and Water. (2025, September 24). *International climate action*. 
https://www.dcceew.gov.au/climate-change/international-climate-action
- Department of Climate Change, Energy, the Environment and Water. (2025, October 2). *Capacity Investment Scheme*. 
https://www.dcceew.gov.au/energy/renewable/capacity-investment-scheme
- Department of Climate Change, Energy, the Environment and Water. (2019). *Climate Solutions Package*. 
https://www.dcceew.gov.au/sites/default/files/documents/climate-solutions-package.pdf
- Department of Industry, Science, Energy and Resources. (2020). *Technology Investment Roadmap: First Low Emissions Technology Statement - 2020*. Department of Industry, Science, Energy and Resources. https://www.dcceew.gov.au/sites/default/files/documents/first-low-emissions-technology-statement-2020.pdf
- Energy.gov.au (Department of Climate Change, Energy, the Environment and Water). (2024, August 28). *Australian Energy Update 2024*. 
https://www.energy.gov.au/publications/australian-energy-update-2024
- Government of Australia. (2022). *Australia’s Nationally Determined Contribution - 2022 Update* (UNFCCC submission), esp. Tables 1.1.2 and 1.4.7. https://unfccc.int/sites/default/files/NDC/2022-06/Australias%20NDC%20June%202022%20Update%20%283%29.pdf
- International Energy Agency. (2022, February 18). *National Energy Productivity Plan*. https://www.iea.org/policies/1240-national-energy-productivity-plan
- Parliament of Australia. (2011). *Bills search results: Clean Energy Bill 2011*. https://www.aph.gov.au/Parliamentary_Business/Bills_Legislation/Bills_Search_Results/Result?bId=r4653
- Parliament of Australia. (2022). *Bills search results: Climate Change Bill 2022*. https://www.aph.gov.au/Parliamentary_Business/Bills_Legislation/Bills_Search_Results/Result?bId=r6885 
- Parliament of Australia, Senate Environment and Communications References Committee. (n.d.). *Australia’s greenhouse performance and strategy (Part a)*. https://www.aph.gov.au/Parliamentary_Business/Committees/Senate/Environment_and_Communications/Completed_inquiries/1999-02/gobalwarm/report/c04
- Parliament of Australia, Senate Environment and Communications References Committee. (n.d.). *Chapter 2 - Climate change and the Kyoto Protocol*. https://www.aph.gov.au/Parliamentary_Business/Committees/Senate/Environment_and_Communications/Completed_inquiries/2002-04/kyoto/report/c02
- Parliament of Australia, Senate Environment and Communications References Committee. (n.d.). *Chapter 2 - The Energy White Paper*
https://www.aph.gov.au/Parliamentary_Business/Committees/Senate/Environment_and_Communications/Completed_inquiries/2004-07/energywhitepaper/report/c02
- United Nations Treaty Collection. (1997, December 11). *Kyoto Protocol to the United Nations Framework Convention on Climate Change*. https://treaties.un.org/pages/viewdetails.aspx?src=treaty&mtdsg_no=XXVII-7-a&chapter=27&clang=_en


