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

## How to Update

First close OSATE if open, then update HAMR Codegen by updating Sireum

```
cd $SIREUM_HOME
git pull --recurse
bin/build.cmd
```

This will update ``$SIREUM_HOME/bin/sireum.jar`` which will be used by the AADL GUMBO plugins when OSATE is relaunched.

To update the OSATE plugins themselves simply rerun the ``hamr phantom`` command from the [How to Install](#how-to-install) section (only needed when new versions of the plugin are released)
