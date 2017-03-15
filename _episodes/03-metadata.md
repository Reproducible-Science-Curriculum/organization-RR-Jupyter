---
title: "Metadata"
teaching: 10
exercises: 5
questions:
- "Why should we use README files?"
- "What format should README files be in?"
- "What type of information goes into a README file?"
- "When should a README file be updated?"
objectives:
- "Describe the purpose of including README files with your project."
- "Describe common locations for README files."
- "Describe the appropriate level of detail to include in a README."
keypoints:
- "All projects should include a README file in the top directory."
- "README files should include contact points and names of maintainers, date, brief description of the intent of the project, and the source of any data files."
- "Use a README to include changes made over time."
- "README files should be made in a plain text format."
---
## Why READMEs

Every project should describe to users what the purpose of the project is. This is commonly done in a README file. As the starting point for a project the README file is formatted as plain text (or [markdown](https://guides.github.com/features/mastering-markdown/)) to make it easily readable. A README file should include the following information:

- The project name
- The date the README was created
- Contact information for the person(s) who maintains the project
- Three or four sentences about the goal of the project
- If the project uses data from an external source, where the data is from

Think about the beginning of this lesson, when we had nothing but a file with a name. These are the things that would have made it easy to make sense of that data.

So, before we make any modifications to the raw data, we need a practice for how to record the initial state of the data, as well as our modifications.

## Adding a Top Level README

To add a README to our project, open a text editor. For Mac users this can be [BBEdit](http://www.barebones.com/products/bbedit/index.html), [NotePad++](https://notepad-plus-plus.org/) for Windows users.

Now, let's make a README

* Open text editor
* Start writing

~~~
Project name
Today's date
Maintainer's contact info
Data Origin
3-4 sentences about the goal of the project
~~~
{: .source}

* Save as `README` in the project directory.

This file serves as the starting point for future you, or anyone who receives this data.

## Adding a README in a Subdirectory

README files in subdirectories are a good idea too. Often there are many files, and it's distracting to fill the top-level README with details about smaller pieces of the project.

- For raw data directories, you should include the location (e.g URL) where the file was retrieved or generated.
- For modified data directories, you should include the exact tools and steps used to modify the data, along with dates
- For other directories like code or documentation, the README should communicate what the directories contain.

## Keeping the READMEs up-to-date

- Dates are good on file names here
- When changing something in a directory, you should add a line at the README

## Self-documenting Projects

READMEs are commentary on what we consider the "real work", and realistically can be an afterthought. We've all had projects under a deadline or someone asking for a result, and the documentation step is easy to defer until later.

Later never comes, or we forget the details by the time it does. So another good practice is to use good, descriptive names on files, directories, and in code. These are for our benefit, not the computer.

> ## Project README
> `gapminder/README.md`
> ~~~
> gapminder
> =========
>
> ## Project Summary
>
> This project analyzes population-level statistics about many countries to
> determine if there is a relationship between x and y.
>
> Started: 2017-03-15
> Maintainer: Dan Leehr dan.leehr@duke.edu
>
> ## Data Origin
>
> This data is the gapminder dataset, originally collected and published in XXX,
> and retrieved from [1]. The dataset reflects population-level statistics about
> many countries spanning the last several decades.
>
> [1] https://github.com/Reproducible-Science-Curriculum/organization-RR-Jupyter/raw/gh-pages/data/gapminderDataFiveYear_superDirty.xlsx
>
>
> ## Summary of changes
>
> 2017-03-15	dan.leehr@duke.edu	Inherited gapminderDataFiveYear_superDirty.xlsx from Frank Grimes.
> 					Placed raw data in 00_raw.
> 2017-03-15	dan.leehr@duke.edu	Cleaned gapminderDataFiveYear_superDirty.xlsx file in 01_cleaning and
> 					exported to CSV format in 02_cleaned.
> ~~~
> {: .source}
{: .solution}

> ## Good, Better, Best
>
> - **Good** Plain text
> - **Better** Date, name, contact info, short summary, Markdown
> - **Best** Plus history of all changes to the project, checksums
{: .checklist}





