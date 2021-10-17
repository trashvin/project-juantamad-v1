# Project JuanTamad v1

Just Another TimeIn/Out Automated Management Application Duh! or JuanTamad is a daily email time recording system app using Power Automate Desktop. Ok, this is not a standalone app, you need Microsoft Power Automate Desktop to use it. And, unlike a regular app, you cant just download and install, you need to recreate the flow... manually, inside PAD.

<p align="center">
  <img src="_poster.png" />
</p>

## Who is JuanTamad ?

JuanTamad is a fictitious person known to Filipinos representing the lazy portion of the population. In an old story, he used to lay with mouth wide open under a mango tree waiting for the fruit to fall due to gravity. This app, however, does not glorify laziness :) It aims to make the boring task of emailing our whereabouts before and after our daily shift simpler and easier using Power Automate Desktop. 

## Requirement

- Power Automate Desktop
- Microsft Outlook 
- Email Account

## 'Installation' Steps

<p align="center">
  <img src="https://i.imgur.com/897gqyt.png" />
</p>

### JuanTamad main app

- Download the repo to your local machine.
- Create a new flow in your Power Automate Desktop application. You can name it JuanTamad or any name.
- Copy the contents of src\JuanTamad\Main.pad to the Main flow.
- Create a subflow named 'load_configs'.
- Copy the contents of src\JuanTamad\load_configs.pad to the load_configs subflow.
- Create a subflow named 'log_to_excel'.
- Copy the contents of src\JuanTamad\log_to_excel.pad to the log_to_excel subflow.

### JuanTamad side kick app 

JuanTamadFT is a side-kick app for JuanTamad, it allows you to enter completed task within a day.

- Download the repo to your local machine.
- Create a new flow in your Power Automate Desktop application. You can name it JuanTamadFT or any name.
- Copy the contents of src\JuanTamadFT\Main.pad to the Main flow.
- Create a subflow named 'load_configs'.
- Copy the contents of src\JuanTamadFT\load_configs.pad to the load_configs subflow.

### Configure the app

Open the bin\settings.xml and modify the settings based on your need.

```
<settings>
 <name value="Trashvin Tester" />
 <reason value="Telework" />
 <version value="1.1" />
 <sendTo value="to@test.com" />
 <sendBy value="by@test.com" />
 <outSpeed value="False" />
</settings>
```

Settings :
- name : the main header of the email body
- reason : the reason for the email. Usually becase your doing a telework for the day.
- sendTo : the email address of the recipient
- sendBy : your email
- outSpeed : do you need to send your current internet speed when you do time-out?

## How To Use JuanTamad

Using JuanTamad is straight forward, you just need to run the flow in the morning when you do a time-in and in the late afternoon when you do the time-out. The app will record the data you are providing in text files and excel file. If you need to recall all the task you have accomplished for the week, you can just open bin\records.xlsx.

During your shift, if you have finished or currently doing a task that you want to record, just run the JuanTamadFT flow. Any data recorded by JuanTamadFT will appear when you do your time-out.

## NOTE 
This was created for fun while learning  Power Automate Desktop, enjoy!
