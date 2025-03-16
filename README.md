# flutter-fvm-dart-sdk-action

An action that parses an [FVM](https://github.com/leoafarias/fvm) config file `.fvmrc` to get Dart SDK version followed by Flutter version.

## Usage

You can assign an ID to each usage of this action and retrieve the Dart SDK version from its outputs.

```yaml
    steps:
      - uses: actions/checkout@v4

      - uses: offich/flutter-fvm-dart-sdk-action@v1
        id: flutter-fvm-dart-sdk-version

      - name: Echo Dart SDK Version
        run: echo ${{ steps.flutter-fvm-dart-sdk-version.outputs.dart-version }}
```

## Configuration inputs

All the sample options below can be combined with each other.

### Custom config path

If you have a custom path for your `.fvmrc` file, you can set it with the `path` input.

```yaml
    steps:
      - uses: actions/checkout@v4

      - uses: offich/flutter-fvm-dart-sdk-action@v1
        with:
          path: 'some-path/.fvmrc'
```
