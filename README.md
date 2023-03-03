# posterSML

The poster (see SMLPrinciples.pdf) is to be presented at the International Convention of Psychological Science (ICPS) 9th - 11th March 2023. The poster will be presented on Thursday, 9th March (11:45 - 12:45 h) at Panoramic Hall (Location: SQUARE - Brussels Convention Centre), board number is TI-11.

The poster is based on this manuscript which is currently under review:

Miché, M., Zander-Schellenberg, T., Wahl, K., & Lieb, R. (2022). *A demonstration of supervised machine learning for psychological researchers* [Manuscript submitted for publication]

## What do you want to know next about SML?

### I provide various files which you might be interested in (see main posterSML folder).

#### Q&A
A collection of questions which in hindsight I would have liked to be answered when I was an SML newbie. As with any answer, the answers I provide reflect my current point of view. Other people may see things differently.

#### SML recommended reading
Just import the SMLrecommendations.bib document into your reference management software, e.g., zotero. This is of course only a very short list of articles. Browsing the web for 'supervised machine learning tutorial' will provide plenty of information to select from.

#### Hands-on SML
You can start experimenting with SML right away by downloading and using the [supplementary material of the manuscript](https://github.com/mmiche/demoSML "mmiche/demoSML") which this poster is based upon.

If you know how to use R, you can download the supplementary material within R like this:
```R
install.packages("devtools")
devtools::install_github(repo="https://github.com/mmiche/demoSML",
                      dependencies = "Imports", build_vignettes = TRUE)
library(demoSML)
help(package="demoSML")
```

#### Which software to use for SML
Use whatever software you are most comfortable with. I use [R](https://www.r-project.org/ "R"), like (probably) most psychologists nowadays. The advantage of R may at the same time be its disadvantage: It is free. Everybody can contribute to it, meaning that everybody can write a software package, upload it to [CRAN](https://cran.r-project.org/mirrors.html "CRAN") and/or to GitHub, from where everybody can download and then use it. Therefore, several individuals and teams provide 'their' SML software solutions within R. For instance, currently two competitors are [Tidymodels](https://www.tidymodels.org/ "Tidymodels") and [mlr3](https://mlr3book.mlr-org.com/ "mlr3"). Both provide an interface to a very large number of SML relevant R software packages. Due to each single package having idiosyncrasies of its developer(s), e.g., column.names, column_names, colNames, ..., using an interface may be a good decision in the long run, because of its consistent use of commands.
