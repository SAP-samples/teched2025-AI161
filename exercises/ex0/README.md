# Getting started

In this exercise, you will chose your mode of interaction with the AI Core services. You can either use our UI the SAP AI Launchpad, the Bruno API client or our Jupyter Notebook and VSCode to work through the following exercises.

Either way you will experience how to evaluate and optimize prompts using the AI Core services for prompt optimization and evaluation based on a demo scenario.

## Familiarize yourself with our Demo Scenario

Our Scenario for this hands-on session is an existing AI use-case that supports a facility management team in analysing messages the team receives from employees about issues in the office. 
For this scenario we have an existing prompt as well as data sets for optimization and evaluation prepared for you.

Let's get familiar with the scenario by checking out the prompt and data sets.

### Basic Prompt

You can find the basic prompt in the `data/prompts` folder stored as `facility_prompt_basic.yaml`. 
It contains a basic system message to the LLM and a user message including a placeholder for the actual facility management message and instructions what to extract from this message and how to classify it.

Open [basic prompt for this scenario](../../data/prompts/facility_prompt_basic.yaml) and read it.

### Data Sets

You can find the data sets in the `data/datasets` folder stored as `facility_eval_data.json` and `facility_optim_data.json`. Each dataset contains a list of messages with the corresponding expected output when this message is used with the prompt. 

Open one of [the data sets for this scenario](../../data/datasets/facility_optim_data.json) and read through a few entries in each of the this files.

## Summary

Now that you have familiarized yourself with the scenario, prompt and data sets, you can chose your preferred mode of interaction to work through the exercises and setup your tooling accordingly.

### Choose how you want to work in this tutorial

1.	AI Launchpad - follow the instructions in the following readme to use the SAP AI Launchpad UI for working through the exercises.
<br>- Continue to - [Exercise 1 - Setup AI Launchpad](../ex1/README-AIL.md)  

2.	Bruno API client - Open the Bruno API client and follow the instructions in the following readme to use the Bruno API client for working through the exercises.
<br>- Continue to - [Exercise 1 - Setup Bruno API Client](../ex1/README-BRUNO.md)

3.  Jupyter Notebook / VSCode - Open VS Code and follow the instructions in the following readme to use Jupyter Notebook or VSCode for working through the exercises.
<br>- Continue to - [Exercise 1 - Setup Jupyter Notebook / VSCode](../ex1/README-IPYNB.md)
