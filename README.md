# nitpicky

This package is a fork of [pedantic][] for VGV Dart/Flutter style.

See that package for more information.

[pedantic]: https://pub.dev/packages/pedantic

## Using the Lints

To use the lints add a dependency in your `pubspec.yaml`:

```yaml
# If you just want `analysis_options.yaml`, it can be a dev dependency.
dev_dependencies:
  nitpicky: 
    git:
      url: git@github.com:VGVentures/nitpicky
      ref: 1.0.0  # pin a specific version/branch
```

Then, add an include in your `analysis_options.yaml`. If you want to always
use the latest version of the lints, add a dependency on the main
`analysis_options` file:


```yaml
include: package:nitpicky/analysis_options.yaml
```

If your continuous build and/or presubmit check lints then they will likely
fail whenever a new version of `package:nitpicky` is released. To avoid this,
specify a specific version of `analysis_options.yaml` instead:

```yaml
include: package:nitpicky/analysis_options.1.0.0.yaml
```
