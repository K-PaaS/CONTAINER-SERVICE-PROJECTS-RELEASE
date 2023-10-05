## CONTAINER-SERVICE-PROJECTS-RELEASE   

### Notices   
- Use CONTAINER-SERVICE-PROJECTS-RELEASE >= v.2.0.1    
  - K-PaaS >= v.5.0.2    
  - service-deployment >= v5.0.2    
- Use CONTAINER-SERVICE-PROJECTS-RELEASE =< v.2.0.0     
  - K-PaaS =< v.5.0.1    
  - service-deployment =< v5.0.1    

### Container Service Projects Configuration   
- container-service-api :: N machine(s)   
- container-service-broker :: N machine(s)   
- container-service-common-api :: N machine(s)   
- container-service-dashboard :: 1 machine   
- haproxy :: 1 machine   
- mariadb :: 1 machine   
- private-image-repository :: 1 machine   
- container-jenkins-broker :: 1 manchne   

### Create Container Service Projects   
- Download the latest Container Service Projects Release   
  ```   
  $ git clone https://github.com/K-PaaS/CONTAINER-SERVICE-PROJECTS-RELEASE.git   
  $ cd CONTAINER-SERVICE-PROJECTS-RELEASE   
  ```   
- Download & Copy "source files" into the src directory      
  ```   
  ## download source files   
  $ wget -O src.zip https://nextcloud.paas-ta.org/index.php/s/GjwtbxDdcMkEGq8/download 

  ## unzip download source files   
  $ unzip src.zip   
  $ mv container-service-release-src src     
  ```   
- Create Container Service Projects   
  ```   
  ## <VERSION> :: release version (e.g. 2.0.1)      
  ## <RELEASE_TARBALL_PATH> :: release file path (e.g. /home/ubuntu/workspace/container-service-projects-release-<VERSION>.tgz)      
  $ bosh -e <bosh_name> create-release --name=container-service-projects-release --version=<VERSION> --tarball=<RELEASE_TARBALL_PATH> --force    
  ```   
### Deployment   
- https://github.com/K-PaaS/service-deployment   
