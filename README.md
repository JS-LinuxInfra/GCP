## Scope
This project contains a variaty of GCP tasks related to various services such as Compute, IAM, APIs, Storage, Spend, etc.

## Environment & Services
- GCP Console
- GCP Cloudshell 
- gcloud CLI
- GCP Compute
- GCP IAM
- GCP APIs

## Tasks

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

### View the past seven days of spend as well as projected forecast in the billing account overview.
![Step16](images/step16.png)

### View spend report sorting by the amount each service is costing per the specified date duration.
![Step17](images/step17.png)

### View the cost each service accrued over the last 30 days.
![Step18](images/step18.png)
