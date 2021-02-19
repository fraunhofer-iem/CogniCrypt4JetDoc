# CogniCrypt for IntelliJ-based IDEs

## Information
CogniCrypt is an intelligent open-source platform ensuring the secure usage of crypto components.

CogniCrypt for IntelliJ-based IDEs is developed by [Fraunhofer IEM](https://www.iem.fraunhofer.de). It provides a static code analysis that allows developers to quickly identify misuses of cryptographic libraries.

## Installation

1. In the Settings/Preferences dialog *(Ctrl+Alt+S)*, select **Plugins**.
2. On the **Plugins** page, click the **gear icon** and then click **Manage Plugin Repositories**.
3. In the **Custom Plugin Repositories** dialog, click The **+** icon and enter the URL: `https://raw.githubusercontent.com/fraunhofer-iem/CogniCrypt4JetBuilds/master/updatePlugins.xml`. 
4. Click **OK** in the dialog to save the list of plugin repositories.
5. Search for CogniCrypt in the search box. 
6. Click **Install** and restart the IDE when asked. 

#### **Important Additional Setup**  
To assure you don't receive any StackOverflowError exceptions while the analysis is running you need to increase the stack size and allocated memory of the IDE:

1. Go to **Help** > **Edit custom VM options...** 
2. Enter the lines: 
```
-Xmx4g 
-Xss100m
```

*`-Xmx4g` can be replaced with a custom GB number. Recommended are at least 4GB.* 


## Getting Started
After installing CogniCrypt you can run an analysis for the opened IDE Project. 

In the Main Menu open the **Analyze** menu and click **Run CogniCrypt**.

## Documentation
For further information about the CogniCrypt Plugin please see the full documentation **[here](UsingCogniCrypt.md).**

## Updates
The IDEs manage updates of CogniCrypt automatically. To check if a new update is available, regularly check the Plugins settings. 

1. In the Settings/Preferences dialog *(Ctrl+Alt+S)*, select Plugins.
2. Use the Installed tab to browse for CogniCrypt.
3. Press the Update button and restart the IDE if required.

## Terms of Use and License
This repository purposely comes **without** a LICENSE. Read [here](https://choosealicense.com/no-permission/) what this means.


[//]: <> (# Terms of Usegf
This repository, the content it holds and the link of this repository must not be shared, forked, copied, processed or distributed in any other forms other than IntelliJ-based IDEs required it to manage the plugin installation.)

[//]: <> (# License
Until further notice the builds and code of CogniCrypt for IntelliJ-based IDEs are exclusively owned by Fraunhofer IEM. Permission and conditions of usage can only be granted by Staff of the Fraunhofer IEM department Software Engineering and IT Security.)

## Credits

 

This work is part of the research project "AppSecure.nrw - Security-by-Design of Java-based Applications". The project is funded by the European Regional Development Fund (ERDF-0801379). 
<br/>
  <br/><img src="https://github.com/AppSecure-nrw/funding-notice/blob/main/Logo_48_lang_Zeichenfl%C3%A4che%201.png" alt="AppSecure.nrw Logo" height="50"/>
  
<img src="https://github.com/AppSecure-nrw/funding-notice/blob/main/EFRE_Foerderhinweis_englisch_farbig.jpg" alt="EFRE Logo" height="50"/> <img src="https://github.com/AppSecure-nrw/funding-notice/blob/main/Ziel2NRW_RGB_1809_jpg.jpg" alt="Ziel2NRW Logo" height="50"/>
