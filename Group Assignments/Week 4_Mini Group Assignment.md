# Mini Group Assignment: Week 4 Status Updated

## Parks and Public Transit in LA County
[Project proposal](https://github.com/ashley-yao/up206a-groupProject/blob/main/Group%20Assignments/ProjectProposal.md)

### Roles 
* **Public Issues Officer** Katrina is taking the lead on developing the overarching project goal and identifying what factors we need to consider in our analysis.
* **Chief Transit Officer** Ashley is taking the lead on identifying the transit stops of interest and developing a process for calculating travel time on transit.

### Status update
Feeling pretty good still
A little concerned about scope, but feel like our methodology is working

**Ashley:** I'm a little worried about how to upload the data from the Metro website if needed. Hopefully, future coursework will help with problem solving this. 

**Katrina:** As we talked about during office hours, figuring out the right scope for this project has been a little challenging. The lab on isochrones brought that challenge up for me again (see concerns section below). Overall, though, mapping out demographics by census tract and isochrones around central points has made me feel that our project will be achievable. 

### Data update: 

**Ashley:**: In addition to the data listed in our original proposal, we will be adding OSMnx data to build walksheds around the parks.
**Katrina:**: In addition to the data we listed in our original proposal, we will be adding maps to represent LA County demographics by census tract: specifically, race, income, and education level. 

### Concerns

Number of parks + park entrances/exits
Identifying transit stops around parks

**Ashley:** I think we'll have to address the location points in the isochrones using the entrances and exits. My concern with this is that we'll end up having several maps and have to figure out how to combine them for even an individual park. I think once we've accomplished this for one park it will be replicable for the other parks. Major concern is time. I think my minor concern is if there is a way to consider or generalize which groups we feel are most impacted in the end results, but that's a bridge we'll cross when we get there. 

**Katrina:** Doing the lab on isochrones and testing out some new isochrones on my own has brought up a few concerns. 
* Major concern: 
  * Many of the parks that we're mapping only lie within a single neighborhood area (as mapped by OSMnx), but LA as a whole is too large to be used as the map area. I'm still texting out different neighborhoods to see if there's a way to get around this.
* Minor concerns: 
  * I realized that we couldn't use the center point of a park as the center for each isochrone; since we selected regional recreation parks, most of them are very large, and the entirety of the isochrone could theoretically be contained within a park. This made me realize we would need to identify entrances to the parks and build isochrones around each entrance instead. This seems very feasible, just a little more time-consuming than I'd realized. 
  * In order to visually represent differential transportation access to parks by census tract, we'll need to develop benchmarks corresponding to different levels of transit access to parks (ex. 5 or more bus/train stops that connect to parks; 2 to 4 bus/train stops; 1 or no bus/trains stops) and assign them to each census tracts. This also seems feasible but time-consuming!
