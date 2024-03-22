This log is created for the weekly checklist items in our course web design to satisfy the academic credits.
This log is for week 10 group project items, and the group project is developing a Lindsay transit map.

Week 10:
On the lab on Friday we met Our instructor, we as a group had an idea to use the JS API to route the transit and the frequency of those using. But our instructor suggested us to use the various technologies that would be compatible within ESRI suit as we will be working on that in future, so our scope of the project changed from coding the routes to minimal coding required project. Since the timeline for the project were also quite tensed, this was a better idea to move forward.
We had the updated GFTS dataset collected from the fellow members of the college from other course who was doing network analysis with this data set.
On that lab I personally created a map in AGOL with the stops added to that. After that I had to make a group so that I was accessible to others to edit within the group. So, I created a group in AGOL and gave access to all the add and edit the existing files in that folder.
After that we as a group decided to split the parts and parcel of the project to efficiently work on each task assigned to the individuals. Finally we decided that I will do the analysis part in ArcGIS since the raw dataset has some works to do with ArcGIS Pro environment. Those methodologies as follows.
Reference: https://www.youtube.com/watch?v=AEC37x04tcw&list=PLGZUzt4E4O2KQz9IxGKrEyKB8rA0UVx1W&index=1&ab_channel=ArcGIS
Understanding GFTS:
• Generalized transit feed specification is the general form for transit data along the world which includes stops, schedules, routes (shape). My dataset contains, trips, stops, stop times, shapes, routes, feed info, calendar dates, agency, all these in txt file.
• The preprocessing includes converting the point features such as stops and routes to their respective features. 
• Pro environment has a toolbox specific to transit data that is Public transit toolbox. Firstly converted stops.txt file to stops in map. Followed by converting the shapes to line features representing the routes. This was executed by GFTS stops to features and GFTS shapes to features tools respectively.
