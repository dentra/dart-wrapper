# Wraps Dart executables like gradlew or mvnw.

## Installation
Download `pubw` (https://github.com/dentra/dart-wrapper/raw/master/pubw) into the root of your project directory beside to `pubspec.yaml` location.

Make `pubw` executable by command:
```bash
$ chmod +x pubw
```

## Running
You can run command with explicit version of Dart SDK with -f switch as first parameter and version string as second. Version string may be:
 * explicit version for example 1.3.24 
 * `latest` - means latest version from stable channel 
 * `latest-dev` - means lates version from dev channel
 * `auto` - means detect version from `pubspec.yaml`
 
Examples:

Run `pub` command with Dart SDK 1.3.24:
```bash
$ ./pubw -f 1.3.24 get
```

Run `pub` command with latest Dart SDK stable channel:
```bash
$ ./pubw -f latest get
```

Run `pub` command witdh Dart SDK dev channel:
```bash
$ ./pubw -f latest-dev get
```

Run `pub` command witdh Dart SDK and version detected from `pubspec.yaml` automaticaly:
```bash
$ ./pubw -f auto get
```

Run `pub` command witdh Dart SDK and version detected path, if not found from, look in path 
specified in `DART_SDK` environment variable, and if not found again detects from `pubspec.yaml` automaticaly:
```bash
$ ./pubw get
```
