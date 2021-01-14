# SCA-Cloud-School-Application
How to deploy a HTML site using Nginx and Docker
-------------------------------------------
Step 1:I created an Index.html and Dockerfile as attached in the repository

Step 2:To Build the Docker image for the HTML server i used the command below: docker build -t sca-cloud-html-image .

Step 3: To confirm the i used the command " docker images" to list and the output shows as below:

Step 4:To run the docker container i used the command docker run -d -p 80:80 sca-cloud-html-image
![build docker](https://user-images.githubusercontent.com/57386428/104592866-2d854780-566f-11eb-8387-0410b48d8c0b.JPG)

The result is as follows: 06f36915e4b568015c84748a8a9a812bf8a6674fae31247716bfba0828fe2d11

Step 5:I viewed it in the browser using localhost:80
![localhost](https://user-images.githubusercontent.com/57386428/104592875-31b16500-566f-11eb-9283-22b386d7c598.JPG)

To push the docker image from my github to docker hub
-------------------------------------------------
I created a reprository called SCA cloud Application on Docker hub
2.Connected my DOcker hub to my github account
3.To create a  workflow ,On my Github reprository the (stable)branch,Created actions>New Workflow>Docker Image CI>Set up this workflow as shown below:
![workflow](https://user-images.githubusercontent.com/57386428/104597943-404f4a80-5676-11eb-9613-7a148cf882eb.JPG)
![workflow](https://user-images.githubusercontent.com/57386428/104598025-5bba5580-5676-11eb-879f-ebe4b93b828a.png)


4.It generated a workflow called main.yml as shown below:
![workflow2](https://user-images.githubusercontent.com/57386428/104598366-c9ff1800-5676-11eb-9cad-fadfcd550b46.JPG)

5.On my Dockerhub repository i configured an automated build by doing the follwoing:
Clicked on the repository>Configure Automated builds

I clicked on the github repository as shown below
![dockerhub](https://user-images.githubusercontent.com/57386428/104598825-4eea3180-5677-11eb-9290-deffaa8bc753.JPG)

To build rules i used the following rules as shown below then save and build:
![build 2](https://user-images.githubusercontent.com/57386428/104597810-17c75080-5676-11eb-85f6-c099ee392c52.JPG)

The build was successful as shown below:

![build 3](https://user-images.githubusercontent.com/57386428/104598899-65908880-5677-11eb-95bb-26ee43e3bd0b.JPG)

