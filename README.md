## > **Docker Comments**

**To Build image file**

*myapp --> image name*

*(.) --> indicates the relative path*

*to built the image with version*

> docker build -t myapp:v1 .

    docker build -t myapp .

**To List all images**

    > docker images

![Screenshot_5](https://github.com/user-attachments/assets/4fa0e739-2bb4-499e-a01b-d212a8d39083)

**To List all running containers**

    docker ps
    
![Screenshot_6](https://github.com/user-attachments/assets/9fb972a6-702c-432f-81fe-2023b0120791)

**List all containers**

    docker ps -a
    
![Screenshot_9](https://github.com/user-attachments/assets/139c5014-0783-4829-bbfb-7cf136e8e682)

**To run container**

*(name --> container name) (p --> port)  (d --> detached) (myapp --> image)*

     docker run -- name myapp_c1 -p 4000:4000 -d myapp

![Screenshot_7](https://github.com/user-attachments/assets/3242bbbf-90c6-405f-9fe8-6725a661232e)

*to run container with the version*

> docker run --name myapp_c -p 4000:4000 myapp:v1

It will run the container and removes the container when it stops.

> docker run -- name myapp_c1 -p 4000:4000 --rm myapp 

**To run the container wit volume**

* (c:/user/Documents/ --> path)  (exampleapp --> Folder name of the project) (app --> file name where the program starts)*

    docker run -- name myapp_c1 -p 4000:4000 --rm -v c:/user/Documents/exampleapp:/app myapp

![Screenshot_15](https://github.com/user-attachments/assets/8d810886-2b93-48bf-8f89-7ced4a6aa052)

**To stop the container**

*myapp_c1 --> container name*

    docker stop myapp_c1
  ![Screenshot_8](https://github.com/user-attachments/assets/988906ca-fbb4-40ef-a18e-7cbb01783b7a)

**To delete images**

*myapp --> image name*

--> if the image is in use we use 1st comment

    docker image rm myapp1 -f --> if the image is in use we use this comment
    
    docker image rm myapp
    
![Screenshot_10](https://github.com/user-attachments/assets/03509139-d3cc-46fa-888b-007ee1e57691)

**To delete container**

*myapp_c1 --> container name*

--> to remove multiple container use 2nd comment
    
    docker container rm myapp_c1

    docker container rm myapp_c2 myapp_c3

**To delete all containers and images**

    docker system prune -a
  
