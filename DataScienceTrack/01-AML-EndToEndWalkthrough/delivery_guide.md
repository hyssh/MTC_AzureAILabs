# Delivering the lab as a half-a-day workshop.

This lab was designed to be instructor led. It is expected that the instructor will walk students through the lab's notebooks 
explaining key concepts, code snipptets, and answering any questions.

You can run the lab as a four part workshop, each part taking roughly 45 minutes. *Part 2 - feature engineering* and *Part 3 - training* can take a little bit longer but *Part 1 - introduction*  and *Part 4 -  deployment* will most likely take a little bit less then 45 minutes. 

If you account for breaks the workshop will take about 4 hours.


This is the recommended flow through the workshop. By no means this is cast in stone. Please feel free to fine tune based on your audience. 




1. Part 1 - Introduction - `00-intro.ipynb`

   1. Start with an overview of Azure AI using the current *Azure AI Pitch* and *Machine Learning Pitch* decks. The latest and greatest version of the decks are maintained on MTC AI community site. 
   2. After the presentation, walk the students through the pre-requisites setup  
   3. Explain the lab scenario.
   4. Deep diving into Deep Learning IS NOT the goal of this lab, but be prepared to briefly describe (at a very high level) key Deep Learning concepts including Transfer Learning. 
   5. Go over key Azure Machine Learning service components and a typical machine learning workflow in the context of Azure ML
   6. Walk the students through the Workspace provisioning code 
   7. Go through AML web interface in Azure Portal, drilling down to each section.
   
2. Part 2 - Feature Engineering - `01-feature-engineering.ipynb`
   1. Explain what a script is in the context of Azure Machine Learning service
   2. Explain how to control the script's behaviour through command line parameters
   3. Quickly go over `ImageGenerator` class and emphasize the importance of taking performance and hardware limitations into consideration when dealing with real life data sets. For example, it would not be feasible to load all images into memory and the `ImageGenerator` class addresses that by reading and processing images in chunks.
   4. Explain how **ResNet50** is instantiated with pre-trained parameters and how it is used to pre-process images.
   5. Explain what AML Compute Target is and walk through the code that provisions Azure DSVM.
   6. Explain what AML Datastore is and how to use Datastores to manage both input training and validation data and output files created by the job
   7. Explain what AML Experiment is.
   8. Explain what AML Run is.
   9. Explain the concept of Estimators and Run configurations. Deep dive into the details of configuring custom run environments and connecting Compute Targets to Datastores
   10. Explain what AML Jupyter widgets are and how to use them to monitor the AML jobs.
 
3. Part 3 - Training and Hyper Parameter Tuning - `02-train.ipynb`
   1. Go over the training script. Explain how the script uses `Run` object to track `training and validation accuracy` in AML Experiment. Elaborate on the role of AML Experiment in managing artifacts created by training runs.
   2. You don't need to go into the details of the Artificial Neural Network architecture used in the lab. It is not critical in the context of the goal of the lab. Just explain that AML supports any framework and that in this lab we are using TensorFlow Keras to create a simple Fully Connected Neural Network to act as an image classifier. And that there are a few hyperparameters that control the training behaviour of the network.
   
   3. Dive a little bit deeper into Azure Batch AI and how we are using Azure Batch AI cluster as a compute target in this lab.
   4. Explain what `hyperdrive` is and how it can be used to run distributed hyper parameter tuning jobs. The students may ask about different parameter sampling and termination strategies. Be prepared to explain which ones we support in Azure ML.
   5. Deep dive into Model Registry and how it can be used to manage multiple versions of a model.
   
4. Part 4 - Operationalization - `03-deploy.ipynb`
   1. Deep dive into different options for model deployment
   2. Deep dive into how to write scoring scripts
   3. Explain how AML creates custom docker images to support different deployment runtimes
   4. Explain what AML Deployments are.
   
  

