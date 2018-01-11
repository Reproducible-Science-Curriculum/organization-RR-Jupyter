---
layout: page
title: "Instructor Notes"
permalink: /guide/
---

## Overview

The heart of this lesson is episode 02, project organization and file naming. That episode consists primarily of two parts:
1. Activity 
2. Lesson

## Activity

One of the main functions of this activity is to provide an icebreaker for the group.  Allow them to laugh at the demo files, identify with bad habits, and share strategies on how their organize their projects.  

### Take Aways

- Every person organizes their files differently 
- Everyone has organization strategies that cause problems for themselves
- Everyone has creative ways to solve these problems 

## Slide Show

Make sure you regenerate (and commit) the HTML version of the slides if you modify the source Juputer Notebook. See the top-level `README`.

### To run slideshow locally

You can also serve the slides locally from your (the instructor's) computer. In a shell terminal run the following:

~~~
$ jupyter nbconvert --to slides 02_slideshow_organization.ipynb --post serve
~~~
{: .source}

You must be in the directory that contains slideshows (`slides/`).

## Timing and modifications

As noted above, the heart of the lesson is episode 02. The following modifications to the sequence of episodes allow shortening the total time required by 15-20 minutes:
- You can discuss the value of README files in essence as part of episode 02, i.e., without a separate exercise in creating and populating a README file (which is otherwis part of episode 03).
- Within the full curriculum for the Reproducible Science using Jupyter Notebooks workshop, Episode 04 ("Modifying Data") is largely covered in the [Data Exploration](https://reproducible-science-curriculum.github.io/data-exploration-RR-Jupyter/) lesson, so should probably be skipped here (except for the major points that modifications never be made to the original data).
