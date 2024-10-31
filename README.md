# Overview
Building a CI/CD Pipeline in Udacity Cloud DevOps using Microsoft Azure course


Azure Pipeline status bar
[![Build Status](https://dev.azure.com/huongttt13/HuongTTT13-Project2/_apis/build/status%2FTranThuHuong0510.azure-devops-project2?branchName=master)](https://dev.azure.com/huongttt13/HuongTTT13-Project2/_build/latest?definitionId=3&branchName=master)

Action Status bar
[![Python application test with GitHub Actions](https://github.com/TranThuHuong0510/azure-devops-project2/actions/workflows/master.yml/badge.svg)](https://github.com/TranThuHuong0510/azure-devops-project2/actions/workflows/master.yml)

## Project Plan
* Trello board: https://trello.com/b/vGzvcnls/q4-2024-huongttt13-udacity-devopsproject-2
* A link to a spreadsheet: https://docs.google.com/spreadsheets/d/1I132F0j7iaG-qobK8dAlahcKzY2KG57JmJ3UAfut7n8/edit?usp=sharing

## Instructions
* Architectural Diagram
  ![diagram](https://github.com/user-attachments/assets/50fdc747-c71b-41f6-baad-7ef7b5ed1cf1)


Instructions for running the Python project.  How could a user with no context run this project without asking you for any help.  Include screenshots with explicit steps to create that work. Be sure to at least include the following screenshots:

1. Clone this repository in Cloud Shell
   - If use SSH, you need to add SSH key to Github
2. Create the Python Virtual Environment
   python3 -m venv ~/.myrepo
  source ~/.myrepo/bin/activate
3. Run make all and make sure it is successfully (like my screenshot)
4. Deploy webapp by execute ./commands.sh
   Test predict:
   cat make_prediction.sh
  chmod +x make_predict_azure_app.sh
  ./make_predict_azure_app.sh
In a new Azure Cloud Shell terminal run the following command az webapp log tail to view the current logs of our web application
5. Create project in Devops
 - Create project
 - Add Service Connections
 - Create an Agent Pool
 - Create an Agent (VM)
 - Configure the Agent (VM) - Install Agent Services - Make sure status is Running as my screenshot in Images
 - Create a Pipeline with gihub repository with azure-pipelines.yml6.
 - Azure Pipelines will now run for the first time and it will update the deployed project application
6. Start locust in your local environment by locusttest.sh
* Project running on Azure App Service
![image](https://github.com/user-attachments/assets/0ccbb556-31ee-4144-862a-95461421c71e)

* Project cloned into Azure Cloud Shell
![image](https://github.com/user-attachments/assets/acea23b0-127c-4aa1-84bb-fd024429d463)

* Passing tests that are displayed after running the `make all` command from the `Makefile`
![image](https://github.com/user-attachments/assets/bc57d9c7-7e4f-48de-81fd-dba7d1d09942)
![image](https://github.com/user-attachments/assets/7ce93ebc-ec6b-4bf2-bc92-be2213cd00b6)



* Output of a test run
![image](https://github.com/user-attachments/assets/80aad8e7-6016-4d24-9907-3be9b538bf77)

* Successful deploy of the project in Azure Pipelines.  [Note the official documentation should be referred to and double checked as you setup CI/CD](https://docs.microsoft.com/en-us/azure/devops/pipelines/ecosystems/python-webapp?view=azure-devops).
  ![image](https://github.com/user-attachments/assets/696bd3a4-ac54-41fe-a158-5627810e8182)


* Running Azure App Service from Azure Pipelines automatic deployment
  ![image](https://github.com/user-attachments/assets/43c1ecd3-8eb4-4ca4-82c7-4fb2c8167dc2)

![image](https://github.com/user-attachments/assets/7061f51e-afb5-48d6-bd1b-93c7f0a80420)


* Successful prediction from deployed flask app in Azure Cloud Shell.  [Use this file as a template for the deployed prediction](https://github.com/udacity/nd082-Azure-Cloud-DevOps-Starter-Code/blob/master/C2-AgileDevelopmentwithAzure/project/starter_files/flask-sklearn/make_predict_azure_app.sh).
The output should look similar to this:
![image](https://github.com/user-attachments/assets/f88b9a52-0239-4206-9c02-7c2ed7626a89)

```bash
udacity@Azure:~$ ./make_predict_azure_app.sh
Port: 443
{"prediction":[20.35373177134412]}
```

* Output of streamed log files from deployed application
![image](https://github.com/user-attachments/assets/1e2ca055-81c4-4ef3-b477-eff2f9bcd9d6)

>
> Locust test
![image](https://github.com/user-attachments/assets/a37bd98a-47a0-494e-bc2e-1ab89e00b176)
![image](https://github.com/user-attachments/assets/50127b3d-d2b9-4d2d-9e27-c750e2c53c33)


## Enhancements

<TODO: A short description of how to improve the project in the future>

- UI design
- Pipeline improvement for dev, staging, production

## Demo 

<TODO: Add link Screencast on YouTube>


