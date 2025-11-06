# Exercise 1 - Setup Bruno API Client

In this exercise, we will setup the Bruno API client to work through the following exercises.

## Prerequisites

Install the Bruno API client on your local machine. You can download it from [here](https://www.usebruno.com/downloads).

## Exercise 1.0 Setup Bruno API Client

After completing these steps you will have setup the Bruno API client with the collection provided in this tutorial.

1. Find the Bruno API client on your local machine and open it. 
2. On the start screen click "Open Collection".
<br>![](/exercises/ex1/images/bru01_0.png)

3. Find the folder with this tutorial on your local machine and select the subfolder `tools/Bruno Collection/AI161 - Bruno Collection`.
<br>![](/exercises/ex1/images/bru01_1.png)
You should now see the collection in your Bruno API client, expand it by clicking on it.
<br>![](/exercises/ex1/images/bru01_2.png)
Now expand 'Exercise-1 Setup' to see the requests included in this exercise and click on '1-1 Get Auth Token' to open it.
<br>![](/exercises/ex1/images/bru01_3.png)

4. Next we need to setup the environment variables for the collection. Click on the environments selection in the top left corner. 
<br>![](/exercises/ex1/images/bru01_4.png)
Now click on "Configure".
<br>![](/exercises/ex1/images/bru01_5.png)

5. We have preconfigured this environment for you so you will only have to make slight changes:
- Ask your session hosts for the actual `CLIENT_ID` and `CLIENT_SECRET`.
- Set the value for the variable `group_ID` to your groupID as discussed with your session hosts.

All other environment variables will be filled by scripts during this tutorial.
Now save your changes and make sure the "AI-161" environment is selected.

Your Bruno API client is now ready to make request to the provided AI Core instance. Let's setup the authentication token next.

## Exercise 1.1 Get Auth Token

1. Click on "1-1 Get Auth Token" and click on the arrow to the left to execute the request.
<br>![](/exercises/ex1/images/bru01_6.png)
This request will fetch an authentication token from the AI Core instance and store it in the environment variable TOKEN for all following requests. Tokens are valid for one day.

## Exercise 1.2 Find Orchestration Service Deployment

Both the evaluation service and the prompt optimizer we use in this tutorial make llm requests against the orchestration service. AI Core instances create a default orchestration deployment that we need to find in order to finish setting up.

1. Click on "1-2 Find Orchestration Service Deployment" and click on the arrow to the left to execute the request.

This request will check all your deployments and store the url to your orchestration deployment in the environment variable ORCH_URL for following requests.

## Summary

You've now setup your Bruno API client and have done all necessary steps to work through the exercises in this tutorial.
For each exercise in the readme files there is a corresponding bruno request you can execute instead of using the UI as described.

Continue to - [Exercise 2 - Evaluate Basic Prompt](../ex2/README.md)

