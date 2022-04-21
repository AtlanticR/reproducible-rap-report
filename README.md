### Background

This Technical Report provides an overview of the work involved in creating a Spatial Reproducible Reporting Tool, which generates automated reports to enable data-discovery of DFO and non-DFO information within the Maritimes region. This Reporting Tool was created by a team of self-proclaimed Strategic Reproducible Analytical Pipelines (RAP) Champions, formed within the Strategic Science Programming and Integrity Division of DFO Maritimes. This Technical Report therefore including a description of the workflow and code to create this Reporting Tool, lessons learned, and future directions.

### Notes
This Technical Report was created using the R package [csasdown](https://github.com/pbs-assess/csasdown), developed by members of DFO’s Pacific Region. *csasdown* facilitates the creation of reproducible Canadian Science Advisory Secretariat (CSAS) documents and Technical Reports using **R Markdown** and **bookdown**. In an attempt to follow reproducible data practices, we therefore used **csasdown** for the creation of this Technical Report. Guidelines for creating Technical Reports and other DFO science report series are available [here](https://publications.gc.ca/site/eng/9.874714/publication.html).

The code for the Spatial Reproducible Reporting Tool mentioned throughout this Technical Report is available from: <https://github.com/dfo-mar-odis/shinySpatialApp>

### Installation:
We recommend using [RStudio](https://rstudio.com) as the integrated development environment (IDE). If the user is using Windows, then it is highly recommended to also install [Rtools](https://cran.r-project.org/bin/windows/Rtools/), which are tools to compile R packages from source; a feature that is occasionally required.

Run the following commands to install the **remotes** and **csasdown** packages. The **remotes** package allows you to install remote repositories (i.e., from GitHub). This may take some time to load.

``` r
> install.packages("remotes")
> remotes::install_github("pbs-assess/csasdown")
``` 
Next, install the version of LaTeX that will be used to generate the PDF version of the report. This wiki page provides instructions for installing LaTeX for use with **csasdown**: <https://github.com/pbs-assess/csasdown/wiki/Latex-Installation-for-csasdown> This might also take some time to load. Click "Yes" to any pop-up windows that may appear.

``` r
> tinytex::install_tinytex()
```

This work uses the **renv** package to track all of the additional R packages required to create the Technical Report. One of the useful functions of **renv** is being able to see if your environment has changed; i.e., it is out of sync with the lockfile (a text file storing information about the packages that have been installed in the environment). 

To check if the environment is out of sync, execute the `renv::status`
command below. You will see that the project is synced with the
lockfile.

``` r
> renv::status()
* The project is already synchronized with the lockfile.
```

If new packages are installed, Use 'renv::snapshot()' to add these packages to the lockfile, and save the current state of the project.


### Collaborative Workflow 
Suggestions for reviewers as to how review this Technical Report via GitHub:

1. Branch from main (e.g., from main create and checkout a new branch: `git checkout -b my_dev_branch` or in RStudio)

2. Do work in branch, e.g., addressing some issue.

3. Add and commit changes.

4. Routinely Push work to the remote version of `my_dev_branch`: `git push -u origin my_dev_branch`

5. Routinely Pull (i.e. git fetch + git merge) from origin/main to deal with any conflicts `git pull origin main`

6. Once the original issue is fixed, ensure the report can still be generated through the app and that the test suite passes: `testthat::test_local()`

7. If everything still runs correctly, make a pull request from GitHub website to merge `my_dev_branch` into `main`.

8.  Other developers will then respond to the request and test out the code in their dev branches to make sure there are no issues.

9.  Once all lights are green, the pull request will be accepted and the new code merged into main branch.