# CreditSense

## Introduction

CreditSense is MLaaS for approving loans.

## Description

### Tech Stack

- Build: Gradle
- ML: Python/R, H2O, Six
- REST API: Java, Spring Boot

## Contributing

- Build project
  ```
   ./gradlew build                    # Run R script (loan-approver-model.R) to generate POJOs
   ./gradlew build -PpythonBasedMLModel=true   # Run Python script (loan-approver-model.py) to generate POJOs
  ```
- Run Load Approver Spring Boot Application

  ```
   java -jar loanapprover-0.0.1-SNAPSHOT.jar
  ```

  Alternatively, once loanapprover-0.0.1-SNAPSHOT.jar is build, docker container can be launched as shown below:

        1. build docker image

             docker build -t loanapprover .

        2. build docker image

             docker run loanapprover

- Swagger Definition of the Load Approver application
  ```
  http://localhost:8080/swagger-ui.html
  ```