## Background

In 2018, requests to the Strategic Science Planning and Program Integrity division within DFO Maritimes to identify and summarize the available DFO and non-DFO datasets were becoming increasingly frequent. Born out of frustration and a need for swift and effective approaches, a team of self-proclaimed Strategic Reproducible Analytical Pipeline (RAP) Champions was formed to automate the creation of these Reports. The primary objective of this initiative has been to develop a web-based tool to generate Reproducible Reports to identify and describe DFO and non-DFO datasets within a user-defined area. Specifically, we address internal requests that support processes that provide frequent and standardized advice, such as CSAS, Aquaculture Siting Responses, and Environmental Response, which typically focus on Species at Risk. We have encountered multiple challenges regarding data storage, access, and duplication of effort; therefore, a broad, secondary objective has been to spearhead discussions within DFO to advance reproducible workflows and improve data management practices, aligned with Open Government mandates to make information more accessible to everyone (PCO 2018; DFO 2020a; Gomez et al. 2021;
SCC 2021). This technical report provides an overview of the work done so far to create this Spatial Reproducible Reporting Tool including a description of the workflow and code, lessons learned, and future directions. We present a snapshot of the progress made in the hopes that
these efforts, while fulfilling a specific reporting need, will also facilitate increased collaboration and reproducibility in monitoring and research relevant to decision-making within DFO.

### Notes
R package [csasdown](https://github.com/pbs-assess/csasdown) was
recently developed by members of DFO’s Pacific Region to facilitate the
creation of reproducible CSAS documents using **R Markdown** and
**bookdown**. The package also includes scripts for generating
reproducible DFO technical reports (see [Guide for the production of
Fisheries and Oceans Canada science report
series](https://publications.gc.ca/site/eng/9.874714/publication.html)
for more information)

In an attempt to follow reproducible data practices, we used the **csasdown** R package for the creation of this Technical Report.



## Collaborative Workflow - Suggestions for reviewers as to how review this technical report via GitHub
•	Branch from main (e.g., from main create and checkout a new branch: git checkout -b my_dev_branch or in RStudio)
•	Do work in branch, e.g., addressing issues, comments, suggestions.
•	Add and commit changes.
•	Routinely Push work to the remote version of my_dev_branch: git push -u origin my_dev_branch
•	Routinely Pull (i.e., git fetch + git merge) from origin/main to deal with any conflicts git pull origin main
•	Once the original issue is fixed, ensure the report can still be generated 
•	If everything still runs correctly, make a pull request from GitHub website to merge my_dev_branch into main.
•	Authors will then respond to the request and test out the code in their dev branches to make sure there are no issues.
•	Once all lights are green, the pull request will be accepted and the new code merged into main branch. This will finalize the code review.
