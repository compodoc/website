# General information

Documentation coverage is calculated only for all statement of the file, even decorators.

Private functions are not part of the calculation.

The command `--coverageTest` gives the ability to test under a CI context the level of documentation coverage.

![screenshot](../assets/img/screenshots/8.png)

The command `--coverageMinimumPerFile` gives the ability to specify a minimum of coverage per file.

The command `--coverageTestThresholdFail` gives the ability to specify if command will fail with error or just warn user (true: error, false: warn) (default: true)