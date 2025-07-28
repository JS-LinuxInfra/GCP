## Scope
This project contains a variaty of GCP tasks related to various services such as Compute, IAM, APIs, GKE, Spend, etc.

## Environment & Services
- GCP Console
- GCP Cloudshell 
- gcloud CLI
- GCP Compute
- GCP IAM
- GCP API

*******************************************************************************************************************
To-Do
1. Upload remaining GKE screencaptures and document per the above
2. Apply the same process to K8 repo
3. Create folders by task and service for all screen captures, move all images and update pointers, confirm everything looks good
4. Make Linked Post announcing changes and hashtag GCP, K8, Go
5. Finish Udacity GCP course - upload and annotate all
6. Start PluralSite GCP CDL cert course and use format going forward

```
├── README.md
├── Service: Task(s) | Troubleshooting | Building | Log Analysis
│   ├── Console, API & IAM
|   |   └── Review available projects
|   |   └── Create and manage a new principal -> assign desired permissions -> validate they are set per the desired permissions schema
|   |   └── Enable the Dialogflow API -> configure desired permissions -> manage the zones in the region -> export both the project and zone paramaters to variables -> validate
│   ├── Compute
|   |   └── Create a new VM with the desired SKU then configure applicable VARs
|   |   └── Create an RSA keypair -> validate functionality -> install and validate NGINX functionality
|   |   └── Print and configure the active firewall rules for the new VM -> validate browser SSH functionality 
|   |   └── Create and configure additional VMs -> assign to desired zone and region 
|   |   └── Install NGINX on additional VMs -> validate SSH functionality via CloudShell
│   ├── Billing and Spend
|   |   └── Forecast projected spend utilizing a variaty of filtering 
|   |   └── Investigate spend over a specified range -> filtering by service, range, project, SKU, discount, zone and region 
│   ├── APIs and AppEngine service 
│   │   ├── Enable the AppEngine API-> clone the Python repo from GitHub -> update the OS -> configure the Python environment for the web server deployment and scheduled changes to be pushed 
│   │   └── Validate the application's status -> start the web server -> update the Python config file -> confirm change is now live on the web server via browser check
|   |   └── Validate the app has started -> deploy the app to the AppEngine service -> confirm config changes went through and are present as expected via a browser
│   ├── CloudRun
│   │   └── Build, deploy, then test a function
|   |   └── Update the application then validate the WebServer functionality 
|   |   └── Create the repo -> set required permissions per defined standards -> start the build process 
|   |   └── Update the application then validate the WebServer functionality 
|   |   └── Build the Docker image needed for the application -> start required services and deploy to CloudBuild -> validate functionality
|   |   └── Redeploy and test the app with both the default Concurrency of 80 as oncurrency well as 1 for performance analysis 
|   |   └── Build the website update using Docker then push out with zero noticible downtime to enduser
│   ├── GKE
│   │   └── Set both the region and zone using CloudShell
│   │   └── Create the new cluster -> configure authentication -> create the service and then expose to external traffic
│   │   └── Validate the external IP has been assigned and gthe app is reachable via browser -> Delete the cluster then validate it has been deleted
```

## Services and associated tasks, building and troubleshooting

### Console, API & IAM
- 07202025 Review currently available projects using the console.![Step1](images/step1.png)
- 07202025 Access the Management Services then the API service![Step2](images/step2.png)
- 07202025 Create a new principal and then confirm it only has the viewer role permission assigned![Step3](images/step3.png)
- 07202025 Confirm the roles assigned to each principal![Step4](images/step4.png)
- 07202025 Enable the Dialogflow API and then confirm that this service is now usable with the current principal![Step5](images/step5.png)
- 07202025 Confirm the region, change to a different zone in the region, then validate this new zone is active![Step6](images/step6.png)
- 07202025 Export both the PROJECT and ZONE paramaters to their respective variables, then echo the output for each to CloudShell![Step7](images/step7.png)

### Compute
- 07262025 Create an e2-medium SKU VM after configuring the $ZONE variable to specify the desired location![Step8](images/step8.png)
- 07262025 Print the VMs to CloudShell![Step9](images/step9.png)
- 07262025 Print out running instances to CloudShell, filtering for the most recently created VM![Step10](images/step10.png)
- 07262025 Create an RSA keypair for the most recently created VM, assign to the active zone, then validate SSH functionality using CloudShell![Step11](images/step11.png)
- 07262025 Install NGINX on the newest created VM![Step12](images/step12.png)
- 07262025 Validate NGINX is up and running on the new VM utilizing curl in CloudShell![Step13](images/step13.png)
- 07262025 Print the current firewall rules for compute; then validate if they are enabled or not![Step14](images/step14.png)
- 07262025 Create a new ingress firewall rule for compute that allows TCP80 (HTTP), set both the priority and tag(s), validate the rule is now enforcing on the VM![Step15](images/step15.png)
- 07262025 Set the region, then assign a VAR for both region and zone![Step23](images/step23.png)
- 07262025 Create a new VM, set the zone and region, select the series, type, OS, bootdisk, and enable required firewall rules![Step24](images/step24.png)
- 07262025 Validate SSH functionality in the browser is functioning as expected![Step25](images/step25.png)
- 07262025 Update the OS, install NGINX, and confirming running on the VM![Step26](images/step26.png)
- 07262025 Confirm the web server is available via browser![Step27](images/step27.png)
- 07262025 Create a new VM using CloudShell, then validate running![Step28](images/step28.png)
- 07262025 Validate that created VMs are showing as both created and available![Step29](images/step29.png)
- 07262025 Validate SSH functionality for the additional VMs also using CloudShell![Step30](images/step30.png)

### Billing and Spend
- 07262025 View the past seven days of spend, as well as the projected spend forecast in the billing account overview![Step16](images/step16.png)
- 07262025 View the spend report; sorting by the amount each service is costing in a pre-defined spend period![Step17](images/step17.png)
- 07262025 View the cost that each service accrued on a certain day within a targeted spend range![Step18](images/step18.png)
- 07262025 Filter and view the cost for each service accrued over a certain date by zone and region![Step19](images/step19.png)
- 07262025 View total spend for the month without the Sustained Use discount being applied![Step20](images/step20.png)
- 07262025 Filter cost reporting for the month by both the project and the SKU of VMs specified![Step21](images/step21.png)
- 07262025 View the spend for the month for each service by utilized![Step22](images/step22.png)

### APIs and App Engine service
- 07272025 Enable the App Engine Admin API using the console![Step31](images/step31.png)
- 07272025 Clone the "Hello World" Python repo from GitHub to the project, update the OS, then setup the Python env![Step32](images/step32.png)
- 07272025 Validate the app is accesible from a browser![Step33](images/step33.png)
- 07272025 Start the web server, validate the accesibility, then stop the server![Step34](images/step34.png)
- 07272025 Update Python so that the greeting of the public facing web application has changed![Step35](images/step35.png)
- 07272025 Validate the application starts and that it is now reachable from a browser![Step36](images/step36.png)
- 07272025 Deploy the web application to the App Engine service![Step37](images/step37.png)
- 07272025 Confirm the web application change went through and is now reachable via a browser![Step38](images/step38.png)

### CloudRun
- 07272025 Build and Deploy a CloudRun function using the web console![Step39](images/step39.png)
- 07272025 Test the Function Payload and validate the run in logging![Step40](images/step40.png)
- 07272025 Clone the repo, update nodeJS using CloudShell, then start the web server![Step41](images/step41.png)
- 07272025 Confirm the front end GUI is both up and available ![Step42](images/step42.png)
- 07272025 Create an artifact repository![Step43](images/step43.png)
- 07272025 Set the repo permissions, start needed services, then start the build process![Step44](images/step44.png)
- 07272025 Pull down files, build Docker image, start services![Step45](images/step45.png)
- 07272025 Validate the build status execution in CloudBuild![Step46](images/step46.png)
- 07272025 Deploying the image to CloudBuild![Step47](images/step47.png)
- 07272025 Validate the deployment is running![Step48](images/step48.png)
- 07272025 Reploy the app with a concurrency of 1, as opposed to the default concurrency of 80![Step49](images/step49.png)
- 07272025 Validate the revised build is showing in CloudRun with the updated concurrency of 1![Step50](images/step50.png)
- 07272025 Validate the second revised build deployed with the default concurrency of 80![Step51](images/step51.png)
- 07272025 Build an update to the website by updating and pushing the Docker image(s) being used for this task![Step52](images/step52.png)
- 07272025 Update and then validate the website with zero downtime for endusers![Step53](images/step53.png)

### GKE 
- 07272025 - Set the region and the zone in CloudShell![Step54](images/step54.png)
- 07272025 - Create a new GKE cluster with 3 nodes![Step55](images/step55.png)
- 07272025 - Obtain authentication credentials for new cluster![Step56](images/step56.png)
- 07272025 - Create kubernetes service -> expose the app to external traffic -> validate services are running -> confirm the externalIP has been generated via CloudShell![Step57](images/step57.png)
- 07272025 - Validate the application is available via browser access![Step58](images/step58.png)
- 07272025 - Delete the cluster then validate this has been completed using CloudShell![Step59](images/step59.png)
