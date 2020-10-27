Azure SQL Database: Daily Database Restore to Copy Database
===========================================================

            

**Summary:**


The purpose of this PowerShell workflow is to demonstrate how to programatically restore a database daily to a new copy database with day old data. This workflow will take a specified database and delete the copy of the database (if the copy exists) then
 restore from the database to a new copy. The restore capability used is point in time restore. In this example I restore to 24 hours prior to the current time. One usecase for this workflow is for refreshing a copy of a database with the previous day's data
 on a schedule. By leveraging Azure Automation's scheduling capabilities, this workflow can be automated to run every day.


**Prerequisites:**


This workflow is intended to be used with Azure Automation. To use this make sure you set up an Automation Account and configure the appropriate permissions.


The guide for setting up Azure Automation using Azure Active Directory can be found here: [http://azure.microsoft.com/blog/2014/08/27/azure-automation-authenticating-to-azure-using-azure-active-directory/](http://azure.microsoft.com/blog/2014/08/27/azure-automation-authenticating-to-azure-using-azure-active-directory/)

 

        
    
TechNet gallery is retiring! This script was migrated from TechNet script center to GitHub by Microsoft Azure Automation product group. All the Script Center fields like Rating, RatingCount and DownloadCount have been carried over to Github as-is for the migrated scripts only. Note : The Script Center fields will not be applicable for the new repositories created in Github & hence those fields will not show up for new Github repositories.
