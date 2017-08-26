# DevExpress End-User Documentation

This **End-User Documentation** targets application end-users and explains how to use UI elements implemented by DevExpress. This information helps software developers create their own help files for projects that incorporate DevExpress technologies.

> For **Developer Documentation with API Reference** see [https://documentation.devexpress.com](https://www.devexpress.com/Support/Documentation/).

## The Scope
DevExpress products for WinForms, WPF and ASP.NET WebForms/MVC. 

## Licensing
By accessing this repository, you agree to be bound by the terms of the [DevExpress End-User Documentation License Agreement](LICENSE.md).

## Two Ways to Browse Content
To browse this repository's content, start with [index.md](index.md).  

We have also compiled this End-User Documentation into a sample website available at [devexpress.github.io/dotnet-eud](https://devexpress.github.io/dotnet-eud/).

## Document Format and Supported Output Types
Documents in this repository are written in markdown. One way to use them is to manually copy required information to your own help file.

The repository also includes a [docfx.json](docfx.json) file, which enables you to convert a set of topics to an HTML website or a PDF file using [DocFX](https://dotnet.github.io/docfx/) and [wkhtmltopdf](https://github.com/wkhtmltopdf/wkhtmltopdf).   

## Build an HTML Website
To create a documentation website for your application:

- Download and install the [latest version of DocFX](https://github.com/dotnet/docfx/releases). 
- Clone the repository to your computer and checkout the branch corresponding to the version of DevExpress controls your application uses. Make sure not to use the **master** branch, which represents the version currently under development.
    ```
    git clone https://github.com/DevExpress/dotnet-eud.git --branch 17.1
    ```
  If you do not have [Git](https://git-scm.com/) installed, select the required branch using the GitHub web interface and then download and extract the ZIP archive.
  
  ![Download ZIP](https://user-images.githubusercontent.com/20167812/29712204-4ffaee9e-89a1-11e7-8a0e-3ff0464adda4.png)
- If you want to reuse the end-user documentation as is, skip this step. Otherwise, make changes as required, which may include:
  - removing files that are not needed in your documentation;
  - adding new documents specific to your application;
  - changing screenshots to match your app UI;
  - creating a [custom DocFX template](https://dotnet.github.io/docfx/tutorial/howto_create_custom_template.html).
  > Make sure to update *toc.yml* ([table-of-content](https://dotnet.github.io/docfx/tutorial/intro_toc.html)) files if you have added or removed topics.
- Open a console window, change the current directory to the repository root folder and call the DocFX executable with the *build* and *docfx.json* parameters. DocFX will place the generated documentation content into the *\_site* folder. Add the *--serve* switch to preview the generated website at http://localhost:8080 once the build process is complete. 
    ```
    docfx.exe build docfx.json --serve
    ```
- Finally, deploy the created documentation to a web server or browse the documentation directly from local file system. Since DocFX creates static HTML files only, no additional deployment or configuration steps are required.

## Build Printer-Friendly PDF Files
If your end-users require a printed version, you can create a PDF file:
- Ensure that you can successfully build a website with DocFX (see the [previous section](#build-your-own-documentation-website)).
- Download and install [wkhtmltopdf](https://wkhtmltopdf.org/downloads.html).
- Open a console window and add the **wkhtmltopdf** executable path to the %PATH% environment variable:
    ```
    set PATH=%PATH%;C:\Program Files\wkhtmltopdf\bin
    ```
- Change the current directory to the repository root folder and call the DocFX executable with the *pdf* and *docfx.json* parameters. This will generate a *_pdf* subfоlder with a PDF file for each included table-of-contents file.
    ```
    docfx.exe pdf docfx.json
    ```

## Obtain End-User Documentation for Versions Prior to 17.1
This repository provides help files for DevExpress versions 17.1 and above. End-user documentation for previous versions is published in CHM and PDF formats at https://www.devexpress.com/Support/Documentation/download.xml?platform=user-dev-docs.
