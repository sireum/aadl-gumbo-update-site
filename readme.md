# AADL GUMBO Update Site

## How to Install

Install [Sireum](https://github.com/sireum/kekinian#installing) (or update an existing installation, see below) and then execute the following on Mac/Linux

```
$SIREUM_HOME/bin/sireum hamr phantom -u
```

or the following on Windows

```
%SIREUM_HOME%\bin\sireum.bat hamr phantom -u
```

**NOTE**: the ``-u`` phantom option also installs/updates the following Sireum OSATE plugins: 
* Base - transforms core AADL to [AIR](https://github.com/sireum/air)
* CLI - provides a CLI for Sireum based OSATE plugins ***(documentation forthcoming)***
* [AWAS](https://awas.sireum.org/) - information flow analyzer and visualizer for component-based systems
* [HAMR](https://hamr.sireum.org) - code generation from AADL models

Pass phantom's ``--help`` option for more information (e.g. how to install plugins into an existing OSATE installation)

## How to Install into FMIDE

```
$SIREUM_HOME/bin/install/fmide.cmd
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
- [1.2022.06242122.c1af472](1.2022.06242122.c1af472)
- [1.2022.06282118.230473f](1.2022.06282118.230473f)
- [1.2022.07051018.a740565](1.2022.07051018.a740565)
- [1.2022.08091444.f63660a](1.2022.08091444.f63660a)
- [1.2022.08111537.0f97c79](1.2022.08111537.0f97c79)
- [1.2022.08191219.82466d5](1.2022.08191219.82466d5)
- [1.2022.08221314.0e4052e](1.2022.08221314.0e4052e)
- [1.2022.08231211.b12db9b](1.2022.08231211.b12db9b)
