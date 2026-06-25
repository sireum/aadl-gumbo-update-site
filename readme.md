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

To update the OSATE plugins themselves simply rerun the ``hamr phantom`` command from the
[How to Install](#how-to-install) section (only needed when new versions of the plugin are released)

## Version History

Each release published under this update site is identified as
`1.YYYY.MMDDHHMM.<kekinian-commit>`, where the timestamp is the build/publish date.
The notes below list the [`aadl-gumbo`](https://github.com/sireum/aadl-gumbo) plugin
commits included in each release, matched by commit date. Mechanical commits (grammar
regeneration, version bumps, merges, generated artifacts) are omitted, and each change
is attributed to the earliest release that shipped it.

<!-- current-release -->

### [1.2026.06240925.18efbba7](1.2026.06240925.18efbba7)
*Released 2026-06-24*

- add support for abstract system properties and property specializations ([`4623787`](https://github.com/sireum/aadl-gumbo/commit/4623787))

### [1.2026.06200727.3a432955](1.2026.06200727.3a432955)
*Released 2026-06-20*

- subclause function cannot refer to the component's ports or state vars ([`284f45a`](https://github.com/sireum/aadl-gumbo/commit/284f45a))
- extend scope to component types ([`34b5508`](https://github.com/sireum/aadl-gumbo/commit/34b5508))

### [1.2026.06151729.97c0f302](1.2026.06151729.97c0f302)
*Released 2026-06-15*

- add composition support ([`6e09df2`](https://github.com/sireum/aadl-gumbo/commit/6e09df2))

### [1.2026.06091605.b80bbff1](1.2026.06091605.b80bbff1)
*Released 2026-06-09*

- sys assert checkpoint ([`4f0a5b3`](https://github.com/sireum/aadl-gumbo/commit/4f0a5b3))
- allow for KerML short-circuit binary and unary ops ([`ab08654`](https://github.com/sireum/aadl-gumbo/commit/ab08654))
- add system-level schedule contracts ([`9e9e9bb`](https://github.com/sireum/aadl-gumbo/commit/9e9e9bb))

### [1.2026.05261555.6cc8f3e1](1.2026.05261555.6cc8f3e1)
*Released 2026-05-26*

- Add cross-referencing and scoping for GUMBO member access expressions ([`57b96eb`](https://github.com/sireum/aadl-gumbo/commit/57b96eb))

### [1.2026.05201117.a8293090](1.2026.05201117.a8293090)
*Released 2026-05-20*

- adapt to Slang changes ([`0cbfdcd`](https://github.com/sireum/aadl-gumbo/commit/0cbfdcd))

### [1.2026.03261303.8534bc4d](1.2026.03261303.8534bc4d)
*Released 2026-03-26*

- Maintenance/rebuild release — no `aadl-gumbo` plugin changes in this window.

### [1.2026.02111228.64318e46](1.2026.02111228.64318e46)
*Released 2026-02-11*

- check if contract is null ([`56e2a70`](https://github.com/sireum/aadl-gumbo/commit/56e2a70))
- added other compute_cases ([`5dac33c`](https://github.com/sireum/aadl-gumbo/commit/5dac33c))

### [1.2026.02030957.27955316](1.2026.02030957.27955316)
*Released 2026-02-03*

- add compute_cases alternative, add spec functions ([`9ebd35a`](https://github.com/sireum/aadl-gumbo/commit/9ebd35a))
- revert to Java 17 ([`adbaa4d`](https://github.com/sireum/aadl-gumbo/commit/adbaa4d))

### [1.2025.11101714.aaeb57a0](1.2025.11101714.aaeb57a0)
*Released 2025-11-10*

- limit call expr to fully-qualified, non-dotted syntax ([`8515764`](https://github.com/sireum/aadl-gumbo/commit/8515764))

### [1.2025.11041321.4ee73dec](1.2025.11041321.4ee73dec)
*Released 2025-11-04*

- adapt to 2025-06 dev environment ([`5c14481`](https://github.com/sireum/aadl-gumbo/commit/5c14481))

### [1.2025.10031007.8a6c7684](1.2025.10031007.8a6c7684)
*Released 2025-10-03*

- General updates and maintenance (grammar regeneration / dependency bumps).

### [1.2025.09161533.4336a133](1.2025.09161533.4336a133)
*Released 2025-09-16*

- Maintenance/rebuild release — no `aadl-gumbo` plugin changes in this window.

### [1.2025.06020757.f5a533c1](1.2025.06020757.f5a533c1)
*Released 2025-06-02*

- add SysMLv2 instructions ([`bbfb741`](https://github.com/sireum/aadl-gumbo/commit/bbfb741))
- add array support ([`dfc0d51`](https://github.com/sireum/aadl-gumbo/commit/dfc0d51))
- refactor expression grammar ([`ef1796e`](https://github.com/sireum/aadl-gumbo/commit/ef1796e))
- split assume/guarantees, allow case assume to be optional, add assume and cases to handlers ([`cf8f0a0`](https://github.com/sireum/aadl-gumbo/commit/cf8f0a0))
- use preferred Slang BinaryOp symbols ([`c4a90d7`](https://github.com/sireum/aadl-gumbo/commit/c4a90d7))

### [1.2025.04121759.d7c92769](1.2025.04121759.d7c92769)
*Released 2025-04-12*

- adapt to MethodSig mods ([`cec5144`](https://github.com/sireum/aadl-gumbo/commit/cec5144))

### [1.2025.03090911.ff179091](1.2025.03090911.ff179091)
*Released 2025-03-09*

- ensure int lit values are valid ([`8d4cb0d`](https://github.com/sireum/aadl-gumbo/commit/8d4cb0d))
- build Attr rather than passing null ([`7eed939`](https://github.com/sireum/aadl-gumbo/commit/7eed939))

### [1.2025.02250914.79d7f526](1.2025.02250914.79d7f526)
*Released 2025-02-25*

- Maintenance/rebuild release — no `aadl-gumbo` plugin changes in this window.

### [1.2024.11051400.1c0b1259](1.2024.11051400.1c0b1259)
*Released 2024-11-05*

- update OSATE versions for 2.15.0 ([`6f29fc0`](https://github.com/sireum/aadl-gumbo/commit/6f29fc0))

### [1.2024.10181001.07c00045](1.2024.10181001.07c00045)
*Released 2024-10-18*

- Maintenance/rebuild release — no `aadl-gumbo` plugin changes in this window.

### [1.2024.08211808.e0a2706](1.2024.08211808.e0a2706)
*Released 2024-08-21*

- refactored to use Attr ([`c0a736d`](https://github.com/sireum/aadl-gumbo/commit/c0a736d))
- allow grammar to be adapted to SysMLv2 ('cases' has to be converted to 'compute_cases' and the grammar must be case sensitive) ([`b1d0246`](https://github.com/sireum/aadl-gumbo/commit/b1d0246))
- modify grammar for use in SysMLv2 ([`361b467`](https://github.com/sireum/aadl-gumbo/commit/361b467))
- update feature ([`b033c44`](https://github.com/sireum/aadl-gumbo/commit/b033c44))
- refine error position loc ([`32449e8`](https://github.com/sireum/aadl-gumbo/commit/32449e8))

### [1.2024.04181415.5990efb](1.2024.04181415.5990efb)
*Released 2024-04-18*

- checks for well-formedness ([`1e9842a`](https://github.com/sireum/aadl-gumbo/commit/1e9842a))
- adapt to unaryExp changes ([`76cb80b`](https://github.com/sireum/aadl-gumbo/commit/76cb80b))

### [1.2024.02261857.2928b1b](1.2024.02261857.2928b1b)
*Released 2024-02-26*

- update MethodSig ([`0882134`](https://github.com/sireum/aadl-gumbo/commit/0882134))

### [1.2024.02220830.4d67aa7](1.2024.02220830.4d67aa7)
*Released 2024-02-22*

- General updates and maintenance (grammar regeneration / dependency bumps).

### [1.2023.10061732.b0cf3cb](1.2023.10061732.b0cf3cb)
*Released 2023-10-06*

- adapt to Stmt.Method signature change ([`5642697`](https://github.com/sireum/aadl-gumbo/commit/5642697))

### [1.2023.08021014.21d7eb2](1.2023.08021014.21d7eb2)
*Released 2023-08-02*

- process state var types ([`bd80d6a`](https://github.com/sireum/aadl-gumbo/commit/bd80d6a))

### [1.2023.07271345.065b5fa](1.2023.07271345.065b5fa)
*Released 2023-07-27*

- add HasEvent uif ([`f3fa5ed`](https://github.com/sireum/aadl-gumbo/commit/f3fa5ed))

### [1.2023.04051454.3dcd426](1.2023.04051454.3dcd426)
*Released 2023-04-05*

- Add F64 and F32 lit objects allowing for, e.g., F32.Nan ([`b7bc86d`](https://github.com/sireum/aadl-gumbo/commit/b7bc86d))

### [1.2023.03231646.2bf1dca](1.2023.03231646.2bf1dca)
*Released 2023-03-23*

- allow flow from/to clauses to have 0 or more ports and state variables, add AIR support ([`478073b`](https://github.com/sireum/aadl-gumbo/commit/478073b))
- Added 'infoflow' constructs and scoping rules. ([`727049d`](https://github.com/sireum/aadl-gumbo/commit/727049d))
- adapt to TypeParam changes ([`a033428`](https://github.com/sireum/aadl-gumbo/commit/a033428))

### [1.2022.11022102.e599639](1.2022.11022102.e599639)
*Released 2022-11-02*

- update modelsupport dep ([`12b2ef1`](https://github.com/sireum/aadl-gumbo/commit/12b2ef1))

### [1.2022.10111602.ca0ff6f](1.2022.10111602.ca0ff6f)
*Released 2022-10-11*

- add better feedback when unhandled GUMBO nodes are visited ([`8c71f4a`](https://github.com/sireum/aadl-gumbo/commit/8c71f4a))
- add support for Java float 'f' and double 'd' lits ([`476f1d4`](https://github.com/sireum/aadl-gumbo/commit/476f1d4))
- allow 'In' in compute assume clauses, add true/false literals ([`0f722e9`](https://github.com/sireum/aadl-gumbo/commit/0f722e9))

### [1.2022.10071304.a32b5c7](1.2022.10071304.a32b5c7)
*Released 2022-10-07*

- General updates and maintenance (grammar regeneration / dependency bumps).

### [1.2022.08231211.b12db9b](1.2022.08231211.b12db9b)
*Released 2022-08-23*

- standardize on using AGREE-like syntax ([`23ab351`](https://github.com/sireum/aadl-gumbo/commit/23ab351))

### [1.2022.08221314.0e4052e](1.2022.08221314.0e4052e)
*Released 2022-08-22*

- add support for Slang binary op precedence ([`c59b9af`](https://github.com/sireum/aadl-gumbo/commit/c59b9af))

### [1.2022.08191219.82466d5](1.2022.08191219.82466d5)
*Released 2022-08-19*

- adapt to Slang AST changes ([`39b71c4`](https://github.com/sireum/aadl-gumbo/commit/39b71c4))

### [1.2022.08111537.0f97c79](1.2022.08111537.0f97c79)
*Released 2022-08-11*

- add support for pure methods with contracts ([`7ad34b9`](https://github.com/sireum/aadl-gumbo/commit/7ad34b9))

### [1.2022.08091444.f63660a](1.2022.08091444.f63660a)
*Released 2022-08-09*

- add method support ([`cc0fbd9`](https://github.com/sireum/aadl-gumbo/commit/cc0fbd9))
- add support for annex libraries ([`f3dc53f`](https://github.com/sireum/aadl-gumbo/commit/f3dc53f))
- adapt to interface changes ([`b4f305b`](https://github.com/sireum/aadl-gumbo/commit/b4f305b))

### [1.2022.07051018.a740565](1.2022.07051018.a740565)
*Released 2022-07-05*

- add reporter ([`be2b8c9`](https://github.com/sireum/aadl-gumbo/commit/be2b8c9))

### [1.2022.06282118.230473f](1.2022.06282118.230473f)
*Released 2022-06-28*

- begin adding GCL function support ([`647aeea`](https://github.com/sireum/aadl-gumbo/commit/647aeea))
- support Slang XOR ([`6474de5`](https://github.com/sireum/aadl-gumbo/commit/6474de5))

### [1.2022.06242122.c1af472](1.2022.06242122.c1af472)
*Released 2022-06-24*

- Use Exp.Input, separate uifs for MustSend, add NoSend ([`2135aea`](https://github.com/sireum/aadl-gumbo/commit/2135aea))
- add NoSend, fix short-circuit implies ([`ce1ec0d`](https://github.com/sireum/aadl-gumbo/commit/ce1ec0d))

### [1.2022.06222050.06a7060](1.2022.06222050.06a7060)
*Released 2022-06-22*

- allow for spec statements in compute, introduce implication ops ([`4d7fe13`](https://github.com/sireum/aadl-gumbo/commit/4d7fe13))
- check for null ([`ee85af2`](https://github.com/sireum/aadl-gumbo/commit/ee85af2))

### [1.2022.06161903.68c1896](1.2022.06161903.68c1896)
*Released 2022-06-16*

- allow Slang-style strings inside string interpolations ([`e8aa957`](https://github.com/sireum/aadl-gumbo/commit/e8aa957))
- use fully qualified name ([`13d84ac`](https://github.com/sireum/aadl-gumbo/commit/13d84ac))

### [1.2022.06151822.8f00475](1.2022.06151822.8f00475)
*Released 2022-06-15*

- handle In, MaySend, MustSend ([`1202f80`](https://github.com/sireum/aadl-gumbo/commit/1202f80))
- Corrected the handling of enums on non-implementation data components, and components in the same package as the reference. ([`aefc7be`](https://github.com/sireum/aadl-gumbo/commit/aefc7be))

### [1.2022.06081955.eb93186](1.2022.06081955.eb93186)
*Released 2022-06-08*

- add pos info to state vars, fully qualify enum refs ([`5b7b965`](https://github.com/sireum/aadl-gumbo/commit/5b7b965))
- Changed the syntax of enum references from 'enum(a::b, c)' to 'a::b.c'. ([`49284f8`](https://github.com/sireum/aadl-gumbo/commit/49284f8))

### [1.2022.06011655.d0c1d8e](1.2022.06011655.d0c1d8e)
*Released 2022-06-01*

Initial release. Notable functionality included at this point:

- adapt to GCL changes ([`33e9fe3`](https://github.com/sireum/aadl-gumbo/commit/33e9fe3))
- enable backtracking, use new description field rather than id for now so tests still pass ([`6d949b3`](https://github.com/sireum/aadl-gumbo/commit/6d949b3))
- Added value expressions as parameters to the 'MaySend' and 'MustSend' operators. ([`384a719`](https://github.com/sireum/aadl-gumbo/commit/384a719))
- Added implication ('->:') statements and handle clauses to the annex grammar; fitted all named assume, guarantee, and implication statements with a mandatory ID and an optional string descriptor. ([`5c51e34`](https://github.com/sireum/aadl-gumbo/commit/5c51e34))
- Added 'MaySend' and 'MustSend' statements to the annex grammar. ([`e07d450`](https://github.com/sireum/aadl-gumbo/commit/e07d450))
- Added the 'In' expression to the annex grammar. ([`888d0dd`](https://github.com/sireum/aadl-gumbo/commit/888d0dd))
- resolving Mac case issue ([`11b52ff`](https://github.com/sireum/aadl-gumbo/commit/11b52ff))
- add modifies to entrypoints ([`e118e00`](https://github.com/sireum/aadl-gumbo/commit/e118e00))
- change to gumbo2air ([`3e3584b`](https://github.com/sireum/aadl-gumbo/commit/3e3584b))
- remove unused deps ([`3e10bd0`](https://github.com/sireum/aadl-gumbo/commit/3e10bd0))
- add gumbo2air projects ([`90066ea`](https://github.com/sireum/aadl-gumbo/commit/90066ea))
- add literal interpolation ([`b1e3232`](https://github.com/sireum/aadl-gumbo/commit/b1e3232))
- changes required for AIR encoding ([`47cf97d`](https://github.com/sireum/aadl-gumbo/commit/47cf97d))
- Further improvements to the GUMBO annex grammar. ([`33e2e2f`](https://github.com/sireum/aadl-gumbo/commit/33e2e2f))
- Updated the annex grammar to include most of the Slang expression grammar. ([`e08df6d`](https://github.com/sireum/aadl-gumbo/commit/e08df6d))
- First crack at adding function definitions/calls to the GUMBO annex. Function bodies are GUMBO expressions; types are AADL data components. ([`86eafdc`](https://github.com/sireum/aadl-gumbo/commit/86eafdc))
- Removed OSATE development environment dependencies from plugin projects. ([`b20c4e0`](https://github.com/sireum/aadl-gumbo/commit/b20c4e0))
- Added containment-path-style references into the interiors of AADL data components (ports, subcomponents, or state variables). ([`3bf1952`](https://github.com/sireum/aadl-gumbo/commit/3bf1952))
- small updates to contracts in temp control component ([`d5ffde9`](https://github.com/sireum/aadl-gumbo/commit/d5ffde9))
- Add TempControlSimpleTemp model artifacts ([`4393529`](https://github.com/sireum/aadl-gumbo/commit/4393529))
- Fixed resolution of enum fields. ([`4c0252f`](https://github.com/sireum/aadl-gumbo/commit/4c0252f))
- Added support for record literals to the GUMBO annex grammar; checked in the updated 'FooBar' package. ([`7234a8f`](https://github.com/sireum/aadl-gumbo/commit/7234a8f))
- change PortRef to point to a FeatureElement, update unit tests ([`b36e756`](https://github.com/sireum/aadl-gumbo/commit/b36e756))
- Introduced several productions from the AGREE expression grammar, and corresponding scoping rules. ([`f3e93da`](https://github.com/sireum/aadl-gumbo/commit/f3e93da))
- Removed files generated by the Xtend compiler. ([`1650ef5`](https://github.com/sireum/aadl-gumbo/commit/1650ef5))
- Incorporated changes to the GUMBO annex grammar from @John-Hatcliff; corrected scoping on state variable references and the types of state variables. ([`bad264e`](https://github.com/sireum/aadl-gumbo/commit/bad264e))
- adapt to OSATE dev 2021.03 ([`feca099`](https://github.com/sireum/aadl-gumbo/commit/feca099))
- add tests ([`15d1fcc`](https://github.com/sireum/aadl-gumbo/commit/15d1fcc))
- add test ([`dc2581e`](https://github.com/sireum/aadl-gumbo/commit/dc2581e))
- add hyperperiod scoping ([`ec0aad4`](https://github.com/sireum/aadl-gumbo/commit/ec0aad4))
- add rest of acl grammar ([`1073b10`](https://github.com/sireum/aadl-gumbo/commit/1073b10))
- scoping ([`a8ded3d`](https://github.com/sireum/aadl-gumbo/commit/a8ded3d))
- add comp model and flows ([`d774ea0`](https://github.com/sireum/aadl-gumbo/commit/d774ea0))
- add readme ([`1f7b3d4`](https://github.com/sireum/aadl-gumbo/commit/1f7b3d4))
- initial ([`fdef528`](https://github.com/sireum/aadl-gumbo/commit/fdef528))

