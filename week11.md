Week 11 Log 

This log is submitted in the partial requirement for the Team project that is Lindsay transit application.

Creating a Template:
• Create a experience builder using the ArcGIS online component from the menu button Click the experience builder app.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/20757a83-1604-4ea5-8a08-d1d7d7677529)

• Create a new Experience builder using the create new button in the right side.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/f80177ec-2402-4634-96ef-f90f2cfa1f83)

• There will be a whole lot of web page regarding to create a new one choose wisely for the application of your interest. In my case we are creating a Transit application for Lindsay, so this application should be Map centric.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/d6b5abd4-74d8-4919-8e33-067727503472)

• In this I am selecting the route feature with the experience builder as it may help with the stops and routing in the area.

• Click create to create that template and then play around it to get familiarize with the widgets and the features along with that.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/e5f53999-0e54-4c2d-9eda-961474770a2c)


• This is the first view of the application built using this template edited the topic/ label name that is Lindsay Transit.

• Enabling the locate and layer features in the sidebar from the map settings in the right hand side. The locate features can help people in locating them to the bus stops and the layer feature can help us in adding the respective layers.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/4f61a306-982e-41ba-9e12-7c234549ad49)

• Enabling the popup feature as I am planning to enable the popup feature for the bus stops and timings if the bus had left the stop then next bus timing will be switched.

Add data: 
• Add data from the select map tab in the right hand side after clicking on the map in the center screen, this enables users to add data from the either ArcGIS online or local database.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/a4661962-f31b-4d62-8177-672150eb6a65)

• I am adding the stops to the template I am creating, this data was uploaded by Sharmila from our group.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/6ff4eba0-96fa-4276-bb8b-e9ae68254616)

• After adding the data, the template showed the stops and routes of the Lindsay transit in the application.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/64efc984-b421-4758-8260-eaadd650ae19)

• By selecting the routing utility in the right hand side a routing facility panel will show up in the navigation bar. I am going to try and add data to that for stops and routing service.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/36192529-9f17-4219-be3f-f02069acbbde)

• Trying out the where clause in the Blue stops csv to add any stops to the search window.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/911bf942-23e8-4997-897d-103173717ee7)

• Added the Blue bus timing in the AGOL as the feature layer as CSV can only be added as feature layer.

• Adding that CSV as the timelines for the Experience builder in the timeline widget, hope it works.

• ArcGIS online Is not recognizing the CSV as it doesn’t contain any geographic attributes, and so the Experience builder.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/66cc3595-22fc-4565-badf-17d8c74d8ef9)

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/f47cba8b-4844-4fb7-ba85-832fee135b79)


Adding the Stops in the tables list:

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/ec6082ed-d08a-478c-b026-a3ee15284db5)

• Drag and drop the tables widget and time line widget from the side bar and add the data.

• For adding the data in the right hand side there will be new sheet> add data> data published in the AGOL.

Note: Only if the data is added in the AGOL you can access in the Experience builder.

• Adding the table view for every stop, in this layer in a drop down menu.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/49489b17-bd46-4234-b7d9-f7ac9e480eeb)

• Added every stop to the table view and made this as a drop down menu.

• Edit the viewable fields in the table view by clicking the eye icon to unselect the items.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/437fc127-9f5f-452c-bc54-235072be99ee)

• Edit the table view for each stop.

Creating the directions Widget:

• From the side bar select the directions widget and add that to the map layer.

• Select the routing facility in that so that user could search for the place and nearby locations.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/1efa8f06-4467-431d-85bc-510dc7dce06e)

• Published the Application for testing purpose and can edit in future for any addition in the template.


Adding Triger functionality to the template:

• Adding trigger functionality for the data to show only green stops if green table pops up.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/ea845be5-594d-49f2-ab14-0ee92c9fe328)

• Initially, I set the trigger fields as address and stop ID if the stop ID has crossed by the buss it should disappear.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/e4c6cfd7-bc66-4cdd-a9fc-07aefc38352b)

• Trying out this feature to test that out. Published the template and checking this feature whether it works.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/d6e43451-5c46-43b1-a733-95e029901200)

• The service routes were also not visible in my case. Should try any other methods to solve this problem.

• The trigger function was also not working and I was not able to make this work. I should try some other methodology to make this work.

```https://experience.arcgis.com/experience/2c270ac78cf940e78812bc452c8ad672#data_s=id%3AdataSource_1-18e6dfb3775-layer-8%3A2```

The template is available in this link.







