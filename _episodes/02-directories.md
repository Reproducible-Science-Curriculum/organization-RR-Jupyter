---
title: "Project Structure"
teaching: 10
exercises: 5
questions:
- "How can you organize a project so it makes sense to your future self?"
objectives:
- "Recognize the difference between raw and modified data"
- "Document the life history of a file as it gets modified"
- "Associate file history with directory structure and explain why it is important to make apparent in project"
keypoints:
- "Make it easy to answer the 5 W's"
- "Raw data remains raw and should never be modified"
- "For something to be reproducible every step needs to be written down"
- "Clearly label the file for future you and collaborators"
- "Use folders and sub-folders to illustrate the history of the files in your project"
---

Here are some characteristics of files that you should pay attention to

1. File history
2. File function
3. File format
4. File origin

We will start thinking about how to capture these characteristics using folders and simple naming schemes.

## Activity: Sanity-check the data

Let's take a look at the data in Excel before we start working on it. Does everything look correct?

![Screenshot]({{ page.root }}/assets/img/gapminderDataFiveYear_superDirty-screenshot.png)

**Discuss with your partner:** Are we sure that we everything is correct by just looking at the file in excel?

> ## Should we fix any of the problems we see in this file? Why or why not?
>
> No, keep original data forever unchanged.
>
> There should always be a copy of the data in its most raw state. Never make corrections to the original data file. There are several ways to ensure that the original data stays unchanged.
{: .callout}

What if we were to change this file?

- Changes made by hand (in GUI applications) are incredibly hard to track. Some tools are better than others, but this is outside our control.
- If we changed our only copy of the raw data, we may never be able to reproduce what we did.
- We want to track **exactly** what changed in the file, and if we must do it by hand, we should make that easy to see.

Some ideas to detect changes:

- Include the date stamp in the file name
    - `2017-03-15_01_dleehr-fixes_gapminderDataFiveYear_superDirty.xlsx`
- Color the changed cells to highlight the changes
- Side-by-side comparison with original
- Record exact changes in a README file.

Clearly label the file or make the location for the file that makes sense to future you and collaborators.

## How to structure your project folders

The most important way to delineate file types and organize the workflow of your project is to design your file structure at the very start of your project's history.

Often you do not know exactly where your project will lead, so it is okay if your intitial design evolves as the project does. There are a few standards that we will walk through that work well for most projects.

Create a folder that will house all of your projects and call it `projects`.

```
projects/
```

Now let's make a folder within that folder for our new project, called `gapminder`:

```
projects/
    gapminder/
```

Since we have data, we want to create a `data` folder.

```
projects/
    gapminder/
        data/
```

Since we have this Excel spreadsheet as our original, raw data, we will save it in a folder called `00_raw` to indicate that it is the starting point for our project. Create a subfolder in `data/` called `00_raw` and put the `gapminderDataFiveYear_superDirty.xlsx` file there. Now you should have a folder structure that looks like this:

```
projects/
    gapminder/
        data/
            00_raw/
                gapminderDataFiveYear_superDirty.xlsx
```


Since we want to change something in this file, we will create a *new* folder in `data/` that shows that it is different from `00_raw/`, and we will call it `01_cleaning/`. Make a subfolder in `data/` called `01_cleaning/` and put a copy of the `gapminderDataFiveYear_superDirty.xlsx` file there. Then, make an *empty* subfolder called `02_cleaned` in the `data/` folder.

```
projects/
    gapminder/
        data/
            00_raw/
                gapminderDataFiveYear_superDirty.xlsx
            01_cleaning/
                gapminderDataFiveYear_superDirty.xlsx
            02_cleaned/
```

With this structure, we can capture and communicate most of the characteristics of data as it exsts in our project: history, function, and format. In addition, there is a clear understanding of how to proceed to the next step, data cleaning.

## Why `01_cleaning` and `02_cleaned`?

Realistically, we may not completely **clean** a file in one pass. Sometimes we'll get interrupted, and sometimes we'll catch things later and need to revise the file.

1. Copy the original raw data into `01_cleaning` (e.g. the xlsx file)
2. Edit the file in `01_cleaning`, saving there and recording changes.
3. Export a cleaned version in CSV or Tab-delimited format to `02_cleaned`.

If we catch things later, we
don't put a file in `02_cleaned` until we're done with it. And if we have more cleaning to do, we start from `01_cleaning` and produce a new file in `02_cleaned`.

> ## Tips and Tricks
>
> - Make your raw data read-only, so you cannot inadvertently change the file.
> - Put gnarly incoming data in **quarantine**, then convert, rename, and document.
> - Use ISO 8601 (YYYY-MM-DD) dates at the beginning of data file names to make them sortable
{: .callout}

## Record keeping

There are other characteristics of the data that don't fit into file and directory names, such as the origin of the data. A common solution to keeping this detailed information in the project is adding metadata files. We will cover practices for metadata in the next section.

> ## Good, Better, Best
> * **Good** Separate input, code, and from output using different folders or file names and keep track of all the input->output changes in separate files. Use descriptive file/directory names that convey function and history
> * **Better** Consistent folder structure across projects, ISO 8601 date stamps in file and directory names, read-only raw data
> * **Best** Script to generate folder structures, Version control to track modifications
{: .checklist}
