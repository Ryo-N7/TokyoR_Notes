With the arrival of summer, another [TokyoR User
Meetup](https://tokyor.connpass.com/event/130254/)! On May 25th, useRs
from all over Tokyo (and some even from further afield - including Kan
Nishida of [Exploratory](https://exploratory.io/), all the way from
California!) flocked to Jimbocho, Tokyo for another jam-packed session
of \#rstats hosted by [Mitsui Sumitomo Insurance
Group](https://www.ms-ins.com/english/).

<img src="https://i.imgur.com/UlstyyS.png" style="display: block; margin: auto;" width = "350" />

Like my previous round up posts (for [TokyoR
\#76](https://ryo-n7.github.io/2019-03-07-tokyoR-76-roundup/) and
[TokyoR \#77](https://ryo-n7.github.io/2019-04-24-tokyoR-77/)) I will be
going over around half of all the talks. Hopefully, my efforts will help
spread the vast knowledge of Japanese R users to the wider R community.
Throughout I will also post helpful blog posts and links from other
sources if you are interested in learning more about the topic of a
certain talk. You can follow **Tokyo.R** by searching for the
[\#TokyoR](https://twitter.com/hashtag/TokyoR) hashtag on Twitter.

Unlike most R Meetups a lot of people present using just their Twitter
handles so I’ll mostly be referring to them by those instead. I’ve been
going to events here in Japan for a bit over a year but even now
sometimes I’m like, “Whoahh that’s what
`@very_recognizable_twitter_handle_in_the_japan_r_community` actually
looks like?!”

Anyways…

Let’s get started!

BeginneR Session
================

As with every [TokyoR](http://tokyor.connpass.com/) meetup, we began
with a set of beginner user focused talks:

-   [Reading in data with R by
    y\_mattu](https://github.com/ymattu/TokyoR78)
-   [Visualization with R by
    koriakane](https://speakerdeck.com/nozomi_miyazaki/tokyo-dot-r-number-77-chu-xin-zhe-setusiyon1-ke-shi-hua-pato)
-   [Data analysis with R by
    kilometer00](https://speakerdeck.com/kilometer/tokyo-dot-r-number-78-beginnersession-data-analysis)

Main Talks
==========

[tanakafreelance](https://twitter.com/tanaka_marimo): Radiant for Data Analysis!
--------------------------------------------------------------------------------

-   [Slides](https://www.slideshare.net/ssuser5aee94/78th-tokyor-radiant)

`@tanakafreelance` talked about
[Radiant](https://radiant-rstats.github.io/), which is a
platform-independent browser-based GUI for business analytics that was
developed by [Vincent Nijs](). It is a tool for business analytics
purposes and is based on `Shiny`. After installation from CRAN you can
launch it via using `radiant::launcher()`. Most of this presentation was
a live demo by `@tanakafreelance` showing a lot of the functionality
offered by Radiant such as creating reproducible reports with R
Markdown, writing your own R code to use within the GUI, creating and
evaluating models (linear/logistic regression, neural networks, naive
Bayes, and more), and design of experiments (DOE)!

![](https://i.ytimg.com/vi/7L3hDpLw53I/maxresdefault.jpg)

You can run it from a variety of set ups from online, offline, on
`shinyapps.io`, Shiny server, and even on a cloud service like AWS via a
customized Docker container. For a comprehensive introduction to
Radiant’s full capabilities you can check out its awesome website
[here](https://radiant-rstats.github.io/docs/index.html), full of videos
and vignettes!

-   [Radiant website](https://radiant-rstats.github.io/docs/)
-   [Radiant Github](https://github.com/radiant-rstats/radiant)

[kotaku08](https://twitter.com/kotaku08): Transitioning a Company to Use R!
---------------------------------------------------------------------------

-   [Slides](https://speakerdeck.com/kosshi/r-package-for-a-team)

`@kotaku08` talked about his experiences in data analytics and ways he
pushed for the usage of R at his company, VALUES. One of the first
things he realized upon entering the company was how the skill set of
the team was more of that of data/system engineers rather than data
analysts. After some time he found three big problems with his working
environment that he wanted to solve:

1.  Mismatch between the tool used and the task needed done
    -   easy data manipulation with PHP.
    -   complicated data manipulation with Excel.
2.  What was this again?! (Illegible! Non-reproducible! Non-reusable!)
    -   Extremely convoluted Excel formulas that look like they could be
        banned by the `Malleus Maleficarum`.
    -   Excel sheets only contain the **results**.
    -   If it was a visualization task, it was all done in Tableau…
3.  Data extraction being a painful process…
    -   Connecting to `Redshift` is a pain!

While pondering these problems, he came across [this
article](https://medium.com/airbnb-engineering/using-r-packages-and-education-to-scale-data-science-at-airbnb-906faa58e12d)
from AirBnB that highlighted their transition to building R tools and
teaching R across the company. The key takeaways that `@kotaku08` took
from the article was:

-   Most analysts at AirBnB use R.
-   Intracompany package: `Rbnb`.
-   Efforts put into R education and conducting workshops.
-   Data analysis is both efficient AND reproducible!

Taking these lessons to heart he decided to implement \#rstats learning
sessions as well as create a company R package! One of the main
functionalities of VALUES’ main R package is being able to access data
from Redshift and in tandem with the various packages in the `cloudyr`
project has made getting data much more easier for `@kotaku08` and his
team.

Another big step was educating fellow employees about \#rstats.

For **existing** employees:

1.  Spread rumors about how accessing data is much easier with R…
2.  Those skilled in other scripting languages organically come over to
    check R out!

For **new** employees:

-   Emphasize how R is **THE** standard at the company,
-   “Graduate hires”, most of whom have no programming experience, are
    put into R boot camps
-   After 3 months of hard work, able to use the `tidyverse` for
    analytical tasks!

As a result of these efforts 80% of employees can now use R and the
internal company package has two new maintainers (both graduate hires!)
to work alongside `kotaku08`.

Some other resources:

-   [List of Companies Using R! (With explanatory
    blogposts/articles)](https://github.com/ThinkR-open/companies-using-r)
-   [Scaling Knowledge at
    AirBnB](https://medium.com/airbnb-engineering/scaling-knowledge-at-airbnb-875d73eff091)
-   [Enterprise Web Services with Neural Networks Using R and
    Tensorflow](https://opensource.t-mobile.com/blog/posts/r-tensorflow-api/)
-   [“Putting empathy in action: Building a ‘community of practice’ for
    analytics in a global corporation” - JD Long (at
    RStudio::Conf 2019)](https://resources.rstudio.com/rstudio-conf-2019/putting-empathy-in-action-building-a-community-of-practice-for-analytics-in-a-global-corporation)
-   [itdepends - A dialogue about
    dependencies](https://www.tidyverse.org/articles/2019/05/itdepends/)

[tomkxy](https://twitter.com/tomkXY/): Making Your Code Faster - Introduction to Vectorisation and Parallel Computing (English with demonstrations)
---------------------------------------------------------------------------------------------------------------------------------------------------

-   [Slides](https://github.com/TomKellyGenetics/TokyoR78)

`@tomkxy` presented in English (he’s a Kiwi that works for RIKEN!) on
vectorizing your code and parallel computing with R. In response to a
lot of the accusations that “R is slow”, Tom talked about different
techniques to use to make your R code faster along with some some
demonstrations (the RMD can be found
[here](https://github.com/TomKellyGenetics/TokyoR78/blob/master/demo.Rmd)).

![](https://i.imgur.com/KxNrMZN.png)

One of my key take-aways from this talk was, “Code first, optimize
later!”. In that it’s important to not get stuck doing premature
optimization, especially if you might not actually need to use the code
again anyways! Also, sometimes parallel computing may not always be the
fastest solution due to overhead costs associated with setting up
clusters and communication between clusters.

![](https://i.imgur.com/dVmhXgE.png)

In addition, the newly developed “Jobs” pane in RStudio 1.2, [released
last month](https://blog.rstudio.com/2019/04/30/rstudio-1-2-release/),
means you can keep being productive even while you have your scripts
running in the background. A great resource for those interested is the
CRAN Task View for high performance and parallel computing available
[here](https://cran.r-project.org/web/views/HighPerformanceComputing.html).

A few other resources:

-   [Vectorization in R - Noam
    Ross](http://www.noamross.net/blog/2014/4/16/vectorization-in-r--why.html)
-   Chapters 3 & 4 on vectorization of the classic: [R Inferno - Patrick
    Burns](http://www.burns-stat.com/pages/Tutor/R_inferno.pdf)
-   [“What does it mean to write ‘vectorized’ code in R?” -
    Win-Vector](http://www.win-vector.com/blog/2019/01/what-does-it-mean-to-write-vectorized-code-in-r/)
-   The [functionals](http://adv-r.had.co.nz/Functionals.html) and
    [Optimizing code](http://adv-r.had.co.nz/Profiling.html) sections of
    [Advanced R - Hadley Wickham](http://adv-r.had.co.nz/)
-   [Using RStudio Jobs for training many models in parallel - Edwin
    Thoen](https://edwinth.github.io/blog/parallel-jobs/)

LTs
===

[ill\_identified](https://twitter.com/ill_Identified): Guide to MCMC with the `bayesplot` package!
--------------------------------------------------------------------------------------------------

-   [Slides](https://www.slideshare.net/SatoshiKatagiri2/bayesplot)

`@ill_identified` presented on using Markov chain Monte Carlo (MCMC)
with R, specifically using the `bayesplot` package. MCMC are a series of
methods that contain algorithms for sampling from a probability
distribution. These methods involve drawing random samples from a target
distributions using algorithms (such as Metropolis-Hastings algorithm,
reversible jump, HMC, etc.) then we attempt to construct a Markov chain
such that its equilibrium probability distribution is as close to our
target distribution as possible by iterating the chain many times.

![](https://i.imgur.com/yuwkwO2.png)

As I’m not familiar with MCMC very much I won’t go into too much detail
here, however for others unfamiliar with MCMC and Bayesian
inference,`@ill_identified` provided a nice list of books to get you
started:

-   [Bayesian Data Analysis - Gelman et al.]()
-   [Introduction to Bayesian Statistics with R (Japanese) - Okumura et
    al.](https://github.com/okumuralab/bayesbook)
-   [Bayesian Modeling with Stan & R (Japanese) - Matsuura et
    al.](https://github.com/MatsuuraKentaro/RStanBook)

Just recently [TJ Mahr](https://twitter.com/tjmahr), one of the authors
of `bayesplot`, presented on the package at Chicago SatRDays. You can
check out the slides out
[here](https://www.tjmahr.com/bayesplot-satrdays-2019). The new version
of `bayesplot`, 1.7.0, will also support tidyselect:

![](https://i.imgur.com/9nMS5nu.png)

Other resources:

-   [CRAN Task View: Bayesian
    Inference](https://cran.r-project.org/web/views/Bayesian.html)
-   [bayesplot vignette: Plotting MCMC
    draws](https://cran.r-project.org/web/packages/bayesplot/vignettes/plotting-mcmc-draws.html)
-   [Statistical Rethinking with brms, ggplot2, and the tidyverse -
    Solomon
    Kurz](https://bookdown.org/ajkurz/Statistical_Rethinking_recoded/markov-chain-monte-carlo.html)

[Atsushi776](https://twitter.com/Atsushi776): May I `felp` you?
---------------------------------------------------------------

-   [Slides](https://presentation.atusy.net/20190525-tokyor76-felp/#/)

`@Atsushi776`, known in the Japanese R Community for his “headphones”
avatar, created a new package called
[felp](https://github.com/atusy/felp) as he was annoyed that he couldn’t
look at the source code while looking at the help files of a function.
Also there was the added annoyance of having to jump back to the start
of the function to type `?` back in AND deleting it once you’re done.

``` r
source("https://install-github.me/atusy/felp")
library(felp)
library(printr)

## From this:
?help()

## To this:
help?
## Alternatively:
felp(help)
felp("help")
```

``` r
## Source code is nicely highlighted by `prettycode`:
## Output shortened for brevity...
grep()?.
```

    ## function (pattern, x, ignore.case = FALSE, perl = FALSE, value = FALSE, 
    ##     fixed = FALSE, useBytes = FALSE, invert = FALSE) 
    ## {
    ##     if (!is.character(x)) 
    ##         x <- structure(as.character(x), names = names(x))
    ##     .Internal(grep(as.character(pattern), x, ignore.case, value, 
    ##         perl, fixed, useBytes, invert))
    ## }
    ## <bytecode: 0x000000001750ad50>
    ## <environment: namespace:base>

    ## Pattern Matching and Replacement
    ## 
    ## Description:
    ## 
    ##      'grep', 'grepl', 'regexpr', 'gregexpr' and 'regexec' search for
    ##      matches to argument 'pattern' within each element of a character
    ##      vector: they differ in the format of and amount of detail in the
    ##      results.
    ## 
    ##      'sub' and 'gsub' perform replacement of the first and all matches
    ##      respectively.
    ## 
    ## Usage:
    ## 
    ##      grep(pattern, x, ignore.case = FALSE, perl = FALSE, value = FALSE,
    ##           fixed = FALSE, useBytes = FALSE, invert = FALSE)
    ##      
    ##      grepl(pattern, x, ignore.case = FALSE, perl = FALSE,
    ##            fixed = FALSE, useBytes = FALSE)
    ##      
    ##      sub(pattern, replacement, x, ignore.case = FALSE, perl = FALSE,
    ##          fixed = FALSE, useBytes = FALSE)
    ##      
    ##      gsub(pattern, replacement, x, ignore.case = FALSE, perl = FALSE,
    ##           fixed = FALSE, useBytes = FALSE)
    ##      
    ##      regexpr(pattern, text, ignore.case = FALSE, perl = FALSE,
    ##              fixed = FALSE, useBytes = FALSE)
    ##      
    ##      gregexpr(pattern, text, ignore.case = FALSE, perl = FALSE,
    ##               fixed = FALSE, useBytes = FALSE)
    ##      
    ##      regexec(pattern, text, ignore.case = FALSE, perl = FALSE,
    ##              fixed = FALSE, useBytes = FALSE)
    ##      
    ## Arguments:
    ## 
    ##  pattern: character string containing a regular expression (or
    ##           character string for 'fixed = TRUE') to be matched in the
    ##           given character vector.  Coerced by 'as.character' to a
    ##           character string if possible.  If a character vector of
    ##           length 2 or more is supplied, the first element is used with
    ##           a warning.  Missing values are allowed except for 'regexpr'
    ##           and 'gregexpr'.
    ## 
    ##  x, text: a character vector where matches are sought, or an object
    ##           which can be coerced by 'as.character' to a character vector.
    ##           Long vectors are supported.
    ## 
    ## ignore.case: if 'FALSE', the pattern matching is _case sensitive_ and
    ##           if 'TRUE', case is ignored during matching.
    ## 
    ##     perl: logical.  Should Perl-compatible regexps be used?
    ## 
    ##    value: if 'FALSE', a vector containing the ('integer') indices of
    ##           the matches determined by 'grep' is returned, and if 'TRUE',
    ##           a vector containing the matching elements themselves is
    ##           returned.
    ## 
    ##    fixed: logical.  If 'TRUE', 'pattern' is a string to be matched as
    ##           is.  Overrides all conflicting arguments.
    ## 
    ## useBytes: logical.  If 'TRUE' the matching is done byte-by-byte rather
    ##           than character-by-character.  See 'Details'.
    ## 
    ##   invert: logical.  If 'TRUE' return indices or values for elements
    ##           that do _not_ match.
    ## 
    ## replacement: a replacement for matched pattern in 'sub' and 'gsub'.
    ##           Coerced to character if possible.  For 'fixed = FALSE' this
    ##           can include backreferences '"\1"' to '"\9"' to parenthesized
    ##           subexpressions of 'pattern'.  For 'perl = TRUE' only, it can
    ##           also contain '"\U"' or '"\L"' to convert the rest of the
    ##           replacement to upper or lower case and '"\E"' to end case
    ##           conversion.  If a character vector of length 2 or more is
    ##           supplied, the first element is used with a warning.  If 'NA',
    ##           all elements in the result corresponding to matches will be
    ##           set to 'NA'.
    ## 
    ## Details:
    ## 
    ##      Arguments which should be character strings or character vectors
    ##      are coerced to character if possible.
    ## 
    ##      Each of these functions operates in one of three modes:
    ## 
    ##        1. 'fixed = TRUE': use exact matching.
    ## 
    ##        2. 'perl = TRUE': use Perl-style regular expressions.
    ## 
    ##        3. 'fixed = FALSE, perl = FALSE': use POSIX 1003.2 extended
    ##           regular expressions (the default).
    ## 
    ##      See the help pages on regular expression for details of the
    ##      different types of regular expressions.
    ## 
    ##      The two '*sub' functions differ only in that 'sub' replaces only
    ##      the first occurrence of a 'pattern' whereas 'gsub' replaces all
    ##      occurrences.  If 'replacement' contains backreferences which are
    ##      not defined in 'pattern' the result is undefined (but most often
    ##      the backreference is taken to be '""').
    ## 
    ##      For 'regexpr', 'gregexpr' and 'regexec' it is an error for
    ##      'pattern' to be 'NA', otherwise 'NA' is permitted and gives an
    ##      'NA' match.
    ## 
    ##      The main effect of 'useBytes' is to avoid errors/warnings about
    ##      invalid inputs and spurious matches in multibyte locales, but for
    ##      'regexpr' it changes the interpretation of the output.  It
    ##      inhibits the conversion of inputs with marked encodings, and is
    ##      forced if any input is found which is marked as '"bytes"' (see
    ##      'Encoding').
    ## 
    ##      Caseless matching does not make much sense for bytes in a
    ##      multibyte locale, and you should expect it only to work for ASCII
    ##      characters if 'useBytes = TRUE'.
    ## 
    ##      'regexpr' and 'gregexpr' with 'perl = TRUE' allow Python-style
    ##      named captures, but not for _long vector_ inputs.
    ## 
    ##      Invalid inputs in the current locale are warned about up to 5
    ##      times.
    ## 
    ##      Caseless matching with 'perl = TRUE' for non-ASCII characters
    ##      depends on the PCRE library being compiled with 'Unicode property
    ##      support': an external library might not be.
    ## 
    ## Value:
    ## 
    ##      'grep(value = FALSE)' returns a vector of the indices of the
    ##      elements of 'x' that yielded a match (or not, for 'invert =
    ##      TRUE').  This will be an integer vector unless the input is a
    ##      _long vector_, when it will be a double vector.
    ## 
    ##      'grep(value = TRUE)' returns a character vector containing the
    ##      selected elements of 'x' (after coercion, preserving names but no
    ##      other attributes).
    ## 
    ##      'grepl' returns a logical vector (match or not for each element of
    ##      'x').
    ## 
    ##      'sub' and 'gsub' return a character vector of the same length and
    ##      with the same attributes as 'x' (after possible coercion to
    ##      character).  Elements of character vectors 'x' which are not
    ##      substituted will be returned unchanged (including any declared
    ##      encoding).  If 'useBytes = FALSE' a non-ASCII substituted result
    ##      will often be in UTF-8 with a marked encoding (e.g., if there is a
    ##      UTF-8 input, and in a multibyte locale unless 'fixed = TRUE').
    ##      Such strings can be re-encoded by 'enc2native'.
    ## 
    ##      'regexpr' returns an integer vector of the same length as 'text'
    ##      giving the starting position of the first match or -1 if there is
    ##      none, with attribute '"match.length"', an integer vector giving
    ##      the length of the matched text (or -1 for no match).  The match
    ##      positions and lengths are in characters unless 'useBytes = TRUE'
    ##      is used, when they are in bytes (as they are for an ASCII-only
    ##      matching: in either case an attribute 'useBytes' with value 'TRUE'
    ##      is set on the result).  If named capture is used there are further
    ##      attributes '"capture.start"', '"capture.length"' and
    ##      '"capture.names"'.
    ## 
    ##      'gregexpr' returns a list of the same length as 'text' each
    ##      element of which is of the same form as the return value for
    ##      'regexpr', except that the starting positions of every (disjoint)
    ##      match are given.
    ## 
    ##      'regexec' returns a list of the same length as 'text' each element
    ##      of which is either -1 if there is no match, or a sequence of
    ##      integers with the starting positions of the match and all
    ##      substrings corresponding to parenthesized subexpressions of
    ##      'pattern', with attribute '"match.length"' a vector giving the
    ##      lengths of the matches (or -1 for no match).  The interpretation
    ##      of positions and length and the attributes follows 'regexpr'.
    ## 
    ##      Where matching failed because of resource limits (especially for
    ##      PCRE) this is regarded as a non-match, usually with a warning.
    ## 
    ## Warning:
    ## 
    ##      The POSIX 1003.2 mode of 'gsub' and 'gregexpr' does not work
    ##      correctly with repeated word-boundaries (e.g., 'pattern = "\b"').
    ##      Use 'perl = TRUE' for such matches (but that may not work as
    ##      expected with non-ASCII inputs, as the meaning of 'word' is
    ##      system-dependent).
    ## 
    ## Performance considerations:
    ## 
    ##      If you are doing a lot of regular expression matching, including
    ##      on very long strings, you will want to consider the options used.
    ##      Generally PCRE will be faster than the default regular expression
    ##      engine, and 'fixed = TRUE' faster still (especially when each
    ##      pattern is matched only a few times).
    ## 
    ##      If you are working in a single-byte locale and have marked UTF-8
    ##      strings that are representable in that locale, convert them first
    ##      as just one UTF-8 string will force all the matching to be done in
    ##      Unicode, which attracts a penalty of around 3x for the default
    ##      POSIX 1003.2 mode.
    ## 
    ##      If you can make use of 'useBytes = TRUE', the strings will not be
    ##      checked before matching, and the actual matching will be faster.
    ##      Often byte-based matching suffices in a UTF-8 locale since byte
    ##      patterns of one character never match part of another.
    ## 
    ##      PCRE-based matching by default puts additional effort into
    ##      'studying' the compiled pattern when 'x'/'text' has length at
    ##      least 10.  As from R 3.4.0 that study may use the PCRE JIT
    ##      compiler on platforms where it is available (see 'pcre_config').
    ##      The details are controlled by 'options' 'PCRE_study' and
    ##      'PCRE_use_JIT'.  (Some timing comparisons can be seen by running
    ##      file 'tests/PCRE.R' in the R sources (and perhaps installed).)
    ##      People working with PCRE and very long strings can adjust the
    ##      maximum size of the JIT stack by setting environment variable
    ##      'R_PCRE_JIT_STACK_MAXSIZE' before JIT is used to a value between
    ##      '1' and '1000' in MB: the default is '64'.  (Then it would usually
    ##      be wise to set the option 'PCRE_limit_recursion'.)
    ## 
    ## Source:
    ## 
    ##      The C code for POSIX-style regular expression matching has changed
    ##      over the years.  As from R 2.10.0 (Oct 2009) the TRE library of
    ##      Ville Laurikari (<URL: http://laurikari.net/tre/>) is used.  The
    ##      POSIX standard does give some room for interpretation, especially
    ##      in the handling of invalid regular expressions and the collation
    ##      of character ranges, so the results will have changed slightly
    ##      over the years.
    ## 
    ##      For Perl-style matching PCRE (<URL: http://www.pcre.org>) is used:
    ##      again the results may depend (slightly) on the version of PCRE in
    ##      use.
    ## 
    ## References:
    ## 
    ##      Becker, R. A., Chambers, J. M. and Wilks, A. R. (1988) _The New S
    ##      Language_.  Wadsworth & Brooks/Cole ('grep')
    ## 
    ## See Also:
    ## 
    ##      regular expression (aka 'regexp') for the details of the pattern
    ##      specification.
    ## 
    ##      'regmatches' for extracting matched substrings based on the
    ##      results of 'regexpr', 'gregexpr' and 'regexec'.
    ## 
    ##      'glob2rx' to turn wildcard matches into regular expressions.
    ## 
    ##      'agrep' for approximate matching.
    ## 
    ##      'charmatch', 'pmatch' for partial matching, 'match' for matching
    ##      to whole strings, 'startsWith' for matching of initial parts of
    ##      strings.
    ## 
    ##      'tolower', 'toupper' and 'chartr' for character translations.
    ## 
    ##      'apropos' uses regexps and has more examples.
    ## 
    ##      'grepRaw' for matching raw vectors.
    ## 
    ##      Options 'PCRE_limit_recursion', 'PCRE_study' and 'PCRE_use_JIT'.
    ## 
    ##      'extSoftVersion' for the versions of regex and PCRE libraries in
    ##      use, 'pcre_config' for more details for PCRE.
    ## 
    ## Examples:
    ## 
    ##      grep("[a-z]", letters)
    ##      
    ##      txt <- c("arm","foot","lefroo", "bafoobar")
    ##      if(length(i <- grep("foo", txt)))
    ##         cat("'foo' appears at least once in\n\t", txt, "\n")
    ##      i # 2 and 4
    ##      txt[i]
    ##      
    ##      ## Double all 'a' or 'b's;  "\" must be escaped, i.e., 'doubled'
    ##      gsub("([ab])", "\\1_\\1_", "abc and ABC")
    ##      
    ##      txt <- c("The", "licenses", "for", "most", "software", "are",
    ##        "designed", "to", "take", "away", "your", "freedom",
    ##        "to", "share", "and", "change", "it.",
    ##        "", "By", "contrast,", "the", "GNU", "General", "Public", "License",
    ##        "is", "intended", "to", "guarantee", "your", "freedom", "to",
    ##        "share", "and", "change", "free", "software", "--",
    ##        "to", "make", "sure", "the", "software", "is",
    ##        "free", "for", "all", "its", "users")
    ##      ( i <- grep("[gu]", txt) ) # indices
    ##      stopifnot( txt[i] == grep("[gu]", txt, value = TRUE) )
    ##      
    ##      ## Note that in locales such as en_US this includes B as the
    ##      ## collation order is aAbBcCdEe ...
    ##      (ot <- sub("[b-e]",".", txt))
    ##      txt[ot != gsub("[b-e]",".", txt)]#- gsub does "global" substitution
    ##      
    ##      txt[gsub("g","#", txt) !=
    ##          gsub("g","#", txt, ignore.case = TRUE)] # the "G" words
    ##      
    ##      regexpr("en", txt)
    ##      
    ##      gregexpr("e", txt)
    ##      
    ##      ## Using grepl() for filtering
    ##      ## Find functions with argument names matching "warn":
    ##      findArgs <- function(env, pattern) {
    ##        nms <- ls(envir = as.environment(env))
    ##        nms <- nms[is.na(match(nms, c("F","T")))] # <-- work around "checking hack"
    ##        aa <- sapply(nms, function(.) { o <- get(.)
    ##                     if(is.function(o)) names(formals(o)) })
    ##        iw <- sapply(aa, function(a) any(grepl(pattern, a, ignore.case=TRUE)))
    ##        aa[iw]
    ##      }
    ##      findArgs("package:base", "warn")
    ##      
    ##      ## trim trailing white space
    ##      str <- "Now is the time      "
    ##      sub(" +$", "", str)  ## spaces only
    ##      ## what is considered 'white space' depends on the locale.
    ##      sub("[[:space:]]+$", "", str) ## white space, POSIX-style
    ##      ## what PCRE considered white space changed in version 8.34: see ?regex
    ##      sub("\\s+$", "", str, perl = TRUE) ## PCRE-style white space
    ##      
    ##      ## capitalizing
    ##      txt <- "a test of capitalizing"
    ##      gsub("(\\w)(\\w*)", "\\U\\1\\L\\2", txt, perl=TRUE)
    ##      gsub("\\b(\\w)",    "\\U\\1",       txt, perl=TRUE)
    ##      
    ##      txt2 <- "useRs may fly into JFK or laGuardia"
    ##      gsub("(\\w)(\\w*)(\\w)", "\\U\\1\\E\\2\\U\\3", txt2, perl=TRUE)
    ##       sub("(\\w)(\\w*)(\\w)", "\\U\\1\\E\\2\\U\\3", txt2, perl=TRUE)
    ##      
    ##      ## named capture
    ##      notables <- c("  Ben Franklin and Jefferson Davis",
    ##                    "\tMillard Fillmore")
    ##      # name groups 'first' and 'last'
    ##      name.rex <- "(?<first>[[:upper:]][[:lower:]]+) (?<last>[[:upper:]][[:lower:]]+)"
    ##      (parsed <- regexpr(name.rex, notables, perl = TRUE))
    ##      gregexpr(name.rex, notables, perl = TRUE)[[2]]
    ##      parse.one <- function(res, result) {
    ##        m <- do.call(rbind, lapply(seq_along(res), function(i) {
    ##          if(result[i] == -1) return("")
    ##          st <- attr(result, "capture.start")[i, ]
    ##          substring(res[i], st, st + attr(result, "capture.length")[i, ] - 1)
    ##        }))
    ##        colnames(m) <- attr(result, "capture.names")
    ##        m
    ##      }
    ##      parse.one(notables, parsed)
    ##      
    ##      ## Decompose a URL into its components.
    ##      ## Example by LT (http://www.cs.uiowa.edu/~luke/R/regexp.html).
    ##      x <- "http://stat.umn.edu:80/xyz"
    ##      m <- regexec("^(([^:]+)://)?([^:/]+)(:([0-9]+))?(/.*)", x)
    ##      m
    ##      regmatches(x, m)
    ##      ## Element 3 is the protocol, 4 is the host, 6 is the port, and 7
    ##      ## is the path.  We can use this to make a function for extracting the
    ##      ## parts of a URL:
    ##      URL_parts <- function(x) {
    ##          m <- regexec("^(([^:]+)://)?([^:/]+)(:([0-9]+))?(/.*)", x)
    ##          parts <- do.call(rbind,
    ##                           lapply(regmatches(x, m), `[`, c(3L, 4L, 6L, 7L)))
    ##          colnames(parts) <- c("protocol","host","port","path")
    ##          parts
    ##      }
    ##      URL_parts(x)
    ##      
    ##      ## There is no gregexec() yet, but one can emulate it by running
    ##      ## regexec() on the regmatches obtained via gregexpr().  E.g.:
    ##      pattern <- "([[:alpha:]]+)([[:digit:]]+)"
    ##      s <- "Test: A1 BC23 DEF456"
    ##      lapply(regmatches(s, gregexpr(pattern, s)),
    ##             function(e) regmatches(e, regexec(pattern, e)))

Short for **f** unctional h **elp**, he got this to work by modifying
the `?` operator to show the inner structure of a function along with
the help page. This works for both a function as seen above and on
packages by `package_name?p`. You can also use the `?` on data set
objects to return what you’ll normally get from a `str()` call in
addition the the help page.

``` r
iris?. ## also opens "Help" page for the dataset
```

    ## 'data.frame':    150 obs. of  5 variables:
    ##  $ Sepal.Length: num  5.1 4.9 4.7 4.6 5 5.4 4.6 5 4.4 4.9 ...
    ##  $ Sepal.Width : num  3.5 3 3.2 3.1 3.6 3.9 3.4 3.4 2.9 3.1 ...
    ##  $ Petal.Length: num  1.4 1.4 1.3 1.5 1.4 1.7 1.4 1.5 1.4 1.5 ...
    ##  $ Petal.Width : num  0.2 0.2 0.2 0.2 0.2 0.4 0.3 0.2 0.2 0.1 ...
    ##  $ Species     : Factor w/ 3 levels "setosa","versicolor",..: 1 1 1 1 1 1 1 1 1 1 ...

    ## Edgar Anderson's Iris Data
    ## 
    ## Description:
    ## 
    ##      This famous (Fisher's or Anderson's) iris data set gives the
    ##      measurements in centimeters of the variables sepal length and
    ##      width and petal length and width, respectively, for 50 flowers
    ##      from each of 3 species of iris.  The species are _Iris setosa_,
    ##      _versicolor_, and _virginica_.
    ## 
    ## Usage:
    ## 
    ##      iris
    ##      iris3
    ##      
    ## Format:
    ## 
    ##      'iris' is a data frame with 150 cases (rows) and 5 variables
    ##      (columns) named 'Sepal.Length', 'Sepal.Width', 'Petal.Length',
    ##      'Petal.Width', and 'Species'.
    ## 
    ##      'iris3' gives the same data arranged as a 3-dimensional array of
    ##      size 50 by 4 by 3, as represented by S-PLUS.  The first dimension
    ##      gives the case number within the species subsample, the second the
    ##      measurements with names 'Sepal L.', 'Sepal W.', 'Petal L.', and
    ##      'Petal W.', and the third the species.
    ## 
    ## Source:
    ## 
    ##      Fisher, R. A. (1936) The use of multiple measurements in taxonomic
    ##      problems.  _Annals of Eugenics_, *7*, Part II, 179-188.
    ## 
    ##      The data were collected by Anderson, Edgar (1935).  The irises of
    ##      the Gaspe Peninsula, _Bulletin of the American Iris Society_,
    ##      *59*, 2-5.
    ## 
    ## References:
    ## 
    ##      Becker, R. A., Chambers, J. M. and Wilks, A. R. (1988) _The New S
    ##      Language_.  Wadsworth & Brooks/Cole. (has 'iris3' as 'iris'.)
    ## 
    ## See Also:
    ## 
    ##      'matplot' some examples of which use 'iris'.
    ## 
    ## Examples:
    ## 
    ##      dni3 <- dimnames(iris3)
    ##      ii <- data.frame(matrix(aperm(iris3, c(1,3,2)), ncol = 4,
    ##                              dimnames = list(NULL, sub(" L.",".Length",
    ##                                              sub(" W.",".Width", dni3[[2]])))),
    ##          Species = gl(3, 50, labels = sub("S", "s", sub("V", "v", dni3[[3]]))))
    ##      all.equal(ii, iris) # TRUE

In the near future `@Atsushi776` wants to get rid of not just the `.`
but the `?` altogether and wants to work on using a prefix `p?` in front
of the package name to bring up the documentation for an entire package.
Go `felp` yourself by taking a look at the [package
website](https://felp.atusy.net/)!

[0\_u0](https://twitter.com/0_u0): Marketing Science & R!
---------------------------------------------------------

-   [Slides](https://8-u8.github.io/TokyoR/20190525/Presentation.html#1)

`@0_u0` (better known as `きぬいと` or `Kinuito`) talked about his
successful attempt to integrate R into his workflow at the marketing
department of a very non-technical traditional Japanese company.

Most of the work being done for customers by his company is
**descriptive** statistics. Nothing fancy or A.I. or even simple linear
regression. As such, a lot of the problems that are given to his
department can be solved by tables and `ggplot`s. As a consequence he
had been fighting an uphill battle as the company standard is to just
use Excel for … well literally everything.

Trying to find some way to incorporate R and Python to make his workflow
easier `Kinuito` started using the `tidyverse` to simplify the data
cleaning processes!

![](https://i.imgur.com/tjNyIMv.png)

Key takeaways:

-   Reduce overtime by using the `tidyverse` to clean data and automate
    a lot of the grunt work involved with cleaning and transforming
    marketing data.
-   Not have to open up extraordinarily large Excel files (as much as
    before…).
-   Great success in using `ggplot2` and `DiagrammeR` for creating
    informative output.
-   Start with descriptive statistics, you can’t do anything more
    advanced unless you have the infrastructure to do so!

`Kinuito` also highlighted some things he wanted to do in the near
future:

-   Document R and Python tips for new graduate hires using R Markdown!
-   Consolidate the company’s R environment:
    -   Currently version control is a mess as everybody is still only
        working in their own local environments.
    -   Solution: Docker?

Along with `@kotaku08`’s talk it was great to get more insight into how
R is used at various companies. I’ve personally only heard things from
an American or English company’s point of view (from the various R
conferences/meetups I’ve been to) so it was nice to hear about the
differences and similarities in the challenges faced by Japanese
corporations at this month’s `TokyoR`!

Other Talks
===========

-   [don\_du\_maru](https://twitter.com/don_du_maru): [Levenshtein
    distance for remembering the name of the city that I live in!]()
-   [saltcooky](https://twitter.com/saltcooky): [Statistical Network
    Analysis with
    R](https://speakerdeck.com/saltcooky12/sutoritosunatupudetani-tong-ji-de-netutowakufen-xi-falseshi-yong-woshi-mita)
-   [GotaMorishita](https://twitter.com/GotaMorishita): [The origin of
    importance weight approach for covariate shift correction]()
-   [neronkai](): [Creating pdf documents with
    R](https://www.slideshare.net/toirenomitorizudesu/rbinomn10-size-probsizeprobsize)

Food, Drinks, and Conclusion
============================

Following all of the talks, those who were staying for the after-party
were served sushi and drinks! With a loud rendition of “kampai!”
(cheers!) R users from all over Tokyo began to talk about their
successes and struggles with R. A fun tradition at `TokyoR` is a
**Rock-Paper-Scissors** tournament with the prize being free data
science books!

The prizes for this month was:

-   [Pandas for
    Everyone](https://github.com/chendaniely/pandas_for_everyone) by
    [Daniel Chen](https://twitter.com/chendaniely) provided by [Tom
    Kelly](https://twitter.com/tomkXY)

`TokyoR` happens almost monthly and it’s a great way to mingle with
Japanese R users as it’s the largest regular meetup here in Japan. Talks
in English are also welcome so if you’re ever in Tokyo come join us!
