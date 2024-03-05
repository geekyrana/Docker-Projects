# Multi Stage Docker Build

The main purpose of choosing a golang based applciation to demostrate this example is golang is a statically-typed programming language that does not require a runtime in the traditional sense. Unlike dynamically-typed languages like Python, Ruby, and JavaScript, which rely on a runtime environment to execute their code, Go compiles directly to machine code, which can then be executed directly by the operating system.

So the real advantage of multi stage docker build and distro less images can be understand with a drastic decrease in the Image size.

# Steps To Check The Real Difference Of Image Sizes

1. Clone the Repo
2. In your terminal, go to the project directory (golang-multi-stage-docker-build)

Here, let's first run the dockerfile without multistage and check the image size

3. cd dockerfile-without-multistage
4. docker build -t simplecalculator .
5. docker images

Here, notice the image size, it will be around 869 MBs. Now, let’s run the docker file with multistage and check the image size.

6. cd ..  {golang-multi-stage-docker-build}
7. docker build -t simplecalculator-multistage .
8. docker images

Here, you’ll notice the actual difference in the image sizes. The image size now reduced to around 1.83 MBs from 869 MBs which is a drastic decrease of ~800% in image size. That’s the advantage of using multi-stage docker builds.
