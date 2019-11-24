# BitSignificant CSharp

## 0. Getting Started with Your Integrated Development Environment (IDE) and .NET Setup

### In order to begin this course there are a few programs we need to download first:  

#### 1. [Visual Studio Code](https://code.visualstudio.com/)  
This will be our IDE for this course, it's a free and extremely flexbile IDE with a lot of community support making it one of the most preferred IDEs. 

#### 2. The [.NETCore SDK](https://dotnet.microsoft.com/download/dotnet-core)
Since we are going to be learning C# we are also going to use its official framework and run-time, called .NET. This framework makes writing C# much faster and the run-time helps us by managing things that aren't always nice to manage on our own, like memory allocation and deallocation.  
.NETCode is also the newest iteration of the .NET framework from Microsoft.

#### 3. [C# Extension for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-vscode.csharp)
This is a C# extenstion for our IDE and it helps with syntax highlighting so we can easily distinguish between certain statements and keywords, as well as helps us format our code, and avoid silly syntax errors before running our programs.

*If you do get stuck with these steps please head over to [Get Started with C# and Visual Studio Code](https://docs.microsoft.com/en-us/dotnet/core/tutorials/with-visual-studio-code) for detailed documentation.*

#### Once you've installed everything you can following the below instructions to make sure everything is installed correctly:
1. Open a command prompt window or Windows Powershell and type `dotnet` (close any existing open terminal windows)
2. Create a folder where you want to keep all your projects you create in this course, this can be anywhere, for simplicity you can create a folder under the root of your C drive: `C:\csharp-projects` 
3. In your newly created folder create another folder called `dotnet-test`
4. Open your folder `dotnet-test` in Visual Studio Code, navigate to View -> Integrated Terminal (shortcut is _Ctrl + `_), and type the following in the terminal which will create a new dotnet console project:  
```
dotnet new console
```
You will see some files automagically created for you, a `HelloWorld.cs` file and a `HelloWorld.csproj` file. Don't worry about what those files mean for now, we'll explain those later!  
In your terminal type the following two commands and run it:  
```
dotnet restore  
dotnet run
```  
You should see the following output in your terminal:
```
Hello World!
```
  
*Everything is working! You're all set to continue to the next section.*