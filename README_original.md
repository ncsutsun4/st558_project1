# ST558 Project 1
Creating a vignette and a blog post

Project description:
   You are going to create a vignette for reading and summarizing a JSON data set. You’ll contact the National Hockey League (NHL) API. The components that must be present in each vignette include:
    
  - Describe Json data. 
  - Discuss the possible packages/functions taht are available for reading JSON data into R. (Choose 1 of 3)
  - Write function to contact the NHL records "Franchise" API  (https://gitlab.com/dword4/nhlapi/-/blob/master/records-api.md) and return data
    * /franchise(Retuns id, firstSeasonID and lastSeasonID and names of every team in history)
    * /franchise-team-totals (Returns Total stats for every franchise (ex: roadTies, roadWins, etc.))
    * /site/api/franchise-season-records?cayenneExp=franchiseId=ID (Drill-down into season records for a specific franchise)
      - User should be able to specify the franchise
    * /franchise-goalie-records?cayenneExp=franchiseId=ID (Goalie records for the specified franchise)
      - User should be able to specify the franchise
    * /franchise-skater-records?cayenneExp=franchiseId=ID (Skater records, same interaction as goalie endpoint)
      - User should be able to specify the franchise
  
  - Perform basic exploratory data analysis. (graphs and discussion)
    * Create new variables
    * Create contingency tables and numeric summaries by some categorical variables
    * Create some plots
  
  - Code chunks should be shown in the final document (except setup chuncks)
  
Blog Post and RepoStuff

  - on the project repo - go into settings and enable github pages.
  - knit .rmd with output style (output: rmakedown::github_document) in the YAML header
  - rename it to README.md
  - write a blot : what woudl you do differetly
      - what was the moset difficult part for you?
      - what are your big  take-away from this project.
      
  
