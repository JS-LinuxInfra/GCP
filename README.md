## Scope
This project contains a variaty of GCP tasks related to various services such as Compute, IAM, APIs, Storage, Spend, etc.

## Environment & Services
- GCP Console
- GCP Cloudshell 
- gcloud CLI
- GCP Compute
- GCP IAM
- GCP API

*******************************************************************************************************************
To-Do
1. List each service by logical section and label screenshots
2. Create tree showing all services and tasks, cleanup formatting
3. Ensure formatting is standardized across all services and documented in about me repo for going forward
4. Upload remaining GKE screencaptures and document per the above
5. Apply the same process to K8 repo
6. Create folders by task and service for all screen captures, move all images and update pointers, confirm everything looks good
7. Finish Udacity GCP course - upload and annotate all
8. Start PluralSite GCP CDL cert course and use format going forward

├── README.md
├── tasks
│   ├── service 
│   │   ├── task
│   │   └── task
│   ├── service
│   │   └── task
*******************************************************************************************************************
## Tasks
- Console & API
### Review currently available projects in the console.
![Step1](images/step1.png)

### Access Management Services then the API service.
![Step2](images/step2.png)

### Create a new principal and then confirm it only has the viewer role assigned.
![Step3](images/step3.png)

### Confirm the roles assigned to each principal.
![Step4](images/step4.png)

### Enable the Dialogflow API and confirm this service is now usable with the current principal in use.
![Step5](images/step5.png)

### Confirm the region, change to a different zone in the region, validate new zone is active. 
![Step6](images/step6.png)

### Export the PROJECT and ZONE paramaters to applicable VARs then echo the output to the cloud shell terminal.
![Step7](images/step7.png)

****************************************************************************
- Compute
### Create an e2-medium VM using the $ZONE variable for location.
![Step8](images/step8.png)

### List out VMs to cloud shell.
![Step9](images/step9.png)

### List out instances to cloud shell, filtering for the VM that was just created.
![Step10](images/step10.png)

### Create RSA keypair for new VM, assign to active zone, validate SSH functionality in cloudshell.
![Step11](images/step11.png)

### Installing NGINX on new VM.
![Step12](images/step12.png)

### Validating NGINX is up and running on the new VM via curl.
![Step13](images/step13.png)

### List out current firewall rules for compute, validate if enabled or not.
![Step14](images/step14.png)

### Create new ingress firewall rule for compute that allows TCP80 (HTTP), set priority and tag(s), validate rule is set on the VM - filter for  port 80.
![Step15](images/step15.png)

### Set the region, then assign a variable for both the region (REGION) and the zone (ZONE).
![Step23](images/step23.png)

### Create a new VM, set the zone, set the region, select the series, type, OS, bootdisk, and enable desired firewall rules.
![Step24](images/step24.png)

### Validate SSH functionality in the browser is functioning as expected after provisioning new VM.
![Step25](images/step25.png)

### Update the OS, install NGINX, and confirming it is running on the VM.
![Step26](images/step26.png)

### Confirm the web server is available via using an external IP in the browser.
![Step27](images/step27.png)

### Create a new VM using gcloud shell and validate that it is running.
![Step28](images/step28.png)

### Validate that both VMs are showing as created and available.
![Step29](images/step29.png)

### Validate that SSH is functional for the second VM using Cloud Shell.
![Step30](images/step30.png)

**********************************************************
- Billing and Spend
### View the past seven days of spend as well as projected forecast in the billing account overview.
![Step16](images/step16.png)

### View spend report sorting by the amount each service is costing per the specified date duration.
![Step17](images/step17.png)

### View the cost each service accrued on a certain day within the designated date range.
![Step18](images/step18.png)

### Filter and view the cost for each service accrued over a certain date range sorting for a specific zone and region. 
![Step19](images/step19.png)

### View cost for the month without the Sustained Use discount being applied.
![Step20](images/step20.png)

### Filter cost reporting for the month by both project and SKU.
![Step21](images/step21.png)

### View the spend for the month for each service.
![Step22](images/step22.png)

***********************************************************************
- API/App Engine

### Enable the App Engine Admin API.
![Step31](images/step31.png)

### Clone the "Hello World" Python repo from GitHub to the current GCP project, update the OS, then setup the Python environment.
![Step32](images/step32.png)

### Confirm the app server is accesible from the browser.
![Step33](images/step33.png)

### Start the web server, validate the front-end, then stop the web server.
![Step34](images/step34.png)

### Update Python so the greeting of the web application is changed.
![Step35](images/step35.png)

### Validating the application starts and is now accesible from the browser.
![Step36](images/step36.png)

### Deploying the web application to the App Engine service.
![Step37](images/step37.png)

### Confirm the change went through on the front-end.
![Step38](images/step38.png)

********************************************************************************
- CloudRun |Artifact Repo
### Build and Deploy a CloudRun function.
![Step39](images/step39.png)

### Test the Function Payload and validate the run in logging.
![Step40](images/step40.png)

### Clone the repo from the main GCP repo, update nodeJS using CloudShell, start the web server.
![Step41](images/step41.png)

### Confirm the front end GUI is both up and available.
![Step42](images/step42.png)

### Create an artifact repository.
![Step43](images/step43.png)

### Set the repo permissions, start needed services, start the build process.
![Step44](images/step44.png)

******************************************

### CloudRun - Build, tune and update website

- 07192025 - Pull down files, build Docker image, start services![Step45](images/step45.png)
- 07192025 - Validate the build status execution in CloudBuild![Step46](images/step46.png)
- 07192025 - Deploying the image to CloudBuild![Step47](images/step47.png)
- 07192025 - Validate the deployment is running![Step48](images/step48.png)
- 07192025 - Reploy the app with a concurrency of 1, as opposed to the default concurrency of 80![Step49](images/step49.png)
- 07192025 - Validate the revised build is showing in CloudRun with the updated concurrency of 1![Step50](images/step50.png)
- 07192025 - Validate the second revised build deployed with the default concurrency of 80![Step51](images/step51.png)
- 07192025 - Build an update to the website by updating and pushing the Docker image(s) being used for this task![Step52](images/step52.png)
- 07192025 - Update and then validate the website with zero downtime for endusers![Step53](images/step53.png)

### GKE - TBD 
- 07192025 - Set the region and the zone in CloudShell![Step54](images/step54.png)
