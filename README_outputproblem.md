ST558 Project 1
================
Tao Sun
2020-06-08

# **JSON data description**

**JSON** (JavaScript Object Notation) is a lightweight and flexible data
format that is easy for humans to read and for machines to parse. JSON
has become a common format used in:

  - Public APIs (e.g., Twitter)
  - NoSQL databases as a document format (e.g., MongoDB)
  - Relational databases as a new column type (e.g., PostgreSQL)

JSON format is text only and independent to any programming language, so
it is a good way to store data.

[Wikipedia introduction](https://en.wikipedia.org/wiki/JSON) and [JSON
syntax introduction](http://json.org/).

# **Ways to read JSON data into R**

There three major R packages available for reading JSON data into R
(rjson, RJSONIO and jsonlite). Examples to compare behavior and
performance of those three packages are
[here](https://rstudio-pubs-static.s3.amazonaws.com/31702_9c22e3d1a0c44968a4a1f9656f1800ab.html).
I prefer jsonlite because it provides more options for manipulating the
format and most importantly we can get well formatted data by default.

# **Access NHL records ‘Franchise’ API and pulldown JSON data**

Function used to pull down “Francise” records.

Pull down data.

# **Exploratory data analysis**

<!--html_preserve-->

<div id="htmlwidget-3ec778fb060ca780d006" class="datatables html-widget" style="width:100%;height:auto;">

</div>

<script type="application/json" data-for="htmlwidget-3ec778fb060ca780d006">{"x":{"filter":"none","caption":"<caption>Current NHL teams<\/caption>","data":[[1,5,6,10,11,12,14,15,16,17,18,19,20,21,22,23,24,25,26,27,28,29,30,31,32,33,34,35,36,37,38],[19171918,19171918,19241925,19261927,19261927,19261927,19671968,19671968,19671968,19671968,19671968,19701971,19701971,19721973,19721973,19741975,19741975,19791980,19791980,19791980,19791980,19911992,19921993,19921993,19931994,19931994,19981999,19992000,20002001,20002001,20172018],["Canadiens","Maple Leafs","Bruins","Rangers","Blackhawks","Red Wings","Kings","Stars","Flyers","Penguins","Blues","Sabres","Canucks","Flames","Islanders","Devils","Capitals","Oilers","Hurricanes","Avalanche","Coyotes","Sharks","Senators","Lightning","Ducks","Panthers","Predators","Jets","Blue Jackets","Wild","Golden Knights"],["Montréal","Toronto","Boston","New York","Chicago","Detroit","Los Angeles","Dallas","Philadelphia","Pittsburgh","St. Louis","Buffalo","Vancouver","Calgary","New York","New Jersey","Washington","Edmonton","Carolina","Colorado","Arizona","San Jose","Ottawa","Tampa Bay","Anaheim","Florida","Nashville","Winnipeg","Columbus","Minnesota","Vegas"]],"container":"<table class=\"display\">\n  <thead>\n    <tr>\n      <th>Franchise ID<\/th>\n      <th>First Season<\/th>\n      <th>Team Name<\/th>\n      <th>Team City<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"columnDefs":[{"className":"dt-right","targets":[0,1]}],"order":[],"autoWidth":false,"orderClasses":false}},"evals":[],"jsHooks":[]}</script>

<!--/html_preserve-->

# **The team with highest winning ratio in NHL history**

All records of number of games a team played and wined was retrieved and
ploted as below. all the teams seems have very similar winning ratios,
except team “Montréal Canadiens”(\#1) showed extraordinary winning rate
in both regular season and playoffs. Interestingly, team “Edmonton
Oilers”(\#25) has much better performance in playoffs than in the
regular seasons.

![](ST558_Project_1_files/figure-gfm/unnamed-chunk-2-1.png)<!-- -->

We can also see this from below two tables. Montréal Canadiens has the
highest wining ratio among teams who played more than 2500 games. Again,
Edmonton Oilers’s wining ratio is much higher in playoffs than in
regular seasons.

<!--html_preserve-->

<div id="htmlwidget-2e59dc8abb38ae921c15" class="datatables html-widget" style="width:100%;height:auto;">

</div>

<script type="application/json" data-for="htmlwidget-2e59dc8abb38ae921c15">{"x":{"filter":"none","caption":"<caption>Winning rato in regular seasons<\/caption>","data":[["Vegas Golden Knights","Dallas Stars","Montréal Canadiens","Winnipeg Jets","Philadelphia Flyers","Colorado Avalanche","Boston Bruins","Nashville Predators","Minnesota Wild","Ottawa Senators (1917)","New Jersey Devils","Washington Capitals","Calgary Flames","Anaheim Ducks","San Jose Sharks","Toronto St. Patricks","Buffalo Sabres","Detroit Red Wings","St. Louis Blues","Pittsburgh Penguins","Carolina Hurricanes","Edmonton Oilers","Phoenix Coyotes","Toronto Arenas","New York Islanders","New York Rangers","Ottawa Senators","Toronto Maple Leafs","Tampa Bay Lightning","Columbus Blue Jackets","Montreal Maroons","Chicago Blackhawks","Florida Panthers","Vancouver Canucks","Los Angeles Kings","Atlanta Flames","Quebec Nordiques","Arizona Coyotes","Atlanta Thrashers","Winnipeg Jets (1979)","Hartford Whalers","Minnesota North Stars","Hamilton Tigers","Detroit Falcons","Detroit Cougars","Brooklyn Americans","Pittsburgh Pirates","New York Americans","Oakland Seals","Cleveland Barons","California Golden Seals","Colorado Rockies","St. Louis Eagles","Montreal Wanderers","Quebec Bulldogs","Kansas City Scouts","Philadelphia Quakers"],[38,15,1,35,16,27,6,34,37,3,23,24,21,32,29,5,19,12,18,17,26,25,28,5,22,10,30,5,31,36,7,11,33,20,14,21,27,28,35,28,26,15,4,12,12,8,9,8,13,13,13,23,3,2,4,23,9],[235,2053,6731,693,4115,1922,6570,1675,1511,542,2937,3577,3098,2055,2218,230,3889,6237,4117,4115,1756,3179,1360,40,3732,6504,2139,6460,2138,1512,622,6504,2053,3889,4116,636,1256,480,902,1338,1420,2062,126,92,176,48,212,736,226,160,472,480,48,6,24,160,44],[133,1061,3449,352,2054,968,3208,821,724,258,1375,1664,1471,973,1049,109,1790,2872,1902,1866,791,1434,615,18,1656,2856,948,2838,949,660,271,2788,852,1626,1733,268,497,190,342,506,534,758,47,34,64,16,67,239,66,47,116,113,11,1,4,27,4],[0.57,0.52,0.51,0.51,0.5,0.5,0.49,0.49,0.48,0.48,0.47,0.47,0.47,0.47,0.47,0.47,0.46,0.46,0.46,0.45,0.45,0.45,0.45,0.45,0.44,0.44,0.44,0.44,0.44,0.44,0.44,0.43,0.42,0.42,0.42,0.42,0.4,0.4,0.38,0.38,0.38,0.37,0.37,0.37,0.36,0.33,0.32,0.32,0.29,0.29,0.25,0.24,0.23,0.17,0.17,0.17,0.09]],"container":"<table class=\"display\">\n  <thead>\n    <tr>\n      <th> <\/th>\n      <th>Franchise ID<\/th>\n      <th>Team Name<\/th>\n      <th>Number of games played<\/th>\n      <th>Number of games wined<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"columnDefs":[{"className":"dt-right","targets":[1,2,3,4]},{"orderable":false,"targets":0}],"order":[],"autoWidth":false,"orderClasses":false}},"evals":[],"jsHooks":[]}</script>

<!--/html_preserve-->

<!--html_preserve-->

<div id="htmlwidget-8a6b0f7b93407e01c462" class="datatables html-widget" style="width:100%;height:auto;">

</div>

<script type="application/json" data-for="htmlwidget-8a6b0f7b93407e01c462">{"x":{"filter":"none","caption":"<caption>Winning rato in regular seasons<\/caption>","data":[["Edmonton Oilers","Vegas Golden Knights","Montréal Canadiens","Toronto Arenas","Colorado Avalanche","Anaheim Ducks","New York Islanders","Pittsburgh Penguins","New Jersey Devils","Carolina Hurricanes","Tampa Bay Lightning","Detroit Red Wings","Dallas Stars","Philadelphia Flyers","Boston Bruins","Chicago Blackhawks","San Jose Sharks","Buffalo Sabres","Ottawa Senators","Toronto Maple Leafs","Washington Capitals","Minnesota North Stars","New York Rangers","Nashville Predators","St. Louis Blues","Calgary Flames","Vancouver Canucks","Los Angeles Kings","Quebec Nordiques","Ottawa Senators (1917)","Florida Panthers","Winnipeg Jets","Montreal Maroons","Phoenix Coyotes","Hartford Whalers","Minnesota Wild","Toronto St. Patricks","Columbus Blue Jackets","New York Americans","Winnipeg Jets (1979)","Oakland Seals","Pittsburgh Pirates","Atlanta Flames","Atlanta Thrashers","Colorado Rockies","Detroit Cougars","Detroit Falcons"],[25,38,1,5,27,32,22,17,23,26,31,12,15,16,6,11,29,19,30,5,24,15,10,34,18,21,20,14,27,3,33,35,7,28,26,37,5,36,8,28,13,9,21,35,23,12,12],[264,27,749,7,194,162,272,381,257,93,137,618,173,433,651,539,241,256,151,533,282,166,515,111,391,211,229,255,80,41,44,27,50,57,49,73,11,31,18,62,11,4,17,4,2,2,2],[159,16,429,4,109,89,148,206,137,49,73,325,90,221,321,264,119,124,72,254,135,80,244,51,180,98,101,111,35,18,18,11,20,22,18,26,4,11,6,19,3,1,2,0,0,0,0],[0.6,0.59,0.57,0.57,0.56,0.55,0.54,0.54,0.53,0.53,0.53,0.53,0.52,0.51,0.49,0.49,0.49,0.48,0.48,0.48,0.48,0.48,0.47,0.46,0.46,0.46,0.44,0.44,0.44,0.44,0.41,0.41,0.4,0.39,0.37,0.36,0.36,0.35,0.33,0.31,0.27,0.25,0.12,0,0,0,0]],"container":"<table class=\"display\">\n  <thead>\n    <tr>\n      <th> <\/th>\n      <th>Franchise ID<\/th>\n      <th>Team Name<\/th>\n      <th>Number of games played<\/th>\n      <th>Number of games wined<\/th>\n    <\/tr>\n  <\/thead>\n<\/table>","options":{"columnDefs":[{"className":"dt-right","targets":[1,2,3,4]},{"orderable":false,"targets":0}],"order":[],"autoWidth":false,"orderClasses":false}},"evals":[],"jsHooks":[]}</script>

<!--/html_preserve-->

# **Further check Montreal Canadiens team’s plalyers in each position**

## The former and active players in each position.

Seems that Montreal Canadiens need more player on the right wing
position.

|                | Center | Defence | Left Wing | Right Wing |
| -------------- | -----: | ------: | --------: | ---------: |
| Former player  |    178 |     218 |       165 |        163 |
| Current player |     17 |      27 |        12 |          8 |

## Who is the active player got highest average scores/season in the team.

Tomas Tatar is the player in the team who got the highest average
scores/season. Max Pacioretty is definitely the super star in the team
who performed so well in the past 10 seasons.

    ## # A tibble: 64 x 4
    ##    Name              seasons points AvergePoints
    ##    <chr>               <int>  <int>        <dbl>
    ##  1 Tomas Tatar             2    119         59.5
    ##  2 Max Domi                2    116         58  
    ##  3 Alexander Radulov       1     54         54  
    ##  4 Max Pacioretty         10    448         44.8
    ##  5 Alex Galchenyuk         6    255         42.5
    ##  6 Brendan Gallagher       8    334         41.8
    ##  7 Nick Suzuki             1     41         41  
    ##  8 P.K. Subban             7    278         39.7
    ##  9 Jonathan Drouin         3    114         38  
    ## 10 Phillip Danault         5    170         34  
    ## # ... with 54 more rows
