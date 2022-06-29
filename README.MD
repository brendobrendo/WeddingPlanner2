# ASP.NET CORE SET UP INSTRUCTIONS
Replace {ProjName} with your project's name
## Create New Project
1. In terminal, navigate to where you want your project folder
2. In terminal, enter, `dotnet new mvc --no-https -o ProjName` **Don't forget to change _ProjName_**
3. In terminal, enter, `cd ProjName`
## Install Dependencies
1. In terminal, in your project folder, enter `dotnet add package Pomelo.EntityFrameworkCore.MySql --version 3.1.1`
2. In terminal, in your project folder, enter `dotnet add package Microsoft.EntityFrameworkCore.Design --version 3.1.5` This will add an installed package line to your .csproj file
3. In terminal, in your project folder, enter `code .`
4. If a box that says, "Required assets are missing" click, "Yes" ONLY if we are opening the actual project folder, NOT the parent folder.
## Update DB Name and Password (appsettings.json)
Copy and paste into the appsettings.json file. **Don't forget to change _YOUR-DB-NAME_**
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
## Create ProjectNameContext.cs model (ProjNameContext.cs)
Create a new file under the <sup>Models</sup> project directory.

Name it, ProjNameContext.cs (but replace ProjName with your projects's name. For example, if your project name was, "CatFeeder", name the file, <sup>CatFeederContext.cs<cs>)

This file will direct the ORM to connect each DB table to the correct model/class.

**Remember DbSet properties should be named _plural_. So if the model is Cat, the DbSet name should be Cats**

