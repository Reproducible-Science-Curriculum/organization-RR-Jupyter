---
title: "Concluding thoughts"
teaching: 5
exercises: 0
questions:
- "How do you organize data to encourage reproducibility across different projects?"
- "How do you record the origin and history of data?"
- "How do build up a project that can be understood by yourself or others in the future?"
objectives:
- "Design and justify the directory structure and file naming for your project"
- "Describe two ways to maintain the integrity of raw data"
keypoints:
- "Organize files so that they make intuitive sense and follow the narrative of the data analysis."
- "Populate folders with metadata that describes the folder contents, where those contents came from, and gives context for the analyses that you're about to perform."
- "Always make copies of data for modification, and never over-write the raw data."
- "Keep a clear record of every modification that has been made. Ideally, this is in the form of a script that can automatically generate cleaned data from the raw data."
- "If manual cleaning is necessary, create a README file that details every single change that has been made, such that a newcomer could re-create these changes."

---
## Completing our project directory

Now that we've finished cleaning our data, it's time to move on to exploring the data. For this, we'll need some scripts. Since we anticipate writing a lot of code to analyze this data, we'll create another root-level folder called `code`. We'll keep all analysis scripts in here.

Finally, we'll also want to create some outputs from this project, perhaps in the form of figures or a document that summarizes our work. As such, we'll create the following folders in the root-level:

1. `output` will store results of any analysis. These may be statistics we've calculated, the results of fitting a model, or features extracted from the cleaned data.
2. `doc` will contain any documents we are generating from this data. It could contain a [LaTeX](https://www.latex-project.org/about/) document for a manuscript we're prepping for publication.

Now that our folder is ready to go, it's time to start getting our hands dirty with the data. This will be covered in the next module.

## The value of record keeping

Most data needs to be cleaned, re-organized, or otherwise prepared for subsequent data analysis. In order to do this reproducibly and effectively. When beginning a new project or analyzing new data, always remember these lessons.
