# addTextLabels
## Author: Joseph Crispell
## Repository created: 05-02-19
## Licence: GPL-3
A function to add points onto boxplot that are symmetrically spread out to minimise overlap

Package can be directly installed into R using:
```
install.packages("devtools")
library("devtools")
install_github("JosephCrispell/spreadPoints")
library(spreadPoints)
```

Once installed test it out with the following code:
```
# Set the seed
set.seed(254534)

# Generate some example points - drawn from exponential distribution
values <- rexp(n=50, rate=2)
 
# Plot a boxplot
boxplot(values, xlab="",  ylab="", frame=FALSE, las=1, pch=19, outcol=rgb(1,0,0, 0.5),
        horizontal=FALSE)
        
# Plot the points spread along the X axis
spreadPoints(values, position=1)
```

![](Example.png)