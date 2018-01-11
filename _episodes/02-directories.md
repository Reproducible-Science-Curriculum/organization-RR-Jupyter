---
title: "Project Structure"
teaching: 10
exercises: 10
questions:
- "How can you organize a project so it makes sense to your future self?"
- "What are some useful file naming strategies?"
- "Why and for what should we use README files?"
- "How do you document modifications that have been made?"
objectives:
- "Recognize the difference between origjnal and modified data"
- "Record modifications to data as they get made"
- "Describe cardinal rules for structuring a project directory hierarchy to promote future reproducibility"
- "Describe patterns for naming files in project directories to promote future reproducibility"
- "Describe the purpose of including README files with your project."
keypoints:
- "Organize and name files so that they make intuitive sense to your future self, and follow the narrative of the data analysis."
- "Populate folders with README files that describe the project and gives context for the analyses."
- "Original/raw data remains original and should never be modified."
- "Keep a clear record of every modification that has been made. Ideally, this is in the form of a script that can automatically generate cleaned data from the raw data."
- "Generated files (processed data, figures, etc) should not be intermingled in the same directory as files that must be backed up."
- "For something to be reproducible as a whole every step needs to be reproducible."
---

# How to structure project folders and name files

Here are some characteristics of files that you should pay attention to

1. File history
2. File function
3. File format
4. File origin

We will start by thinking about how to capture these characteristics using folders and simple naming schemes.

* [**Project organization slides**]({{ page.root }}/slides/02_slideshow_organization.slides.html)

# Putting it into practice

![files]({{ page.root }}/fig//organization_case_study.png)

> ## Exercise
>
> Pair up with someone next to you, spend 5-10 minutes looking at the provided example project folder and answer these questions:
>
> - What features help you understand what the project is about?
> - What features are useful for creating a reproducible pipeline?
> - What features help you understand the relationship of the individual files to each other?
> - What features do you find most useful to help organize your projects?
>
> After discussing with your partner, share one or two of the most salient points with the room.
>
{: .challenge}

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
