**Sauce Demo Test Automation**

This document explains about the framework components and steps to execute the scripts.

**Prerequisites**

1. Install JAVA (JDK) and update the environment variable with JDK installation path
2. Install GIT and configure to clone the project from repository
3. Install IntelliJ IDE
4. Update POM.xml dependencies with the latest Selenium and TestNG versions.

**Framework Components**

**1. resources folder (src/main/resources):**

Place where all the browser drivers, configuration files are placed and used by scripts to run on specific browser.

**1.1 Config.properties file:**
File where environment specific details are placed.

**2. pageobjects folder (src/main/java/com/saucedemo/test/pageobjects):**
This folder contains all the page level elements, getters and setters.

**3. utils folder (src/main/java/com/saucedemo/test/utils):**
This folder contains all the common util class files which are reusable.

**4. testcases folder (src/test/java/com/saucedemo/testcases):**
This folder contains all the TestNG classes (Test scripts) designed by using page objects and utils classes.

**5. TestNG-XML folder:**
This folder contains all the TestNG xml files used to execute TestNG classes. We can create a regression suite by placing all the test scripts in these TestNG xml files.

**6. pom.xml file:**
All the project level dependencies are placed in this file. We can create profiles to execute regression suite either local or through Jenkins.

**7. .gitignore file:**
This file contains all the folders and files which we want to ignore while pushing the code to Git repository.

**How to run the tests:**

1. Clone this project to local
2. Navigate to Build -> Build Project (Which installs all the dependencies of the project)
3. Navigate to TestNG-XML folder and select an xml file which user wants to execute
4. Right click the xml file and select "Run 'xml file name'"
5. Execution log should be displayed in the IDE console

**Reporting:**
Once the xml execution is completed follow below steps to get the emailable report
1. Refresh the project
2. Navigate to test-output folder
3. Select emailable-report.html file -> right click -> select open with browser to view the report in html format
