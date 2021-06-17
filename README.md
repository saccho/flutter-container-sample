# flutter-container-sample

Sample repository to launch flutter app using vscode devcontainer.

You can connect to the host's Android emulator from the container by using the [matsp/docker-flutter](https://github.com/matsp/docker-flutter) image.

## Requirements

### In your host PC

- Android emulator
- Android SDK

## Setup

1. Launch the Android emulator in your host PC.

2. Execute the following command so that you can connect to the emulator via the network.

``` shell
# in your host PC
$ adb tcpip 5555
```

``` shell
# in your devcontainer
$ adb connect host.docker.internal:5555
```

3. Start the app (or run debug `lib/main.dart` from vscode).

``` shell
$ flutter run
```
