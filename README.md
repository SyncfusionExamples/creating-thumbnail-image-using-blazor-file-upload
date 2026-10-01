# Create Thumbnail Images Using Syncfusion Blazor File Upload

## Overview

This sample demonstrates how to use the Syncfusion [Blazor File Upload](https://www.syncfusion.com/blazor-components/blazor-file-upload) component to upload image files and automatically generate thumbnail images on the server. When a user selects a file, the application reads the uploaded stream, creates a reduced-size thumbnail image, and saves the generated image into the application's web root folder.

The sample shows a practical upload-processing workflow that can be used for profile photos, image galleries, content management systems, and other scenarios where smaller preview images are required to improve performance and storage efficiency.

## Key Features

- Uses the `SfUploader` component from `Syncfusion.Blazor.Inputs`.
- Handles file selection through the `OnChange` event.
- Processes uploaded files using `UploadChangeEventArgs`.
- Accesses uploaded content with `file.File.OpenReadStream(long.MaxValue)`.
- Reads image data into a `MemoryStream`.
- Creates thumbnail images using `System.Drawing.Image.GetThumbnailImage(...)`.
- Saves generated thumbnail files by combining paths with `Path.Combine(...)`.
- Stores created thumbnail images in the application's `wwwroot` directory.
- Uses uploaded file metadata through `file.FileInfo.Name`.

## Prerequisites

- [Visual Studio 2022](https://visualstudio.microsoft.com/vs/) or [Visual Studio Code](https://code.visualstudio.com/)
- [.NET SDK](https://dotnet.microsoft.com/en-us/download/dotnet) compatible with the project's target framework

## How to Run the Project

**Visual Studio 2022**

1. Clone or download the repository.
2. Open the solution file:

   `UploaderServer.sln`

3. Restore NuGet packages.
4. Ensure the `UploaderServer` project is selected as the startup project.
5. Build the solution.
6. Run the application using `Ctrl+F5`.
7. Navigate to the URL displayed by the application launch profile.

**Visual Studio Code**

1. Clone or download the repository.
2. Open the repository folder in Visual Studio Code.
3. Navigate to the project directory.

```bash
cd UploaderServer
dotnet restore
dotnet run
```

4. Open the URL displayed in the terminal after the application starts.

## Project Structure

`Pages/Index.razor` - Primary sample page containing the uploader implementation and thumbnail-generation logic.

## Support and Feedback

- For general product questions, visit the [Syncfusion Community Forum](https://www.syncfusion.com/forums) or [Syncfusion Support](https://www.syncfusion.com/support).
- To report an issue specific to this sample, open a GitHub issue in this repository.
- Documentation for the Syncfusion Blazor File Upload component: https://blazor.syncfusion.com/documentation/file-upload/getting-started

## License

This is a Syncfusion sample project provided to demonstrate product usage. Review the [Syncfusion license terms](https://www.syncfusion.com/sales/pricing?category=ui-components) before using Syncfusion components in your own applications.