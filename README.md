# News-Data-classification-
This project's objective is to categorize real-time data from a Kafka Server. This data source is linked to the Guardian API, responsible for delivering news updates. Our stream producer script continuously sends data to the Kafka Server at 20-second intervals. The data received from the Kafka Server will be categorized based on news topics. To achieve this, we'll initially train our model using historical data and then apply this model to classify the incoming streaming data from Kafka.
Ultimately, we plan to employ Elastic Search and Kibana for result visualization. Elastic Search will serve as the repository for our categorized data, organized into indexes. These indexes will be utilized by Kibana to create various visual representations

To run these project you need to follow these steps :
**Step 1 : Data Extraction from Guardian APIs**
To use this API, you will need to sign up for API key here:
https://open-platform.theguardian.com/access/
**Step 2 : Create a model using the extracted data**
create the pipeline model using model.ipynb . This file will save the model in a folder and will show its accuracy .
**Step 3 :**
Create a topic and then start it .
**Step 4 :**
Run the producer.py to create a kafka stream data 
**Step 5:** 
 Run  consumer.py file to read the stream , load the created model and generate the prediction on the fly. Then send data to elasticsearch 
       **!!** Please, add the saved model full path in the consumer.py file.
      **!!** you have to specify the ip address of your kafka broker in :producer.py and consumer.py
       **!!** if you didn't use any separate virtual machine all ip adresses must be set to :127.0.0.1 on producer.py and consumer.py 
[![image](https://www.linkpicture.com/q/Screenshot-2023-09-25-161902.png)](https://www.linkpicture.com/view.php?img=LPic651196ef0b7b4909732268)

[![image](https://www.linkpicture.com/q/Screenshot-2023-09-25-161848.png)](https://www.linkpicture.com/view.php?img=LPic6511972dd68c91453229749)
