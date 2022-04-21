### Background

This technical report provides an overview of the work to create a Spatial Reproducible Reporting Tool, created by a team of self-proclaimed Strategic Reproducible Analytical Pipelines (RAP) Champions, formed within the Strategic Science Programming and Integrity Division of DFO Maritimes. 

This Technical Report including a description of the workflow and code, lessons learned, and future directions. We present a snapshot of the progress made in the hopes that these efforts, while fulfilling a specific reporting need, will also facilitate increased collaboration and reproducibility in monitoring and research relevant to decision-making within DFO.


### Notes
This Technical Report was created using the R package [csasdown](https://github.com/pbs-assess/csasdown),  developed by members of DFO’s Pacific Region to facilitate the creation of reproducible CSAS documents and Technical Reports using **R Markdown** and **bookdown**. In an attempt to follow reproducible data practices, we used the **csasdown** R package for the creation of this Technical Report.

The code for the Spatial Reproducible Reporting Tool mentioned throughout this Technical Report is available [here] (https://github.com/dfo-mar-odis/shinySpatialApp)

### How to run this Technical Report:
We recommend using [RStudio](https://rstudio.com) as the integrated development environment (IDE). If the user is using Windows then it is highly recommended to also install [Rtools](https://cran.r-project.org/bin/windows/Rtools/), which are tools to compile R packages from source; a feature that is occasionally required.




### Collaborative Workflow 
Suggestions for reviewers as to how review this technical report via GitHub:

* Branch from main (e.g., from main create and checkout a new branch: git checkout -b my_dev_branch or in RStudio)
* Do work in branch, e.g., addressing issues, comments, suggestions.
* Add and commit changes.
* Routinely Push work to the remote version of my_dev_branch: git push -u origin my_dev_branch
* Routinely Pull (i.e., git fetch + git merge) from origin/main to deal with any conflicts git pull origin main
* Once the original issue is fixed, ensure the report can still be generated 
* If everything still runs correctly, make a pull request from GitHub website to merge my_dev_branch into main.
* Authors will then respond to the request and test out the code in their dev branches to make sure there are no issues.
* Once all lights are green, the pull request will be accepted and the new code merged into main branch. This will finalize the code review.
