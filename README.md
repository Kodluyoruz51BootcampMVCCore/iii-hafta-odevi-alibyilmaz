# III-hafta-odevi


1.Task vs process- task vs Thread vs .. ve c# task vs thread vs .. kıyaslamalarını ve task haricinde diğer yöntemler nelerdir araştırınız.

#Why we need Tasks
It can be used whenever you want to execute something in parallel. Asynchronous implementation is easy in a task, using’ async’ and ‘await’ keywords.
#Why we need a Thread
When the time comes when the application is required to perform few tasks at the same time.
#Differences Between Task And Thread
 
Here are some differences between a task and a thread.
The Thread class is used for creating and manipulating a thread in Windows. A Task represents some asynchronous operation and is part of the Task Parallel Library, a set of APIs for running tasks asynchronously and in parallel.
The task can return a result. There is no direct mechanism to return the result from a thread.
Task supports cancellation through the use of cancellation tokens. But Thread doesn't.
A task can have multiple processes happening at the same time. Threads can only have one task running at a time.
We can easily implement Asynchronous using ’async’ and ‘await’ keywords.
A new Thread()is not dealing with Thread pool thread, whereas Task does use thread pool thread.
A Task is a higher level concept than Thread.
#Process
process is the set of instruction as code which operates on related data and process has its own various state, sleeping, running, stopped etc. when program gets loaded into memory it becomes process. Each process has atleast one thread when CPU is allocated called sigled threaded program.

2.Extension Nedir? --> Extra paket ekleme. <br/>
An Extension Method is:

It is a static method.
It must be located in a static class.
It uses the "this" keyword as the first parameter with a type in .Net and this method will called by a given type instance on the client side.
It also shown by VS intellisense. When we press the dot (.) after a type instance then it comes in VS intellisense.
An Extension Method should be in the same namespace as it is used or you need to import the namespace of the class by a using statement.
You can give any name of for the class that has an Extension Method but the class should be static.
If you want to add new methods to a type and you don't have the source code for it then the solution is to use and implement Extension Methods of that type.
If you create Extension Methods that have the same signature methods as the type you are extending then the Extension Methods will never be called. 

#example 
```
using System;  
namespace ExtensionMethodsExample  
{  
   public static class Extension  
    {  
       public static int WordCount(this string str)  
       {  
           string[] userString = str.Split(new char[] { ' ', '.', '?' },  
                                       StringSplitOptions.RemoveEmptyEntries);  
           int wordCount = userString.Length;  
           return wordCount;  
       }   
       public static int TotalCharWithoutSpace(this string str)  
       {  
           int totalCharWithoutSpace = 0;  
           string[] userString = str.Split(' ');  
           foreach (string stringValue in userString)  
           {  
               totalCharWithoutSpace += stringValue.Length;  
           }  
           return totalCharWithoutSpace;  
       }  
    }  
}   
``` 
src: https://www.c-sharpcorner.com/UploadFile/3d39b4/extension-method-in-C-Sharp/#:~:text=Extension%20Methods%20are%20a%20new,or%20modify%20the%20original%20types.&text=An%20Extension%20Method%20is%20a%20static%20method%20to%20the%20existing%20static%20class.

3.SQLite, bunu doğru şekilde (en güncel yol ile) nasıl kullanmalıyız? (Aktif halde kullanıp uygulama) 
# repoda
