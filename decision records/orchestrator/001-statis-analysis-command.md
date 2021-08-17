# Introduce a orchestrator command for static analysis

* Status: Open  <!-- optional -->

## Context and Problem Statement

sfpowerscripts utilize pmd for static analysis and does provide a command with a baselined rules.
However to use it, you have to issue the command one by one (by each package) and often in another stage of a pipeline to enable to trigger static analysis in parallel. 

refer to [issue ticket 549](https://github.com/Accenture/sfpowerscripts/issues/549)

## Solution
To improve this experience for developers a new command needs to be created in
the orchestrator namespace and provide additional functionality such as

- Auto discovery of a packages similar to other orchestrator commands
- Skip PMD validation if there is no apex classes
- Package Validity Check using sfpowerkit package:valid command

### The proposed command

```bash
sfdx sfpowerscripts:orchestrator:analyze
```

In this command it will be running a function that will auto discover packages. As it discovers each of the packages from project config and perform a static analysis on each of the packages without running the actual code.

If there are no apex classes in the project that it should skip the PMD validation process.

Utilising the sfpowerkit package valid command to check whether it only contains valid metadata. I am thinking this command should run as each package is discovered from the type.

### Command Flags

```bash
--difcheck
```
To only run PMD Analysis on packages that have changes.

```bash
-p , --package=package
```
To be able to select Specific packages

```bash
-f, --configfilepath=configfilepath
```
Relative Path to the pool configuration json file. The schema of the file could be found in the Wiki


Possible flags considered would be having the option to specific for PMD analysis only and package validate.