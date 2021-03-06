---
layout: post
title: "CUAHSI and the WaterML R Package"
date: 2015-11-25
comments: true
categories: 
---

I've been working with water data collected by other people for the past 3 years or so. Typically, I've gotten my hands on it in 3 different ways:

1. email, dropbox, etc. from collaborators. Usually in .xlsx or .csv format. Inconsistently formatted; seldom [tidy](http://www.jstatsoft.org/article/view/v059i10).
2. Downloading manually from a website, e.g. USGS instantaneous flows pre-2007
3. Using an API for web services such as the water quality portal (WQP) or NWIS. I've mostly done this using R functions in the dataRetrieval package put out by USGS.

Of course, method 3 is the best way to do this. APIs are the best way for machines to talk to each other (e.g. my computer's R application talking to a USGS data server) without error-prone humans getting involved. APIs are all over the place on the internet and their ubiquity is only increasing. But I'm not always happy with the formatting of the results I get from WQP, at least as dataRetrieval returns them. 

Today I'm exploring another service I've been aware of for a while, but that I haven't bothered to look into, mostly because I didn't feel the need. That service is the [CUAHSI HydroClient](http://data.cuahsi.org/), which gives web-based access to CUAHSI's hydrologic information system. 

CUAHSI has been instrumental in developing the waterML (and waterML2) markup language for storing hydrologic data and relevant metadata. All I know at the moment is it's an extension of xml (the x is for "extensible", after all) and that it's NOT what WQP uses (they use [WQX-Outbound schema](http://www.waterqualitydata.us/schemas/WQX-Outbound/2_0/docs/index.html) [That's the link I got at the website, and it appears to be broken, very much true to form for EPA web pages]). Also I dataRetrieval does interface with waterML in some capacity; at least it contains functions called `importWaterML1` and `importWaterML2`. CUAHSI also mentions an R package, WaterML in the same section as HydroClient. I'm going to check that out now. 


```r
# install.packages("WaterML")
library(WaterML)
```

Looking under the hood: what's this package contain?


```r
# ??WaterML
ls("package:WaterML")
```

```
##  [1] "AddMethods"                  "AddSites"                   
##  [3] "AddSources"                  "AddValues"                  
##  [5] "AddVariables"                "GetServices"                
##  [7] "GetSiteInfo"                 "GetSites"                   
##  [9] "GetValues"                   "GetVariables"               
## [11] "HISCentral_GetSeriesCatalog" "HISCentral_GetSites"        
## [13] "MakeSOAPEnvelope"            "WaterMLVersion"             
## [15] "WaterOneFlowNamespace"       "WaterOneFlowVersion"
```

Oh look, they have a vignette!


```r
vignette("WaterML-Tutorial")
```

It references a recent article in Ecological Informatics. That's promising. 

...

So I just read the paper, and while it's somewhat enlightening as to the various services CUAHSI has to offer, I'm still confused what this offers that dataRetrieval does not, aside from the ability to upload data. The paper talks about "simplifying access to HydroServer data through the WaterOneFlow web service from within the R environment." So the next question I have is, how does the HydroServer data differ from the data available via NWIS and WQP? But that's a question for another day.




