# chkp-containerlab-images

Packaging done with Boxen

## Packaging:
 
Download the necessary Check Point version from : https://supportcenter.checkpoint.com/supportcenter/portal?eventSubmit_doGoviewsolutiondetails=&solutionid=sk158292

**Required to use the images with “with default admin password”**
 
Download and install Boxen according their website:
> bash -c "$(curl -sL https://raw.githubusercontent.com/carlmontanari/boxen/main/get.sh)"
 
Copy the qcow2 to the machine : it can take a few minutes to complete 
 
 > BOXEN_LOG_LEVEL=debug BOXEN_TIMEOUT_MULTIPLIER=2 BOXEN_DEV_MODE=1 boxen package --disk /home/ofirs/Check_Point_R81.10_Cloudguard_Openstack_Security_Gateway_unsecured.qcow2 --vendor checkpoint --platform cloudguard --version R81.10   
 
Upload the image into private/public registry 
 
> docker images :                                                                                                                                                                                  
REPOSITORY                                 TAG       IMAGE ID       CREATED              SIZE
boxen_checkpoint_cloudguard                R81.10    8f49bedb70d3   About a minute ago   6.33GB

