# Example of using Blazor to execute C# algorithms  compiled to WASM in browser (without any UI)

### Case
You have some calculation logic (probably financial), you have to run it on the server (since you can never trust a client 100%), but you would also like to run an estimation on the client. You want to avoid code duplication, especially between different languages, so you want to run same code in both cases. 

### Solution
This small project showcases how to run C# code compiled to WASM via Blazor project. In particular, it gets rid of any UI stuff and focuses on only loading the assemblies needed to invoke your methods from code. This code is adapted from one of the built-in samples of razor, look at commit history to see, what exactly was removed and added.

### How to run
You will need .NET Core 3.0 SDK, Visual Studio Code https://code.visualstudio.com/docs/languages/dotnet .
Clone repo, go to its root folder and execute `dotnet run`. Follow output of this command, navigate to ` http://localhost:5000/` in the browser (latest Edge / Chrome / other WASM supporting browser). Open DEV tools before loading the page, there is a `debugger` in relevant code. 

###  More info on Blazor
Getting started 
https://docs.microsoft.com/en-us/aspnet/core/blazor/get-started?view=aspnetcore-3.0&tabs=visual-studio
Interop C#=>JS and JS=>C#
https://docs.microsoft.com/en-us/aspnet/core/blazor/javascript-interop?view=aspnetcore-3.0
