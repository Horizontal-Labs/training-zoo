# Run Colab Locally

This document describes how to run the Colab notebook locally. Scince adapting the teams Colab notebook to run on Windows natively takes a lot of time, this might be a better option for us.

## Disclamer
Running Colab on a local docker instance lead to the colab website in my browser to crash. I tried different browsers and running the terminal and dockerhub as admin, but the same issue happened. I am not sure if this is a problem with my machine or the docker image. If you have any issues, please let me know.


## Prerequisites
- [Docker](https://docs.docker.com/get-docker/)
- [Docker Compose](https://docs.docker.com/compose/install/)


## Start a runtime:
In a terminal, run the following command to start a Colab runtime:

```bash
docker run -p 127.0.0.1:9000:8080 us-docker.pkg.dev/colab-images/public/runtime
```
      

For GPU support, with NVIDIA drivers and the NVIDIA container toolkit installed, use:

```bash
docker run --gpus=all -p 127.0.0.1:9000:8080 us-docker.pkg.dev/colab-images/public/runtime
```

After running the command, your docker image will be build and a Colab runtime will be started. This may take a while, depending on your internet connection and the speed of your machine.

After the runtime is started, you will see a message like this:

```bash
[2025-05-19T19:40:36.343Z]  INFO: app/1 on 3a8c4a2f2897: http://127.0.0.1:9000/?token=3e06907575168151b1c4991d32d5960cf158ddac26f19f43 (type=jupyter)
```
This means that the runtime is running and you can access it in your browser.


## Accessing the runtime
    1. Open your browser collab
    2. Click on the "Connect" button in the top right corner of the page.
    3. Select "Connect to local runtime" from the dropdown menu.    
    4. In the dialog that appears, enter the URL of the runtime you started in the previous step. The URL should be `http://127.0.0.1:9000/?token=<token>`
    5. Click "Connect" to connect to the runtime.





