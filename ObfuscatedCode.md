## Information for analyzing obfuscated Code

Currently CogniCrypt has some troubles analyzing **obfuscated Android Apps**.(.apk files).  
 **<span style="color:#0088FF">TODO: Check obfuscated .class and .jar files</span>**.

The noticeable impacts are:
- Analysis taking longer than with non obfuscated code.
- Analysis to source code mapping might not be correct.
- Analysis might not find errors.
- Analysis might report errors which are actually none.

## Guidance for Application Obfuscation and running the Analysis

Obfuscation is a popular method to protect certain assets and making it uneasy for understanding decompiled bytecode. By default in IntelliJ ProGuard can be included into the build pipeline, such as Gradle builds. 

As for now we recommend the following build and analysis steps:

1. Disable or remove ProGuard (or any other tool) from your build task.
2. Rebuild the code you with to analyze. 
3. Analyze the code with CogniCrypt.
4. Process the findings of the analysis 
5. Re-Enable the obfuscation tool and build the code *OR*  
   Manually obfuscate your application (like using the command line interface).