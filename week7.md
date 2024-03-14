# geom99log
This is the repository for the items in the course Advanced Web design and implementation. Excecuting the weekly checklist in the course item.

This is not a time sheet but a activity log which described the process which I was doing in this labs.

Week 7 annd 8 Checklist: 

A - Creating a Spreadsheet with the time log to calculate the total time I spent on each completing item in the academic checklist.
  1 - Open a Microsoft Excel sheet and divide the coloumns for the subject, Date, Time, Activity Description for what you have done, possible outcomes that is what you have learned from the items, Next steps, Productive hours for the hours that you have worked on, Refferences.
    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/111ae533-fce1-4d5d-a5f9-71d9e8a50dbd)
  2 - Assign the cells with their respective data types that is for date its date type and time its time data type. This can be done by right click on the whole cells in the top and select format cells to select the respective data type in the menu given. This is set for the excel types for the
    ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/12ba7309-cbd6-4497-b54d-2c2a2043b016)

  Referrence: ```https://www.mindtools.com/a52felv/activity-logs```


B - Starting a ArcGIS server in the Google Cloud Platform.

Firstly Thanks for Google cloud Platform Team to give the accademic credits to the students for the educational purpose.

For this Google credits we have requested this google credits previously in our labs. 

Steps:
  1 - Initially set the account type to educational account so that the billing goes on that account. Click the Compute engine in the side bar and navigate through the VM instances in the below picture and enable the education account first and then the           Virtual Machine later.
  
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/2dd2ed97-6c53-4371-8dda-a2fa17990663)

  2 - Open google cloud console and enable CGP Compute Engine API (if not already enabled). This is what will be used to create the virtual machine (Virtual Machine).
  3 - Then give the VM a name and proceed further for the setting the location for our server, in this instance we will be creating the server in Iowa in America. 
  ```https://www.google.com/maps/place//@41.2200251,-95.8718679,15z?entry=ttu```
  4 - For machine configuration we will use the defaults. This sets the “size” of the virtual machine, also we can allocate more CPU if wanted but for this project we only want 8 GB ram CPU to run our server as this is the requirement for the ESRI products in                 the server.
  Note : If you want to use higher end CPU that is higher Ram more than 8 GB stated above it costs more depending upon the requirement.
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/008f9bbe-1001-4ed3-9900-d2df4e675cf2)
  5 - we'll opt for Windows systems despite the premium charge associated with Microsoft Windows Server. The selected image is customized with ArcGIS Server already installed and set up on a Windows Server. Click "Change" to locate the image provided by the instructors, that is in his server Shawn's ArcGIS server.
  6 - Next step would be enabling the firewall for both http and https, this allows the server pre installed to work.
  7 - This would be the final step in creating a GCP VM server, now create the server, this may take few minutes to create and this is were the google cloud platform starts to charge you.
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/5872cbc1-76cb-4eca-bb8a-ae220ad8942c) 
  Start or resume will be the function to start or stop the virtual machine. After starting the virtual machine set the username and password so that no other could operate that server pottentially. (Click on Set windows password)
  For the username you can give any name of your preference but for the student account I am providing the username as student and the password will be generated by their own so copy paste that in your secured place. We can also change the username and password if needed (means Forgot those).
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/8a6fa9c0-baaa-492a-bdd4-827d20878a32)

  Change the firewall rules : As this is a fleming hosted server this is internally blocked by the IT team for any pottential security reasons, The default uses 3389 but it is blocked. The image is specifically prepared to listen through the port 444, so we should         change that port to configure that into the Fleming system.
![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/b05cacad-e070-402b-b69a-7124400cde93) 
Click Set up firewall rules > Create firewall > Provide the name as instructed in the instruction > click on all instances in targets so that It applied for all the VM created in my account > For source IP filter change those into your own computer IP address (just google whatsmyip to get yours) > paste that IP in your source IP ranges > In protocols and ports change the TCP port to 444 > Create this rule.

  Changing the firewall rule for the ArcGIS servers that is specifically 6443 and 6080.
  1 - Create a new rule and name that as you wish.
  2 - Same as the above process select all instance and specify the port 6443 and 6080 which is for the ArcGIS ports as this is restricted by the default Google.
  

  Once the Server is started in the windows menu search "remote desktop connection" for the created server to run 
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/d9fe0504-53c6-40c1-bfbf-48567ae70e33)

  Specify the external IP address which is in the server that was turned on.
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/f637a657-e7a5-40d8-b8d3-9b9468e8de30)
  Note: Specify the port :444 at the ending of the external IP address and login with the credentials because we prompted it to work like that.

  Then it will ask for the credentials which you have created using the windows password creator, enter those credentials by selecting the more options choice.
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/6d3a5d29-7ede-4930-a6b9-9fdab5817258)

  This will come up with a popup give yes to proceed. We have a VM running in the background. (Use it wisely or else it would cost much) 
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/eb831fd0-a68e-4a3a-b300-331b12d42069)

  Setting up the firewall in the VM:
  1 - There is a firewall in default with the windows VM so we have to give access for the ArcGIS ports so that it can refer the data present in the Server.
  2 - In search menu type "Windows defender firewall with advanced security" 
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/b94e959a-f4d1-42a0-8eb0-a4cc513e29b0)
  3 - In the inboud rule create a new rule 
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/2f930bfd-11fb-4078-9e5b-98e8e752cafb)

  4 - Specify the port corresponding to the ArcGIS server.
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/136dfd65-8171-4b27-bf16-e0eca4001d7d)

  5 - Name them as you wish and leave everything default
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/d0903de0-26de-40d7-b5b8-b3ba57eb0d04)

  Optionally creating the DNS port for our temporary IP address.

  1 - Go to ```https://www.duckdns.org/domains``` choose your suitable name for your server which is not taken by someonelse. 
  ![image](https://github.com/rahulsaravanabavan/geom99log/assets/142858065/93c2814c-c375-40d8-a96b-caf292e3ddee)
  2 - Update your External IP address in that your IP address and then its done your own domain for your temporary IP address has been created.
  Mine was rsaravan.duckdns.org


  Your ArcGIS server is Ready for the use Now copy the data from the local computer and paste it in the VM so that it is in your server locally and you can refer that data in the web server.

  Publishing the Canada Map in ArcGIS Online (AGOL) 

  1 - Create a Project file in pro and add server connection. 
  
  2 - Paste your url from the DuckDNS followed by /arcgis and give the credentials as instructed in the D2L.
  
  3 - Then refer your folder in your server for the map to display and publish that in your server.
  
  4 - To get your Rest end point add rest/services and you will be prompted for the Manager access, first you will be prompted as insecure connection then go to advanced settings and type "thisisunsafe" you will       be viewing your files as a manager in your own server.
  
  5 - The above process is whether to check that your folder is published in your server or not. If the folder is displayed then your folder is published correctly.

  6 - Get that ArcGIS rest service url to publish the canada map in the AGOL, in the content page > New content > Add URL > Then Name the map and describe the map in description > Then publish the map.


  Note: The map is displayed in the AGOL only if the server is running or else it wont get the data to be displayed as the data is refered from the VM.



  





  

  
