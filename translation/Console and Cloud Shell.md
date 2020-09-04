# LAB: CONSOLE AND CLOUD SHELL

## OBJECTIVES:
In this task, you will learn how to perform the following tasks;

        -Create a Cloud Storage bucket using Cloud Shell.

        -Become familiar with Cloud Shell features.

## STEPS
     
1.         Create a Cloud Storage bucket using Cloud Shell.

                    -Open Cloud Shell
                    -gsutil mb gs://<BUCKET_NAME>

## Replace <BUCKET_NAME> with a globally unique name

          Result:You have created a bucket using the Cloud Shell.

2.          Explore More Cloud Shell Features.

    1. Upload a File

            -Open Cloud Shell
            -Click on the three dot icons in the cloud shell toolbar to display further options. 
            -Click Upload file. Upload any file from your local machine to the Cloud Shell VM. This file will be referred to as [MY_FILE].
            -In Cloud Shell, type ls to confirm that the file was uploaded.
            --gsutil cp [MY_FILE] gs://[BUCKET_NAME]


            -Result: You have uploaded a file to the cloud shell VM and copied it to a bucket. 

    2.  Create a Persistent State in Cloud Shell

        1. Identify Available regions

                -Open Cloud Shell from the cloud Console. 
                --gcloud compute regions list

        2.  Create and Verify an Environment Variable.

                --INFRACLASS_REGION=[YOUR_REGION]
                --echo $INFRACLASS_REGION
       
        3.  Append the Environment Varialbe to a File

                --mkdir infraclass
                --touch infraclass/config
                --echo INFRACLASS_REGION=$INFRACLASS_REGION >> ~/infraclass/config
                --INFRACLASS_PROJECT_ID=[YOUR_PROJECT_ID]
                --echo INFRACLASS_PROJECT_ID=$INFRACLASS_PROJECT_ID >> ~/infraclass/config
                --source infraclass/config
                --echo $INFRACLASS_PROJECT_ID

            Result: You should now see the expected value that you set in the config file.




