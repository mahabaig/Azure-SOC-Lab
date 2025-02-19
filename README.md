# Azure SOC Lab

## Objective
The Azure SOC Lab project aimed to create a hands-on environment for simulating security operations center (SOC) tasks using Azure resources. The project involved setting up an Azure Virtual Machine (VM) as a honeypot, configuring centralized logging, and using Microsoft Sentinel for security log analysis and attack detection. The primary goal was to develop a deeper understanding of how to use SIEM tools, like Sentinel, and strengthen skills in log analysis, query building, and attack detection.

### Skills Learned
- Gained practical experience in setting up and configuring Azure resources, including Virtual Machines and Sentinel.
- Developed skills in creating and managing a centralized logging system using Azure Log Analytics.
- Proficient in writing and executing KQL (Kusto Query Language) queries for security log analysis.
- Learned how to correlate logs with geolocation data for improved attack detection.
- Gained hands-on experience in using Microsoft Sentinel for detecting and investigating security events.

### Tools Used
- **Azure** for virtual machine setup and resource management.
- **Microsoft Sentinel** for log management, analysis, and creating security workbooks.
- **Log Analytics Workspace (LAW)** for aggregating and querying security logs.
- **KQL (Kusto Query Language)** for querying logs in Sentinel.
- **GeoIP watchlist** for enriching security logs with geographic location data.

## Steps
1. **Create Azure Subscription**
<img width="1461" alt="Screenshot 2025-02-18 at 2 54 54 AM" src="https://github.com/user-attachments/assets/13bab287-2341-4a5d-b943-03e9205952a7" />

2. **Create the Honey Pot (Azure Virtual Machine)**  
   Set up a Windows 10 VM in Azure and configure it with an open firewall to act as a honeypot.
   
<img width="1466" alt="Screenshot 2025-02-18 at 3 02 27 AM" src="https://github.com/user-attachments/assets/ea1073ce-2fae-441b-8c82-b5b374575eb7" />


   *Ref 2: Configuring Network Security Group and VM firewall settings*

4. **Logging into the VM and Inspecting Logs**  
   Simulate failed login attempts and check the security logs in Event Viewer to identify the failed logins.
   
   ![Step 3: Inspecting Logs](https://path-to-your-screenshot.com)

   *Ref 3: Reviewing security logs for failed login attempts (Event ID 4625)*

5. **Log Forwarding and KQL**  
   Set up a Log Analytics Workspace (LAW) and connect Microsoft Sentinel to forward and analyze logs from the VM.

   ![Step 4: Log Forwarding](https://path-to-your-screenshot.com)

   *Ref 4: Configuring Log Analytics Workspace and Sentinel instance*

6. **Log Enrichment and Finding Location Data**  
   Enrich the logs with geolocation data using a GeoIP watchlist to better understand the geographic origin of security events.

   ![Step 5: GeoIP Enrichment](https://path-to-your-screenshot.com)

   *Ref 5: Enriching logs with GeoIP information to visualize attack locations*

7. **Attack Map Creation**  
   Use Sentinel’s workbook feature to create a visual attack map based on the enriched logs.

   https://portal.azure.com/#view/AppInsightsExtension/WorkbookViewerBlade/ComponentId/%2Fsubscriptions%2F28376de7-0e82-43ca-8488-5f62dfcbadd5%2Fresourcegroups%2Frg-soc-lab%2Fproviders%2Fmicrosoft.operationalinsights%2Fworkspaces%2Flaw-soc-lab-0001/ConfigurationId/%2Fsubscriptions%2F28376de7-0e82-43ca-8488-5f62dfcbadd5%2Fresourcegroups%2Frg-soc-lab%2Fproviders%2Fmicrosoft.insights%2Fworkbooks%2Fc6f11c22-e2ed-47b6-9994-a2ca4389401e/Type/sentinel/WorkbookTemplateName/Windows%20VM%20Attack%20Map

   *Ref 6: Creating an attack map in Sentinel to visualize attack patterns*
