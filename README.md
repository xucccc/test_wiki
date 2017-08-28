**volasystems App Project**

Table of Contents

[IMPORTANT ! 4](#__RefHeading___Toc478163903)

[volasystems: name of our company 5](#__RefHeading___Toc478163904)

[Purpose of the App 5](#__RefHeading___Toc478163905)

[Surface (= smart surface light volaTiles)
5](#__RefHeading___Toc478163906)

[The Server (web service or called back end)
5](#__RefHeading___Toc478163907)

[Functional requirements 5](#__RefHeading___Toc478163908)

[Actors 5](#__RefHeading___Toc478163909)

[Owner-User 5](#__RefHeading___Toc478163910)

[Visitor-User 5](#__RefHeading___Toc478163911)

[Use cases/scenarios 5](#__RefHeading___Toc478163912)

[Set access control for visitors scenario
6](#__RefHeading___Toc478163913)

[Set available features for visitors scenario
6](#__RefHeading___Toc478163914)

[Turn on/off sensors scenario 6](#__RefHeading___Toc478163915)

[User (Owner) wants to see all of his scenes scenario
6](#__RefHeading___Toc478163916)

[User (Visitor) wants to see all available scenes scenario
7](#__RefHeading___Toc478163917)

[Normal Start of app scenario 7](#__RefHeading___Toc478163918)

[General exceptions and variants: 7](#__RefHeading___Toc478163919)

[Initialize surface scenario (pairing with WiFi, connect for the first
time) 8](#__RefHeading___Toc478163920)

[General exceptions and variants 9](#general-exceptions-and-variants-1)

[General exceptions and variants 9](#__RefHeading___Toc478163922)

[Add (install) new scene scenario 9](#__RefHeading___Toc478163923)

[Select scene scenario 10](#__RefHeading___Toc478163924)

[exceptions and variants 10](#exceptions-and-variants)

[Play scene from automatic screen scenario
10](#__RefHeading___Toc478163926)

[exceptions and variants 10](#exceptions-and-variants-1)

[Change scene properties scenario 10](#__RefHeading___Toc478163928)

[Turn surface on/off scenario 11](#__RefHeading___Toc478163929)

[General exceptions and variants 11](#__RefHeading___Toc478163930)

[Update firmware 11](#update-firmware)

[Data Objects used in the API and app logic
11](#__RefHeading___Toc478163932)

[SCENE (read only) 11](#__RefHeading___Toc478163933)

[SCENE\_DATA (used for storing scenes on the phone)
12](#__RefHeading___Toc478163934)

[SURFACE\_INFO 12](#__RefHeading___Toc478163935)

[SURFACE\_DATA (used for storing surface related data on the phone)
13](#__RefHeading___Toc478163936)

[PUBLIC\_ALLOWED\_OPERATIONS 13](#__RefHeading___Toc478163937)

[SURFACE\_SETTINGS 14](#__RefHeading___Toc478163938)

[USER-CRED 14](#__RefHeading___Toc478163939)

[USER-SETTINGS (TBD) 14](#__RefHeading___Toc478163940)

[DIAGNOSTICS 15](#__RefHeading___Toc478163941)

[FIRMWARE\_INFO 15](#__RefHeading___Toc478163942)

[Surface interface (App to surface)
15](#surface-interface-app-to-surface)

[Authentication 15](#__RefHeading___Toc478163944)

[Ports of the surface and operation accessibility
15](#__RefHeading___Toc478163945)

[1) Port without encryption 15](#port-without-encryption)

[2) Port for Vis-Key-encryption 16](#port-for-vis-key-encryption)

[3) Port for Master-Key-encryption 16](#port-for-master-key-encryption)

[General error responses to functions 16](#__RefHeading___Toc478163949)

[Private functions 17](#__RefHeading___Toc478163950)

[get\_surface\_info 17](#__RefHeading___Toc478163951)

[get\_WiFi 17](#__RefHeading___Toc478163952)

[set\_sec\_mode 17](#__RefHeading___Toc478163953)

[get\_allowed\_operations 17](#get_allowed_operations)

[set\_allowed\_operations 17](#__RefHeading___Toc478163955)

[get\_settings 18](#__RefHeading___Toc478163956)

[set\_settings 18](#__RefHeading___Toc478163957)

[set\_adapter 18](#__RefHeading___Toc478163958)

[firmware\_update 19](#firmware_update)

[set\_surface\_name 19](#set_surface_name)

[get\_diagnostics 20](#get_diagnostics)

[reset\_surface 20](#reset_surface)

[Public functions 20](#__RefHeading___Toc478163963)

[blink\_identify 20](#blink_identify)

[get\_sec\_mode 20](#get_sec_mode)

[get\_scene\_parameters 21](#get_scene_parameters)

[set\_speed 21](#__RefHeading___Toc478163967)

[set\_brightness 21](#__RefHeading___Toc478163968)

[set\_color 21](#__RefHeading___Toc478163969)

[set\_color\_temperature 22](#set_color_temperature)

[get\_surface\_name 22](#get_surface_name)

[get\_installed\_scenes 22](#get_installed_scenes)

[scene\_install 22](#__RefHeading___Toc478163973)

[play\_scene 23](#play_scene)

[set\_standby 23](#__RefHeading___Toc478163975)

[check\_key 23](#__RefHeading___Toc478163976)

[Encryption tool operations 23](#__RefHeading___Toc478163977)

[request\_vis\_key 23](#__RefHeading___Toc478163978)

[check\_touch 24](#check_touch)

[Always public operations 24](#__RefHeading___Toc478163980)

[get\_serial\_number 24](#get_serial_number)

[get\_pub\_info 24](#get_pub_info)

[Encryption with AES 24](#__RefHeading___Toc478163983)

[Web Service Interface (app to server) 25](#__RefHeading___Toc478163984)

[Authentication 25](#__RefHeading___Toc478163985)

[Security 25](#__RefHeading___Toc478163986)

[Images of scenes 25](#__RefHeading___Toc478163987)

[Operations 25](#__RefHeading___Toc478163988)

[URL: /scene/&lt;scene\_id&gt; 25](#__RefHeading___Toc478163989)

[URL: /scenes 26](#__RefHeading___Toc478163990)

[URL: /scene/buy/&lt;scene\_id&gt; - Not implemented in first version!
26](#__RefHeading___Toc478163991)

[URL: /scene/fetch/&lt;scene\_id&gt; 26](#__RefHeading___Toc478163992)

[URL: /user 26](#__RefHeading___Toc478163993)

[URL: /scenes and /scenes/full 27](#__RefHeading___Toc478163994)

[URL: /autoscenes and /autoscenes/full
28](#url-autoscenes-and-autoscenesfull)

[URL: /p/user 28](#__RefHeading___Toc478163996)

[URL: / user/forgot/password 28](#url-userforgotpassword)

[URL: /diagnostics/ 29](#url-diagnostics)

[URL: /firmware/version 29](#url-firmwareversion)

[URL: /firmware/fetch 29](#url-firmwarefetch)

[App data storage 29](#__RefHeading___Toc478164001)

[Persistent Data 29](#__RefHeading___Toc478164002)

[Cached Surface Data 30](#__RefHeading___Toc478164003)

[Discovery of Surfaces 30](#__RefHeading___Toc478164004)

[Firmware update: data transfer in many packages
30](#__RefHeading___Toc478164005)

[Glossary 30](#glossary)

[Non-functional requirements 31](#__RefHeading___Toc478164007)

[General 31](#__RefHeading___Toc478164008)

[iPhone/iOS compatibility 31](#__RefHeading___Toc478164009)

[Programming style 31](#__RefHeading___Toc478164010)

[Delivery 31](#__RefHeading___Toc478164011)

[Demo servers for the API 31](#__RefHeading___Toc478164012)

1.  <span id="__RefHeading___Toc478163903" class="anchor"><span id="__RefHeading__663_1453772314" class="anchor"><span id="__RefHeading__535_1208072552" class="anchor"><span id="__RefHeading__269_594866139" class="anchor"><span id="__RefHeading__108_995001476" class="anchor"><span id="__RefHeading__586_594866139" class="anchor"><span id="__RefHeading__239_451558443" class="anchor"><span id="__RefHeading__2321_866041415" class="anchor"></span></span></span></span></span></span></span></span>IMPORTANT !
    ======================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

    <span id="__RefHeading___Toc478163904" class="anchor"><span id="__RefHeading__665_1453772314" class="anchor"><span id="__RefHeading__537_1208072552" class="anchor"><span id="__RefHeading__588_594866139" class="anchor"><span id="__RefHeading__241_451558443" class="anchor"><span id="__RefHeading__2323_866041415" class="anchor"></span></span></span></span></span></span>volasystems: name of our company
    =================================================================================================================================================================================================================================================================================================================================================================================================================

**volaTiles:** name of the physical lighting modules (luminaire), the
output medium (also called “surface”)

**volaPlay:** name of the app, the control unit

1.  

    <span id="__RefHeading___Toc478163905" class="anchor"><span id="__RefHeading__667_1453772314" class="anchor"><span id="__RefHeading__539_1208072552" class="anchor"><span id="__RefHeading__590_594866139" class="anchor"><span id="__RefHeading__243_451558443" class="anchor"><span id="__RefHeading__2325_866041415" class="anchor"></span></span></span></span></span></span>Purpose of the App
    ===================================================================================================================================================================================================================================================================================================================================================================================================

“Interaction with the smart surface/ambient Light System”

VolaPlay is a simple app created to interact with the smart surface
ambient light system. It is used to fetch light scenes from the server
and upload them to the surface, choose which of the installed scenes are
played on the surface, change properties of the scene (color, dimming,
speed, hue, etc.) while it is running and to turn the surface on/off
(soft).

Is is also used to configure how visitors and users can interact with
the surface and to configure the security settings of the surface.

<span id="__RefHeading___Toc478163906" class="anchor"><span id="__RefHeading__4337_677526150" class="anchor"><span id="__RefHeading__6694_763101493" class="anchor"><span id="__RefHeading__8895_492320541" class="anchor"><span id="__RefHeading__669_1453772314" class="anchor"><span id="__RefHeading__541_1208072552" class="anchor"><span id="__RefHeading__271_594866139" class="anchor"><span id="__RefHeading__110_995001476" class="anchor"><span id="__RefHeading__592_594866139" class="anchor"><span id="__RefHeading__245_451558443" class="anchor"><span id="__RefHeading__2327_866041415" class="anchor"><span id="__RefHeading__1147_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Surface (= smart surface light volaTiles)
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The surface is an ambient light system which is connected to a router or
creates its own AP (WiFi Access Point).

The phone with the app is either connected to the same router as the
surface or connects to the AP that the surface is providing. All data
transfer with the surface is performed using TCP over the local network.

<span id="__RefHeading___Toc478163907" class="anchor"><span id="__RefHeading__4339_677526150" class="anchor"><span id="__RefHeading__6696_763101493" class="anchor"><span id="__RefHeading__8897_492320541" class="anchor"><span id="__RefHeading__671_1453772314" class="anchor"><span id="__RefHeading__543_1208072552" class="anchor"><span id="__RefHeading__273_594866139" class="anchor"><span id="__RefHeading__112_995001476" class="anchor"><span id="__RefHeading__594_594866139" class="anchor"><span id="__RefHeading__247_451558443" class="anchor"><span id="__RefHeading__2329_866041415" class="anchor"><span id="__RefHeading__1149_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>The Server (web service or called back end)
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The server is a HTTP server on the Internet that provides secure REST
operations. These operations are called from the app using REST/HTTPS.

regardsm,

1.  <span id="__RefHeading___Toc478163908" class="anchor"><span id="__RefHeading__673_1453772314" class="anchor"><span id="__RefHeading__545_1208072552" class="anchor"><span id="__RefHeading__275_594866139" class="anchor"><span id="__RefHeading__122_995001476" class="anchor"><span id="__RefHeading__596_594866139" class="anchor"><span id="__RefHeading__249_451558443" class="anchor"><span id="__RefHeading__2331_866041415" class="anchor"></span></span></span></span></span></span></span></span>Functional requirements
    ==================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

    1.  <span id="__RefHeading___Toc478163909" class="anchor"><span id="__RefHeading__4341_677526150" class="anchor"><span id="__RefHeading__6698_763101493" class="anchor"><span id="__RefHeading__8899_492320541" class="anchor"><span id="__RefHeading__675_1453772314" class="anchor"><span id="__RefHeading__547_1208072552" class="anchor"><span id="__RefHeading__277_594866139" class="anchor"><span id="__RefHeading__124_995001476" class="anchor"><span id="__RefHeading__598_594866139" class="anchor"><span id="__RefHeading__251_451558443" class="anchor"><span id="__RefHeading__2333_866041415" class="anchor"><span id="__RefHeading__1151_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Actors
        ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The users of the app are classified into two groups of actors.

1.  ### 

    ### <span id="__RefHeading___Toc478163910" class="anchor"><span id="__RefHeading__4343_677526150" class="anchor"><span id="__RefHeading__6700_763101493" class="anchor"><span id="__RefHeading__8901_492320541" class="anchor"><span id="__RefHeading__677_1453772314" class="anchor"><span id="__RefHeading__549_1208072552" class="anchor"><span id="__RefHeading__279_594866139" class="anchor"><span id="__RefHeading__126_995001476" class="anchor"><span id="__RefHeading__600_594866139" class="anchor"><span id="__RefHeading__253_451558443" class="anchor"><span id="__RefHeading__2335_866041415" class="anchor"><span id="__RefHeading__1153_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Owner-User

A user that has all the rights to configure and operate the surface with
the app. This can be the private owner or a family member of the owner
or an employee of a company owning the surface.

### <span id="__RefHeading___Toc478163911" class="anchor"><span id="__RefHeading__4345_677526150" class="anchor"><span id="__RefHeading__6702_763101493" class="anchor"><span id="__RefHeading__8903_492320541" class="anchor"><span id="__RefHeading__679_1453772314" class="anchor"><span id="__RefHeading__551_1208072552" class="anchor"><span id="__RefHeading__602_594866139" class="anchor"><span id="__RefHeading__255_451558443" class="anchor"><span id="__RefHeading__2337_866041415" class="anchor"><span id="__RefHeading__1155_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span>Visitor-User

A user with restricted access to the surface. The Owner-User of a
surface defines what operations the Visitor-User can perform with the
surface using the app. A Owner-User of one surface may be the visitor of
an other surface. This means there are visitors that have a account on
the web service.

1.  <span id="__RefHeading___Toc478163912" class="anchor"><span id="__RefHeading__4347_677526150" class="anchor"><span id="__RefHeading__6704_763101493" class="anchor"><span id="__RefHeading__8905_492320541" class="anchor"><span id="__RefHeading__681_1453772314" class="anchor"><span id="__RefHeading__553_1208072552" class="anchor"><span id="__RefHeading__283_594866139" class="anchor"><span id="__RefHeading__196_995001476" class="anchor"><span id="__RefHeading__604_594866139" class="anchor"><span id="__RefHeading__257_451558443" class="anchor"><span id="__RefHeading__2339_866041415" class="anchor"><span id="__RefHeading__1157_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Use cases/scenarios
    -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

    1.  ### <span id="__RefHeading___Toc478163913" class="anchor"><span id="__RefHeading__4349_677526150" class="anchor"><span id="__RefHeading__6706_763101493" class="anchor"><span id="__RefHeading__8907_492320541" class="anchor"><span id="__RefHeading__683_1453772314" class="anchor"><span id="__RefHeading__555_1208072552" class="anchor"><span id="__RefHeading__285_594866139" class="anchor"><span id="__RefHeading__208_995001476" class="anchor"><span id="__RefHeading__606_594866139" class="anchor"><span id="__RefHeading__259_451558443" class="anchor"><span id="__RefHeading__2341_866041415" class="anchor"><span id="__RefHeading__1159_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Set access control for visitors scenario

Precondition:

- the user is logged in and is connected to a surface.

- the user has entered the master key for the surface~++~

1\. the user enters the screen '02.01' surfaces

2\. the user taps the edit button of the surface

3\. id the does not have the current access control setting it will fetch
them by calling the api operation **get\_sec\_mode**

4\. screen '02.01.02': the user taps either 'Not shared', 'Public',
'Protected'

5\. if the access control settings have changed the app must use the api
operation **set\_sec\_mode **

### <span id="__RefHeading___Toc478163914" class="anchor"><span id="__RefHeading__4351_677526150" class="anchor"><span id="__RefHeading__6708_763101493" class="anchor"><span id="__RefHeading__8909_492320541" class="anchor"><span id="__RefHeading__685_1453772314" class="anchor"><span id="__RefHeading__557_1208072552" class="anchor"><span id="__RefHeading__287_594866139" class="anchor"><span id="__RefHeading__210_995001476" class="anchor"><span id="__RefHeading__608_594866139" class="anchor"><span id="__RefHeading__261_451558443" class="anchor"><span id="__RefHeading__2343_866041415" class="anchor"><span id="__RefHeading__1161_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Set available features for visitors scenario

Precondition:

- the user is logged in and is connected to a surface.

- the user has entered the master key for the surface

1\. the user enters the screen '02.01' surfaces

2\. the user taps the edit button of the surface

3\. screen '02.01.02': the user taps sharing options

4\. if the app does not have the current restriction settings of the
surface it must call api operation **get\_allowed\_operations** to get
the current settings

5\. screen '02.01.03.01 sharing options': the screen must show the
current state of the restriction settings.

6\. the user changes any of the restriction settings

7\. the will use api operation set\_allowed\_operations to change the
settings in the app

### <span id="__RefHeading___Toc478163915" class="anchor"><span id="__RefHeading__4353_677526150" class="anchor"><span id="__RefHeading__6710_763101493" class="anchor"><span id="__RefHeading__8911_492320541" class="anchor"><span id="__RefHeading__687_1453772314" class="anchor"><span id="__RefHeading__559_1208072552" class="anchor"><span id="__RefHeading__289_594866139" class="anchor"><span id="__RefHeading__212_995001476" class="anchor"><span id="__RefHeading__610_594866139" class="anchor"><span id="__RefHeading__263_451558443" class="anchor"><span id="__RefHeading__2345_866041415" class="anchor"><span id="__RefHeading__1163_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Turn on/off sensors scenario

Short description:

- only allowed for owner users

- uses api operations **get\_settings**, **set\_settings**

- screens: “02.01.03 Surface Settings - expert”

1.  ### 

    ### <span id="__RefHeading___Toc478163916" class="anchor"><span id="__RefHeading__4355_677526150" class="anchor"><span id="__RefHeading__6712_763101493" class="anchor"><span id="__RefHeading__8913_492320541" class="anchor"><span id="__RefHeading__689_1453772314" class="anchor"><span id="__RefHeading__561_1208072552" class="anchor"><span id="__RefHeading__265_451558443" class="anchor"><span id="__RefHeading__2347_866041415" class="anchor"><span id="__RefHeading__1165_19721096" class="anchor"></span></span></span></span></span></span></span></span></span>User (Owner) wants to see all of his scenes scenario

Precondition:

- the user is logged in and is connected to a surface.

- the user has entered the master key for the surface

1\. the app uses web service api call to **/scenes/user/{user\_id}** to
get a list of all scene ids owned by the user

2\. for each scene id the app checks if the scene data of the scene is in
the app data store. If this is not the case the app will use web service
api call to /scene/&lt;scene\_id&gt; (for the scene meta data) and
/scene/fetch/&lt;scene\_id&gt; (for the scene file) to get the data for
each scene

3\. screen: '01.02 My Scenes' shows all the scenes of the user by
category

### <span id="__RefHeading___Toc478163917" class="anchor"><span id="__RefHeading__4357_677526150" class="anchor"><span id="__RefHeading__6714_763101493" class="anchor"><span id="__RefHeading__8915_492320541" class="anchor"><span id="__RefHeading__691_1453772314" class="anchor"><span id="__RefHeading__563_1208072552" class="anchor"><span id="__RefHeading__267_451558443" class="anchor"><span id="__RefHeading__2349_866041415" class="anchor"><span id="__RefHeading__1167_19721096" class="anchor"></span></span></span></span></span></span></span></span></span>User (Visitor) wants to see all available scenes scenario

Precondition:

- the user is *not* logged in and is connected to a surface.

- the user has entered the vis key for the surface (if sec mode is
protected)

1\. the app uses surface api operation get\_installed\_scenes to get the
IDs of the installed scenes on the surface

2\. for each scene id the app checks if the scene data of the scene is in
the app data store. If this is not the case the app will use web service
api call to /scene/&lt;scene\_id&gt; (for the scene meta data) to get
the data for each scene. The app will not need to load the scene files
because they are installed already

3\. screen: '01.02 My Scenes' shows all the scenes available to the user
by category

### <span id="__RefHeading___Toc478163918" class="anchor"><span id="__RefHeading__4359_677526150" class="anchor"><span id="__RefHeading__6716_763101493" class="anchor"><span id="__RefHeading__8917_492320541" class="anchor"><span id="__RefHeading__693_1453772314" class="anchor"><span id="__RefHeading__565_1208072552" class="anchor"><span id="__RefHeading__2351_866041415" class="anchor"><span id="__RefHeading__1169_19721096" class="anchor"></span></span></span></span></span></span></span></span>Normal Start of app scenario

Precondition:

- the user is registered at the web service (this is only needed if the
will not use the visitor mode)

1\. The user logs in (screen '00.01 login\_register') either as
registered user or not registered

2\. (If not started as visitor) the app uses web service operation
**/user/{user\_id}** to check if the user data stored in the app is
correct. (if the http code of the response is 200 the authentication is
ok, otherwise not).

3\. The app searches for surfaces in the local net. (see Discovery of
Surfaces)

4\. The app asks each surface for its serial number. Use API operation
**get\_serial\_number** for this.

5\. If only one surface and this are already known to the user (this
means it is stored in the app already), the app must automatically use
this surface as used surface.

### <span id="__RefHeading___Toc478163919" class="anchor"><span id="__RefHeading__4361_677526150" class="anchor"><span id="__RefHeading__6718_763101493" class="anchor"><span id="__RefHeading__8919_492320541" class="anchor"><span id="__RefHeading__695_1453772314" class="anchor"><span id="__RefHeading__567_1208072552" class="anchor"><span id="__RefHeading__1171_19721096" class="anchor"></span></span></span></span></span></span></span>General exceptions and variants:

1b If the user enters the app without a web service account the web
service is not available for the user. (Only the images and descriptions
of a scene can be loaded from the web service).

2b. If the authentication test is not ok the app should show a pop up
and go back to 1

3b. If no surface was found in the local net, the app must show the
'00.02 Instructions' screen

5b. If more than one surface, that was found, is known to the user the
screen '02.01 surfaces' must be shown. The user can choose the surface
(or group) to be used.

5c. If surfaces are found, but none of them is known to the user/app,
the unknown surfaces should be shown in the '02.01 surfaces' screen.

5d If no surface was found the screen '00.02 instruction' must be shown.

### <span id="__RefHeading___Toc478163920" class="anchor"><span id="__RefHeading__4363_677526150" class="anchor"><span id="__RefHeading__6720_763101493" class="anchor"><span id="__RefHeading__8921_492320541" class="anchor"><span id="__RefHeading__697_1453772314" class="anchor"><span id="__RefHeading__569_1208072552" class="anchor"><span id="__RefHeading__271_451558443" class="anchor"><span id="__RefHeading__2353_866041415" class="anchor"><span id="__RefHeading__1173_19721096" class="anchor"></span></span></span></span></span></span></span></span></span>Initialize surface scenario (pairing with WiFi, connect for the first time)

1.  Press the “+” Button on the surfaces screen.

2\. screen '00.02 instruction' shows up. (instruction says: …. Connect to
the Wifi router with the name “volatiles\_” and a number (for example
“volatiles\_44995839458). Then come back to the app.

3\. the user enters the iOS settings and connects the phone to the AP of
the surface

The is periodicaly trying to send get\_pub\_info to ip address
192.168.0.1:5555). If you get a response you can proceed to the next
step.

4\. the app sees that it is connected to the AP and spawns an iOS –
notification (screen '00.03 continue setup')

5\. the user clicks the notification and is forwarded to the app again or
manually reenters the app.

6\. screen '00.04 enter Master-Key '

- the user enters the Master-Key

7\. screen '00.05 Standalone or Router': the user taps the WiFi button

8\. the app uses the API operation **get\_WiFi** to get all WiFi routers
seen by the surfaces (using the port 5557)

9\. screen '00.06 available WiFi' the app shows all WiFi routers in a
list

10\. the user selects the WiFi router that he wants to connect the
surface to.

11\. screen: '00.07 WiFi password': the user enters the WiFi password for
the selected user

12\. the user taps the connect button

13\. the app used the API operation **set\_adapter (port 5557)** to tell
the surface to connect to the router. If the answer is ok (see
operations) then the surface is connected to the router. While the app
waits for the answer to the operation **set\_adapter** the screen '00.08
Connecting' is shown.

**{“adapter”: “OK”, “ip”:”111.222.333.444”}**

The return value of the command contains the ip of the surface in the
new joined wifi network. Store this ip address for the next steps.

The surface now closes its AP. The phone is then returning to the last
used wifi network.

13.2 Now the app should periodicaly try to call get\_surface\_name(port
5557) on IP that was scored in the last step. Use the respone of
get\_surface\_name to check if the surface is named already. (Will
return an empty name (“”), if the surface was not named)

14\. the app shows the screen '00.08 rename' the user enters a name for
the new surfaces (if the surface was named before the old name is shown
in the text field)

15\. the user taps the Done button

16\. the app uses the API operation **set\_surface\_name** to assign a
new name to the surface (if the name has changed)

17.. '02.01 Surfaces': the app shows all surface including the new
initialized surface

General exceptions and variants
-------------------------------

5b. if the user does not click the notification he can enter the app
manually and proceed to the next screen by tapping the “x” (left upper
corner)

12b. The user presses the cancel button to get back to 8

13b. If the returned message of the surface is “connection failed” then
the screen '00.08.01 surface router connection error' must be shown. If
user taps the OK button, go to 8

16b. If the surface was not renamed, no API operation must be done

### <span id="__RefHeading___Toc478163922" class="anchor"><span id="__RefHeading__4365_677526150" class="anchor"><span id="__RefHeading__6722_763101493" class="anchor"><span id="__RefHeading__8923_492320541" class="anchor"><span id="__RefHeading__699_1453772314" class="anchor"><span id="__RefHeading__571_1208072552" class="anchor"><span id="__RefHeading__2355_866041415" class="anchor"><span id="__RefHeading__1175_19721096" class="anchor"></span></span></span></span></span></span></span></span>General exceptions and variants

5b. if the user does not click the notification he can enter the app
manually and proceed to the next screen by tapping the “x” (left upper
corner)

9b. the user taps the button Standalone-Mode to use the surface in AP
mode

16b. If the returned message of the surface is “connection failed” then
the screen '00.08.01 surface router connection error' must be shown. If
user taps the OK button, go to 12

15b. The user presses the cancel button to get back to 12

20b. If the surface was not renamed, no API operation has to be done

### <span id="__RefHeading___Toc478163923" class="anchor"><span id="__RefHeading__4367_677526150" class="anchor"><span id="__RefHeading__6724_763101493" class="anchor"><span id="__RefHeading__8925_492320541" class="anchor"><span id="__RefHeading__701_1453772314" class="anchor"><span id="__RefHeading__573_1208072552" class="anchor"><span id="__RefHeading__295_594866139" class="anchor"><span id="__RefHeading__134_995001476" class="anchor"><span id="__RefHeading__616_594866139" class="anchor"><span id="__RefHeading__273_451558443" class="anchor"><span id="__RefHeading__2357_866041415" class="anchor"><span id="__RefHeading__1177_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Add (install) new scene scenario

Precondition:

- the app is started and the surface is reachable through WiFi (router
or AP).

- the user is logged in at the server (via app)

- the scene was not installed on the surface in prior

- only allowed for owner

1\. the user selects a scene

2\. the app uses web service operation **/scene/fetch/{scene\_id}** to
load the scene from the server.

3\. the app uploads the scene to the surface using the API operation
**scene\_install**.

4\. the surface installs and displays the scene

1.  ### 

    ### <span id="__RefHeading___Toc478163924" class="anchor"><span id="__RefHeading__4369_677526150" class="anchor"><span id="__RefHeading__6726_763101493" class="anchor"><span id="__RefHeading__8927_492320541" class="anchor"><span id="__RefHeading__703_1453772314" class="anchor"><span id="__RefHeading__575_1208072552" class="anchor"><span id="__RefHeading__299_594866139" class="anchor"><span id="__RefHeading__138_995001476" class="anchor"><span id="__RefHeading__618_594866139" class="anchor"><span id="__RefHeading__275_451558443" class="anchor"><span id="__RefHeading__2359_866041415" class="anchor"><span id="__RefHeading__1179_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Select scene scenario

Precondition:

- the app is started and the surface is connected

2\. the user selects a scene in screen **'01.02 My Scenes'**.

2\. the app checks if the scene is installed on the surface. If this is
not known the app uses the API operation **get\_installed\_scenes** to
get the ids of all scenes installed on the surface. This ids should be
persistently saved.

3\. the app signals the surface to play scene using the API operation
**play\_scene.**

4\. the surface displays the scene

#### exceptions and variants

3b. if the scene is not installed on the surface the scene will be
installed first (see Add (install) new scene scenario)

1.  ### <span id="__RefHeading___Toc478163926" class="anchor"><span id="__RefHeading__4371_677526150" class="anchor"><span id="__RefHeading__6728_763101493" class="anchor"><span id="__RefHeading__8929_492320541" class="anchor"><span id="__RefHeading__1181_19721096" class="anchor"></span></span></span></span></span>Play scene from automatic screen scenario

    Precondition:

    - the app is started and the surface is connected

    1\. the user taps on “automatic”

    2\. the app used the back end method
    **/auto\_scenes/user/&lt;user\_id&gt;** to get the ids of the scenes.
    The categories of that scene will be shown in the automatic screen
    (sorted by the number of scenes for each category. The app fetches scene
    data of scenes that are not known over the API. The app loads the images
    from the back end /categoryimages/&lt;category\_id&gt;.png.

3\. the user taps on a category in screen '01.01 Automatic'

4\. the app selects randomly a scene (from the scenes of the user) from
this category. (If a scene is playing in the moment this scene should
not be selected again). This is done by searching all scenes known by
the user for such scenes with the selected category id.

5\. the app signals the surface to play scene using the API operation
**play\_scene.**

6\. the surface displays the scene

#### exceptions and variants

3b. if the scene is not installed on the surface the scene will be
installed first (see Add (install) new scene scenario)

### <span id="__RefHeading___Toc478163928" class="anchor"><span id="__RefHeading__4373_677526150" class="anchor"><span id="__RefHeading__6730_763101493" class="anchor"><span id="__RefHeading__8931_492320541" class="anchor"><span id="__RefHeading__705_1453772314" class="anchor"><span id="__RefHeading__577_1208072552" class="anchor"><span id="__RefHeading__303_594866139" class="anchor"><span id="__RefHeading__142_995001476" class="anchor"><span id="__RefHeading__620_594866139" class="anchor"><span id="__RefHeading__277_451558443" class="anchor"><span id="__RefHeading__2361_866041415" class="anchor"><span id="__RefHeading__1183_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Change scene properties scenario

Precondition: the app is started and the surface is reachable through
WiFi (router or AP)

1\. the user presses remote button

2\. the app uses API operation **get\_scene\_parameters** to get the
current parameter values

2\. now the user can choose what to change in the scene (options here are
color, speed and color temperature, reset scene to default setting). The
app uses one the following API operation **set\_speed, set\_brightness,
set\_color, set\_color\_temperature.**

### <span id="__RefHeading___Toc478163929" class="anchor"><span id="__RefHeading__4375_677526150" class="anchor"><span id="__RefHeading__6732_763101493" class="anchor"><span id="__RefHeading__8933_492320541" class="anchor"><span id="__RefHeading__707_1453772314" class="anchor"><span id="__RefHeading__579_1208072552" class="anchor"><span id="__RefHeading__305_594866139" class="anchor"><span id="__RefHeading__144_995001476" class="anchor"><span id="__RefHeading__622_594866139" class="anchor"><span id="__RefHeading__279_451558443" class="anchor"><span id="__RefHeading__2363_866041415" class="anchor"><span id="__RefHeading__1185_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Turn surface on/off scenario

Precondition: the app is started and the surface is reachable through
WiFi (router or AP)

1\. the user presses the remote button

2\. the user uses the on or off button to turn the surface on or off.

3\. the app uses API operation **set\_standby** to turn the surface on or
off. (Use **{„set\_standby“ : false}** to turn the surface on or
**{„set\_standby“ : true}** to turn the surface of.)

### <span id="__RefHeading___Toc478163930" class="anchor"><span id="__RefHeading__4377_677526150" class="anchor"><span id="__RefHeading__6734_763101493" class="anchor"><span id="__RefHeading__8935_492320541" class="anchor"><span id="__RefHeading__711_1453772314" class="anchor"><span id="__RefHeading__583_1208072552" class="anchor"><span id="__RefHeading__628_594866139" class="anchor"><span id="__RefHeading__283_451558443" class="anchor"><span id="__RefHeading__2367_866041415" class="anchor"><span id="__RefHeading__1187_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span>General exceptions and variants

G1a. the surface is not reachable. This should show a pop up message to
the user with an option to retry.

1.  ### 

    ### Update firmware

Precondition:

- the app is started and the surface is reachable through WiFi (router
or AP).

- the sever is reachable

1\. The user presses the “firmware update” button in the settings screen

2\. when connecting to a surface, the app uses the API operation
get\_surface\_info to fetch the SURFACE\_INFO data. This contains the
firmware version number of the surface

3\. the app uses web service operation /firmware/version to load
FIRMWARE\_INFO data for the most recent firmware version. The
FIRMWARE\_INFO contains the firmware version number.

4\. the app compares the firmware versions; if the surface uses the most
recent version nothing must be done,

5\. if the firmware of the surface is older than the most recent firmware
the screen: '0X.0X Update Firmware' is shown. The screen must display
the text “user\_info” of the FIRMWARE\_INFO data.

6.the app downloads the firmware file using the web service operation
**firmware/fetch.**

7\. the app uploads the firmware file to the module using the API
operation firmware\_update. Please notice information for transferring
firmware data in chapter Firmware update: data transfer in many
packages.

1.  <span id="__RefHeading___Toc478163932" class="anchor"><span id="__RefHeading__4379_677526150" class="anchor"><span id="__RefHeading__6736_763101493" class="anchor"><span id="__RefHeading__8937_492320541" class="anchor"><span id="__RefHeading__713_1453772314" class="anchor"><span id="__RefHeading__585_1208072552" class="anchor"><span id="__RefHeading__313_594866139" class="anchor"><span id="__RefHeading__152_995001476" class="anchor"><span id="__RefHeading__630_594866139" class="anchor"><span id="__RefHeading__285_451558443" class="anchor"><span id="__RefHeading__2369_866041415" class="anchor"><span id="__RefHeading__1189_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Data Objects used in the API and app logic
    ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

    1.  ### <span id="__RefHeading___Toc478163933" class="anchor"><span id="__RefHeading__4381_677526150" class="anchor"><span id="__RefHeading__6738_763101493" class="anchor"><span id="__RefHeading__8939_492320541" class="anchor"><span id="__RefHeading__715_1453772314" class="anchor"><span id="__RefHeading__587_1208072552" class="anchor"><span id="__RefHeading__315_594866139" class="anchor"><span id="__RefHeading__154_995001476" class="anchor"><span id="__RefHeading__632_594866139" class="anchor"><span id="__RefHeading__287_451558443" class="anchor"><span id="__RefHeading__2371_866041415" class="anchor"><span id="__RefHeading__1191_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>*SCENE (read only)*

  --------------------------------- ----------------- ---------------------------------------------------------------
  ***Field***                       ***Type***        ***Description***
  name                              String            The name of the scene
  id                                Int32             The unique ID of the scene
  author                            String            The author of the scene
  category                          String            The category of the scene
  category\_id                      Int32             The id of the category of the scene.
  tags                              Array of String   The tags of the scene
  can\_change\_color                Bool              Is it possible for the user to change the color.
  can\_change\_color\_temperature   Bool              Is it possible for the user to change the color temperature.
  can\_change\_speed                Bool              Is it possible for the user to change the speed of the scene.
  scene\_image\_url                 String (url)      The full purl of the image in the form http://\*.png
  category\_image\_url              String (url)      The full purl of the image in the form http://\*.png
  --------------------------------- ----------------- ---------------------------------------------------------------

### <span id="__RefHeading___Toc478163934" class="anchor"><span id="__RefHeading__4383_677526150" class="anchor"><span id="__RefHeading__6740_763101493" class="anchor"><span id="__RefHeading__8941_492320541" class="anchor"><span id="__RefHeading__717_1453772314" class="anchor"><span id="__RefHeading__589_1208072552" class="anchor"><span id="__RefHeading__2373_866041415" class="anchor"><span id="__RefHeading__1193_19721096" class="anchor"></span></span></span></span></span></span></span></span>*SCENE\_DATA* (used for storing scenes on the phone)

  -------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------
  ***Field***    ***Type***                                                                                                                                                                                                    ***Description***
  scene          <span id="__RefHeading__719_1453772314" class="anchor"><span id="__RefHeading__591_1208072552" class="anchor"><span id="__RefHeading__2375_866041415" class="anchor"></span></span></span>SCENE (see above)   A SCENE object.
  scene\_image   image                                                                                                                                                                                                         The image showed in the front end of the app as pictorial description of the scene. May be null.
  scene\_file    binary                                                                                                                                                                                                        Scene file that is playable by the surface. The app never interprets this file. It is just send to surfaces to be installed there.
  -------------- ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------

### <span id="__RefHeading___Toc478163935" class="anchor"><span id="__RefHeading__4385_677526150" class="anchor"><span id="__RefHeading__6742_763101493" class="anchor"><span id="__RefHeading__8943_492320541" class="anchor"><span id="__RefHeading__721_1453772314" class="anchor"><span id="__RefHeading__593_1208072552" class="anchor"><span id="__RefHeading__317_594866139" class="anchor"><span id="__RefHeading__156_995001476" class="anchor"><span id="__RefHeading__634_594866139" class="anchor"><span id="__RefHeading__289_451558443" class="anchor"><span id="__RefHeading__2377_866041415" class="anchor"><span id="__RefHeading__1195_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>*SURFACE\_INFO*

+--+
|  |
+--+
|  |
+--+
|  |
+--+
|  |
+--+
|  |
+--+
|  |
+--+
|  |
+--+
|  |
+--+
|  |
+--+
|  |
+--+

### <span id="__RefHeading___Toc478163936" class="anchor"><span id="__RefHeading__4387_677526150" class="anchor"><span id="__RefHeading__6744_763101493" class="anchor"><span id="__RefHeading__8945_492320541" class="anchor"><span id="__RefHeading__723_1453772314" class="anchor"><span id="__RefHeading__595_1208072552" class="anchor"><span id="__RefHeading__1197_19721096" class="anchor"></span></span></span></span></span></span></span>*SURFACE\_DATA* (used for storing surface related data on the phone)

  -------------------- --------------------------- -------------------------------------------
  ***Field***          ***Type***                  ***Description***

  surface              SURFACE\_INFO (see above)   A SURFACE\_INFO object.

  Master-Key           String                      May be null

  Vis-Key              String                      May be null

  Last\_Access\_Role   int8                        0 == last access as visitors
                                                   
                                                   1 == last access as visitors with vis-key
                                                   
                                                   2 == last access as Owner
  -------------------- --------------------------- -------------------------------------------

### <span id="__RefHeading___Toc478163937" class="anchor"><span id="__RefHeading__4389_677526150" class="anchor"><span id="__RefHeading__6746_763101493" class="anchor"><span id="__RefHeading__8947_492320541" class="anchor"><span id="__RefHeading__727_1453772314" class="anchor"><span id="__RefHeading__599_1208072552" class="anchor"><span id="__RefHeading__319_594866139" class="anchor"><span id="__RefHeading__158_995001476" class="anchor"><span id="__RefHeading__636_594866139" class="anchor"><span id="__RefHeading__291_451558443" class="anchor"><span id="__RefHeading__2379_866041415" class="anchor"><span id="__RefHeading__1199_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>*PUBLIC\_ALLOWED\_OPERATIONS*

  ---------------------------- ------------ -----------------------------------
  ***Field***                  ***Type***   ***Description***
  change\_brightness           Bool         Allow operation for Visitor-User.
  change\_color                Bool         Allow operation for Visitor-User.
  change\_color\_temperature   Bool         Allow operation for Visitor-User.
  change\_scene                Bool         Allow operation for Visitor-User.
  change\_speed                Bool         Allow operation for Visitor-User.
  standby                      Bool         Allow operation for Visitor-User.
  ---------------------------- ------------ -----------------------------------

### <span id="__RefHeading___Toc478163938" class="anchor"><span id="__RefHeading__4391_677526150" class="anchor"><span id="__RefHeading__6748_763101493" class="anchor"><span id="__RefHeading__8949_492320541" class="anchor"><span id="__RefHeading__729_1453772314" class="anchor"><span id="__RefHeading__601_1208072552" class="anchor"><span id="__RefHeading__321_594866139" class="anchor"><span id="__RefHeading__160_995001476" class="anchor"><span id="__RefHeading__638_594866139" class="anchor"><span id="__RefHeading__293_451558443" class="anchor"><span id="__RefHeading__2381_866041415" class="anchor"><span id="__RefHeading__1201_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>*SURFACE\_SETTINGS*

  ------------------- ------------ ----------------------------------------------
  ***Field***         ***Type***   ***Description***
  ambient\_sensor     Bool         Turn on the ambient sensor on the surface.
  touch\_sensor       Bool         Turn on the touch sensor on the surface.
  proximity\_sensor   Bool         Turn on the proximity sensor on the surface.
  ------------------- ------------ ----------------------------------------------

### <span id="__RefHeading___Toc478163939" class="anchor"><span id="__RefHeading__4393_677526150" class="anchor"><span id="__RefHeading__6750_763101493" class="anchor"><span id="__RefHeading__8951_492320541" class="anchor"><span id="__RefHeading__731_1453772314" class="anchor"><span id="__RefHeading__603_1208072552" class="anchor"><span id="__RefHeading__295_451558443" class="anchor"><span id="__RefHeading__2383_866041415" class="anchor"><span id="__RefHeading__1203_19721096" class="anchor"></span></span></span></span></span></span></span></span></span>*USER-CRED*

  -------------------------------------------------- ---------------- ----------------------------------------------------------------------------------------------------
  1.  ***Field***                                    1.  ***Type***   1.  ***Description***
                                                                      
                                                                      

  1.  user\_name/email (TBD)                         1.  String       1.  User name for web service (must be unique)
                                                                      
                                                                      

  1.  device\_id                                     1.  String       1.  Device id of telephone
                                                                      
                                                                      

  1.  language                                       1.  String       1.  A ISO 639-1 Code. This is used to determine the language of the user (from the phone settings)
                                                                      
                                                                      

  1.  password (optional in JSON)                    1.  String       1.  Password for user. Unsure if this feature will exist in the future.
                                                                      
      **DO not use this!!! For testing purposes.**                    
                                                                      
                                                                      
  -------------------------------------------------- ---------------- ----------------------------------------------------------------------------------------------------

1.  1.  ### <span id="__RefHeading___Toc478163940" class="anchor"><span id="__RefHeading__4395_677526150" class="anchor"><span id="__RefHeading__6752_763101493" class="anchor"><span id="__RefHeading__8953_492320541" class="anchor"><span id="__RefHeading__733_1453772314" class="anchor"><span id="__RefHeading__605_1208072552" class="anchor"><span id="__RefHeading__297_451558443" class="anchor"><span id="__RefHeading__2385_866041415" class="anchor"><span id="__RefHeading__1205_19721096" class="anchor"></span></span></span></span></span></span></span></span></span>*USER-SETTINGS (TBD)*

  ----------------- ---------------- -----------------------------------------
  1.  ***Field***   1.  ***Type***   1.  ***Description***
                                     
                                     

  1.  user\_id      1.  Int32        1.  Numeric user id for the web service
                                     
                                     
  ----------------- ---------------- -----------------------------------------

1.  1.  ### <span id="__RefHeading___Toc478163941" class="anchor"><span id="__RefHeading__4397_677526150" class="anchor"><span id="__RefHeading__6754_763101493" class="anchor"><span id="__RefHeading__8955_492320541" class="anchor"><span id="__RefHeading__735_1453772314" class="anchor"><span id="__RefHeading__607_1208072552" class="anchor"><span id="__RefHeading__299_451558443" class="anchor"><span id="__RefHeading__2387_866041415" class="anchor"><span id="__RefHeading__1207_19721096" class="anchor"></span></span></span></span></span></span></span></span></span>*DIAGNOSTICS*

  ------------------------------ --------------------- --------------------------------------------------
  1.  ***Field***                1.  ***Type***        1.  ***Description***
                                                       
                                                       

  1.  minutes\_app\_foreground   1.  Int32             1.  How long was the app displayed in foreground
                                                       
                                                       

  1.  surface\_errors            1.  Array of String   1.  Errors reported by surface
                                                       
                                                       

  1.  app\_errors                1.  Array of String   1.  Errors reported by app
                                                       
                                                       
  ------------------------------ --------------------- --------------------------------------------------

1.  ### 

    ### <span id="__RefHeading___Toc478163942" class="anchor"><span id="__RefHeading__4399_677526150" class="anchor"><span id="__RefHeading__6756_763101493" class="anchor"><span id="__RefHeading__8957_492320541" class="anchor"><span id="__RefHeading__737_1453772314" class="anchor"><span id="__RefHeading__609_1208072552" class="anchor"><span id="__RefHeading__323_594866139" class="anchor"><span id="__RefHeading__162_995001476" class="anchor"><span id="__RefHeading__640_594866139" class="anchor"><span id="__RefHeading__301_451558443" class="anchor"><span id="__RefHeading__2389_866041415" class="anchor"><span id="__RefHeading__1209_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>*FIRMWARE\_INFO*

  ----------------------- ---------------- ----------------------------------------------------------------
  1.  ***Field***         1.  ***Type***   1.  ***Description***
                                           
                                           

  1.  firmware\_version   1.  String       1.  Version number.
                                           
                                           

  user\_info              1.  String       Text to be displayed to useres using a older version then this
                                           
                                           
  ----------------------- ---------------- ----------------------------------------------------------------

1.  

    Surface interface (App to surface)
    ----------------------------------

The communication is realized using the TCP protocol. For all private
operations, the data is AES encrypted. Depending on the security
settings the public operations also need to be encrypted with AES (see
Encryption with AES).

The sent-and-received data is formatted in JSON.

### <span id="__RefHeading___Toc478163944" class="anchor"><span id="__RefHeading__4401_677526150" class="anchor"><span id="__RefHeading__6758_763101493" class="anchor"><span id="__RefHeading__8959_492320541" class="anchor"><span id="__RefHeading__739_1453772314" class="anchor"><span id="__RefHeading__611_1208072552" class="anchor"><span id="__RefHeading__325_594866139" class="anchor"><span id="__RefHeading__164_995001476" class="anchor"><span id="__RefHeading__642_594866139" class="anchor"><span id="__RefHeading__303_451558443" class="anchor"><span id="__RefHeading__2391_866041415" class="anchor"><span id="__RefHeading__1211_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Authentication

The owner of the surface has a Master-Key. This key will be handed to
the owner when the product (surface) is delivered. All critical
communication with the surface will be encrypted with the master key.

1.  ### 

    ### <span id="__RefHeading___Toc478163945" class="anchor"><span id="__RefHeading__4403_677526150" class="anchor"><span id="__RefHeading__6760_763101493" class="anchor"><span id="__RefHeading__8961_492320541" class="anchor"><span id="__RefHeading__741_1453772314" class="anchor"><span id="__RefHeading__613_1208072552" class="anchor"><span id="__RefHeading__327_594866139" class="anchor"><span id="__RefHeading__336_995001476" class="anchor"><span id="__RefHeading__644_594866139" class="anchor"><span id="__RefHeading__305_451558443" class="anchor"><span id="__RefHeading__2393_866041415" class="anchor"><span id="__RefHeading__1213_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Ports of the surface and operation accessibility

The surface is an IP device that can be accessed through three different
ports.

#### <span id="__RefHeading__329_594866139" class="anchor"><span id="__RefHeading__338_995001476" class="anchor"></span></span> 1) Port without encryption

*port 555*

Connections to this port cannot be encrypted.

The encryption tool operations can be accessed from this port.

If the security mode of the surface is public, this port allows the
access to all public functions.

#### <span id="__RefHeading__331_594866139" class="anchor"><span id="__RefHeading__340_995001476" class="anchor"></span></span> 2) Port for Vis-Key-encryption

*port 556*

Connections to this port must be encrypted with the Vis-Key.

This ports allows access to all public functions.

#### <span id="__RefHeading__333_594866139" class="anchor"><span id="__RefHeading__342_995001476" class="anchor"></span></span> 3) Port for Master-Key-encryption

*port 557*

Connections to this port must be encrypted with the Master-Key.

Private functions are only accessible using this port.

All functions are available using this port.

### <span id="__RefHeading___Toc478163949" class="anchor"><span id="__RefHeading__4405_677526150" class="anchor"><span id="__RefHeading__6762_763101493" class="anchor"><span id="__RefHeading__8963_492320541" class="anchor"><span id="__RefHeading__743_1453772314" class="anchor"><span id="__RefHeading__615_1208072552" class="anchor"><span id="__RefHeading__335_594866139" class="anchor"><span id="__RefHeading__350_995001476" class="anchor"><span id="__RefHeading__646_594866139" class="anchor"><span id="__RefHeading__307_451558443" class="anchor"><span id="__RefHeading__2395_866041415" class="anchor"><span id="__RefHeading__1215_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>General error responses to functions 

If the function is not permitted over the used port:

{“Error”: “Operation not allowed.”}

If the function was called with illegal parameters:

{“Error”: “Parameter error.”}

If the execution of the function failed

{“Error”: “Execution failed.”}

Also:

{“Error”: “Unknown operation.”}

1.  ### <span id="__RefHeading___Toc478163950" class="anchor"><span id="__RefHeading__4407_677526150" class="anchor"><span id="__RefHeading__6764_763101493" class="anchor"><span id="__RefHeading__8965_492320541" class="anchor"><span id="__RefHeading__745_1453772314" class="anchor"><span id="__RefHeading__617_1208072552" class="anchor"><span id="__RefHeading__337_594866139" class="anchor"><span id="__RefHeading__166_995001476" class="anchor"><span id="__RefHeading__648_594866139" class="anchor"><span id="__RefHeading__309_451558443" class="anchor"><span id="__RefHeading__2397_866041415" class="anchor"><span id="__RefHeading__1217_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Private functions

    1.  #### <span id="__RefHeading___Toc478163951" class="anchor"><span id="__RefHeading__339_594866139" class="anchor"><span id="__RefHeading__242_995001476" class="anchor"></span></span></span>get\_surface\_info

Fetch surface information from the surface.

JSON formatted input

**{“get\_surface\_info”: null}**

Response from surface

SURFACE\_INFO object

#### <span id="__RefHeading___Toc478163952" class="anchor"><span id="__RefHeading__341_594866139" class="anchor"><span id="__RefHeading__244_995001476" class="anchor"></span></span></span>get\_WiFi

Get available WiFi networks.

JSON formatted input

**{“get\_WiFi”: null}**

Response from surface

Array of **{&lt;network\_name&gt;, &lt;sec\_type&gt;}** - elements

#### <span id="__RefHeading___Toc478163953" class="anchor"><span id="__RefHeading__343_594866139" class="anchor"><span id="__RefHeading__246_995001476" class="anchor"></span></span></span>set\_sec\_mode

Set security mode.

JSON formatted input

**{“set\_sec\_mode ”: &lt;sec\_mode&gt;}** with **&lt;sec\_mode&gt;** in
**\[“locked', “protected', “public''\] **

Response from surface

**{“sec\_mode”: &lt;sec\_mode&gt;} with &lt;sec\_mode&gt; in \[“locked',
“protected', “public''\] **

#### <span id="__RefHeading___Toc478163955" class="anchor"><span id="__RefHeading__349_594866139" class="anchor"><span id="__RefHeading__264_995001476" class="anchor"></span></span></span>set\_allowed\_operations

Set functions that a Visitor-User can execute.

JSON formatted input

**{“get\_settings”: null}**

Example: **{“set\_allowed\_operations” : {„change\_brightness“: true,
„change\_color“: true, „change\_scene“: true, „change\_speed“: false,
standby: false}} **

Response from surface

**PUBLIC\_ALLOWED\_OPERATIONS object. Every field of
PUBLIC\_ALLOWED\_OPERATIONS object JSON representation is optional.**

#### <span id="__RefHeading___Toc478163956" class="anchor"><span id="__RefHeading__351_594866139" class="anchor"><span id="__RefHeading__272_995001476" class="anchor"></span></span></span>get\_settings

Get current settings of the surface.

JSON formatted input

**{“get\_allowed\_operations”: null}**

Response from surface

**SURFACE\_SETTINGS object **

Example: **{ambient\_sensor: true, touch\_sensor:false,
proximity\_sensor: false}**

#### <span id="__RefHeading___Toc478163957" class="anchor"><span id="__RefHeading__353_594866139" class="anchor"><span id="__RefHeading__274_995001476" class="anchor"></span></span></span>set\_settings

Set general settings of the surface.

JSON formatted input

**{“set\_settings”: &lt;SURFACE\_SETTINGS object&gt;}** with
**&lt;SURFACE\_SETTINGS object&gt;** is SURFACE\_SETTINGS object.

Example: **{„set\_settings“ : {ambient\_sensor: true,
touch\_sensor:false, proximity\_sensor: false}}**

Response from surface

**SURFACE\_SETTINGS object. Every field of SURAFCE-SETTINGS object JSON
representation is optional.**

#### set\_adapter\_hex

Set SSID and password.Fetch IP of surface in the newly joined wifi
network.

JSON formatted input

**{“set\_adapter”: {“ssid”:&lt;ssid\_hex&gt;,“pw”:&lt;pw\_hex&gt;}} with
both parameters are hex encoded **

Response from surface

**{“adapter”: “OK”, “ip”:”111.222.333.444”}**

**“ip” is the ip-address of the surface in the new joined wifi
network.**

**or**

**{“adapter”: “connection failed”}**

**or**

**{“adapter”, “unknown adapter”}**

#### <span id="__RefHeading___Toc478163958" class="anchor"><span id="__RefHeading__355_594866139" class="anchor"><span id="__RefHeading__300_995001476" class="anchor"></span></span></span>set\_adapter 

Set SSID and password.Fetch IP of surface in the newly joined wifi
network.

JSON formatted input

**{“set\_adapter”: {“ssid”:&lt;ssid&gt;,“pw”:&lt;pw&gt;}}**

Response from surface

**{“adapter”: “OK”, “ip”:”111.222.333.444”}**

**“ip” is the ip-address of the surface in the new joined wifi
network.**

**or**

**{“adapter”: “connection failed”}**

**or**

**{“adapter”, “unknown adapter”}**

#### firmware\_update

Update firmware.

The firmware will be send divided into n chunks. This is done to be more
robust to transmission errors. The client sends the first chunk. After a
chunk is send the module will answer what should be the next chunk to be
send by the app. Chunks have the size of 4 KB. Please notice information
for transferring firmware data in chapter Firmware update: data transfer
in many packages.

JSON formatted input

**{„firmware\_update“: {“filename”:&lt;filename&gt;,
“file\_size”:&lt;file-size&gt;, “chunk\_length”:&lt;chunk-size&gt;,
“chunk\_nr”:&lt;chunk number&gt;,
”chunk\_adler32”:&lt;chunk\_adler32\_hex&gt;,
”file\_adler32”:&lt;file\_adler32\_hex&gt;}}\\n&lt;chunk\_binary\_data&gt;**

**with **

**&lt;filename&gt; name of the file**

**&lt;file-size&gt; file size in bytes of the file to be transfered**

**&lt;chunk number&gt; number of the chunk(part) of the file. (First
number is 0)**

**&lt;chunk\_adler32\_hex&gt; adler32 checksum of chunk formated as hex
number**

**&lt;file\_adler32\_hex&gt; adler32 checksum of file formated as hex
number**

**&lt;chunk\_data&gt; data bytes of the chunk**

**&lt;chunk-size&gt; data bytes in the chunk**

Response from surface

**{„firmware\_update“: {“next\_chunk” : &lt;next chunk number&gt;}}**

**{„firmware\_update“: “successful”}**

**with **

**&lt;next chunk number&gt; number of next chunk to be send**

1.  #### 

    #### set\_surface\_name

Set name of surface.

JSON formatted input

**{“set\_surface\_name”:&lt;surface\_name&gt;}** with
**&lt;surface\_name&gt;** in string

Response from surface

**{„set\_surface\_name“: “successful”}**

#### get\_diagnostics

Gets sets of diagnostic texts from the surface.

JSON formatted input

**{“get\_diagnostics”: null}**

Response from surface

**{&lt;text\_type&gt;:\[&lt;text&gt;, &lt;text&gt;, ...\],
&lt;text\_type&gt;:\[&lt;text&gt;, &lt;text&gt;, …\]}**

**with &lt;text\_type&gt; is “errors” or “warnings”, and &lt;text&gt; is
a ascii text.**

Example: **{“errors”:\[“error 1 text”, “error 2 text”\],
warnings:\[“warning 1 text”, “warning 2 text”\]}**

1.  #### 

    #### reset\_surface

Reset all (user-) data of the surface. After that step the surface will
be in the same state as it was newly installed.

JSON formatted input

**{“reset\_surface”:null}**

Response from surface

**{„reset\_surface“: “successful”}**

1.  ### <span id="__RefHeading___Toc478163963" class="anchor"><span id="__RefHeading__4409_677526150" class="anchor"><span id="__RefHeading__6766_763101493" class="anchor"><span id="__RefHeading__8967_492320541" class="anchor"><span id="__RefHeading__747_1453772314" class="anchor"><span id="__RefHeading__619_1208072552" class="anchor"><span id="__RefHeading__359_594866139" class="anchor"><span id="__RefHeading__168_995001476" class="anchor"><span id="__RefHeading__650_594866139" class="anchor"><span id="__RefHeading__311_451558443" class="anchor"><span id="__RefHeading__2399_866041415" class="anchor"><span id="__RefHeading__1219_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Public functions

    1.  #### blink\_identify

Let the surface blink for some time to let the user know what surface he
is connected to.

JSON formatted input

**{“blink\_identify”: null}**

Response from surface

**{“blink\_identify”: “successful”}**

#### 

#### get\_allowed\_operations

Get current allowed functions of the surface.

JSON formatted input

**{“get\_allowed\_operations”: null}**

Response from surface

**PUBLIC\_ALLOWED\_OPERATIONS object **

Example: **{„change\_brightness“: true, „change\_color“: true,
„change\_scene“: true, „change\_speed“: false, standby: false} **

#### get\_sec\_mode

Get security mode.

JSON formatted input

**{“get\_sec\_mode”: null}**

Response from surface

**{“sec\_mode”: &lt;sec\_mode&gt;}** with **&lt;sec\_mode&gt;** in
**\[“locked', “protected', “public''\]**

#### get\_scene\_parameters

Get all values of scene parameters.

JSON formatted input

**{“get\_scene\_parameters”: null}**

Response from surface

**{“speed”: &lt;speed\_value&gt;, “brightness”:&lt;brightness&gt;,
“color”:\[&lt;color\_value: Red&gt;,&lt;color\_value:
Green&gt;,&lt;color\_value: Blue&gt;,&lt;color\_value: White&gt;\],
“color\_temperature”:&lt;color\_temperature&gt;}**

with **&lt;speed\_value&gt;** in **\[1..100\], &lt;brightness&gt;** in
**\[0..100\], &lt;color\_value&gt;** in **\[0..255\],
&lt;color\_temperature&gt;** in **\[1500..10000\]**

#### <span id="__RefHeading___Toc478163967" class="anchor"><span id="__RefHeading__361_594866139" class="anchor"><span id="__RefHeading__304_995001476" class="anchor"></span></span></span>set\_speed

Set speed of current scene.

JSON formatted input

**{“set\_speed”: &lt;speed\_value&gt;}** with **&lt;speed\_value&gt;**
in **\[1..100\]**

Response from surface

**{„set\_speed“: “successful”}**

#### <span id="__RefHeading___Toc478163968" class="anchor"><span id="__RefHeading__363_594866139" class="anchor"><span id="__RefHeading__306_995001476" class="anchor"></span></span></span>set\_brightness

Set brightness of current scene.

JSON formatted input

**{“set\_brightness”: &lt;brightness&gt;}** with **&lt;brightness&gt; in
\[0..100\] **

Response from surface

**{„set\_brightness“: “successful”}**

#### <span id="__RefHeading___Toc478163969" class="anchor"><span id="__RefHeading__365_594866139" class="anchor"><span id="__RefHeading__308_995001476" class="anchor"></span></span></span>set\_color

Set changeable color in current scene.

JSON formatted input

**{“set\_color” :\[&lt;color\_value: Red&gt;,&lt;color\_value:
Green&gt;,&lt;color\_value: Blue&gt;,&lt;color\_value: White&gt;\]} with
&lt;color\_value&gt; in \[0..255\] **

Response from surface

**{„set\_color“: “successful”}**

1.  #### 

    #### set\_color\_temperature

Set color temperature in scene.

JSON formatted input

**{“set\_color\_temperature”:&lt;color\_temperature&gt;} with
&lt;color\_temperature&gt; in \[1500..10000\]**

Response from surface

**{„set\_color\_temperature“: “successful”}**

#### get\_surface\_name

Get name of surface. Will return an empty name (“”) if the surface was
not named.

JSON formatted input

**{“get\_surface\_name”: null}**

Response from surface

**{“surface\_name”: &lt;surface\_name&gt;} with &lt;surface\_name&gt; is
the name of the surface**

1.  #### 

    #### get\_installed\_scenes

Get ids of the scenes installed on the surface.

JSON formatted input

**{“get\_installed\_scenes”: null}**

Response from surface

Will return an array of scene IDs.

Sample: \[38423,472864\]

#### <span id="__RefHeading___Toc478163973" class="anchor"><span id="__RefHeading__369_594866139" class="anchor"><span id="__RefHeading__312_995001476" class="anchor"></span></span></span>scene\_install

Install new scene

JSON formatted input

**{„scene\_install“, {“scene\_id”:&lt;scene\_id&gt;,
“file\_size”:&lt;file-size&gt;,”file\_adler32”:&lt;file\_adler32\_hex&gt;,
“encoding”:”hex”}}\\n&lt;scene-file&gt;**

**with **

**&lt;scene\_id&gt; numeric id of scene**

**&lt;length&gt; file size in bytes of the file to be transfered**

**&lt;scene-file&gt; data bytes of the file **

**&lt;file\_adler32\_hex&gt; adler32 checksum of file formated as hex
number**

**“encoding”:”hex” is optional. If not given the data is sended in
binary format**

Response from surface

**{„scene\_install“: “successful”}**

#### play\_scene

Play a scene that is installed on the surface.

The parameters “speed”, “brightness”, “color”, “color\_temperature” are
optional.

JSON formatted input

**{„play\_scene“: {“scene\_id”:&lt;scene\_id&gt;,**

**“speed”: &lt;speed\_value&gt;,**

**“brightness”: &lt;brightness&gt;,**

**“color” : \[&lt;color\_value: Red&gt;,&lt;color\_value:
Green&gt;,&lt;color\_value: Blue&gt;,&lt;color\_value: White&gt;\], **

**“color\_temperature”:&lt;color\_temperature&gt;** **}}**

**with &lt;scene\_id&gt; numeric id of scene **

**example:
{"play\_scene":{"scene\_id":1,"speed":"50","color\_temperature":"1500","color":\[9,0,255,0\]}}**

Response from surface

**{„play\_scene“: “successful”}**

#### <span id="__RefHeading___Toc478163975" class="anchor"><span id="__RefHeading__371_594866139" class="anchor"><span id="__RefHeading__314_995001476" class="anchor"></span></span></span>set\_standby

Wake the surface from standby or put the surface in standby mode.

JSON formatted input

**{“set\_standby”: boolean}** with **boolean** in **\[true, false\]**

Response from surface

**{“standby”: boolean}** with **boolean in \[true, false\]**

#### <span id="__RefHeading___Toc478163976" class="anchor"><span id="__RefHeading__373_594866139" class="anchor"><span id="__RefHeading__344_995001476" class="anchor"></span></span></span>check\_key

Send encrypted message to verify key

JSON formatted input

**{“check\_key”, null}**

Response from surface

**{“secret”: “ok”}**

1.  ### 

    ### <span id="__RefHeading___Toc478163977" class="anchor"><span id="__RefHeading__4411_677526150" class="anchor"><span id="__RefHeading__6768_763101493" class="anchor"><span id="__RefHeading__8969_492320541" class="anchor"><span id="__RefHeading__749_1453772314" class="anchor"><span id="__RefHeading__621_1208072552" class="anchor"><span id="__RefHeading__375_594866139" class="anchor"><span id="__RefHeading__170_995001476" class="anchor"><span id="__RefHeading__652_594866139" class="anchor"><span id="__RefHeading__313_451558443" class="anchor"><span id="__RefHeading__2401_866041415" class="anchor"><span id="__RefHeading__1221_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Encryption tool operations

All encryption tool operations can be executed over a non-encrypted
port.

#### <span id="__RefHeading___Toc478163978" class="anchor"><span id="__RefHeading__377_594866139" class="anchor"><span id="__RefHeading__346_995001476" class="anchor"></span></span></span>request\_vis\_key 

Request pairing code (vis-key) to be shown on the surface.

JSON formatted input

**{“request\_vis\_key”, null}**

Response from surface

**{“vis\_key”: “ok”}**

#### check\_touch

Sets surface to touch sensitive mode for user security. Idea is that the
user must be in the same room as the surface so that nobody from outside
the room can initialize the surface. This is an alternative operation to
get the vis-key.

JSON formatted input

**{“check\_touch”: null}**

Response from surface

**{“check\_touch”: &lt;vis-key&gt;}**

**or**

**{“check\_touch”: 'time out'} (if the surface was not touched in a time
frame of 20 seconds)**

### <span id="__RefHeading___Toc478163980" class="anchor"><span id="__RefHeading__4413_677526150" class="anchor"><span id="__RefHeading__6770_763101493" class="anchor"><span id="__RefHeading__8971_492320541" class="anchor"><span id="__RefHeading__751_1453772314" class="anchor"><span id="__RefHeading__623_1208072552" class="anchor"><span id="__RefHeading__2479_866041415" class="anchor"><span id="__RefHeading__1223_19721096" class="anchor"></span></span></span></span></span></span></span></span>Always public operations

Operations that are public and usable always without any encryption

#### get\_serial\_number

Gets the serial number of the surface

JSON formatted input

**{“get\_serial\_number”: null}**

Response from surface

**{“serial\_number”: &lt;serial\_number&gt;}** with **serial\_number is
a String**

#### get\_pub\_info

Gets all available information for this surface. The returned values are
depended on the details of calling this operation. If you call this
operation with the master key it will return all data of this surfaces,
but not the installed scenes.

JSON formatted input

**{“get\_pub\_info”: null}**

Response from surface (this data will always be present)

**{“sec\_mode”: &lt;sec\_mode&gt;, “serial\_number”:
&lt;serial\_number&gt; }** with **&lt;sec\_mode&gt;** in **\[“locked',
“protected', “public''\] and serial\_number is a String**

Response from surface (when using master key):
{"serial\_number":"1F2807F004D7","sec\_mode":"public","scene\_parameters":{"speed":50,"brightness":100,"color":\[0,0,0,0\],"color\_temperature":7000},"surface\_info":{"number\_tiles":30,"serialNumber":"1F2807F004D7","power\_on":true,"width\_tiles":5,"height\_tiles":6,"name":"DEFAULT\_NAME","surface\_runtime":0,"firmware\_version":"V0.0beta"},"allowed\_operations":{"change\_brightness":true,"change\_color\_temperature":true,"change\_speed":true,"standby":true,"change\_scene":true,"change\_color":true},"settings":{"touch\_sensor":true,"proximity\_sensor":true,"ambient\_sensor":true}}

Response from surface (when no key, and surface sec mode is public):
{"serial\_number":"1F2807F004D7","sec\_mode":"public","scene\_parameters":{"speed":50,"brightness":100,"color":\[0,0,0,0\],"color\_temperature":7000}}

**These properties will only be shown when the access rights system
allows access to this information for the user.**

  --------------------- -------------------------------------------------------- ---------
  surface\_info         Information on the surface                               private
                                                                                 
                        See get\_surface\_info                                   

  allowed\_operations   Information on allowed operations                        private
                                                                                 
                        see get\_allowed\_ operations                            

  scene\_parameters     Get the scene parameters of the currently played scene   public
                                                                                 
                        See get\_scene\_parameters                               

  settings              See get\_settings\_operation                             private
  --------------------- -------------------------------------------------------- ---------

### <span id="__RefHeading___Toc478163983" class="anchor"><span id="__RefHeading__4415_677526150" class="anchor"><span id="__RefHeading__6772_763101493" class="anchor"><span id="__RefHeading__8973_492320541" class="anchor"><span id="__RefHeading__753_1453772314" class="anchor"><span id="__RefHeading__625_1208072552" class="anchor"><span id="__RefHeading__379_594866139" class="anchor"><span id="__RefHeading__67_1609929419" class="anchor"><span id="__RefHeading__172_995001476" class="anchor"><span id="__RefHeading__654_594866139" class="anchor"><span id="__RefHeading__315_451558443" class="anchor"><span id="__RefHeading__2403_866041415" class="anchor"><span id="__RefHeading__1225_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span></span>Encryption with AES

The encryption method used is “AES/CFB” with no padding. At the start of
the transmission, an extra iV must be transferred. (We have a demo
encryption application written in Java).

All private functions can only be called using the Master-Key.

Public functions can be performed without encryption if the
security-mode is set to public.

If security-mode (of the surface) is protected, the public functions can
only be performed using the Vis-Key.

All public functions can always be performed with the Master-Key.

<span id="__RefHeading___Toc478163984" class="anchor"><span id="__RefHeading__4417_677526150" class="anchor"><span id="__RefHeading__6774_763101493" class="anchor"><span id="__RefHeading__8975_492320541" class="anchor"><span id="__RefHeading__755_1453772314" class="anchor"><span id="__RefHeading__627_1208072552" class="anchor"><span id="__RefHeading__381_594866139" class="anchor"><span id="__RefHeading__174_995001476" class="anchor"><span id="__RefHeading__656_594866139" class="anchor"><span id="__RefHeading__317_451558443" class="anchor"><span id="__RefHeading__2405_866041415" class="anchor"><span id="__RefHeading__1227_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Web Service Interface (app to server)
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The communication is realized using a REST/HTTPS interface.

### <span id="__RefHeading___Toc478163985" class="anchor"><span id="__RefHeading__4419_677526150" class="anchor"><span id="__RefHeading__6776_763101493" class="anchor"><span id="__RefHeading__8977_492320541" class="anchor"><span id="__RefHeading__757_1453772314" class="anchor"><span id="__RefHeading__629_1208072552" class="anchor"><span id="__RefHeading__383_594866139" class="anchor"><span id="__RefHeading__176_995001476" class="anchor"><span id="__RefHeading__658_594866139" class="anchor"><span id="__RefHeading__319_451558443" class="anchor"><span id="__RefHeading__2407_866041415" class="anchor"><span id="__RefHeading__1229_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Authentication

For authentication with the server basic (HTTP) access authentication is
used.

If the authentication data is not correct the web service will answer
with:

**401 Unauthorized**

### <span id="__RefHeading___Toc478163986" class="anchor"><span id="__RefHeading__4421_677526150" class="anchor"><span id="__RefHeading__6778_763101493" class="anchor"><span id="__RefHeading__8979_492320541" class="anchor"><span id="__RefHeading__759_1453772314" class="anchor"><span id="__RefHeading__631_1208072552" class="anchor"><span id="__RefHeading__385_594866139" class="anchor"><span id="__RefHeading__178_995001476" class="anchor"><span id="__RefHeading__660_594866139" class="anchor"><span id="__RefHeading__321_451558443" class="anchor"><span id="__RefHeading__2409_866041415" class="anchor"><span id="__RefHeading__1231_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Security

The connection between the app and the server is secured with a HTTPS
connection.

1.  ### 

    ### <span id="__RefHeading___Toc478163987" class="anchor"><span id="__RefHeading__4423_677526150" class="anchor"><span id="__RefHeading__6780_763101493" class="anchor"><span id="__RefHeading__8981_492320541" class="anchor"><span id="__RefHeading__761_1453772314" class="anchor"><span id="__RefHeading__633_1208072552" class="anchor"><span id="__RefHeading__425_594866139" class="anchor"><span id="__RefHeading__662_594866139" class="anchor"><span id="__RefHeading__323_451558443" class="anchor"><span id="__RefHeading__2411_866041415" class="anchor"><span id="__RefHeading__1233_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span>Images of scenes

The preview image for a scene, that must be shown in the app, will be
available on the server at the URL /images/&lt;scene\_id&gt;.jpg

The resolution of the preview image is 512x512 pixel.

This resource is available to everyone and not protected by HTTP
authentication.

### <span id="__RefHeading___Toc478163988" class="anchor"><span id="__RefHeading__4425_677526150" class="anchor"><span id="__RefHeading__6782_763101493" class="anchor"><span id="__RefHeading__8983_492320541" class="anchor"><span id="__RefHeading__763_1453772314" class="anchor"><span id="__RefHeading__635_1208072552" class="anchor"><span id="__RefHeading__387_594866139" class="anchor"><span id="__RefHeading__180_995001476" class="anchor"><span id="__RefHeading__664_594866139" class="anchor"><span id="__RefHeading__325_451558443" class="anchor"><span id="__RefHeading__2413_866041415" class="anchor"><span id="__RefHeading__1235_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Operations

#### <span id="__RefHeading___Toc478163989" class="anchor"><span id="__RefHeading__389_594866139" class="anchor"></span></span>URL: /scene/&lt;scene\_id&gt;

(HTTP method) **GET**

Get metadata of the scene.

**(Status) 200 OK**

The scene was found. Return the corresponding SCENE object.

**404 Not found**

There is no scene with the given ID.

This resource is available to everyone and not protected by HTTP
authentication.

1.  #### 

    #### <span id="__RefHeading___Toc478163990" class="anchor"><span id="__RefHeading__391_594866139" class="anchor"></span></span>URL: /scenes

**POST**

Filter all scenes by the given tags.

post data sample: \[{“tag”:”colorful”},{“tag”:”slow”}\]

**200 OK**

Will return the scene\_ids in an array.

Sample: \[38423, 472864\]

**400 Bad Request**

If the request couldn't be fulfilled due to an erroneous array of tags.

1.  #### 

    #### <span id="__RefHeading___Toc478163991" class="anchor"><span id="__RefHeading__393_594866139" class="anchor"></span></span>URL: /scene/buy/&lt;scene\_id&gt; - Not implemented in first version!

POST

Buy the corresponding scene from the scene store.

**TBD**

#### <span id="__RefHeading___Toc478163992" class="anchor"><span id="__RefHeading__395_594866139" class="anchor"></span></span>URL: /scene/fetch/&lt;scene\_id&gt;

**GET**

Download the scene in binary format.

**200 OK**

Will return the scene in binary format.

**403 Forbidden**

If the scene could not be purchased.

**404 Not found**

There is no scene with the given ID.

#### <span id="__RefHeading___Toc478163993" class="anchor"><span id="__RefHeading__397_594866139" class="anchor"></span></span>URL: /user

**PUT (**This PUT operation uses no HTTP-Auth**)**

create new user. Data sent: **USER-CRED object (TBD).**

**200 OK**

User was created. Will return the user\_id.

Sample: {“user\_id”: “12345”}

**409 Conflict**

Something went wrong.

**GET (Uses HTTP-Auth)**

Fetch user settings/data.

**200 OK**

Will return **USER-SETTINGS** object (**TBD**).

**404 Not found**

There is no user with the given id

**POST (Uses HTTP-Auth)**

Upload current user data. Data send: **USER-SETTINGS object** and
**SURFACE\_INFO** **object**. Both objects are sent together in a
JSON-array: \[**USER- SETTINGS object**, **SURFACE\_INFO** **object**\].

Sample: \[{"user\_id":1234},
{"number\_tiles":30,"serialNumber":"TP345223",
"power\_on":true,"width\_tiles":5,"height\_tiles":6,"name":"main room",
"surface\_runtime":0,"firmware\_version":"V2.3beta","playing\_scene\_id":1}\]

**200 OK**

Data was uploaded successfully.

**400 Bad Request**

If the request couldn't be fulfilled due to erroneous data received.

#### <span id="__RefHeading___Toc478163994" class="anchor"><span id="__RefHeading__399_594866139" class="anchor"></span></span>URL: /scenes and /scenes/full

The sub path “full” is used to optionally set the return value type to a
list of full SCENE objects.

**GET**

Get the ids of all scenes of the given user.

If the path full is set a list of full SCENE objects is the returned.

**200 OK**

Will return an array of scene ids.

Sample: \[38423,472864\]

**404 Not found**

There are no scenes for this user

1.  #### 

    #### URL: /autoscenes and /autoscenes/full

    The sub path “full” is used to optionally set the return value type
    to a list of full SCENE objects.

**GET**

Get the ids of all automatic mode scenes of the user.

If the path full is set a list of full SCENE objects is the returned.

**200 OK**

Will return an array of scene ids.

Sample: \[38423,472864\]

**404 Not found**

There are no scenes for this user

#### <span id="__RefHeading___Toc478163996" class="anchor"><span id="__RefHeading__403_594866139" class="anchor"></span></span>URL: /p/user

**POST**

reset user password. Send user-email address.

Data sent: {“pw”:&lt;new\_password&gt;}

Until milestone 4 the password is changed directly without sending a
email.

**200 OK**

Will send email to user with link to reset email. (The server sends the
email)

**404 Not found**

There is no user with the given id or the email address is not matching
the id.

**400 Bad Request**

If the request couldn't be fulfilled due to erroneous data received.

#### URL: / user/forgot/password

Always use fixed credentials here:

Username: "forgotPasswordUser"

Password: "9wmDF%o9B-ur%.Amgs.sf"

**POST**

Will trigger server to send a email to change password in external
webpage.

Data sent: {“ userEMail”:”&lt;email\_of\_user&gt;”}

**200 OK**

Will send email to user with link to reset email. (The server sends the
email)

**404 Not found**

There is no user with the given email address.

**400 Bad Request**

If the request couldn't be fulfilled due to erroneous data received.

#### URL: /diagnostics/

**POST**

send diagnostic data to server. Data send: **DIAGNOSTICS object (TBD).**

#### URL: /firmware/version

**GET **

Get the version number and information on the most recent firmware.

**200 OK**

Will return information on the most recent firmware version.

**404 Not found**

There is no recent firmware

#### URL: /firmware/fetch

**GET **

Get the most recent firmware file for the surface.

**200 OK**

Will return the most recent firmware in binary format

**404 Not found**

There is no recent firmware

Passwords and Keys
------------------

Master Key:

Is a full 128 bit AES key encoded as Hex. This means it is a 32
character hex string. (Possible are 256 bits, but this seems to add
little to security, but makes a manual typing of the code much harder.

Example: 10a58869d74be5a374cf867cfb473859

Vis Key:

Currently a String of 8 characters

Wifi-AP password:

Up to 63 characters

Is initialized with a 16 character string.

Web-Interface password:

Is the same password as the Wifi-AP password

### Persistent Data 

1.  <span id="__RefHeading___Toc478164001" class="anchor"><span id="__RefHeading__4427_677526150" class="anchor"><span id="__RefHeading__6784_763101493" class="anchor"><span id="__RefHeading__8985_492320541" class="anchor"><span id="__RefHeading__765_1453772314" class="anchor"><span id="__RefHeading__637_1208072552" class="anchor"><span id="__RefHeading__405_594866139" class="anchor"><span id="__RefHeading__214_995001476" class="anchor"><span id="__RefHeading__666_594866139" class="anchor"><span id="__RefHeading__327_451558443" class="anchor"><span id="__RefHeading__2415_866041415" class="anchor"><span id="__RefHeading__1237_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>App data storage
    ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

    1.  ### <span id="__RefHeading___Toc478164002" class="anchor"><span id="__RefHeading__4429_677526150" class="anchor"><span id="__RefHeading__6786_763101493" class="anchor"><span id="__RefHeading__8987_492320541" class="anchor"><span id="__RefHeading__767_1453772314" class="anchor"><span id="__RefHeading__639_1208072552" class="anchor"><span id="__RefHeading__407_594866139" class="anchor"><span id="__RefHeading__116_995001476" class="anchor"><span id="__RefHeading__668_594866139" class="anchor"><span id="__RefHeading__329_451558443" class="anchor"><span id="__RefHeading__2417_866041415" class="anchor"><span id="__RefHeading__1239_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Persistent Data 

Data that must be stored on the phone.

- for each surface ever connected: all known keys and other infos on the
surface. This must be permanently stored in a list of SURFACE\_DATA
objects on the phone.

- all scene info data, scene description pictures and scene file in
binary format. This must be done by permanently store a list of
SCENE\_DATA objects on the phone. If a new scene is loaded from the web
service it then must be put into this list. A limit of the used memory
of the list is a nice-to-have feature.

- group information: All groups of surfaces, meaning a list of groups
with names. And for each group all surface-serial numbers of the
surfaces belonging to this group.

### <span id="__RefHeading___Toc478164003" class="anchor"><span id="__RefHeading__4431_677526150" class="anchor"><span id="__RefHeading__6788_763101493" class="anchor"><span id="__RefHeading__8989_492320541" class="anchor"><span id="__RefHeading__769_1453772314" class="anchor"><span id="__RefHeading__641_1208072552" class="anchor"><span id="__RefHeading__409_594866139" class="anchor"><span id="__RefHeading__118_995001476" class="anchor"><span id="__RefHeading__670_594866139" class="anchor"><span id="__RefHeading__331_451558443" class="anchor"><span id="__RefHeading__2419_866041415" class="anchor"><span id="__RefHeading__1241_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Cached Surface Data

Data that can temporarily be stored on the phone, but which should at
least be reloaded if the app connects to a surface. The surface itself
stores this data and other users may have changed it.

- the last known settings (SURFACE\_SETTINGS) and allowed settings
(PUBLIC\_ALLOWED\_OPERATIONS) for *each* surface.

- the list of scenes installed on each surface

<span id="__RefHeading___Toc478164004" class="anchor"><span id="__RefHeading__771_1453772314" class="anchor"><span id="__RefHeading__643_1208072552" class="anchor"><span id="__RefHeading__333_451558443" class="anchor"><span id="__RefHeading__2421_866041415" class="anchor"></span></span></span></span></span>Discovery of Surfaces
=========================================================================================================================================================================================================================================================================================================================================

To acquire the IP address of surfaces a UDP broadcast method is used.

This is done by sending a UDP broadcast packet to the port 0x7FFE
(30718). The packet must contain 0x000000F6 (0,0,0,246).

All surfaces will answer a packet (starting with 0x000000F9
(0,0,0,249)). The IP of the answering surfaces is the IP of the
answering IP device.

<span id="__RefHeading___Toc478164005" class="anchor"><span id="_Ref472447185" class="anchor"><span id="__RefHeading__773_1453772314" class="anchor"><span id="__RefHeading__645_1208072552" class="anchor"><span id="__RefHeading__411_594866139" class="anchor"><span id="__RefHeading__182_995001476" class="anchor"><span id="__RefHeading__672_594866139" class="anchor"><span id="__RefHeading__335_451558443" class="anchor"><span id="__RefHeading__2423_866041415" class="anchor"></span></span></span></span></span></span></span></span></span>Firmware update: data transfer in many packages
=========================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================================

The firmware data transfer to the surface is done in small
packages/chunks of 4KB size. This is done because of data transfer
errors when large files are transmitted.

The firmware update screen must show the progress in a progress bar. The
app must look at the response of the operation. The surface will (after
the first chunk has been transferred) answer with the next chunk number
to be transmitted. The app must then transfer this chunk in the next
call to scene\_install.

After all chunks have been transmitted the system will update itself.
This may take up to 5 minutes.

The App should then call the API operation get\_surface\_info every 15
seconds. While updating there will be no valid answer to the request. If
the app gets a valid answer then the update process is finished.

After app should then show a message “Update finished” and after a touch
on ok the app should leave the firmware\_update screen.

Glossary
========

**Surface (=volaTiles):** the physical smart surface ambient light
system. From the perspective of the app, it’s a single device. The App
is connected to the surface over a WiFi connection.

**Scene:** a file that can be uploaded to the surface and displayed by
the surface. The surface stores the scene files to ensure that it must
not be uploaded again.

**AP:** short for WiFi Access Point.

**Master-Key:** The secret key used to identify the Owner-User. It is a
16-byte code.

**Vis-Key:** This key can be visually displayed on the surface. It is
then used to secure the data transfer of Visitor-Users to the surface.
Size is \~6 bytes.

1.  

    <span id="__RefHeading___Toc478164007" class="anchor"><span id="__RefHeading__775_1453772314" class="anchor"><span id="__RefHeading__647_1208072552" class="anchor"><span id="__RefHeading__674_594866139" class="anchor"><span id="__RefHeading__337_451558443" class="anchor"><span id="__RefHeading__2425_866041415" class="anchor"></span></span></span></span></span></span>Non-functional requirements
    ============================================================================================================================================================================================================================================================================================================================================================================================================

    1.  <span id="__RefHeading___Toc478164008" class="anchor"><span id="__RefHeading__4433_677526150" class="anchor"><span id="__RefHeading__6790_763101493" class="anchor"><span id="__RefHeading__8991_492320541" class="anchor"><span id="__RefHeading__777_1453772314" class="anchor"><span id="__RefHeading__649_1208072552" class="anchor"><span id="__RefHeading__415_594866139" class="anchor"><span id="__RefHeading__186_995001476" class="anchor"><span id="__RefHeading__676_594866139" class="anchor"><span id="__RefHeading__339_451558443" class="anchor"><span id="__RefHeading__2427_866041415" class="anchor"><span id="__RefHeading__1243_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>General
        -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

The keys must not be disclosed to anyone. The app should never show the
keys.

<span id="__RefHeading___Toc478164009" class="anchor"><span id="__RefHeading__4435_677526150" class="anchor"><span id="__RefHeading__6792_763101493" class="anchor"><span id="__RefHeading__8993_492320541" class="anchor"><span id="__RefHeading__779_1453772314" class="anchor"><span id="__RefHeading__651_1208072552" class="anchor"><span id="__RefHeading__417_594866139" class="anchor"><span id="__RefHeading__188_995001476" class="anchor"><span id="__RefHeading__678_594866139" class="anchor"><span id="__RefHeading__341_451558443" class="anchor"><span id="__RefHeading__2429_866041415" class="anchor"><span id="__RefHeading__1245_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>iPhone/iOS compatibility
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

All iPhones ≥ 4

iOS Version ≥ 8

<span id="__RefHeading___Toc478164010" class="anchor"><span id="__RefHeading__4437_677526150" class="anchor"><span id="__RefHeading__6794_763101493" class="anchor"><span id="__RefHeading__8995_492320541" class="anchor"><span id="__RefHeading__781_1453772314" class="anchor"><span id="__RefHeading__653_1208072552" class="anchor"><span id="__RefHeading__419_594866139" class="anchor"><span id="__RefHeading__190_995001476" class="anchor"><span id="__RefHeading__680_594866139" class="anchor"><span id="__RefHeading__343_451558443" class="anchor"><span id="__RefHeading__2431_866041415" class="anchor"><span id="__RefHeading__1247_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Programming style
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

All identifiers and comments in the source code and helper files must be
in English.

Each source code file must be documented at least globally (i.e. in its
head) and shortly explain its purpose and which other parts of the
system use its functionality. Each non-trivial public program element
(such as a method) should be documented (purpose, usage).

<span id="__RefHeading___Toc478164011" class="anchor"><span id="__RefHeading__4439_677526150" class="anchor"><span id="__RefHeading__6796_763101493" class="anchor"><span id="__RefHeading__8997_492320541" class="anchor"><span id="__RefHeading__783_1453772314" class="anchor"><span id="__RefHeading__655_1208072552" class="anchor"><span id="__RefHeading__423_594866139" class="anchor"><span id="__RefHeading__194_995001476" class="anchor"><span id="__RefHeading__682_594866139" class="anchor"><span id="__RefHeading__345_451558443" class="anchor"><span id="__RefHeading__2433_866041415" class="anchor"><span id="__RefHeading__1249_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span></span>Delivery
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

At least every week while to project is active the current state of the
project must be communicated to us (volasystems). This must include the
source files, an executable .ipa file and a written statement naming the
features and their design/implementation state.

<span id="__RefHeading___Toc478164012" class="anchor"><span id="__RefHeading__4441_677526150" class="anchor"><span id="__RefHeading__6798_763101493" class="anchor"><span id="__RefHeading__8999_492320541" class="anchor"><span id="__RefHeading__785_1453772314" class="anchor"><span id="__RefHeading__657_1208072552" class="anchor"><span id="__RefHeading__427_594866139" class="anchor"><span id="__RefHeading__684_594866139" class="anchor"><span id="__RefHeading__347_451558443" class="anchor"><span id="__RefHeading__2435_866041415" class="anchor"><span id="__RefHeading__1251_19721096" class="anchor"></span></span></span></span></span></span></span></span></span></span></span>Demo servers for the API
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

We will provide demo servers for the surface and for the server part.
The app must be capable to communicate with them.
