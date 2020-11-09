# CloudPubSub
A cloud message subscriber for client

The Google Cloud Pub/Sub service allows applications to exchange messages reliably, quickly, and asynchronously. To accomplish this, a data producer publishes messages to a Cloud Pub/Sub topic. A subscriber client then creates a subscription to that topic and consumes messages from the subscription. Cloud Pub/Sub persists messages that could not be delivered reliably for up to 7 days.

# Core Steps:

(1) create a Virtual Evn.

(2) create Pub/Sub topic.

(3) create Pub/Sub subscriber for client.

(4) public message to topic.

(5) to delivery (indivisual) output topic meassage using a Pull Subsriber.

-----

from step 1:

> create a virtual env.

* 1.1, log in and activate the cloud shell, list the proj-id, then type the cmd line below.

      sudo apt-get update
      
      sudo apt-get install virtualenv
      // python virtual env is used to isolate the installation from sys.
      
      virtuallen -p python3 env
      
      source venv/bin/activate
      
 > from step 2:
 
 > create a pubsub client from cloud.
 
 * 2.1, install google-cloud-pubsub to python pkg.
 
       pip install --upgrade google-cloud-pubsub
       
 * 2.2, get pkg from github.
 
       git clone https://github.com/QueenieCplusplus/PubSub_Python_App.git
      
       cd PubSub_Python_App
       
  * 2.3, get Google Proj ID
  
        export GLOBAL_CLOUD_PROJECT=GCP Project ID

  * 2.4, edit/running code file
  
        cat publisher.py
        
        python publisher.py -h
        
        python publisher.py $GLOBAL_CLOUD_PROJECT create MyTopic
        
        
