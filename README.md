# dart_lang_ci
Use CI to compile Dart artifacts (e.g. ASAN-enabled Dart binary).
Mainly used for https://github.com/fzyzcjy/flutter_rust_bridge.

## Release workflow

Run the `Release` workflow manually and provide the Dart SDK git ref to build. For flutter_rust_bridge, this should normally match `FRB_MAIN_DART_VERSION` in its CI configuration.

The workflow builds Linux x64 Dart SDK artifacts for:

- `ReleaseASANX64`
- `ReleaseMSANX64`
- `ReleaseLSANX64`
- `ReleaseTSANX64`
- `ReleaseUBSANX64`

Each release asset includes the `*_dart-sdk.tar.gz` archive, a matching `.sha256` file, and per-sanitizer release notes with the resolved Dart commit and `dart --version` output.
