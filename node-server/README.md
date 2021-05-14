* Build docker image:
    ```
    docker build . --tag node-server:1.0.0
    ```
    * --tag defines an unique name for the image that will be built.
    * Images are read only.
    * New images should be built when the server is updated.
* Run image:
    ```
    docker run -d -p 80:3000 --name node-server-container1 node-server:1.0.0
    ```
    * -d detaches the container from the terminal. (Prevents terminal from being blocked)
    * -p 80:3000 maps port 80 from host to port 3000 in container.
    * --name node-server-container1 defines a name for the container.
* Run two images simultaneously:
    ```
    docker run -d -p 80:3000 --name node-server-container1 node-server:1.0.0
    docker run -d -p 81:3000 --name node-server-container2 node-server:1.0.1
    ```
    * Docker will automatically reuse common layers between the two images.
    * Memory efficient.
* List containers:
    ```
    docker ps 
    ```
    * ps == process?
* Stop container:
    ```
    docker stop [CONTAINER ID]
    ```
    * It is not necessary to specify the entire container id.
    * It is only necessary to specify the first few letters until the string is unique. 
* Start container:
    ```
    docker start [CONTAINER ID]
    ```
* Delete container:
    ```
    docker rm [CONTAINER ID]
    ```
* List images:
    ```
    docker images
    ```
* Delete image:
    ```
    docker rmi [IMAGE ID]
    ```
    * rmi == remove image