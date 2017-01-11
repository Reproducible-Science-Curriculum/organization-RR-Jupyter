---
title: "Project Structure"
teaching: 0
exercises: 0
questions:
- "How can you organize a project so it makes sense to your future self?"
objectives:
- "Recognize the difference between raw and modified data"
- "Document the life history of a file as is gets modified"
- "Associate file history with directory structure and explain why it is important to make apparent in project"
keypoints:
- "Raw data remains raw and should never be modified"
- "For something to be reproducible every step needs to be written down"
- "Clearly label the file for future you and collaborators"
- "Use folder and sub-folders to illustrate the history of the files in your project"
---

Here are some characteristics of files that you want to pay attention to
1. File history
2. File function
3. File format
4. File origin

We will start thinking about how to capture these characteristics using folders and simple naming schemes.

## Activity: Sanity-check the data

Let's take a look at the data in Excel before we start working on it. Does everything look correct?   

![Screenshot]()

**Discuss with your partner:** Are we sure that we everything is correct by just looking at the file in excel?
Should we fix any of the problems we see in this file? Why or why not?

-  No, keep original data forever unchanged.

There should always be a copy of the data in its most raw state. Never make correction the orignal data file. There are several ways to ensure that the original data stays unchanged. 

What if we were to change this file?

-  Yes,

Is it obvious how to go back to the original state of the file?

- save date stamp.
- the cell is a different color.
- compare with original.
- someone wrote down exactly what was changed.  

Clearly label the file or make the location for the file that makes sense to future you and collaborators.

## How to structure your project folders

The most important way to delineate file types and organize the workflow of your project is to design your file structure at the very start of your projects history. Often you do not know exactly where your project will lead, so it is okay if your intitial design evolves as the project does. There are a few standards that we will walk through that are applied to most projects.  

Create a folder that will house all your projects and call it `projects`.

```
projects/
```

Now let's make a folder within that folder for our new project, called `gapminder`:

```
projects/
    gapminder/
```

Since we have data, we want to create a data folder.

```
projects/
    gapminder/
        data/
```

Since we have this Excel spreadsheet as our original, raw data, we will save it in a folder called `00_raw` to indicate that it is the starting point for our project. Create a subfolder in `data/` called `00_raw` and put the `asdf.xlsx` file there. Now you should have a folder structure that looks like this:

```
projects/
    gapminder/
        data/
            00_raw/
                asdf.xlsx
```


Since we want to change something in this file, we will create a *new* folder in `data/` that shows that it is different from `00_raw/`, and we will call it `01_cleaning/`. Make a subfolder in `data/` called `01_cleaning/` and put a copy of the `asdf.xlsx` file there. Then, make an *empty* subfolder called `02_cleaned` in the `data/` folder.

```
projects/
    gapminder/
        data/
            00_raw/
                asdf.xlsx
            01_cleaning/
                asdf.xlsx
            02_cleaned/
```


At this point we are able to capture most of the characteristics of data file, the file function, file type, file history, and format. In addition there is a clear understanding of how to proceed to data cleaning.  Often there are more ways you need to define the project characteristics that you can't fit in the file name or folder structure, for example file origin.  A common solution to the more detailed information on the file and the entire project is metadata. 

Stay tuned for the exciting next episode: Metadata, your projects 

## Tips and Tricks

- Consider making your data readonly, so you do not inadvertantly change the file.
    