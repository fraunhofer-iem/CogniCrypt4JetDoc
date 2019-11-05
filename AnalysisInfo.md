# CogniCrypt Analysis 

## General Overview

![CogniCrypt Marker](Images/CCArch.PNG) 

The above image shows the relevant components for performing the analysis. The IDE plugins are build on top of a [GitHub Project called CryptAnalysis](https://github.com/CROSSINGTUD/CryptoAnalysis). Beside some huge abstractions to the lower components which realize the core analysis also in this component the CrySL Engine is located. The API-specif CrySL rulesets are maintained in [this repository](https://github.com/CROSSINGTUD/Crypto-API-Rules).

The Soot component is mainly responsible for transforming Java Bytecode into a new intermediate language called *Jimple*. The other components like *Boomerang* are realizing the precise Data-Flow analysis upon the Jimple representation.


## Analysis Input
In general there are two main inputs required to run a CogniCrypt analysis.
1. The compiled JVM Bytecode of the user's application
2. A CrySL ruleset

As explained [here](CrySLRules.md) the plugin already comes with an ruleset which can be exchanged. 

As for the compiled JVM Bytecode input a distinction for common java application and Android Apps must be made. 
### IntelliJ

**<span style="color:#0088FF">TODO: Add IntelliJ infos</span>**.

### Android Studio
The primary Bytecode input in Android Studio are compiled Android Apps *(.apk files)*. Such an .apk File must be handled differently than .class or .jar files. By default the Plugin automatically searches for applicable Apps inside the **debug build folders** of the loaded Android App Project.  
### Custom Input

Beside the automatic detection of input files for the analysis the user always has the option to choose custom inputs. Also, when multiple applications to analyze are found, the user will be asked which ones should be included to the analysis. Not analyzing every possible build of a project might be a good idea to save time or keep focus on relevant findings.

Options for changing the behavior of the automatic input search are described [here](AnalysisTargetSettings.md).

### Caching
On every build action performed on the project the plugin (if necessary) invalidates caches that hold information about analysis input choices. E.g. this includes a specific Android App file that was analyzed last time. If the cached information are out of date the user will be asked what to do next time the analysis is started.  

## Analysis Findings
All CogniCrypt findings get displayed in the dedicated [CogniCrypt Tool Window](). Additionally a code marker will be placed on the text editor at the position where the finding is located. Hovering over that marker will give you information what the error is and gives you a hint how to fix it.

![CogniCrypt Marker](Images/CCMarkers.PNG)  
