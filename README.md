# Final Project : Hands-on Introduction to Linux Commands and Shell Scripting, IBM


## Scenario

Imagine that you are a lead Linux developer at the top-tech company ABC International Inc. ABC currently suffers from a huge bottleneck: each day, interns must painstakingly access encrypted password files on core servers and back up any files that were updated within the last 24 hours. This process introduces human error, lowers security, and takes an unreasonable amount of work.

As one of ABC Inc.'s most trusted Linux developers, you have been tasked with creating a script called backup.sh which runs every day and automatically backs up any encrypted password files that have been updated in the past 24 hours.

## Learning Objectives

By completing this final project, you will:
+ Demonstrate your advanced shell scripting skills in a real-world scenario
+ Apply the knowledge you've gained to reviewing and grading technical work submtted by your peers

## Overview
### Hands-on lab: Scheduled Backup Script
#### Instructions

Immediately following this reading, you will complete the hands-on lab portion of your final project where you will create a scheduled backup script.

Your work will be graded by your peers who are also completing this assignment within the same session. Likewise, as part of your final project requirements, you will also review the work done by your peers.
#### Deliverables

You will need to submit the following items for peer review:

    Screenshots clearly displaying both the code and the output for each task
    Your completed script file

Full details are provided for each task within the hands-on lab.


#### Detailed steps

##### Task 0: Getting started
+ Download the template file `backup.sh` when the following command:
```bash
wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/Final%20Project/backup.sh
```

##### Task 1: Code readabilty
+ Set `targetDirectory` to the first command line argument
+ Set `destinationDirectory` to the second command line argument 
##### Task 2: Display the two command line arguments
##### Task 3: Define the variable currentTS as the current timestamp in seconds.
##### Task 4: Define the backupFileName as "backup-[$currentTS].tar.gz"
##### Task 5: Define `oriAbsPath` as the absolute path of thecurrent directory
##### Task 6: Define `destAbsPath` as the absolute path of the destination directory