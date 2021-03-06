# Extensions

Kinetics Toolkit provides very generic functions that should apply to a wide variety of use cases. For more specific use cases, or to quickly develop and share new features, we provide a simple extension mechanism.

## Installing extensions

Here are links to known extensions, where you can find a detailed description, tutorials, and installation procedure. Please [contact us](https://github.com/felixchenier/kineticstoolkit/discussions) to add your own extension to this list.

- [pushrimkinetics](https://github.com/felixchenier/kineticstoolkit_pushrimkinetics): Provide functions to process kinetic data from instrumented wheelchair wheels. Replaces the former `ktk.pushrimkinetics` module that is being moved out from the core library.

## Using extensions

Use [ktk.import_extensions()](api/kineticstoolkit.import_extensions.rst) to import all installed extensions into the `ktk.ext` namespace. For example, if you installed the pushrimkinetics extension above, then its functions will be available as `ktk.ext.pushrimkinetics.read_smartwheel()`, `ktk.ext.pushrimkinetics.calculate_power()`, etc.

If you imported Kinetics Toolkit in [lab mode](ktk_lab_mode.md), the extensions are already imported, no need to use [ktk.import_extensions()](api/kineticstoolkit.import_extensions.rst).

## Developing extensions

Please consult [this page](dev_extensions) to learn how to develop and share your own extensions.
