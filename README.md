##  **gRPC Architecture Monorepo & Bazel Tooling**  

Example taken from the paperback book "GRPC Go for Professionals" by software engineer Clement Jean - PacktPublishing 2023.<br>

Bazel can be a little bit cumbersome to set up but it is worth the effort.<br>
Once  you have your build system set-up , you will be able to build the whole application (generate & build)<br>
and/or run it in one command.<br>


**Structure of the gRPC architecture**<br>

We have a monorepo with 3 submodules: 
  - client .
  - server .
  - proto .<br>

  

**WorkFlow**<br>


1 - We create each sub-modules by going to each of these  3 folders and run "git mod init github.com/PacktPublishing/gRPC-go-for-Professionals/$FOLDER_NAME" . <br>


2 - We create the workspace file (go.work) by going to the root of the project and run : `go work init client server proto` .<br>


3 - We create a `versions.bzl` file that serves as a centralized location for managing version numbers and other constants related to dependencies and build configurations. <br>


4 - We create our WORKSPACE.bazel file where we define our workspace name, import our variables and import some utilities to clone Git repositories and download archives . <br> 


5 - We run `bazel run //:gazelle`<br>
If you have installed Bazel through Bazelisk, Bazel will try to get its newest version each time you run a `Bazel` command.<br>
In order to avoid this, we create a file called .bazelversion containing the version of bazel we have currently installed.<br>



6 - After the dependecies are pulled up and compiled, you should be able to see a BUILD.bazel file in the proto/dummy/v1  directory.<br>


7 - Once your build system is ready, you go on coding the server boilerplate.













