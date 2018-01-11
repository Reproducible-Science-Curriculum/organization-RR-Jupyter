---
title: "Modifying data"
teaching: 10
exercises: 0
questions:
- "What are the pitfalls of modifying data by hand?"
- "How do you document modifications that have been made?"
- "How should you begin and structure the data cleaning process?"
objectives:
- "Understand the importance of separating raw and cleaned data."
- "Motivate the use of automated cleaning methods over by-hand methods."
- "Give intuition for structuring the cleaning process and keeping track of metadata."
keypoints:
- "Raw data should always be in its own folder."
- "Cleaned data should have its own README if any manual cleaning was performed."
- "Any modification should have a clear paper trail."
- "Using GUIs for modifying data often has unexpected results."

---
## Cleaning data by hand
Now that we've created a README for our data, it's time to begin the cleaning process. Open the data file in `01_cleaning` using Excel (Or if you prefer a text editor, [here is the tab-delimited version]({{ page.root }}/data/gapminderDataFiveYear_superDirty.txt)). Let's take a look at the current state of our data, and find some parts of it worth cleaning.

> ## Review the data
> Open the file, and find a few problems with the data
{: .callout}

As you can see, this data is messy. We can fix various mistakes, fill in missing values, etc. However, how can we remember what has been done? How do we know what's different between this data file and our raw data?

## Recording our actions

Since we've use a GUI editor in order to make these modifications manually, we must also record our actions manually with a README file. READMEs are useful for giving a person context about the data contained within a folder. In this case, the context we wish to give are the steps that have been taken in order to create this cleaned dataset.


> ## Create a README
> Create a new file called `README.md` in the `01_cleaning` directory with a text editor, and make a line for each set of modifications that has been made.
{: .callout}

## Pitfalls of manually cleaning data

You might think that this is a pretty labor-intensive process. Maybe you're even questioning the value of writing each of these steps down manually. It's true - recording each modification by hand is time-consuming. It's also easy to forget steps, mis-represent what you've done, and generally poorly convey the true state of the data. For this reason, it's much preferred to use a *script* to automate the cleaning of your data. We'll cover this in the next section.

Another challenge with using GUIs is that they tend to have different ways of doing the same thing. For example, bring up the `Save As` menu in the editor that you're using. You might notice that there are many options for saving this data on top of simply specifying a file name and location. In addition, some GUIs have different labels for each row / column. Excel begins its rows at `1`, while python begins its rows with `0`. It is important to record all information about the program used to modify the data, as well as any considerations that should be taken when interpreting the cleaned data.

> ## Good, Better, Best
> * **Good** Re-name your modified data, clean it in a `cleaning` folder, and export to `cleaned`
> * **Better** Keep a README in each folder that describes the background and any modifications made to the data
> * **Best** Automate your cleaning process with a commented script that also serves as a record of all modifications made.
{: .checklist}
