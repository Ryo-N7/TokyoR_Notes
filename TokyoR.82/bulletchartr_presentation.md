Tokyo.R #82
========================================================
author: Ryo Nakagawara
date: October 26th, 2019
autosize: true

<style>
.small-code pre code {
  font-size: 1em;
}


.midcenter {
    position: fixed;
    top: 50%;
    left: 50%;
}

img.animated-gif{
  width: 1020px;
  height: auto;
}

img.anim-gif{
  width: 600px;
  height: auto;
}

</style>

About Me
========================================================

<font size = "16">
Ryo Nakagawara
</font>

<font size = "14">

- 学歴: 
  - 学士: Chapman University
  - 修士: University College London
- 専攻：心理学と経済学
- 仕事: Jr. Data Scientist @ [ACDI/VOCA](http://www.acdivoca.org/)
- Also: Editor for [R Weekly](https://rweekly.org/)

</font>

趣味: サッカー/Football & {ggplot2}
========================================================

- サッカーの可視化・分析: [Github: Ryo-N7/soccer_ggplots](https://github.com/Ryo-N7/soccer_ggplots)

<center>
![](https://i.imgur.com/GRPfksN.png)
</center>

{bulletchartr} package
========================================================

<font size = "6">


```r
install_github("ACDIVOCATech/bulletchartr")
library(bulletchartr)
```

</font>

<center>
![](https://i.imgur.com/OmaxMwf.png)
</center>

What IS a bullet chart?
========================================================

- 作：[Stephen Few](https://www.perceptualedge.com/) 
- Measure KPI vs. target and/or qualitative measures of performance
  - Low-Medium-High, Poor-Satisfactory-Good, etc.
- [Design spec](https://www.perceptualedge.com/articles/misc/Bullet_Graph_Design_Spec.pdf)

<center>
![](https://i.imgur.com/64gbgaR.png)
</center>

Example with {bulletchartr}!
========================================================

<font size = "6">

- `bulletchartr::bullet_chart(dataframe = data, ...)`
- "Current" value in <b>black</b>
- Target: <b><font color="red">red</font></b> symbol
- Legend for qualitative labels:
  - "Low", "Medium", "High"
  
</font>

<center>
![](https://i.imgur.com/I2kpDDv.png)
</center>

ACDI/VOCA
========================================================

<font size = "6">

- [ACDI/VOCA website](http://www.acdivoca.org/)
- Implement economic development projects around the world!
- 国際開発・農業開発・農村開発援助のNGO
- To ensure we implement them correctly and make an impact, we create indicators (KPIs) that have yearly targets 
- Monitor progress of projects by tracking these indicators over time.

</font>

<center>
![](https://i.imgur.com/RUUo3nd.png)
</center>

Collecting data during a project
========================================================

<font size = "5">

- Normally, gather data in a linear way throughout the course of the project (<font color="orange">orange line</font>)
- <b>BUT</b> some project activities are <b>NOT</b> linear
- Data accumulates in a <b>non-linear</b> way! (<font color="purple">purple</font> and <font color="green">green</font> lines)

</font>

<center>
<img src="https://i.imgur.com/z7YC3tU.png" />
</center>

Example 1:
========================================================

<font size = "6">

- Based on output from harvest (<font color="purple">purple line</font>)
  - A lot of data gathered only <b>later</b> in the year
  - 収穫が10月＝その時にやっとデータを収集できる
  
</font>

<center>
<img src="https://i.imgur.com/z7YC3tU.png" />
</center>

Example 2:
========================================================

<font size = "6">

- Based on distribution of funds, supplies, loans (<font color="green">green line</font>)
  - A lot of data gathered <b>early</b> in the year
  - 機械・設備投資のプロジェクト＝年明けに融資する

</font>

<center>
<img src="https://i.imgur.com/z7YC3tU.png" />
</center>


Time-comparison bullet chart
========================================================

<font size = "6">

- X-Axis scale:
  - Percent of <b>Target</b>
  - Percent of <b>Year</b>

</font>

<center>
![](https://i.imgur.com/xfy0xtV.png)
</center>

Time-comparison bullet chart (cont.)
========================================================

<font size = "6">

- If "TODAY" = <b>September</b>, then at 75% of the year: 9/12 months
- "Ind. 04" is at 25% because CURRENT VALUE is <b>6</b> and TARGET is <b>24</b>: 6/24 units
- At "TODAY" "Ind. 04" <b>should</b> be at <b>18</b> or 75% of target: 18/24 units

</font>

<center>
![](https://i.imgur.com/QcyLPRS.png)
</center>

bullet_chart_*() variants!
========================================================

<font size = "8">


```r
bullet_chart_symbol()
bullet_chart_vline()
```

</font>

<p float="left" align="center">
<img src="https://i.imgur.com/UYlhJX8.png" width="49%" />
<img src="https://i.imgur.com/LISLVPg.png" width="49%" />
</p>

bullet_chart_*() variants! (cont.)
========================================================
<font size = "8">

```r
bullet_chart_wide()
```
</font>

<center>
![](https://i.imgur.com/c7IBZWV.png)
</center>

{bulletchartr} features: Static vs. Interactive
========================================================

<font size = "6">

- "Static": Default, normal `ggplot2`
- "Interactive": Powered by `ggiraph`


```r
bullet_chart_wide(chart_type = "interactive")
```

</font>

<center>
![](https://i.imgur.com/oL4LKWZ.png)
</center>

{bulletchartr} features: Arguments
========================================================
<font size = "5">

- Legend: `TRUE/FALSE`
- Calendar type: Fiscal Year, Regular (start on January 1st), Custom
- Show text labels: `TRUE/FALSE`
  - Ind 38: "+4 from Last Week", "-16 from Last Year", etc.
  
</font>

<center>
![](https://i.imgur.com/sullZ6y.png)
</center>

Further improvements and CRAN (?)
========================================================

<center>
![life cycle: experimental](https://i.imgur.com/9JZs6Kd.png)
</center>

- Originally ONLY for company usage, difficulty generalizing package for the public
- Lots of function arguments, easy defaults necessary for usability (work-in-progress, see package vignettes!)
- Allow for different qualitative labels (not just "Low"-"Medium"-"High" or "Last Week", "Last Year")
  - "Bad"-"Okay"-"Good", "Unsatisfactory"-"Satisfactory"-"Excellent", etc.
- 年末までにCRANリリースを目指します！

Thank you!
========================================================

- {bulletchartr} パッケージ: [Github: ACDIVOCATech/bulletchartr](https://github.com/ACDIVOCATech/bulletchartr)
- サッカーの可視化・分析: [Github: soccer_ggplots](https://github.com/Ryo-N7/soccer_ggplots)
- 有名なテレビシリーズをテーマしたcolor palettes/ggplot2 themes パッケージ: [Github: tvthemes](https://github.com/Ryo-N7/tvthemes)
- Tokyo.Rのマトメ記事: [Github: TokyoR_Notes](https://github.com/Ryo-N7/TokyoR_Notes)

- Website: [https://ryo-n7.github.io/](https://ryo-n7.github.io/)

- Twitter: [@R_by_Ryo](https://twitter.com/R_by_Ryo)
