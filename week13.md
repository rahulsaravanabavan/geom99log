This log is created for the weekly checklist items in our course web design to satisfy the academic credits. This log is for week 13 group project items, and the group project is developing a Lindsay transit map.

Technical Log Week 13:
• This week While testing the template, it showed that you don’t have access to enable the routes features in the Experience builder.
• It also consumed some credits for providing the access but also didn’t work. 

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/e9f34df7-8e09-4a34-8958-1e59ace9c4dd)

• The next steps would be rearranging the widgets and presenting them in a pleasing way.
• Should add the trigger to the data model and should read about that feature in detail.

Reference: ```https://www.youtube.com/watch?v=xHp1dGoogIk&ab_channel=GeospatialTrainingServices```

Joining the Routes data to the stop ID:

• By using the power query in Excel combining the two tables data with stop ID as the primary key to load those data into the AGOL, so that separate stops can project separate routes according to that.


![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/5c705f58-d0d4-460c-b8e4-05ea151ae047)

• From the data ribbon select the tables/range option and select the tables which your going to merge.

• Then select the attributes which your going to import in the tables.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/0b7d0541-4514-43e5-9c27-af810f6632fc)

• Matchin these two fields. 

• This is going to add a field of that table name, in our case that is stops ID from that we can select which field to add into that table.

• After that select close and load.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/653344ec-b259-486c-a128-c858c6891c7c)

Publishing this CSV as a feature layer in AGOL:

• Creating this Excel as a CSV and exporting that to the ArcGIS online as a feature layer which has times associated with the bus stops.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/64d8d5f3-952b-4b1e-90cd-b6ab8b868cc1)

• Deleting the route finder since that doesn’t work well and required sign in each time. 

• Adding the legend to the Map interface, showing all the routes and stops.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/1f8e778b-3056-4ac2-abe7-90161288f5ff)

• Adding the stops CSV to the experience builder and arranging them in the order to show which one should be useful for the user.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/e9e98a63-19e9-4adf-8b95-554885995564)

• I have selected the stops, Time and latitude and longitude of the stops so that I can add any type of trigger options for that data.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/98163fc8-4756-476a-90c9-3d9ebd0ae525)

• Added the search filter for the stops name alone for the user to search the stops they are in and they can find the timing of the bus route.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/92ecaf15-54b3-4aa8-ae4a-deeba53c8034)

• Going to add a trigger option for the map extent to show the data within its extent, add trigger and alter the map extent framework.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/5f796d8a-6d73-46d4-95ba-e7c5cb4b68bf)

• This trigger option worked, and showed only the stop and its buss routes after zooming into the map extent.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/12a185eb-331a-4edd-a91a-3facfdcdae43)

• This can be done by selecting the trigger > extent changes > Framework > then choose the data table you want and then set the trigger to map extent by enabling the feature map extent.

Modifying the User Interface:

• Changing the title of the published template as “Lindsay Mobility” this is the name adopted by the municipality for the transit here in Lindsay. So, it would make more sense that this also has the same name.


![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/ae642ec3-0b12-401c-b5e5-688cd65bf2c1)

• Providing intuitive design and trying out different fonts and styles for the title. Changed the font to Calibri, as that is the font adopted by San Serif and has a cleaner letterforms and lacks blunting.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/f7cd03fc-a0cc-4829-a1f8-71156f8881ca)

• Changed the background of the Lindsay Mobility to brighter colour.

• Changing the name of each lines and stop such as Green_stop as Green stop so that it could reflect the legend represented.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/aa8aadac-7c8e-4449-a6bf-0418c751a6d1)

• This is done by the data icon in the left hand side bar and modify the name of each layer.

Adding a Near me widget:

• This Near me widget facilitates the user end with the table view of what’s near by them.

• As I have mentioned before in week 9 I have enabled the location so that users can see their own location in the map, along with that I going to try out the Near me widget so that it can show the near by stops.

• I have also planned to enable the navigation icons so that it can navigate them to the stops.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/f75e1361-0da3-4209-8541-03a3dc0e499f)

 • Adding the near me widget from the sidebar.

 ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/e956b866-a999-423e-8979-7a1d5e8ca20b)

 • Setting the map for the near me widget and adding the table and data to show in that. 
 
• Changing the name of the near me widget as “stops near me”.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/a35652d5-2574-4324-87b9-5b6aac4b9d56)

• Then specified the units as Meters and directed the application to a search radius of 400 meters for testing purpose.

• Then click on add analysis tab to set the stops from the data we have imported.

• Adding each stop to the proximity list, so that every stop can be represented in the near me widget.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/24412deb-4ad6-495c-ba1a-246d11669877)


• The end product would look like this.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/4bf4a092-aaac-44bc-a7b8-0ebae308c9c7)

• It shows the exact list of the stops available near by caused by the location.

![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/f7ce72e1-3d33-49dd-85e8-1850b34f3fe2)

• Disabled the line and polygon feature in the near me widget for the location service to impact the widget and get the stops from the location of the user.



This is the final template for this week please review through this.
```https://experience.arcgis.com/experience/2c270ac78cf940e78812bc452c8ad672/```





