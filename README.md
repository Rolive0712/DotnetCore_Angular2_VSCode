# DotnetCore_Angular2_VSCode
My First Dotnet Core Project using Angular 4 SPA javascript services

*** Prerequisites to install
1) Node.js and npm
2) Visual Studio Code (comes with typescript compiler)
3) .NET Core SDK 2.0+ (comes with ASP.NET Core  - formally known as ASP.NET 5)


** Once all installed,
1) Open VS Code
2) Run command "dotnet new --install Microsoft.AspNetCore.SpaTemplates::*"
   (The use of ::* in the above command requests the latest version.)
3) Run command "dotnet new angular" on the terminal. (With this no need to use yeoman generator anymore)
   This will generate the project for you, preconfigured with ASP.NET Core, Angular, Webpack, TypeScript, C#, ASP.NET Core, and so on
   It will create an Angular 4 App.
4) Run command "dotnet restore" (restore the server-side dependencies)
5) Run command "npm install" (restore the client-side dependencies)
6) Create "polyfills.ts" file and refer in "boot.server.ts" file
7) Run command "dotnet run" (this kick starts "kestrel" which is a very fast in process web server)
8) Browse to http://localhost:<port #> (this will be available on completion of dotnet run)


** for source control
integrate with VSTS
check  "https://github.com/Microsoft/vsts-vscode/blob/master/TFVC_README.md#quick-start"



** for enabling chrome debugging (with Asp.NET core Javascript services)
1) Install "Debugger for Chrome" extension
  To get started, open the Extensions view (Ctrl+Shift+X). When the extension list appears, 
  type 'chrome' to filter the list and install the Debugger for Chrome extension
  config:
  https://github.com/Microsoft/vscode-chrome-debug

2) check 
"https://www.youtube.com/watch?v=keuMHy-O7Ns"
"https://offering.solutions/blog/articles/2016/10/16/how-to-debug-an-angular-application-with-chrome-and-vs-code/"


run command 'set ASPNETCORE_ENVIRONMENT=Development' after every new terminal launch as default is production.
then run "dotnet run"
to set at global level, check https://docs.microsoft.com/en-us/aspnet/core/fundamentals/environments?view=aspnetcore-2.1
on windows 10,
Click the Start orb.
Click Control Panel.
Click System and Security.
Click System.
In the left pane, click Advanced System Settings.
If a UAC window opens, click Yes.
The System Properties dialog box opens.
Click the Advanced tab.


** for enabling chrome debugging (with Angular CLI)
check https://stackoverflow.com/questions/42495655/how-to-debug-angular-with-vscode
Angular CLI way of development creates angular 6 app. confirm this.

** anytime webpack config or vendor files are modified, run commands below
=> webpack --config webpack.config.vendor.js
=> webpack
=> dotnet watch run

