```bash
❯ docker run devopsdockeruh/simple-web-service:alpine hello


                The application accepts 1 argument "server". Use the argument server to run the server

                If no arguments are supplied the application will output log strings to a file.


Arguments given: hello
❯ nvim Dockerfile
❯ docker build . -t web-server
DEPRECATED: The legacy builder is deprecated and will be removed in a future release.
            Install the buildx component to build images with BuildKit:
            https://docs.docker.com/go/buildx/

Sending build context to Docker daemon  2.048kB
Step 1/2 : FROM devopsdockeruh/simple-web-service:alpine
 ---> fd312adc88e0
Step 2/2 : CMD server
 ---> Running in 77a3689b94b7
Removing intermediate container 77a3689b94b7
 ---> bea894a1dde8
Successfully built bea894a1dde8
Successfully tagged web-server:latest
❯ docker run web-server
[GIN-debug] [WARNING] Creating an Engine instance with the Logger and Recovery middleware already attached.

[GIN-debug] [WARNING] Running in "debug" mode. Switch to "release" mode in production.
 - using env:   export GIN_MODE=release
 - using code:  gin.SetMode(gin.ReleaseMode)

[GIN-debug] GET    /*path                    --> server.Start.func1 (3 handlers)
[GIN-debug] Listening and serving HTTP on :8080

