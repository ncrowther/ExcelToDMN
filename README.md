#  Excel to DMN Decision Table Generator

## Description

This asset generates DMN decision tables from Excel.  
Its primary purpose is for large decision tables to be created and maintained in excel and then generated into DMN.  

### Build environment

You will need:

* VSC
* Java 11+ installed
* Environment variable JAVA_HOME set accordingly
* Maven 3.5.2+ installed

## Create Excel Decision Table

The type of condition and action can be specified by appending a colon and then the DMN type. <br>
Multiple conditions but only a single action column is supported. <br>
Excel must be saved as CSV into folder `\excel` <br>

Example format here:  [WeatherAdvice.csv](https://github.com/ncrowther/ExcelToDMN/blob/main/excel/WeatherAdvice.csv)


## Generate DMN

* Open [ExcelToDMNGenerator.java](https://github.com/ncrowther/ExcelToDMN/blob/main/src/main/java/com/ibm/generator/ExcelToDMNGenerator.java)
* Right click and Run Java
* DMN files are generated in `\generated`
* Edit DMN files and replace input condition variables with real DMN inputs
* Move DMN file to `\src\main\resources`
* To build and run DMN see next section

#### Compile and Run in Local Dev Mode

```sh
mvn clean compile quarkus:dev
```

## API

```sh
http://localhost:8080/q/swagger-ui
```

