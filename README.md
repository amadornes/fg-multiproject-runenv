# ForgeGradle Multiproject Run Environment

This repository provides a run environment template for multiproject development environments using ForgeGradle.

In most cases none of these files will need to be modified in any way.  
It is a template in the sense that it can be extended, but it should cover most use cases by default.

This repository on its own will **NOT** result in a multiproject development environment.  
It **MUST** be paired with a root buildscript like the one found [here](https://github.com/amadornes/fg-multiproject-template).  
Setup instructions can be found in the aforementioned repository.

## Natively Configurable Elements
The following elements are externally configurable via the `ext` block on the project.
 - `mcversion`: Minecraft version **[required]**
 - `forgeversion`: Forge version **[required]**
 - `javaversion`: Java version
   - Default: 17
 - `mappings`: Mappings
   - Default: mojmap @ \<mcversion>
 - `runArgs`: Run arguments (all runs)
   - Default: []
 - `runProps`: Run properties (all runs)
   - Defaults:
     - `forge.logging.markers`: `REGISTRIES`
     - `forge.logging.console.level`: `debug`
     - `mixin.env.remapRefMap`: `true`
     - `mixin.env.refMapRemappingFile`: `${projectDir}/build/createSrgToMcp/output.srg`
     - 
Any other elements, such as dependencies may be externally configured through an `afterEvaluate` block.

## Verified Compatibility
 - Mixins
 - Access transformers
 - Custom sourcesets

## Contributions
Pull requests adding extended feature support and bugfixes are welcome.  
Please keep them simple if possible.
