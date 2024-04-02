# Deployment of Dtb-api-server on kubernetes 
   Requirement - 3 replicas along with a service to provide api's inbuilt health function output on localhost:8080/health

  ### pre-requites  
   - dtb source code
   - Dockerfile
   - Docker Compose file
   - go.mod
   - go.sum
   - api-server-manifest.yaml
   - service-manifest.yaml

###     Content 

1- operation Steps  
2- Dockerfile
3- Dockercompose file 
4- Push the image 
5- Kubernetes App manifest for api server 
6- Kubernetes Service for output 


1- Operation Steps 

    Step 1 : Docker-compose up 
              in order to compile an image namely dtb-server we will have to perform below command on the pparent directory where docker compose file is present 
              ```
              docker-compose up -d api-service

              ```
    Step 2 : Docker commit container to image and Docker Login 

             ```
             docker commit container_id chonesial/dtb-server:latest
            ```
    
    Step 3 : Docker push to Docker Repository 
    
          ```
          docker push chonesial/dtb-server:latest
         ```
         
    Step 4 : Docker stop and Delete Container 
    
    
    Step 5 : Deploy kubernetes Cluster and service 

    Step 6 : Expose service (as we are running  on windows)

                   minikube service --all
    

2 : Docker file 

         https://github.com/sachin-chand-tc/dtb/blob/master/cmd/api/Dockerfile

         
