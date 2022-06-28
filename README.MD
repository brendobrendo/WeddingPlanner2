# ASP.NET CORE SET UP INSTRUCTIONS
Replace {ProjName} with your project's name
## Create New Project
- 1.) In terminal, navigate to where you want your project folder
- 2.) In terminal, enter, `dotnet new mvc --no-https -o ProjName`
- 3.) In terminal, enter, `cd ProjName`
## Install Dependencies
- 1.) In terminal, in your project folder, enter `dotnet add package Pomelo.EntityFrameworkCore.MySql --version 3.1.1`
- 2.) In terminal, in your project folder, enter `dotnet add package Microsoft.EntityFrameworkCore.Design --version 3.1.5` This will add an installed package line to your .csproj file
- 3.) In terminal, in your project folder, enter `code .`
- 4.) If a box that says, "Required assets are missing" click, "Yes" ONLY if we are opening the actual project folder, NOT the parent folder.
## Update DB Name and Password (appsettings.json)
Copy and paste into the appsettings.json file, 
```
{
  "Logging": {
    "LogLevel": {
      "Default": "Information",
      "Microsoft": "Warning",
      "Microsoft.Hosting.Lifetime": "Information"
    }
  },
  "AllowedHosts": "*",
  "DBInfo": {
    "Name": "MySqlConnect",
    "ConnectionString": "server=localhost;userid=root;password=rootroot;port=3306;database=YOUR_DB_NAME;SslMode=None"
  }
}
```