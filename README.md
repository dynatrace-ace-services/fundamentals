# Fundamentals for deployment & configuration

✅ Fundamentals for deployment & configuration : [quickstart-ace-configurator](https://github.com/dynatrace-ace-services/quickstart-ace-configurator#readme)  
ITSM integration & SLO Quality of Service : [itsm-integration-with-slo](https://github.com/dynatrace-ace-services/itsm-integration-with-slo#readme)  
Dashboarding Dynatrace Simply Smarter : [slo-simply-smarter](https://github.com/dynatrace-ace-services/slo-simply-smarter#readme)  

![image](https://user-images.githubusercontent.com/40337213/216949405-4b6c513d-b097-4251-882c-ea5b90ab1a52.png)

## Useful links
 - Youtube  : [From zero to hero in 2 minutes](https://youtu.be/vyabfN9zt8c)  
 - Youtube  : [Full demo - From zero to hero](https://youtu.be/irxN7PJd43M)  
 - Dynatrace Blog : [host-group-reconfiguration](https://www.dynatrace.com/news/blog/host-group-reconfiguration-is-now-easier-than-ever-eap/)
 - Dynatrace Doc : [best-practice-tagging-at-scale](https://www.dynatrace.com/support/help/how-to-use-dynatrace/tags-and-metadata/basic-concepts/best-practice-tagging-at-scale)
 - Monaco V2 : [doc](https://www.dynatrace.com/support/help/manage/configuration-as-code)  

## Best practices & configurations
In this QuickStart Ace Configurator you will do : 

1) Define the HostGroup (mandatory) : needs contain 

       "env" and "application name"  
       example : prd_easytravel 

More details on how define HostGroup here: [HostGroup](/HostGroup) (for kube monitoring: HostGroup = KubeName)   

2) Deploy configuration for each application with monaco v2 based on 

       HostGroupName = prd_easytravel
       DomainName = www.easytravel.com

 - Step 1 : install monaco on a tool host (your laptop or an activegate...) [monacov2](https://www.dynatrace.com/support/help/manage/configuration-as-code/installation)
 - Step 2 : configure the [manifest.yaml](https://github.com/dynatrace-ace-services/dynatrace-lab/blob/main/manifest.yaml)
 - Step 3 : create your template monaco [example](https://github.com/dynatrace-ace-services/dynatrace-lab/tree/main/project)
 - Step 4 : deploy with monaco [doc](https://www.dynatrace.com/support/help/manage/configuration-as-code):
 
       ./monaco deploy manifest.yaml  

DIY :   
 - [create a free trial](https://www.dynatrace.com/signup/)
 - [install easytravel](https://community.dynatrace.com/t5/Start-with-Dynatrace/easyTravel-Documentation-and-Download/td-p/181271)
 - install OneAgent with HostGroup = prd_easytravel
   ![image](https://user-images.githubusercontent.com/40337213/233843254-384624e3-e6a4-4932-bde8-813531561bdd.png)
 - [run the monaco template](https://github.com/dynatrace-ace-services/dynatrace-lab/tree/main/project)

Old template [monacoV1]
