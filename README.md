# RunClubManager
![RunClubManager](https://github.com/nikolayshangov/runclubmanager/assets/100240526/2fc4b726-fbf8-415a-af3c-b165aaabba52)
##### Web application to serve as a management system for running clubs, their races, and tracking the personal statistics of the users.

## Description
##### Project for "IT Carrer" National Programme of the Ministry of Education and Science (MES) [Module 13 - "Software Engineering"]

### Details
##### This application is capable of adding clubs and running races with specific image, place and type. Registered users can edit their own profiles, create races and clubs or edit/delete their own ones and see statistics of other runners. Unregistered users can see registered users' clubs and races and are not able to see statistics of the other runners. The project relies on external service providers, it is accessing them via their API which requires authentication, the application won't be fully functional without them.

## Installation
##### - Download RunClubManager.dacpac <a href="https://github.com/nikolayshangov/runclubmanager/blob/master/CustomDatabase/RunClubManager.dacpac">[from RunClubManager's GitHub Repository]</a>
##### - Start Visual Studio and open SQL Server Object Explorer.
##### - Locate your SQL Server Instance and expand it to Databases then right-click, press Publish Data-tier Application.
##### - Select RunClubManager.dacpac, make sure Database Name, Publish Script Name are called RunClubManager, then click on Publish.
##### - Download the Code from GitHub, open the project and go back in SQL Server Object Explorer.
##### - Right-click on your SQL Server Instance, click on Properties, find Connection string, copy it and paste it in `appsettings.json`:
```json
{
  "ConnectionStrings": {
    "DefaultConnection": "ReplaceWithConnectionString"
  }
```
##### - Get your CloudName, API Key, API Secret from Cloudinary and paste them in `appsettings.json`:
```json
  "CloudinarySettings": {
    "CloudName": "ReplaceWithYourCloudName",
    "ApiKey": "ReplaceWithYourApiKey",
    "ApiSecret": "ReplaceWithYourApiSecret"
  },
```
##### - Get your Token from IPinfo and paste it in `Controllers/HomeController.cs`:
```
var ipInfo = new IPInfo();
var homeViewModel = new HomeViewModel();
try
{
    string url = "https://ipinfo.io?token=ReplaceWithYourToken";
    var info = new WebClient().DownloadString(url);
```

### Required software, files and API
##### - .NET 6.0
##### - SQL Server 2022 (Express or Developer Edition)
##### - SQL Server Management Studio 20.1 (SSMS)
##### - Visual Studio 2022 (Community, Professional or Enterprise Edition)
##### - Custom Database (RunClubManager.dacpac) <a href="https://github.com/nikolayshangov/runclubmanager/blob/master/CustomDatabase/RunClubManager.dacpac">[from RunClubManager's GitHub Repository]</a>
##### - Cloudinary Account (for CloudName, API Key, API Secret)
##### - IPinfo Account (for Token)

## Built with
#### Programming Languages and Tools
##### - C#
##### - SQL Server
##### - ASP.NET Core Model-View-Controller (MVC) [used Views, Identity, Controller, Dependency Injection for Services]
##### - Entity Framework Core
##### - Javascript
##### - JSON
##### - Bootstrap (Jumbotron) [used Album Example, Wider Cards for Thumbnails]
##### - Cloudinary (.NET SDK)
##### - IPinfo (.NET SDK)

### Screenshots
#### Pages
##### - Home (Logged out)
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/a7919ada-09a1-4f6f-865b-ac830a7c3251)
##### - Races (Logged out)
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/3e529d66-d87b-48c1-bed4-adbbdc2c03ab)
##### - Clubs (Logged out)
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/e6342180-6e73-48f8-995f-a8f305315e04)
##### - Register (Logged out)
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/7f0d3881-feb6-4b5e-812b-555d305dc5f6)
##### - Login (Logged out)
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/9a5eb8af-9f06-405f-b634-aabe4bea9b34)
#### Pages with Special Access
##### - Runners (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/efbebdca-71a7-47f8-8f8f-55cb23a04abf)
##### - Dashboard (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/e892ddc7-ea90-4510-8002-131a79a3a7c2)
##### - Edit Account (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/49dcbbe2-75b4-4435-a8c8-82028a164204)
##### - Create Club (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/8f901bc2-02fd-491d-8131-97ba94fc7b03)
##### - Delete Club (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/c89c6857-c80f-49ae-afa9-443678a65356)
##### - Create Race (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/990cb33c-5948-48b5-84b9-d0f77109a378)
##### - Delete Race (Logged in) [Administrator/User]
![image](https://github.com/nikolayshangov/RunClubManager/assets/100240526/a9bc4446-735c-4792-8f47-a54c263883e8)

## Team
### Leader
##### - Nikolay Shangov ([GitHub Profile](https://github.com/nikolayshangov "Nikolay's GitHub Profile"), [YouTube Account](https://www.youtube.com/@nikolayshangov "Nikolay's YouTube Account"))
#### Members
##### - Kiril Pavlov ([GitHub Profile](https://github.com/KiroBreikabg "Kiril's GitHub Profile"), [Instagram Account](https://www.instagram.com/k.pavlov_05 "Kiril's Instagram Account"))
##### - Gabriela Kirilova ([GitHub Profile](https://github.com/Gabrieella2189 "Gabriela's GitHub Profile"), [Instagram Profile](https://www.instagram.com/g_kirilovaa "Gabriela's Instagram Profile"))
##### - Ivan Vodenicharov ([GitHub Profile](https://github.com/IVanVodenicharov55 "Ivan's GitHub Profile"), [Instagram Account](https://www.instagram.com/ivan_vodenicharov/ "Ivan's Instagram Account"))

###### Note: Members haven't worked on the project. Only on Presentation and Documentation, README by Nikolay Shangov.

## Credits
### Images
##### - <a href="https://unsplash.com/@jennyhill">Jenny Hill</a> on <a href="https://unsplash.com/photos/man-running-on-road-near-grass-field-mQVWb7kUoOE">Unsplash</a>
##### - <a href="https://www.freepik.com/author/mariiaboiko">Mariiaboiko</a> on <a href="https://www.freepik.com/premium-photo/woman-running-autumn-field-sunset-healthy-lifestyle-concept-active-sportive-people-close-up-legs_18210801.htm">Freepik</a>
##### - <a href="https://unsplash.com/@chanderr">Chander R</a> on <a href="https://unsplash.com/photos/man-in-yellow-tank-top-running-near-shore-z4WH11FMfIQ">Unsplash</a>
##### - <a href="https://www.youtube.com/@TeddySmithDev">Teddy Smith</a> on <a href="https://www.youtube.com">YouTube</a>
##### - <a href="https://unsplash.com/@knowjack">Jack Atkinson</a> on <a href="https://unsplash.com/photos/boy-in-white-t-shirt-and-blue-shorts-running-on-gray-concrete-road-during-daytime-CUfDlYxZx8I">Unsplash</a>
##### - <a href="https://unsplash.com/@amutiomi">Miguel A Amutio</a> on <a href="https://unsplash.com/photos/people-running-on-gray-asphalt-road-during-daytime-Y0woUmyxGrw">Unsplash</a>

#### Creators
##### Copyright &copy; 2024 Nikolay Shangov, Kiril Pavlov, Gabriela Kirilova and Ivan Vodenicharov.

## License
##### RunClubManager is distributed under the MIT License, see the file LICENSE for more details.
