# Table of contents
#-- This pseudo-markdown file will be converted to `_toc.yml` during building. We use this file to ease working on the website using knowledge management software such as Obsidian (it allow linking everything together).
#-- -----------------------------------------------------------------------

format: jb-book
root: [](index.md)
parts:

## Manual
  - caption: "Manual"
    chapters:

      - file: [](ktk_getting_started.md)
        sections:

          - file: [](getting_started_python.md)
          - file: [](ktk_installing.md)
          - file: [](ktk_lab_mode.md)


      - file: [](tutorials.md)
        sections:

          - file: [](timeseries.md)
            sections:
              - file: [](timeseries_basics.md)
              - file: [](timeseries_manipulating.md)
              - file: [](timeseries_dataframes.md)

          - file: [](loadsave.md)

          - file: [](filters.md)
            sections:
              - file: [](filters_butter.md)
              - file: [](filters_smooth.md)
              - file: [](filters_savgol.md)
              - file: [](filters_median.md)

          - file: [](cycles.md)

          - file: [](geometry.md)
            sections:
              - file: [](geometry_basics.md)
              - file: [](geometry_dimension_conventions.md)

          - file: [](kinematics.md)
            sections:
              - file: [](kinematics_load_visualize.md)
              - file: [](kinematics_joint_angles.md)
              - file: [](kinematics_reconstructing_occluded_markers.md)
              - file: [](kinematics_reconstructing_removed_markers.md)
              - file: [](kinematics_reconstructing_probed_points.md)

          - file: [](ktk_conventions.md)
          - file: [](extensions.md)

        #-- End tutorials

## API Reference
  - caption: "API Reference"
    chapters:
      - file: [](api_classes.md)
      - file: [](api_functions.md)
      - file: [](api_modules.md)
      - file: [](dev_extensions.md)
      - file: [](ktk_release_notes.md)

## Contributing
  - caption: "Contributing"
    chapters:

      - file: [](ktk_citing.md)

      - file: [](dev_contributing.md)
        sections:
          - file: [](dev_rules.md)
          - file: [](dev_code_of_conduct.md)
          - file: [](dev_installing_from_github.md)
          - file: [](dev_coding_style.md)

      - file: [](dev_tutorials.md)
        sections:
          - file: [](python_installing.md)
          - file: [](python_using_spyder.md)
          - file: [](python_arithmetics_and_variables.md)
          - file: [](python_numbers.md)
          - file: [](python_strings.md)
          - file: [](python_comments_and_docstrings.md)
          - file: [](python_functions.md)
          - file: [](python_conditions.md)
          - file: [](python_lists.md)
          - file: [](python_while.md)
          - file: [](python_for.md)
          - file: [](python_dicts.md)
          - file: [](python_more_advanced.md)
          - file: [](python_integration_exercises.md)
          - file: [](python_external_tutorials.md)
          - file: [](numpy.md)
          - file: [](matplotlib.md)
          - file: [](pandas.md)

      - url: https://github.com/felixchenier/kineticstoolkit
        title: GitHub repository
