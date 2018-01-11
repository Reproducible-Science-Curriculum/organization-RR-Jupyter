# organization-RR-Jupyter
Data and project organization for Reproducible Research with the Jupyter notebook curriculum

Link to extensive notes on the creation to this lesson: [Data-project-org-brainstorm](https://docs.google.com/document/d/1d3Cv4b31xskUVz60Y72VeOspg2rnBKeVZ2yV9o7bt9U/edit?usp=sharing)

## Content generation steps

For certain parts, content needs to be re-generated from the source after
you change the source. _The goal is that this happen automatically through
continuous integration ([Travis CI](https://travis-ci.org)) in the future,
but currently it needs to be done manually._

### Slides

After modifying slides in the form of a Jupyter Notebook in the `slides/`
directory, run the following command. (You must have Jupyter (and GNU Make)
installed for this to work.)

```sh
$ make lesson-ipynb
```

