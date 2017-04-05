# msbuild-run-yourcode-before-or-after-build
Run your code before/after build project with Visual Studio.

## What is this sample.

This sample explain how to use `UsingTask` element of MSBuild project file.  
This is just one of many MSBuild features.

## Source file

Source file of this example is `src/inject-tasks/msdn-task-samples.xml`.

This file designed for running tasks before/after other project's build.
In the other words, this example DOES NOT explain how to create project file for MSBuild to build c#,vb or other source from zero.

## How to use this sample to your Solution/Project

To apply this example to your project.

* Create solution and project with Visual Studio.
* In solution explorer, create new solution folder.
* In windows explorer, create folder. (because creating solution folder will not create file system folder).
* In windows explorer, Put msdn-task-samples.xml to that folder.
* In solution explorer, right click solution folder and select add then select add existing item.
* Select msdn-task-samples.xml you copied with dialog.
* Save and close solution.
* Open your project file (like .csproj, NOT msdn-task-samples.xml) with your favorite text editor ( ex: VScode, Notepad++, Atom ...).
* Put following line before `</Project>`:  
  `<Import Project="..\[folder you named]\msdn-task-samples.xml" />`  
  replace `[folder you named]` to your file system folder name you created.
* Open solution with Visual Studio.
* Select `Rebuild solution` under the Build menu.
* see Build output.

note: You can name solution folder and file system folder you like.  
note: Each name does NOT have to be the same.  

## Why create this

Main reason of create this is to learn how to create helper for NuGet restoring process.

## Reason of Unlicense

It has been published as a document.
