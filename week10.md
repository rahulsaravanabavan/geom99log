This log is created for the weekly checklist items in our course web design to satisfy the academic credits.
This log is for week 10 group project items, and the group project is developing a Lindsay transit map.

Week 10:
On the lab on Friday we met Our instructor, we as a group had an idea to use the JS API to route the transit and the frequency of those using. But our instructor suggested us to use the various technologies that would be compatible within ESRI suit as we will be working
on that in future, so our scope of the project changed from coding the routes to minimal coding required project. Since the timeline for the project were also quite tensed, this was a better idea to move forward.

We had the updated GFTS dataset collected from the fellow members of the college from other course who was doing network analysis with this data set.


On that lab I personally created a map in AGOL with the stops added to that. After that I had to make a group so that I was accessible to others to edit within the group. So, I created a group in AGOL and gave access to all the add and edit the existing files in that folder.


After that we as a group decided to split the parts and parcel of the project to efficiently work on each task assigned to the individuals. Finally we decided that I will do the analysis part in ArcGIS since the raw dataset has some works to do with ArcGIS Pro environment. Those methodologies as follows.


Reference:```https://www.youtube.com/watch?v=AEC37x04tcw&list=PLGZUzt4E4O2KQz9IxGKrEyKB8rA0UVx1W&index=1&ab_channel=ArcGIS```

Understanding GFTS:

• Generalized transit feed specification is the general form for transit data along the world which includes stops, schedules, routes (shape). My dataset contains, trips, stops, stop times, shapes, routes, feed info, calendar dates, agency, all these in txt file.

• The preprocessing includes converting the point features such as stops and routes to their respective features. 

• Pro environment has a toolbox specific to transit data that is Public transit toolbox. Firstly converted stops.txt file to stops in map. Followed by converting the shapes to line features representing the routes. This was executed by GFTS stops to features and GFTS shapes to features tools respectively.

Methodology:

1. GFTS stops to features: From the stops text file converting the point features as stops in the pro environment. These are the updated stops as per 2023.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/85a7c4ba-3414-4e8d-bc74-8911bbaf4e00)

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/83fee5ae-3d49-4e4f-a5a8-9bfde2256041)

2.	GTFS shapes to Features: Converting the shape text file to their corresponding line feature that is route features and segregating them into 4 transit routes, since Lindsay has 4 routes namely green, red, orange, blue.

   ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/f6883348-025c-4fd8-8f72-484012f590da)

   ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/c0da563d-0414-48c7-8673-bd9cab33693f)

  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/b630af5d-b149-4f7d-866d-4f9d850d0d5a)


3.	Creating a new Geodatabase and new feature dataset to store the next process that is GFTS data model in that dataset.
   
   ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/82e5a986-f24b-4745-82b1-1a6e00740c88)

   ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/cf38fc2f-f417-4ac2-a960-d831b69a5649)

4.	GFTS to public transit data model: This is a specific model the ESRI has for processing the transit data to convert them into the data preferred by them. This helps in further processing the to catch the buffer area and analysing the extent of each stops.

   ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/b8efa180-133c-4d47-8384-bc8231aee8b9)

5.  I checked the interpolate blank stop times because if there was any blank stop but the busses fly over them, we can use the stop so that we are not missing any stops in this area.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/cb7cfe5e-415d-4aad-ad71-9e35201b28aa)

    This is the final output of the model generated, from here we are going to process the data model further to suit the data that is going to be imported in the AGOL.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/b3ed24b7-f8e4-4041-9051-9a33f7d29884)

6. 	Creating a service area layer and add the stops and routes to that:

   ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/cf3f297e-0e44-4abf-9c4f-8a98f9d5e5f5)

Create a service area network analysis from the analysis ribbon > network analysis tab > Service area 
-	The service area is a container that normally contains the input and output data which is used for the analysis to run without hassle.
  
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/000583fd-4617-41bb-9cc0-95c109cae66e)

  The facilities are the input and the polygons are the output.

  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/bf7c2c6e-877a-42a4-8cc6-31e91d193d6c)

  I am selecting the walking distance because, this is going to calculate the walking distance to the stops that is quarter KM to each stops and making a buffer so that if I turn on the location services this could show me the nearby stop associated with this.

  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/501b7d7a-cf99-458a-b95c-87e9b8d82fc4)

  Since, this is a pedestrian level analysis I am going with high level precision so that it will give me the greatest level of details.

  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/182300e5-e063-4670-affe-50d939511a77)

  Now, I am going to import the facilities that is the stops 

  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/c715e0e3-6b6b-4923-b7ce-d28cb69a8712)

  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/7af61e30-3d1c-4506-be47-bd5eaecffc3d)


  The stops have been added to the facilities next will be running the tool.

  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/f9eae8c9-09f7-466c-80ee-6e2c0ab755d3)

  These are the areas that could use the transit within 0.4 km buffer area. These are the area reachable within 0.4 km in reach for the people to access each stops.

 7. Enrich tool: Next step will be using the enrich tool to populate the polygon data with the population data.
    
    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/0fe38d4c-3004-4eff-997a-f433d881f3e2)

    This is done because to compare the data with the population data which ESRI has (consumes credits) to show the audience about the density of the people living there for each stops.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/1da66f71-edf5-4567-bc32-c8b14b4895a2)

    Since our focus is to populate the population data I am populating the ESRI population data for popup feature in the AGOL.

    Click variables > The demographic variables that I care about is the population data > so I am going to select that.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/f83e847e-4b89-4565-9fe7-66c3efd63502)

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/32a5a773-65d7-45a0-b353-1db7be16d01a)

8. After this we have extracted the polygon area with the population data with it, so we can throw this data into AGOL and develop a popup and use that feature for indicating the stops and the population data along the nearby stop.

   ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/8b5a8d3f-a45d-4aac-8d3f-40256cac6e2d)

9.	Calculate transit function frequency: This tool calculates the frequency of the transit bus, that is how frequent is the buss service in that stop, since Lindsay we have only one hour once bus service.
10.	While calculating the frequency hours I have to insert parameters that is 60 minutes interval since Lindsay transit stops frequency operates one hour once.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/a7177711-74d6-43ad-8753-bdad838ee26d)

    This method failed and produced 0 services in that area.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/1562a6e7-7f5c-47b2-a98e-4b1bf615e05d)

    Then tried to generate the frequency for the bus stops it also produced the same results.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/967bb703-303c-468d-a1b0-c8d75d792275)

    With the given amount of pre-processing I have decided to not to go further with this analysis, because this is a web course and the instructor has allowed pre-processing only around 2 hours in pro environment.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/60e74dd2-9017-46f7-b593-02df5ad81470)

    The next steps will be uploading the pre-processed data in AGOL and presenting it into the map.
   	
   	![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/6d6a304e-afb8-4765-8caa-49071f6b1f3f)


12. Since there are 2 stops that is associated with every routes, means those two stops will have buss service throughout the area, I am checking the separate counts by transit line.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/e1ae5761-2750-4db3-9423-390bc66c4df9)

    I think this tool failed because of the prefix I did there is no AMRush in Lindsay transit stop so deleting that and running the tool again to see the possible outcomes.
    
    Sharing the data to AGOL, as far as I completed the process and I have reached the time limit for this processing so uploading each layers in to AGOL.
    
    Right click each layer > sharing > share as a web layer.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/fb3c0846-6875-43a0-a11f-daa96a517d4b)

    There will be a common error while uploading the layers that will be assigning the unique numeric ID’s so before clicking the publish click analyse and click on Auto assign numeric ID to assign number by the pro itself. Then publish that as a web layer.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/b64c8271-cf1d-4272-a43f-6007b3da4292)

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/c0fbaa45-ac84-4703-b2d2-fff936f2e405)

    Opening the these data in the AGOL and adding them to the Lindsay Stops map.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/16371f2b-7f44-447c-b21f-76f1613bf965)

    Browse the content in the AGOL, select the Lindsay stop map that was created during the last lab, select add layers and add all the layers that were uploaded in the AGOL.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/56ff6cb0-dea7-4636-b0f2-0187b76db15f)

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/198a3ae9-972b-4d83-a9a5-cfb2403a9a0a)

    This is the final map after loading the processed items in the pro environment and some data layers like service area are not uploading into the AGOL. That was showing the file not supported format.

    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/6720bd3f-874f-4fc0-8b4a-fa7acb68628e)

    While uploading a lyr file from the local disk it was showing file not supported. 


































