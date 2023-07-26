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

## Website details 

This website is built with [Quarto](https://quarto.org/docs/reference/projects/websites.html) and stylized with the files `styles.scss` and `_quarto.yml`. 

The site consist of four pages, each built with a different `.qmd` file:

  - `index.qmd` builds the homepage. Please note that: 
    
    * the div class `hero-heading` references the "hero" banner (avatar & welcome message) at the top of the page 
    * the div class `stripe` toggles the pink background used in alternating sections 
    * the div class `proj` arranges projects and featured publications in a flex-box with a featured image on the right 
    * the div class `people` arranges avatars at the bottom of the page in a flex-box with customized styling for round-shaped avatar images 
    * featured publications are *not* automatically updated when new publications are added to `publications.bib` - this allows you to customize the featured text and images by editing `index.qmd` 
    * `styles.scss` includes a mobile query that rearranges flex-boxes for layout on small screens 
    
  - `publications.qmd` *only* features publications in `publications.bib` where `category = "refereed"` 
  - `about.qmd` is text-only 
  - `teaching.qmd` is text-only 

