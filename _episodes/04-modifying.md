---
title: "Modifying data"
teaching: 5
exercises: 10
questions:
- "What are the pitfalls of modifying data by hand?"
- "How do you document modifications that have been made?"
- "How should you structure the data cleaning process?"
objectives:
- "Understand the importance of separating raw and cleaned data."
- "Motivate the use of automated cleaning methods over by-hand methods."
- "Give intuition for structuring the cleaning process and keeping track of metadata."
keypoints:
- "Cleaned data should have its own README if any manual cleaning was performed."
- "Any modification should have a clear paper trail."
- "Using GUIs for modifying data often has unexpected results."
- "Using GUIs for cleaning up data seems quick, but doing it with even only a modicum of reproducibility becomes laborious fast."
---

# Activity: Sanity-check the data

Let's take a look at the data in Excel before we start working on it. (You can download the data in Excel format.) Does everything look correct?

![Screenshot]({{ page.root }}/fig/gapminderDataFiveYear_superDirty-screenshot.png)

> ## Discuss with your partner
>
> [Download the file]({{ page.root }}/data/gapminderDataFiveYear_superDirty.xlsx) and open in Excel if you want to inspect it using a local copy. Review, and find a few problems with the data.
{: .challenge}

As you can see, this data is messy. We can fix various mistakes, fill in missing values, etc. However, how can we remember what has been done? How do we know what's different between this data file and our raw data?

> ## Should we fix any of the problems we see in this file? Why or why not?
>
> No, keep original data forever unchanged.
>
> There should always be a copy of the data in its most raw state. Never make corrections to the original data file. There are several ways to ensure that the original data stays unchanged.
{: .discussion}

What if we were to change this file?

- Changes made by hand (in GUI applications) are incredibly hard to track. Some tools are better than others, but this is outside our control.
- If we changed our only copy of the raw data, we may never be able to reproduce what we did.
- We want to track **exactly** what changed in the file, and if we must do it by hand, we should make that easy to see.

> ## Some ideas to detect changes:
>
> - Include the date stamp in the file name
>     * `2017-03-15_01_dleehr-fixes_gapminderDataFiveYear_superDirty.xlsx`
> - Color the changed cells to highlight the changes
> - Side-by-side comparison with original
> - Record exact changes in a README file.
>
> Which one would at least be a _good_ or _better_ way?
{: .discussion}

> ## Create a README
> Open or create a `README.md` for documenting the data cleaning operations with a text editor.
> * In which directory would this best be placed?
> * Write a line for each set of modifications that should be (or has been) made, documenting the change.
{: .challenge}

# Pitfalls of manually cleaning data

You might think that this is a pretty labor-intensive process. Maybe you're even questioning the value of writing each of these steps down manually. It's true - recording each modification by hand is time-consuming. It's also easy to forget steps, mis-represent what you've done, and generally poorly convey the true state of the data. For this reason, it's much preferred to use a *script* to automate the cleaning of your data. We'll cover this in the next section.

Another challenge with using GUIs is that they tend to have different ways of doing the same thing. For example, bring up the `Save As` menu in the editor that you're using. You might notice that there are many options for saving this data on top of simply specifying a file name and location. In addition, some GUIs have different labels for each row / column. Excel begins its rows at `1`, while python begins its rows with `0`. It is important to record all information about the program used to modify the data, as well as any considerations that should be taken when interpreting the cleaned data.

> ## Good, Better, Best
> * **Good** Re-name your modified data. Use separate folders for collecting the resulting (data) files, named to indicate the step or status of their files (e.g., `cleaning`; or `01_cleaning`, `02_cleaning`, etc; `cleaned`).
> * **Better** Keep a README in each folder that describes the background and any modifications made to the data
> * **Best** Automate your cleaning process with a commented script that also serves as a record of all modifications made.
{: .checklist}
