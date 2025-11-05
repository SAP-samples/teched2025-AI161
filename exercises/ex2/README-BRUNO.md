# Exercise 2 - Exercise 2 Description

In this exercise, we will evaluate our basic prompt using the evaluation data set provided and the AI Core evaluation service.

## Exercise 2.1 Create a template for the base prompt

After completing these steps you will have created and stored a prompt template, and evaluated it with a set of metrics. 

### 2-1-1 Create the prompt template
First let's create a prompt template for the basic prompt provided in the data folder.
1. Open request 2-1 Create base prompt template in the Bruno API client.
2. Check that the system messages provided in the request body match the basic prompt located in the data/prompts/facility_prompt_basic.yaml file.
3. Execute the request to create the prompt template in the prompt registry by clicking the left arrow.
4. You should receive a response message saying that the prompt was created successfully. A script copies the prompt template id from the response body and stores it in an environment variable for later use.

### 2-1-2 Check your stored template
Let's retrieve and check our stored template.
1. Open request 2-2 Check base prompt template in the Bruno API client.
2. Note that the request uses the environment variable promptTemplateID in the request URL.
3. Execute the request by clicking the left arrow.
4. You should see your stored prompt template in the response.

## Exercise 2.2 Upload Evaluation Data Set

After completing these steps you will have uploaded the evaluation data set as an artifact in AI Core.

1. Open request 2-2-1 Upload evaluation data set in the Bruno API client.
2. Click on the Body Tab.
3. Click on Select File and select the facility_eval_data.json file located in the data/datasets folder.
4. Execute the request to upload the data set to the object store via the dataset API.

Now let's verify that the data set was uploaded successfully to the intended location.

1. Open request 2-2-2 Check your dataset in the Bruno API client.
2. Execute the request to view the contents of your dataset file in the object store.

Now we can register this file as an artifact in AI Core.

1. Open request 2-2-3 Register artifact in the Bruno API client.
2. Check the parameters set in the request body.
3. Execute the request to register the artifact in AI Core.
4. You should receive a response message saying that the artifact was acknowledged. A script copies the artifact id from the response body and stores it in an environment variable for later use.

Finally, let's check that we can access the artifact.
1. Open request 2-2-4 Check your artifact in the Bruno API client.
2. Execute the request to view the details of your artifact in AI Core.

## Exercise 2.3 Configure and run the evaluation

Now that we have successfully prepared a prompt template and an artifact with our evaluation data set, we can configure and run an evaluation with the AI Core evaluation service. 

### 2-3-1 Check available models
1. 

### 2-3-2 Check avialable metrics
1.

### 2-3-3 Configure your Evaluation
1. Open request 2-3-3 Configure the Evaluation in the Bruno API client.

### 2-3-4 Start the Evaluation

## Summary

You ha've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)
