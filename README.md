# The CardGame


**Summary:** The Card Game project is implemented using open source api automation framework called Karate. Karate tests are written in BDD syntax (Given , When Then), easy to understand for non-programmers too.

**Pre-requisites:**
To implement this framework, following tools are required:

- Java (at least java 8)
- Maven
- Git (Git Extensions or GitHub Desktop)
- Visual Studio Code (recommended)
- VS Code Plugins
  - Cucumber (Gherkin) Full support
  - Karate Runner
  - Java Extension pack
  - Maven for Java

**Project Setup:** 
Create a local repository folder (for example: C:\cardGame) Download the cardGame.zip from repository https://github.com/ssyed009/cardGame/

Extract all files in local repository.

Open VSCode and select File >> Open Folder , select the local folder and click Select Folder.

**Framework Implementation:**

The GameCard project has multiple files/folders as part of framework, below is a brief description of each folder.:


**POM.XML:**
The POM.XML has all the dependencies and plugin information.

**Karate-config.js:**
Karate framework expects a config file, and this file contains the environment information like URL, global variables, user login details and authorization token information.

**Helpers Folder:**
This folder contains the common feature files or resusable code needed to execute tests.
isBlackJack.js is a common javascript utility cerated for determining if player hand has a blackjack , which will be called in the feature file.
DataGenerator.java is a common function that generates random data by using faker library.

**deck folder:** deck folder contains all feature files, test data and test runner file.

**testdata:**
testdata folder can be used to store the external files or request payload required for the project. 
For example, json, csv, excel, images .. etc

**Target folder:**

Reports generated after running the tests are stored in target folder. This project implements both Junit and Cucumber reports.

**Execute the Test framework:**

Note: Maven is used as a bulld tool to run the tests , if Maven_Home is not setup, please add maven to path in system environment variables.

**Feature File/Scenarios:** 
CradGame project has one feature file checkForBlackJack.feature with following scenarios:
Navigate to deck of cards website and verify the site is up.
Get a new deck, shuffle the cards , draw the cards for each player and check for blackjack.


**Instructions to execute the tests:**

1. Open the project in VsCode
2. Navigate to deck folder
3. Select checkForBlackJack.feature
4. To run the scenarios individually , Clcik Run option provided by Karate Runner extension.
5. To run all the tests , navigate to the terminal in VSCode and enter  mvn test
6. Once the tests are successfully run , the reports will be generated in target folder.

**Reports:**
HTML Report will be published to DeckOfCards\target\karate-reportsfolder

Cucumber HTML Reports will be published to DeckOfCards\target\cucumber-html-reports



