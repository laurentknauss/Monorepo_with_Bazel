# gRPC Architecture Monorepo_with_Bazel 

Example taken from the paperback book "GRPC Go for Professionals" by software engineer Clement Jean PacktPublishing 2023.

We have a monorepo with 3 submodules: 
  - client .
  - server .
  - proto .

    
1 - We create each sub-modules by going to each of these  3 folders and run "git mod init github.com/PacktPublishing/gRPC-go-for-Professionals/$FOLDER_NAME" . 
2- We create the workspace file (go.work) by going to the root of the project and run : `go work init client server proto` . 






example of a gRPC architecture with Bazel  for  Builds and Tests  tooling
