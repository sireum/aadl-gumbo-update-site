# AADL GUMBO Update Site

## How to Install

Install [Sireum](https://github.com/sireum/kekinian#installing) (or update an existing installation, see below) and then execute the following on Mac/Linux

```
$SIREUM_HOME/bin/sireum hamr phantom -u --features "org.sireum.aadl.gumbo.feature.feature.group=https://raw.githubusercontent.com/sireum/aadl-gumbo-update-site/master;org.sireum.aadl.osate.gumbo2air.feature.feature.group=https://raw.githubusercontent.com/sireum/aadl-gumbo-update-site/master"
```

or the following on Windows

```
%SIREUM_HOME%\bin\sireum.bat hamr phantom -u --features org.sireum.aadl.gumbo.feature.feature.group=https://raw.githubusercontent.com/sireum/aadl-gumbo-update-site/master;org.sireum.aadl.osate.gumbo2air.feature.feature.group=https://raw.githubusercontent.com/sireum/aadl-gumbo-update-site/master
```

**NOTE**: the ``-u`` phantom option also installs/updates the following Sireum OSATE plugins: 
* Base - transforms core AADL to [AIR](https://github.com/sireum/air)
* CLI - provides a CLI for Sireum based OSATE plugins ***(documentation forthcoming)***
* [AWAS](https://awas.sireum.org/) - information flow analyzer and visualizer for component-based systems
* [HAMR](https://hamr.sireum.org) - code generation from AADL models

Pass phantom's ``--help`` option for more information (e.g. how to install plugins into an existing OSATE installation)

## How to Install into FMIDE

First install FMIDE

```
$SIREUM_HOME/bin/install/fmide.cmd
```

The first time the script is run (or when it detects FMIDE needs to be updated) it will indicate where it installed FMIDE.  Copy that location and pass it to phantom via its ``-o`` option.  For example

```
$SIREUM_HOME/bin/sireum hamr phantom -u -o <fmide-loc> --features "org.sireum.aadl.gumbo.feature.feature.group=https://raw.githubusercontent.com/sireum/aadl-gumbo-update-site/master;org.sireum.aadl.osate.gumbo2air.feature.feature.group=https://raw.githubusercontent.com/sireum/aadl-gumbo-update-site/master"
```

## How to Update

First close OSATE if open, then update HAMR Codegen by updating Sireum

```
cd $SIREUM_HOME
git pull --recurse
bin/build.cmd
```

This will update ``$SIREUM_HOME/bin/sireum.jar`` which will be used by the AADL GUMBO plugins when OSATE is relaunched.

To update the OSATE plugins themselves simply rerun the ``hamr phantom`` command from the [How to Install](#how-to-install) section (only needed when new versions of the plugin are released)


**Releases**

- [1.2022.06011655.d0c1d8e](1.2022.06011655.d0c1d8e)
- [1.2022.06081955.eb93186](1.2022.06081955.eb93186)
- [1.2022.06151822.8f00475](1.2022.06151822.8f00475)
- [1.2022.06161903.68c1896](1.2022.06161903.68c1896)
- [1.2022.06222050.06a7060](1.2022.06222050.06a7060)
