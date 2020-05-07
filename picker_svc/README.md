<img src="../../assets/gophernand.png" align="right" width="128" height="auto"/>

<br/>
<br/>
<br/>


# Deployment Lab

---
## <img src="../../assets/lab.png" width="auto" height="32"/> Your Mission...

> Build and Dockerize a word picker web service!

1. Clone the [Labs Repo]()
2. cd picker_svc
3. Ensure docker is installed
4. Create your module file for your repository
5. Ensure all the tests are passing!
6. Build an executable by hand to run on your target operating system
   1. Make sure you can set the service version via your build command by leveraging build flags
   2. Run the picker service locally
   3. Ensure it prints your custom version upon starting!
   4. Exercise the picker by using the URLS below
7. Modify the provided Dockerfile and .dockerignore files to build a Docker image
   1. Make sure you can set the application version via your build command
   2. Make sure to remove all test files and README.md for the image build
8. Run your Docker container via locally via Docker
9. Ensure it prints your custom version upon starting
10. Verify your service endpoints are working correctly on the container
11. Note the size of your current Docker image and your local executable.
12. Next change the Docker base image to use a scratch image
13. Rebuild your Docker image
14. Repeat the step above to launch your new Docker container and validate the
    service
15. Now the surprise!
    Compare the size of this new image you've just build vs the old image?


## Installation

1. Install [Docker Desktop](https://www.docker.com/products/docker-desktop) on your machine (SKIP IF INSTALLED!)

## Commands

1. Exercise service endpoints

   ```shell
   # Load a dictionary
   # Available dictionaries: words, trump or musicians
   curl -XGET http://localhost:4500/api/v1/load?name=musicians
   # Word picker...
   curl -XGET http://localhost:4500/api/v1/picker
   ```

1. Build a Docker images

   ```shell
   docker build --rm -t picker:0.0.1 .
   ```

1. Run a Docker image exposing 4500 locally

   ```shell
   docker run -it -p 4500:4500 picker:0.0.1
   ```

1. List your Docker image

   ```shell
   docker images | grep picker
   ```

---
<img src="../../assets/imhotep_logo.png" width="32" height="auto"/> © 2020 Imhotep Software LLC.
All materials licensed under [Apache v2.0](http://www.apache.org/licenses/LICENSE-2.0)