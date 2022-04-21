### Background

This technical report provides an overview of the work to create a Spatial Reproducible Reporting Tool, created by a team of self-proclaimed Strategic Reproducible Analytical Pipelines (RAP) Champions, formed within the Strategic Science Programming and Integrity Division of DFO Maritimes. 

This Technical Report including a description of the workflow and code to create this Reporting Tool, lessons learned, and future directions. We present a snapshot of the progress made in the hopes that these efforts, while fulfilling a specific reporting need, will also facilitate increased collaboration and reproducibility in monitoring and research relevant to decision-making within DFO.

### Notes
This Technical Report was created using the R package [csasdown](https://github.com/pbs-assess/csasdown),  developed by members of DFO’s Pacific Region to facilitate the creation of reproducible Canadian Science Advisory Secretariat (CSAS) documents and Technical Reports using **R Markdown** and **bookdown**. In an attempt to follow reproducible data practices, we therefore used **csasdown** for the creation of this Technical Report. Guidelines for creating Technical Reports are also available [here](https://publications.gc.ca/site/eng/9.874714/publication.html)

The code for the Spatial Reproducible Reporting Tool mentioned throughout this Technical Report is available here: <https://github.com/dfo-mar-odis/shinySpatialApp>

### Installation:
We recommend using [RStudio](https://rstudio.com) as the integrated development environment (IDE).

If the user is using Windows, then it is highly recommended to also install [Rtools](https://cran.r-project.org/bin/windows/Rtools/), which are tools to compile R packages from source; a feature that is occasionally required.

Run the following commands to install the **remotes** and **csasdown** packages. The **remotes** package allows you to install remote repositories (i.e., from GitHub). This may take some time to load.

``` r
> install.packages("remotes")

> remotes::install_github("pbs-assess/csasdown")
``` 
Next, install the version of LaTeX that will be used to generate the PDF version of the report. This wiki page provides instructions for installing LaTeX for use with **csasdown**: <https://github.com/pbs-assess/csasdown/wiki/Latex-Installation-for-csasdown>.

``` r
> tinytex::install_tinytex()
```




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