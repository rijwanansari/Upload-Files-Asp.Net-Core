# Upload Single or Multiple Files in Asp.Net Core Razor Pages
 Upload Single or Multiple Files in Asp.Net Core Razor Pages
 https://rijsat.com/2021/04/27/upload-single-or-multiple-files-in-asp-net-core-razor-pages-with-insights/
<br> Check this site for step by step details <br>
 In this article, I will explain some file upload insights and show how to upload single or multiples in app.net razor pages. I will cover following points
-	File Upload approaches: Buffering and Streaming
-	File upload security concerns
-	File Upload Storage options
-	Upload Single File in asp.net core razor pages  
-	Upload Multiple files 
-	Storing files in physical storage and database 
# File Upload Approaches: Buffering and streaming
Generally, buffering and streaming are the two scenarios to upload files in asp.net.  <br>
Buffering upload files by reading entire file into an IFormFile. This upload option increases the demand of resources like disk, memory based on file size and numbers in simultaneous uploads. It is recommended for small size file. Warning: the site may crash if we upload too many files using this buffering option.
IFromFile represents a file sent with HttpRequest.<br>
Streaming is another option to upload file which reduces the utilization of resources like disk or memory during the uploads. In this option, the application send file via multipart request and the file is directly saved or processed which does not enhance the performance. It is generally used for large files.
# Security concerns during files upload
File upload is always vulnerable if proper security is not applied to applications. File upload is an opportunity for attackers to upload viruses and malware, break the servers and networks security, run denial of service attacks. <br>
To overcome the above issues and reduce the attach we can take following steps
-	Always validate the file types and extension
-	Rename the file and use safe name, example use GUID for file name
-	Keep storage location into another dedicated storage and non-system storage.
-	Do not upload into app tree folder
-	Validate files in both client and server side. It is easy to break client validation.
-	Limit the file size while uploading. Always check the file size before upload
-	Only allow the required file extension (exclude like exe)
-	Do not replace or overwrite the existing file with new one
-	Use a virus/Malware scanner to on file before upload
-	Validate user before uploading files
-	Keep proper logs during file upload
-	Always grant read and write permission to the location but never execute permission.
# Storage options for Uploaded File
Commonly, there are three storage choices for files: Physical, Database, Data Storage service<br>
Physical Storage: this storage option means to store in file storage or network share. Mostly, we create a folder and store the file over there. This is quite easy to implement, however, it is always recommended to keep the logs and records in database for user access and view purposes. It is expensive compared to database storage; however, this option allows to store large files which might be restricted in database. Then again, this storage cost less than cloud data storage.<br>
Database Storage: This option is quite convenience over the physical storage and is recommended for small files. This is economical compared to both physical and data storage service. It also easy for implementation as we can retrieve the file content from database directly.<br>
Data Storage service (cloud storage service): this storage is option highly scalable and recommended for large storage infrastructures. Example: Azure Blog Storage.<br>
# Prerequisites
-	Visual studio (I will be using visual studio 2019 for this demo)
-	.Net 5 (asp.net core 5.0)
Check this link for step by step implementation
 https://rijsat.com/2021/04/27/upload-single-or-multiple-files-in-asp-net-core-razor-pages-with-insights/
