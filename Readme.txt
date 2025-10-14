--------------------------------------------------------------------------------------------------------------
 Server Info Display
--------------------------------------------------------------------------------------------------------------


List page selection:

1: Hidden and Dangerous 2  Full list
2: Hidden and Dangerous 2 Favorites list
3: Custom list 1	
4: Custom list 2
5: Custom list 3



[Join Server]:
Connect to selected server.
*It requires setting Hidden and Dangerous 2 install location in Settings.ini (HD2dir)
*Double-click on selected server also ables to connect.

[Refresh Selected List]
Manual info update for selected server list.


[Refresh] Checkbox
Automatic (Players)info update for selected server.
*Refresh is switched off if different server is selected.


[<>]
Expands GUI Form on the right side to display additional info:

    Requers response text in list.

    Sent bytes, All sent bytes.

    Recieved bytes, All Recieved bytes.
    
    UDP Error description.

	***most common error value: 10054 (offline server / closed port)

	[Export players list]	Saves players list as file.

	[Export full list]		Saves Hidden and Dangerous 2 Full list as file.


--------------------------------------------------------------------------------------------------------------
Custom list:
Files:
Server_List_1.txt
Server_List_2.txt
Server_List_3.txt

List of IP and PORT in format: IP:PORT

192.168.1.143:11001
192.168.1.143:11005



--------------------------------------------------------------------------------------------------------------
 Settings.ini:
--------------------------------------------------------------------------------------------------------------

[Application]
ActivePage=1		Selected page (server list page) to start with (saved on exit)
SaveErrorLog=0		Set value: 1 to enable error logs (_LogFile.txt)
Style=Windows		Visual style (Theme) selected from style list.

[UDP]
LocalHost=127.0.0.1	Not used in Updated version
LocalPort=9000		Not used in Updated version


[OpenSpy]		Section for OpenSpy related values.


[HTTP]			Section for HTTPS related values.




[ServerList]

Server_List_1_Name=server1	Set server names (max 32 characters).
Server_List_2_Name=HD2	
Server_List_3_Name=HD2
Server_List_4_Name=co-op servers
Server_List_5_Name=deathmatch servers
Server_List_6_Name=occupation servers

***Server 1 is Hidden for user ( meant to be used for master list )

Refresh_List_1_on_start=0	
Refresh_List_2_on_start=0	(0/1) Set value: 1 for server list refresh at program start.
Refresh_List_3_on_start=0
Refresh_List_4_on_start=0
Refresh_List_5_on_start=0
Refresh_List_6_on_start=0

ReadGameMPMasterServerList=1	(0/1) Read Hidden and Dangerous 2 MP list
ReadGameMPFavoritesList=1		(0/1) Read Hidden and Dangerous 2 Favorites list
***valid HD2dir must be set !


Filters_List_1=			Filter out gamestyle(s).
Filters_List_2=
Filters_List_3=
Filters_List_4=
Filters_List_5=
Filters_List_6=

*If only Cooperative should be shown in list #1: 

Filters_List_1= Deathmatch, Objectives, Occupation

*Order or case is not critical.

Filter keywords:
Cooperative, Deathmatch, Objectives, Occupation


[GAME]
HD2dir=D:\Hidden and Dangerous 2		optional Hidden and Dangerous 2 install location.

--------------------------------------------------------------------------------------------------------------


UDP Request data format:
array of byte = (254,253,0,70,85,67,75,9,0,1,3,5,6,8,10,19,51,255,0,0);
It requests selection of data in selected order and response have only data (without keywords).


Format used by Hidden and Dangerous 2 to update servers info in MP servers list:
array of byte = (254,253,0,67,79,82,89,255,255,255);


v1.0 (2018)

--------------------------------------------------------------------------------------------------------------
 v1.7xx

 -Qtracker masterlist part removed
 +UDP connection component replaced
 +different info request data format
 +IP:PORT format error check (custom list files)

--------------------------------------------------------------------------------------------------------------
 +Double-click to Join server
 +Buttons: Export players list and Export Full list


--------------------------------------------------------------------------------------------------------------
v1.7.4.0 (12.oct.2025)

+ Gamestyle filter option
--------------------------------------------------------------------------------------------------------------
v1.7.5.0 (14.oct.2025)

+ Visual style (Theme) selection.	(default style: "Windows")
	*** Themes are not perfect. Some of them create placement shifts of GUI objects.

--------------------------------------------------------------------------------------------------------------






--------------------------------------------------------------------------------------------------------------
--------------------------------------------------------------------------------------------------------------

Idea and code: LARK_1

--------------------------------------------------------------------------------------------------------------
Application created with: Embarcadero RAD Studio XE4
--------------------------------------------------------------------------------------------------------------




