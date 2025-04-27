# <span style="background-color: lightblue;">**The Wage-Unemployment Tightrope: Can Higher Minimum Pay Help Young Workers Without Costing Jobs?**</span>
As a 20-year-old myself, I’ve experienced firsthand the challenges of finding meaningful work in today’s job market. Balancing the need for a fair wage with the reality of limited experience often feels like walking a tightrope. Many young people like me face a tough question: does raising the minimum wage help us earn a decent living, or does it make it harder to get a foot in the door?

Youth unemployment remains stubbornly high in many countries, with young workers disproportionately affected by economic shifts and labour policies. Minimum wage laws, designed to protect workers from exploitation, can sometimes have unintended consequences-especially for those just starting out. Employers may hesitate to hire young workers at higher wage rates, preferring more experienced candidates, which can push many of us to the sidelines.

In this blog, I’ll explore this complex relationship between minimum wage policies and youth unemployment. Drawing on data from the UK and beyond, I’ll examine whether current wage structures truly support young workers or inadvertently create barriers to employment. Through this, I hope to shed light on how policies can strike a better balance-ensuring fair pay without pricing young people out of the job market.
![Unemployment Meme](https://media.tenor.com/PA7u7H6ktE0AAAAe/unemployed-unemployment.png)

### <span style="color:red">What is minimum wage?</span>

Minimum wage refers to the lowest hourly pay that employers are legally required to provide to their employees. This policy serves as a tool for governments to reduce poverty, minimize income inequality, and guarantee that employment provides a living wage. The concept is straightforward: no one should have to work full-time and still find it difficult to meet their essential needs.

However, despite the well-meaning goals, minimum wage regulations can produce unintended consequences, particularly for young individuals entering the workforce. With limited experience and fewer skills, we are often the first to feel the effects of hiring slowdowns or workforce reductions when payroll costs increase.
### <span style="color:red">Youth Unemployment and its importance</span>
Youth unemployment, generally defined as the lack of jobs among individuals aged 15 to 24, is more significant than merely a statistic. It symbolizes unrealized potential, postponed independence, and extended financial reliance on families or government assistance. On a global scale, young workers are almost three times more likely to be unemployed compared to adults.

Elevated youth unemployment not only impacts individual lives but can also hinder economic progress and amplify social inequality. For policymakers, this poses a challenge: how can we promote fair compensation for young employees without making it difficult for them to secure jobs?

### <span style="color:red"> The Economics behind the debate</span>
From an economic perspective, the minimum wage functions as a price floor in the labour market. Basic supply and demand principles indicate that if the cost of labor (wages) rises above the equilibrium level, the demand for labor may decline, potentially resulting in unemployment.

Nevertheless, reality is more intricate. The elasticity of labor demand, referring to how responsive employers are to changes in wages, differs across various industries, regions, and demographic groups. Younger workers often find themselves in job markets that are more elastic (such as retail or hospitality), which makes them especially susceptible to job loss when minimum wages increase.

### <span style="color:red"> Methodology and Data Overview </span>
To gain a clearer insight into the connection between minimum wage and youth unemployment, I've analyzed publicly accessible data from the OECD and the World Bank. The dataset encompasses: Youth unemployment figures (ages 15–24) spanning from 2000 to 2024 and the minimum wage rates (expressed as a percentage of average earnings or in absolute figures) for several countries, including the UK, US, Germany, and others. 

Prior to analysis, I prepared the data by: 

* Eliminating duplicates and irrelevant columns. 
* Standardizing the names of columns. 
* Filtering out entries with excessive missing data. 

To enhance this topic, I will visualize trends across countries with graphs and subsequently employ a random forest regression model to determine if minimum wage is a significant predictor of youth unemployment. This combination of visual representation and machine learning will aid in revealing patterns that simple averages may overlook.

![Minimum wage graph ranodm countries](https://hackmd.io/_uploads/S1ir3N9Jgx.png)
The following graph shows the trends Minimum Wage from 2000 to 2023 for 5 randomly selected countries. The countries were selected by a random country generator found online. 

![Youth Unemployment graph random countries](https://hackmd.io/_uploads/HJ3ShEqJex.png)
The following graph shows the trends Youth Unemployment from 2000 to 2023 for 5 randomly selected countries. The countries were selected by a random country generator found online.
While the graphs alone don't reveal much information, we can get some information about the economic standing and laws of the country by this standalone data. A critiism of the data is that, not all countries are available in both datasets, this makes comparison among countries difficult and our analysis biased.

### <span style="color:red"> United Kingdom </span>

![UK graph](https://hackmd.io/_uploads/HyG3g5s1xe.png)
![UK grpah](https://hackmd.io/_uploads/HJXhg5syll.png)


In line with research that indicates minimum wage increases have not systematically increased unemployment, the regression analysis (R2=0.017, p=0.378) reveals no statistically significant link between UK minimum wage levels and unemployment rates from 1999–2023. University students may experience mixed results, according to sector-specific research, even though overall data seems stable. While increasing minimum wages boost earnings for entry-level positions, they may also increase competition in industries like retail and hospitality, where employers may favour experienced applicants or automate jobs to save labour costs. Students gain from increased income in this complex environment, but they also have to cope with changing expectations of the labour market.

### <span style="color:red"> Mexico </span>
![Mexico](https://hackmd.io/_uploads/H16C4cjyxg.png)

Analysis at the national level in Mexico shows a weak but statistically significant correlation between unemployment rates and minimum wage levels. According to the regression results (R2=0.136, p=0.015), there is a 0.05% drop in unemployment for every 1% increase in the minimum wage (as a percentage of average wages). Despite the seemingly small effect size, the negative coefficient defies assumptions of job losses brought on by the minimum wage and is consistent with Mexico's particular labour dynamics, where targeted wage measures and the absorption of the informal sector may reduce employment hazards. This indicates to policymakers that modest increases in the minimum wage could promote wage growth without substantially upsetting formal employment; nonetheless, given manufacturing's known sensitivity to wage changes, sector-specific evaluations are still crucial.
### <span style="color:red"> United States </span>

![US](https://hackmd.io/_uploads/rJvs_9oygl.png)

Our investigation of the connection between the US minimum wage and unemployment rates shows a statistically significant positive correlation. In particular, the findings show that the unemployment rate typically rises by about 0.22% for every 1% increase in the minimum wage relative to the average wage. Even though this effect size is small, it implies that there may be a little correlation between higher minimum salaries and greater unemployment rates. About 14% of the variation in unemployment can be explained by the model, suggesting that other factors significantly influence labour market outcomes.

This result is consistent with economic theories that claim that raising the minimum wage may result in fewer job options for certain people, especially those in low-wage industries. It is crucial to keep in mind, though, that this relationship may be influenced by geographical variations, the makeup of the industry, and general economic situations. States with higher minimum wages, for instance, frequently have more robust economies, which can have an independent impact on employment trends.

These findings emphasise to policymakers the significance of carefully striking a balance between policies that promote workforce development and job creation and rises in the minimum wage. Low-paid workers' incomes could be increased while potential negative employment consequences are reduced with the help of skill training investments, targeted support for industries that are particularly susceptible, and gradual wage adjustments.

### <span style="color:red"> Analyzing the Relationship Between Minimum Wage and Unemployment (Random Forest Model) </span>

Our research into the relationship between minimum wage policies and unemployment rates across Mexico, the United Kingdom, and the United States has yielded significant insights through statistical modeling.

Using a Random Forest Regression model, we analyzed how minimum wage levels (expressed as a percentage of average wages) correlate with unemployment rates across these three countries. Our model demonstrates strong predictive ability with an R-squared value of 0.76, meaning it explains approximately 76% of the variation in unemployment rates in our dataset.

![RF MODEL](https://hackmd.io/_uploads/SJhtz6jyxg.png)


The most striking finding is that minimum wage levels account for 58.77% of the unemployment rate variation that our model can explain. This makes it the single most influential factor in our analysis, suggesting that minimum wage policies have a substantial relationship with unemployment rates. Importantly, this doesn't mean that other countries cause changes in minimum wage; rather, it indicates that when analyzing data from Mexico, the UK, and the US together, changes in minimum wage levels explain nearly 59% of the predictable differences in unemployment rates.

Country-specific effects account for the remaining 41.23% of our model's explanatory power. Mexico-specific economic factors contribute 36.05%, United Kingdom-specific factors account for 4.22%, and United States-specific factors represent just under 1% (0.96%). These country effects represent unique economic conditions, labor market structures, regulatory environments, and other nation-specific characteristics that influence unemployment rates beyond what minimum wage alone can explain.

![RF MODEL2](https://hackmd.io/_uploads/Bk2ZQpsygx.png)

Our model's accuracy (with a mean squared error of 5.27) and the strong contribution of minimum wage suggest that policymakers should carefully consider minimum wage levels when addressing unemployment concerns. However, the substantial country-specific effects also indicate that one-size-fits-all approaches to minimum wage policy may not be appropriate, as labor markets respond differently based on local economic conditions.
![RF MODEL 3](https://hackmd.io/_uploads/SkaS76syge.png)
![RF MODEL 4](https://hackmd.io/_uploads/rJpS76iJll.png)
![RF MODEL 5](https://hackmd.io/_uploads/r16H7Tjygl.png)

The remaining 24% of variation unexplained by our model suggests other factors not captured in our analysis—such as GDP growth, technological change, education levels, and broader economic cycles—also influence unemployment rates. This research contributes to the ongoing debate about minimum wage policies by quantifying their relative importance compared to other factors in determining unemployment levels across different national economies.

### <span style="color:red"> Conclusion </span>

Navigating the wage-unemployment tightrope for young workers requires a balanced approach. Our analysis across the UK, Mexico, and the US reveals a complex relationship between minimum wage policies and youth unemployment. While a Random Forest Regression model indicates that minimum wage levels are a significant factor, explaining nearly 59% of the variation in unemployment rates, country-specific factors also play a crucial role.

![I130628c](https://hackmd.io/_uploads/SJSDU6s1ll.jpg)


In the UK, no statistically significant link was found between minimum wage and unemployment rates, but sector-specific impacts, especially for students, should be considered. Mexico showed a slight decrease in unemployment with minimum wage increases, possibly due to unique labor dynamics. In contrast, the US exhibited a small positive correlation between higher minimum wages and increased unemployment rates.

The substantial country-specific effects, accounting for over 41% of the model's explanatory power, suggest that a one-size-fits-all minimum wage policy is not appropriate. Local economic conditions, labor market structures, and regulatory environments significantly influence unemployment rates. Policymakers should carefully consider these factors and strive for a balance between fair pay and job creation. Skill training, targeted support for susceptible industries, and gradual wage adjustments can help mitigate potential negative employment consequences.

However, it's crucial to acknowledge the limitations of this analysis. While our study scratches the surface of this intricate debate, the reality is far more nuanced. Each country operates under a unique set of economic conditions, making direct comparisons challenging. Our analysis, focusing on three distinct countries, serves to highlight this very point: the impact of minimum wage on youth unemployment is highly context-dependent. Various factors beyond minimum wage levels influence employment, especially for university students and those in entry-level jobs. Further research should incorporate factors like GDP growth and technological change to provide a more comprehensive understanding of unemployment dynamics.