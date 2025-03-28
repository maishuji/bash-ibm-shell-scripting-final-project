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
##### Task 7: Change directory to target directory
##### Task 8: Define variable with timestamp of yesterday ( today - 24 hours )
##### Task 9: Write command to return ll files and directories in the current folder
##### Task 10: Check whether the file was modified within the last 24 hours
##### Task 11: If is satisfied, add the file to the backup
##### Task 12: Create a tar.gz file with the files that were modified in the last 24 hours
##### Task 13: Move the tar.gz file to the destination directory


##### Task 14: Download the script
##### Task 15: Check executable
+ `ls -l backup.sh`
##### Task 16: Download the following `.zip` file with `wget` :
+ `wget https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBM-LX0117EN-SkillsNetwork/labs/Final%20Project/important-documents.zip`
+ unzip the file : `unzip -DDo important-documents.zip`
+ update the file' s last modified to now : `touch important-documents/*`
+ test the script : `./backup.sh important-documents .`
##### Task 17: Set a cronjob to run the script for every 1 minutes
+ Add in `crontab -e` the entry `*/1 * * * * /usr/local/bin/backup.sh /home/project/important-documents /home/project`
+ `sudo service cron start`
+ `sudo service cron stop`
+ Using crontab, scehdule `usr/local/bin/backup.sh` script to backup the `important-documents` folder every 24 hours to the directory `/home/project`
+ Check the output of `crontab -l`