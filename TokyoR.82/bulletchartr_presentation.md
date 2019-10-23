Introducing the new {bulletchartr} package!
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
- 学歴: Chapman University, University College London
- 専攻：心理学と経済学
- 仕事: Jr. Data Scientist @ [ACDI/VOCA](http://www.acdivoca.org/)
- Also: Editor for [R Weekly](https://rweekly.org/)
</font>

趣味: サッカー/Football/Fútbol & {ggplot2}
========================================================
<font size = "8">
- Ex. 
- [Code](www.google.com)
</font>

<center>
![](http://www.fotballblogg1.com/wp-content/uploads/2015/07/russia-2018.jpg)
</center>

{bulletchartr} package
========================================================


```r
# devtools::install_github("ACDIVOCATech/bulletchartr")
library(bulletchartr)
```

<center>
![](http://www.fotballblogg1.com/wp-content/uploads/2015/07/russia-2018.jpg)
</center>

What IS a bullet chart?
========================================================

- 作：[Stephen Few]() 
- Measure KPI vs. target and/or qualitative measures of performance
  - Low-Medium-High, Poor-Satisfactory-Good, etc.

<center>
![](https://i.imgur.com/hlKr6iLl.png)
</center>

Example with {bulletchartr}!
========================================================

<font size = "6">

- `bulletchartr::bullet_chart(dataframe = data, ...)`
- "Current" value in <b>black</b>
- Target: <b>red</b> symbol
- Legend for qualitative labels:
  - "Low", "Medium", "High"
  
</font>

<center>
![](http://www.fotballblogg1.com/wp-content/uploads/2015/07/russia-2018.jpg)
</center>

ACDI/VOCA
========================================================

<font size = "6">

- Implement economic development projects around the world!
- 国際開発・農業開発・農村開発援助のNGO
- To ensure we implement them correctly and make an impact, we create indicators (KPIs) that have yearly targets 
- Monitor progress of projects by tracking these indicators over time.

</font>

<center>
![](http://www.fotballblogg1.com/wp-content/uploads/2015/07/russia-2018.jpg)
</center>

Collecting data during a project
========================================================

<font size = "6">

- Normally, gather data in a linear way throughout the course of the project
- <b>BUT</b> some project activities are <b>NOT</b> linear
- Data accumulates in a <b>non-linear</b> way!

</font>

<center>
![](http://www.fotballblogg1.com/wp-content/uploads/2015/07/russia-2018.jpg)
</center>

Examples:
========================================================

<font size = "6">

- Based on output from harvest 
  - A lot of data gathered only <b>later</b> in the year
  - 収穫が10月＝その時にやっとデータを収集できる
- Based on distribution of funds, supplies, loans
  - A lot of data gathered <b>early</b> in the year
  - 機械・設備投資のプロジェクト＝年明けに融資する

</font>

<center>
![](http://www.fotballblogg1.com/wp-content/uploads/2015/07/russia-2018.jpg)
</center>

Time-constraint bullet chart
========================================================

<font size = "6">

- X-Axis scale:
  - Percent of <b>Yearly Target</b>
  - Percent of <b>Year</b>

</font>

<font size = "6">


```r
bullet_chart_symbol()
bullet_chart_vline()
```

</font>

<center>
![](http://www.fotballblogg1.com/wp-content/uploads/2015/07/russia-2018.jpg)
</center>

bullet_chart_*() variants!
========================================================

<font size = "8">


```r
bullet_chart_symbol()
bullet_chart_vline()
```

</font>

<center>
![](http://www.fotballblogg1.com/wp-content/uploads/2015/07/russia-2018.jpg)
</center>

bullet_chart_*() variants! (cont.)
========================================================
<font size = "8">

```r
bullet_chart_wide()
```
</font>

<center>
![](http://www.fotballblogg1.com/wp-content/uploads/2015/07/russia-2018.jpg)
</center>

{bulletchartr} features: Static vs. Interactive type
========================================================

- Static: Default, normal `ggplot`
- Interactive: Powered by `ggiraph`



<center>
![](https://i.imgur.com/hlKr6iLl.png)
</center>

{bulletchartr} features: Arguments
========================================================

- Legend: `TRUE/FALSE`
- Calendar type: Fiscal Year, Regular (start on January 1st), Custom
- Show text labels: `TRUE/FALSE`
  - "+12 from Last Week", "-15 from Last Year", etc.



<center>
![](https://i.imgur.com/hlKr6iLl.png)
</center>

Further improvements and CRAN (?)
========================================================

- Originally ONLY for company usage, difficulty generalizing package for the public!
- Lots of function arguments, easy defaults necessary for usability! (work-in-progress, see package vignettes!)
- Allow for different qualitative labels (not just "Low"-"Medium"-"High)
  - "Bad"-"Okay"-"Good", "Unsatisfactory"-, etc.
- 年末までにCRANリリースを目指します！

<center>
![life cycle: experimental](https://i.imgur.com/u6bv8Bo.jpg)
</center>

Thank you!
========================================================

- {bulletchartr} パッケージ: [Github: bulletchartr](https://github.com/ACDIVOCATech/bulletchartr)
- サッカーの可視化・分析: [Github: soccer_ggplots](https://github.com/Ryo-N7/soccer_ggplots)
- 有名なテレビシリーズをテーマしたcolor palettes/ggplot2 themes パッケージ: [tvthemes](https://github.com/Ryo-N7/tvthemes)
- Tokyo.Rのマトメ記事: [Github: TokyoR_Notes](https://github.com/Ryo-N7/TokyoR_Notes)

- Website: [https://ryo-n7.github.io/](https://ryo-n7.github.io/)

- Twitter: [@R_by_Ryo](https://twitter.com/R_by_Ryo)
