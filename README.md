# Android SDK for Docker [![](https://images.microbadger.com/badges/image/dral3x/android-ci-docker.svg)](https://hub.docker.com/r/dral3x/android-ci-docker)

This image contains the latest versions of Android SDK and Gradle. Feel free to contribute ;)

## Examples

### Start a container and open the shell

```
docker run -it dral3x/android-ci-docker bash
```

### Build the project in current directory

```
docker run -it -v $(pwd):/home/user/project -w /home/user/project -u $(id -u):$(id -g) dral3x/android-ci-docker gradle build
```

### Persistent Android SDK and caches

* `-v android-sdk:/home/user/android-sdk-linux`
* `-v gradle-cache:/home/user/.gradle`
* `-v android-cache:/home/user/.android`