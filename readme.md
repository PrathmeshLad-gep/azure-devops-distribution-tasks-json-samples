
# Introduction
DES Azure Distribution Tasks is a set of Build and Release tasks to distribute one or more Taskgroups, variablegroups and service connections to one or more Azure DevOps Team Projects within the same organisation.

This git repository basically created to give sample reference files in order to create your own taskgroups, variablegroups and Azure DevOps service connections to communicate with external system. There are two ways to use this extension i.e. Classic UI pipeline and Pipeline as a code(yaml). I have already written documentation on Classic UI approach here i have explained using pipeline as a code.   

This extension displays the dashboard summary of distributed taskgroups, variablegroups and service connection after extecution of pipelines.

## Classic Pipelines

<img src="https://abnamro-des-azure.gallerycdn.vsassets.io/extensions/abnamro-des-azure/des-azure-distribution-tasks/11.0.45/1578317616692/content/Screenshot-0.png" alt="Classic UI Pipeline Tasks" style="float: left; margin-right: 10px;" />

## Pipeline as a Code

<img src="Images/1-vg-distribution-folder-all-projects.png" alt="Pipeline as a Code Tasks" style="float: left; margin-right: 10px;" />

# Azure Pipelines

[![Build Status](https://dev.azure.com/csharpdocs-github/GitHub/_apis/build/status/Yaml/csharpdocs.azure-devops-distribution-tasks-json-samples?branchName=master)](https://dev.azure.com/csharpdocs-github/GitHub/_build/latest?definitionId=3&branchName=master)

# Azure DevOps Marketplace

Download and install [DES Azure Distribution Tasks](https://marketplace.visualstudio.com/items?itemName=ABNAMRO-DES-AZURE.DES-Azure-Distribution-Tasks) extension from [Microsoft Azure DevOps Marketplace](https://marketplace.visualstudio.com) and install in your organization.

# FAQ's

1. Question: While running pipeline few taskgroup(s) are failed for few project(s)
   </br>Answer: Please refer the taskgroup execution summary and run execution for specific projects and specific teams OR run the same execution again.

1. Question: While running pipeline projects failed due to "Access denied" permission while distributing taskgroups 
   </br>Answer: This error occurs due to you allowed Deny Contributor Edit Permission for taskgroups. In this case you need to Allow contributer permission for failed taskgroups. This can be achieved by changing contributor security permission to Allow

1. Question: While running pipeline projects failed due to "No task definition found matching ID 'GUID' " error
   </br>Answer: You need to check the version and support is available for specific task. Go to https://dev.azure.com/your_organization/your_project/_taskgroups link and import failed taskgroup and save to local hard disk and find the matching GUID mentioned in error. double check that version and update the taskgroup GUID      

1. Question: Do you have plans to provide standard continuous integration taskgroups for various technologies like Java, .Net,          Angular, Node, SQL Server, Testing etc.     
   </br>Answer: No. I dont have any plans to provide it. The given taskgroups are for reference only. I will try to implement all services connections for reference in near future along with current(Splunk and SonarCloud). I never recommend to use Classic UI build pipelines to developers. I would strongly recommend Pipeline as a Code(Yaml).

 1. Question: I want to contribute for this extension.
    </br>Answer: Unfortunetely, we have not published the source code for extension however I would be glad if you could help us to create various service connection json files via pull request.

 1. Question: What type of service connection authorization scheme example this repository explains
    </br>Answer: Please refer below table for authorization schemes covered </br>
         | Service Connection Name | Authorization Scheme | Useful for other types of connection |
         |---|---|---|
         | SonarCloud | Token | To be update |
         | Splunk | UsernamePassword | To be update |   
         | Azure Resource Manager | ServicePrincipal | To be update |

 # Support  
   [Csharpdocs.com](www.csharpdocs.com) continuously seeking feedback about extension so that we can improve our extension. I encourage you to provide feedback on Microsoft DevOps marketplace [DES Azure Distribution Tasks](https://marketplace.visualstudio.com/items?itemName=ABNAMRO-DES-AZURE.DES-Azure-Distribution-Tasks&ssr=false#qna)
