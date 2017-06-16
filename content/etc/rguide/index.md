---
layout: page
title: "rguide"
date: "2016-02-10"
comments: true
sharing: true
footer: true
---


It's not as though there is any shortage of resources for getting started with R. Nonetheless, none of the existing guides do things exactly my way, so one more can't possibly hurt. Here is my own step-by-step guide to getting started with R, to be updated as I find the time.

## Why use R?

There are a few reasons why R is often the language of choice for academic research. 

1. It's free and open-source. No need to petition your advisor for an expensive license. 
2. It has a huge user base, so getting help is never difficult. If you get stuck on something, an answer can usually be found via google or stackexchange. Also a lot of your peers will be using it, so you can reach out to them as well.
3. It's a great skill to have on a resume. More and more employers are using R for data analysis. 

### A little more about R

R is first and foremost a language for *statistical computing*. It was created by statisticians with data analysis in mind. This is contrary to other languages like MATLAB (designed for numerical modeling and matrix operations) and Python (designed to be a general-use object-oriented language). R can be used for other purposes, but it may not be the best choice. But since R plays nice with lower-level languages like C, C++, and FORTRAN, there are lots of R libraries that extend its capabilites beyond mere statistics. 


## Get the absolute essentials

1. [Download R](https://cran.r-project.org/mirrors.html)
2. [Download RStudio Desktop](https://www.rstudio.com/products/rstudio/download/)

RStudio is an IDE (Integrated Development Environment) designed specifically to work with R and make your coding more pleasant. Like R, it is free and open-source. RStudio will not work without R! They are separate things.

Once you have those things, you should be able to get started using R. Also check out the great resources RStudio (the company, not the software) has for learning R ([link](https://www.rstudio.com/resources/training/online-learning/#R)). 

## Organize your projects. 

RStudio has a great feature that it calls a *project*, which makes certain aspects of using R much easier, particularly file navigation. It also all but forces you into the good habit of keeping all your files for an analysis project (code, data, graphs, etc.) in a single folder, along with the .Rproj project file. [More on RStudio projects](https://support.rstudio.com/hc/en-us/articles/200526207-Using-Projects)

There is, of course, a lot more to be said about project organization and good organization practices in general. This is still something I'm trying to improve in my own work, 3 years after starting with R. I've seen many ideas for what best-practice looks like, and I've settled on the organizational structure used in the [ProjectTemplate](http://projecttemplate.net/) package. I would say that RStudio projects are essential; ProjectTemplate structuring is not. The important thing is that you learn to organize your projects consistenly. ProjectTemplate is just one way to do this, but it's a tried and true method and has a pretty modest learning curve.

## Back up your work and use version control

The code you write is likely to take on a life of its own, growing and changing as you improve upon it. Unfortunately, this will sometimes cause your code to break, and you might want to keep a record of the changes you make. Version control is the way to do this. Like code documentation, version control is just good coding practice, especially when you are collaborating with others (but even when you are not).

These days the most popular tool for version control is [Git](https://git-scm.com/). The good news is that it is very powerful and widely used. The bad news is that it will take some time to learn. But it is well worth it. I am certainly not equipped to provide a Git tutorial; many exist online (like [this one](https://try.github.io/levels/1/challenges/1)!).

A separate (but related) tool for version control is [GitHub](https://github.com/). Git is a software package for doing version control; GitHub is a place for storing the versions and collaborating on code. It's built specifically with Git in mind. Beyond this functionality, GitHub has become something of a social network for coders. 

While learning Git can be daunting, RStudio has some simple tools to do basic Git versioning and Github interfacing. [Read more about that here](https://support.rstudio.com/hc/en-us/articles/200532077-Version-Control-with-Git-and-SVN) and [here](http://r-pkgs.had.co.nz/git.html).

## Write good code

3. Understand the basics of R scripts. 
5. Comment your code. 
4. Understand the relationship between objects, functions, vectors, data.frames
5. Understand R packages
6. Know where to get help

Advanced

1. RMarkdown and knitr
    - tools within RStudio
    - integration with LaTeX
  

Modeling

1. Understand the difference between training, validation, and test data