## Scope
This project contains a variaty of GCP tasks related to various services such as Compute, IAM, APIs, GKE, Spend, etc.

## Environment & Services
- GCP Console
- GCP Cloudshell 
- gcloud CLI
- GCP Compute
- GCP IAM
- GCP API

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
- 07202025 Review currently available projects using the console.![CAI1](Console_API_IAM/CAI1.png)
- 07202025 Access the Management Services then the API service![CAI2](Console_API_IAM/CAI2.png)
- 07202025 Create a new principal and then confirm it only has the viewer role permission assigned![CAI3](Console_API_IAM/CAI3.png)
- 07202025 Confirm the roles assigned to each principal![CAI4](Console_API_IAM/CAI4.png)
- 07202025 Enable the Dialogflow API and then confirm that this service is now usable with the current principal![CAI5](Console_API_IAM/CAI5.png)
- 07202025 Confirm the region, change to a different zone in the region, then validate this new zone is active![CAI6](Console_API_IAM/CAI6.png)
- 07202025 Export both the PROJECT and ZONE paramaters to their respective variables, then echo the output for each to CloudShell![CAI7](Console_API_IAM/CAI7.png)

### Compute
- 07262025 Create an e2-medium SKU VM after configuring the $ZONE variable to specify the desired location![compute1-1](Compute/compute1-1.png)
- 07262025 Create a Debian VM and validate SSH via CloudShell![compute1-1a](Compute/compute1-1a.png)
- 07262025 Print the VMs to CloudShell![compute1-2](Compute/compute1-2.png)
- 07262025 Print out running instances to CloudShell, filtering for the most recently created VM![compute1-3](Compute/compute1-3.png)
- 07262025 Create an RSA keypair for the most recently created VM, assign to the active zone, then validate SSH functionality using CloudShell![compute1-4](Compute/compute1-4.png)
- 07262025 Install NGINX on the newest created VM![compute1-5](Compute/compute1-5.png)
- 07262025 Validate NGINX is up and running on the new VM utilizing curl in CloudShell![compute1-6](Compute/compute1-6.png)
- 07262025 Print the current firewall rules for compute; then validate if they are enabled or not![compute1-7](Compute/compute1-7.png)
- 07262025 Create a new ingress firewall rule for compute that allows TCP80 (HTTP), set both the priority and tag(s), validate the rule is now enforcing on the VM![compute1-8](Compute/compute1-8.png)
- 07262025 Set the region, then assign a VAR for both region and zone![compute1-9](Compute/compute1-9.png)
- 07262025 Create a new VM, set the zone and region, select the series, type, OS, bootdisk, and enable required firewall rules![compute1-10](Compute/compute1-10.png)
- 07262025 Validate SSH functionality in the browser is functioning as expected![compute1-11](Compute/compute1-11.png)
- 07262025 Update the OS, install NGINX, and confirming running on the VM![compute1-12](Compute/compute1-12.png)
- 07262025 Confirm the web server is available via browser![compute1-13](Compute/compute1-13.png)
- 07262025 Create a new VM using CloudShell, then validate running![compute1-14](Compute/compute1-14.png)
- 07262025 Validate that created VMs are showing as both created and available![compute1-15](Compute/compute1-15.png)
- 07262025 Validate SSH functionality for the additional VMs also using CloudShell![compute1-16](Compute/compute1-16.png)

### Billing and Spend
- 07262025 View the past seven days of spend, as well as the projected spend forecast in the billing account overview![BAS1](Billing_and_Spend/BAS1.png)
- 07262025 View the spend report; sorting by the amount each service is costing in a pre-defined spend period![BAS2](Billing_and_Spend/BAS2.png)
- 07262025 View the cost that each service accrued on a certain day within a targeted spend range![BAS3](images/BAS3.png)
- 07262025 Filter and view the cost for each service accrued over a certain date by zone and region![BAS4](Billing_and_Spend/BAS4.png)
- 07262025 View total spend for the month without the Sustained Use discount being applied![BAS5](Billing_and_Spend/BAS5.png)
- 07262025 Filter cost reporting for the month by both the project and the SKU of VMs specified![BAS6](Billing_and_Spend/BAS6.png)
- 07262025 View the spend for the month for each service by utilized![BAS7](Billing_and_Spend/BAS7.png)

### APIs and App Engine 
- 07272025 Enable the App Engine Admin API using the console![AAE1](APIs_and_AppEngine/AAE1.png)
- 07272025 Clone the "Hello World" Python repo from GitHub to the project, update the OS, then setup the Python env![AAE2](APIs_and_AppEngine/AAE2.png)
- 07272025 Validate the app is accesible from a browser![AAE3](APIs_and_AppEngine/AAE3.png)
- 07272025 Start the web server, validate the accesibility, then stop the server![AAE4](APIs_and_AppEngine/AAE4.png)
- 07272025 Update Python so that the greeting of the public facing web application has changed![AAE5](APIs_and_AppEngine/AAE5.png)
- 07272025 Validate the application starts and that it is now reachable from a browser![AAE6](APIs_and_AppEngine/AAE6.png)
- 07272025 Deploy the web application to the App Engine service![AAE7](APIs_and_AppEngine/AAE7.png)
- 07272025 Confirm the web application change went through and is now reachable via a browser![AAE8](APIs_and_AppEngine/AAE8.png)

### CloudRun
- 07272025 Build and Deploy a CloudRun function using the web console![CR1-1](CloudRun/CR1-1.png)
- 07272025 Test the Function Payload and validate the run in logging![CR1-2](CloudRun/CR1-2.png)
- 07272025 Clone the repo, update nodeJS using CloudShell, then start the web server![CR1-3](CloudRun/CR1-3.png)
- 07272025 Confirm the front end GUI is both up and available![CR1-4](CloudRun/CR1-4.png)
- 07272025 Create an artifact repository![CR1-5](CloudRun/CR1-5.png)
- 07272025 Set the repo permissions, start needed services, then start the build process![CR1-6](CloudRun/CR1-6.png)
- 07272025 Pull down files, build Docker image, start services![CR1-7](CloudRun/CR1-7.png)
- 07272025 Validate the build status execution in CloudBuild![CR1-8](CloudRun/CR1-8.png)
- 07272025 Deploying the image to CloudBuild![CR1-9](CloudRun/CR1-9.png)
- 07272025 Validate the deployment is running![CR1-10](CloudRun/CR1-10.png)
- 07272025 Reploy the app with a concurrency of 1, as opposed to the default concurrency of 80![CR1-11](CloudRun/CR1-11.png)
- 07272025 Validate the revised build is showing in CloudRun with the updated concurrency of 1![CR1-12](CloudRun/CR1-12.png)
- 07272025 Validate the second revised build deployed with the default concurrency of 80![CR1-13](CloudRun/CR1-13.png)
- 07272025 Build an update to the website by updating and pushing the Docker image(s) being used for this task![CR1-14](CloudRun/CR1-14.png)
- 07272025 Update and then validate the website with zero downtime for endusers![CR1-15](CloudRun/CR1-15.png)

### GKE 
- 07272025 - Set the region and the zone in CloudShell![GKE1-1](GKE/GKE1-1.png)
- 07272025 - Create a new GKE cluster with 3 nodes![GKE1-2](GKE/GKE1-2.png)
- 07272025 - Obtain authentication credentials for new cluster![GKE1-3](GKE/GKE1-3.png)
- 07272025 - Create kubernetes service -> expose the app to external traffic -> validate services are running -> confirm the externalIP has been generated via CloudShell![GKE1-4](GKE/GKE1-4.png)
- 07272025 - Validate the application is available via browser access![GKE1-5](GKE/GKE1-5.png)
- 07272025 - Delete the cluster then validate this has been completed using CloudShell![GKE1-6](GKE/GKE1-6.png)
