# Exercise 3 - Optimize the prompt

Now that we have seen how our prompt performs we will try to automatically optimize the prompt with the Prompt Optimizer feature. 

## Exercise 3.1 Upload Prompt Optimization Data Set
In the UI uploading the data set can be done as part of the optimization configuration. So we will continue with the next step for now.

## Exercise 3.2 Configure and start the optimization
We will now configure and run an optimization with the AI Core prompt optimizer. 

### 3-2-1 Configure the Optimization

As you have seen an optimization an be started from the `Optimization` view. However, there is another way of starting an optimization directly from the prompt template view.

1. Open the `Prompt Management` view by clicking on it in the side menu.
2. Click on the `Templates` tab to see the list of available prompt templates.
3. Find the prompt template you created in Exercise 2 by filtering for your groupID.
<br>![](/exercises/ex3/images/ail03-1.png)

4. Click on your prompt template to open the detail view.
5. Click on `Optimize Prompt` in the top left to configure and start an Optimization for this template.
<br>![](/exercises/ex3/images/ail03-2.png)
A Wizard to configure the optimization opens.

6. As you can see the prompt template is already selected. Next we select the original model the prompt was created for. Click on the selection icon to open the model selection.
<br>![](/exercises/ex3/images/ail03-3.png)

7. Scroll through the list of available and find GPT-4o Version 2024-08-06 and click on it to select it. The prompt optimizer will use the optimization data and the selected model to calculate a baseline score for the original prompt and the original model.
<br>![](/exercises/ex3/images/ail03-4.png)

8. Next we need to select the model or models for which we want to create optimized prompts. Click on the selection icon to open the model selection.
<br>![](/exercises/ex3/images/ail03-5.png)

9. Browse the available models and select the model you want to use for this exercise. Normally, you can configure up to 4 models to compare them for your use-case. For this hands-on session let's coordinate choosing different models across groups and chose one model each. This allows us to distribute the workload of the hands-on evenly across different models and later compare them as we are all using the same technical user.
Click on the model that was chosen for your group and then click `Select`.
<br>![](/exercises/ex3/images/ail03-6.png)

10. Now, we need to select a dataset artifact to be used during the optimization. Click on the selection icon to open the artifact selection.
<br>![](/exercises/ex3/images/ail03-7.png)

9. Since we have not yet uploaded the data we will create the dataset artifact now. Click on `Add` in the top right to create a new Data Set Artifact.
<br>![](/exercises/ex3/images/ail03-8.png)

10. In the dialog that opens, provide the following information:
- Scenario: `AI-161-{{groupID}}`
- Type: `Dataset`
- Name: `{{groupID}}-optim-data`
- Description: `Artifact for prompt optimization`

11. In the section `Upload File` provide the following information:
- Object Store: `default`
- Sub-folder path: `/T-01`
- Overwrite existing file: Yes

Then open the file selection by clicking on the browse icon.
<br>![](/exercises/ex3/images/ail03-9.png)

Now find the `facility_optim_data.json` file located in the `data/datasets` folder and select it.
After the file has finished uploading click on `Add` to create the artifact.
<br>![](/exercises/ex3/images/ail03-10.png)

12. Now select the newly created artifact from the list by clicking on it and then clicking `Select`.
<br>![](/exercises/ex3/images/ail03-11.png) 

13. Fill in the remaining information for the dataset artifact as follows:
- File Type: `JSON`
- Dataset File: `/facility_optim_data.json`
And click `Next` to proceed to the next step.
<br>![](/exercises/ex3/images/ail03-12.png)

14. In the next step we need to configure the metric that is being used to optimize the prompt. At the moment we can choose between two metrics Semantic Similarity and JSON_Match. Read both descriptions to understand which metric fits best for our use-case. Since our use-case requires the LLM to output structured JSON data we will choose the `JSON_Match` metric. Click on it to select it and then click `Next` to proceed to the next step.
<br>![](/exercises/ex3/images/ail03-13.png)

15. Now we need to configure the names under which the optimized prompt templates will be stored. You can either fill in your own names or use the auto-generated names. For this exercise we will use the auto-generated names. Click on `autogenerate`.
<br>![](/exercises/ex3/images/ail03-14.png)

You can also enable or disable few-shot prompting for the optimized prompts by toggling the respective switch. When this is enabled the optimizer will create few-shot examples as part of the prompt that are based on the optimization dataset. For this exercise, we will few-shot prompts disabled.
Now click `Review` to review your configuration.
<br>![](/exercises/ex3/images/ail03-15.png)

### 3-2-2 Start the Optimization

1. Now Review your configuration and click on `Create` to start the optimization.
<br>![](/exercises/ex3/images/ail03-16.png)

You should now see a confirmation that the optimization has been created successfully.

## Exercise 3.3 Check the optimization results

After starting the optimization it will take some time until the optimization is finished. You can monitor the progress of the optimization in the view that opened after clicking on `Create`.

1. Click the refresh icon in the top right to refresh the view.
<br>![](/exercises/ex3/images/ail03-17.png)

2. Check if the status of the optimization has change to running - indicating that the optimization process has started.
<br>![](/exercises/ex3/images/ail03-18.png)

3. Periodically refresh until the optimization status has changed to `Completed`. 
<br>![](/exercises/ex3/images/ail03-19.png)

4. You can now find the finished optimization and your results in the `Optimization` view. Open the `Optimization` view from the side menu. Find your optimization and click on it o view the results.
<br>![](/exercises/ex3/images/ail03-20.png)

5. In the optimization detail view you can now see the results of the optimization. Check the baseline score of the original prompt and the scores of the optimized prompts. 
<br>![](/exercises/ex3/images/ail03-21.png)

6. Click on the optimized prompt to review the optimized prompt template.
<br>![](/exercises/ex3/images/ail03-22.png)

7. Review the optimized prompt template.
<br>![](/exercises/ex3/images/ail03-23.png)

## Summary

You have now optimized the base prompt for one model. Now let's evaluate the optimized prompt to see if it has improved on our evaluation metrics.

Continue to - [Exercise 4 - Evaluate the optimized Prompt ](../ex4/README-AIL.md)
