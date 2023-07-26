# How to Update

This website *and* the file `cv.pdf` both compile information sequestered in the `data` folder. 

To make updates, begin by opening the project via `kathryn-q-grace.Rproj`. Then: 

  1. add information to one or more of the `data` files (see below)
  2. type `quarto render` in the RStudio **Terminal** 
  3. push the results to GitHub (the website hosted on Netlify will update automatically)

## List of `data` files 

  - `publications.bib` - please note that this BibTex file helps to sort publications under 4 different headings in `cv.pdf`. **You must add new entries with one of the following options in the "category" field:** 
  
    * refereed
    * conference papers 
    * conference posters 
    * talks 
    * other 
- `people.csv` - includes fields for each collaborator's name, position, professional website, and *path to an avatar image* (displayed at the bottom of the Home page). Please note that:

  * the path to each avatar should be relative to the `images` folder (e.g. "nina.png")
  * if no path is specified, the default image `avatar.png` will be used as a placeholder
- `grants.csv` 
- `appointments.csv` 
- `additional_training.csv`
- `cv.css` - includes any special styling needed for `cd.pdf` 
- `cv.rmd` - **please do not knit this file directly**, as it is automatically sourced when you run `quarto render` (we want the CV and website to remain in sync)