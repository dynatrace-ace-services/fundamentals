# Fundamentals for deployment & configuration

✅ Fundamentals for deployment & configuration : [fundamentals](https://github.com/dynatrace-ace-services/fundamentals/blob/main/README.md) & [monaco example](https://github.com/dynatrace-ace-services/dynatrace-lab/tree/main/project)  
ITSM integration & SLO Quality of Service : [itsm-integration-with-slo](https://github.com/dynatrace-ace-services/itsm-integration-with-slo#readme) & [monaco-template](https://github.com/dynatrace-ace-services/itsm-integration-with-slo/tree/main/monaco-template)    
Dashboarding Dynatrace Simply Smarter : [slo-simply-smarter with monaco template](https://github.com/dynatrace-ace-services/slo-simply-smarter#readme)  

![image](https://user-images.githubusercontent.com/40337213/216949405-4b6c513d-b097-4251-882c-ea5b90ab1a52.png)

## Useful links
 - Youtube  : [From zero to hero in 2 minutes](https://youtu.be/vyabfN9zt8c)  
 - Youtube  : [Full demo - From zero to hero](https://youtu.be/irxN7PJd43M)  
 - Dynatrace Blog : [host-group-reconfiguration](https://www.dynatrace.com/news/blog/host-group-reconfiguration-is-now-easier-than-ever-eap/)
 - Dynatrace Doc : [best-practice-tagging-at-scale](https://www.dynatrace.com/support/help/how-to-use-dynatrace/tags-and-metadata/basic-concepts/best-practice-tagging-at-scale)
 - Monaco V2 : [doc](https://www.dynatrace.com/support/help/manage/configuration-as-code)  

## 1) Define the HostGroup (mandatory) : needs contain 

       "env" and "application name"  
       example : prd_easytravel 

More details on how define HostGroup here: [HostGroup](/hostgroup.md) (for kube monitoring: HostGroup = KubeName)   

## 2) Create a Management zone for each application with monaco v2 based on 

       HostGroupName = prd_easytravel
       DomainName = www.easytravel.com

 - Step 1 : install monaco on a tool host (your laptop or an activegate...) [monaco V2](https://www.dynatrace.com/support/help/manage/configuration-as-code/installation)
 - Step 2 : configure the [manifest.yaml](https://github.com/dynatrace-ace-services/dynatrace-lab/blob/main/manifest.yaml)
 - Step 3 : create your template monaco : see the full example for "easytravel" [here](https://github.com/dynatrace-ace-services/dynatrace-lab/tree/main/project)
   ![image](https://user-images.githubusercontent.com/40337213/233844339-eb3a682b-de08-4630-abfc-5d647ddca1eb.png)
 - Step 4 : deploy with monaco [doc](https://www.dynatrace.com/support/help/manage/configuration-as-code):
 
       ./monaco deploy manifest.yaml  

## DIY with easytravel and monaco v2:   

 - [create a free trial](https://www.dynatrace.com/signup/)
 - [install easytravel](https://community.dynatrace.com/t5/Start-with-Dynatrace/easyTravel-Documentation-and-Download/td-p/181271)
 - install OneAgent with HostGroup = prd_easytravel
   ![image](https://user-images.githubusercontent.com/40337213/233844181-41f59b62-ca1c-45f0-9744-f786a3a7fc9a.png)
 - [run the monaco template](https://github.com/dynatrace-ace-services/dynatrace-lab/tree/main/project)

## Old template (monaco v1):   

[quickstart configurator](https://github.com/dynatrace-ace-services/quickstart-ace-configurator-monaco-v1)
