# .NET ENVIRONMENT BUILDER - REPOSITORY <h1> 
 
[![build](https://img.shields.io/github/workflow/status/lyscm/environments-dotnet/environment-dotnet%20-%20ci?logo=github)](https://github.com/lyscm/environments-dotnet/blob/master/.github/workflows/build-action.yml)
[![repo size](https://img.shields.io/github/repo-size/lyscm/environments-dotnet?logo=github)](https://github.com/lyscm/environments-dotnet)
[![package](https://img.shields.io/static/v1?label=package&message=dotnet&color=yellowgreen&logo=github)](https://github.com/lyscm/environments-dotnet/pkgs/container/environments%2Fdotnet)

## Initiate package(s): <h2> 

Set parameters:

***Bash:***
```bash
OWNER=lyscm
CONTAINER_NAME=dotnet
TAG=ghcr.io/lyscm/environments/dotnet
```

***Powershell:***
```powershell
$OWNER="lyscm"
$CONTAINER_NAME="dotnet"
$TAG="ghcr.io/lyscm/environments/dotnet"
```

Remove any existing container:

```bash
docker stop $CONTAINER_NAME
docker rm $CONTAINER_NAME
docker pull $TAG
```

Run container:

***Bash:***
```bash
docker run \
    -d \
    --name $CONTAINER_NAME \
    --restart unless-stopped \
    -v /var/run/docker.sock:/var/run/docker-host.sock \
    --net=host \
    --privileged \
    $TAG
```
***Powershell:***
```powershell
docker run `
    -d `
    --name $CONTAINER_NAME `
    --restart unless-stopped `
    -v /var/run/docker.sock:/var/run/docker-host.sock `
    --net=host `
    --privileged `
    $TAG
```