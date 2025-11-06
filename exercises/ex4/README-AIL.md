# Exercise 4 - Evaluate the optimized prompt

In this exercise, we will evaluate our basic prompt using the evaluation data set provided and the AI Core evaluation service.

## Exercise 4.1 Configure and run the evaluation


### 4-1-1 Configure your Evaluation
1. Open the `Optimization` view by clicking on it in the side menu.
You should see a list of optimization and evaluation runs.

2. Click on `Create` in the top left.
<br>![](/exercises/ex4/images/ail04-1.png)

A Dialog to chose between `Optimization` and `Evaluation` opens.

3. Select `Evaluation`.
<br>![](/exercises/ex4/images/ail04-2.png)

4. First we need to select the prompt template we want to evaluate. Click on the selection icon to open the template selection.

5. Now choose your optimized prompt template from the list by clicking on it and then clicking `Select`. 
You can use the filters to find your prompt template more easily.
<br>![](/exercises/ex4/images/ail04-3.png)

6. Next we need to select the model which we want to evaluate. Click on the selection icon to open the model selection.

7. Browse the available models and select the model you used throughout this exercise. 
Click on the model that was chosen for your group and then click `Select`.

8. Finally, we need to select a dataset artifact to be used during the evaluation. We can use the artifact already created in exercise 2. Click on the selection icon to open the artifact selection.

9. Now select the evaluation artifact created in exercise 2 from the list by clicking on it and then clicking `Select`.

13. Fill in the remaining information for the dataset artifact as follows:
- File Type: `JSON`
- Dataset File: `facility_eval_data.json`

14. Now that we have filled out all required Test input information we can move on to selecting evaluation metrics. Click `Next` to proceed to the metrics selection.
<br>![](/exercises/ex4/images/ail04-4.png)

15. TO be able to compare our results we will choose the same metrics as before. 
In the metrics selection view, choose the following metrics by clicking on them:
- Pointwise Correctness
- Pointwise Answer Relevance
- Pointwise Instruction Following
Then click `Next` to proceed to the next step.
<br>![](/exercises/ex2/images/ail02-23.png)

16. In the next step we can configure additional evaluation parameters. We can choose the number of repetitions for the evaluation. We can define a mapping between prompt and dataset variables in case these are mismatched. And we can define Tags to be associated with the evaluation run.
For this exercise, we will leave everything at the default values. Click `Review` to proceed to the next step.
<br>![](/exercises/ex2/images/ail02-24.png)

### 4-1-2 Start the Evaluation

1. Now Review your configuration and click on `Create` to start the evaluation.
<br>![](/exercises/ex4/images/ail04-5.png)

You should now see a confirmation that the evaluation has been created successfully.

## Exercise 4.2 Check the evaluation results

After starting the evaluation it will take some time until the evaluation is finished. You can monitor the progress of the evaluation in the view that opened after clicking on `Create`.

### 4-2-1 Monitor the status of your evaluation
1. Click the refresh icon in the top right to refresh the view.
<br>![](/exercises/ex4/images/ail04-6.png)

2. Check if the status of the evaluation has changed to running - indicating that the evaluation process has started.
<br>![](/exercises/ex4/images/ail04-7.png)

3. Periodically click the refresh icon to update the status of the evaluation run. Once the status has changed to `Completed` the evaluation is finished.
<br>![](/exercises/ex4/images/ail04-8.png)

### 4-2-2 Review the evaluation results

1. You can now find the finished evaluation and your results in the `Optimization` view. Open the `Optimization` view from the side menu. Find your evaluation and click on it to view the results.
<br>![](/exercises/ex4/images/ail04-9.png)

2. In the evaluation detail view you can now see the results of the evaluation. Check the scores for the different metrics we have selected.
<br>![](/exercises/ex4/images/ail04-10.png)

### 4-2-3 Compare with previous evaluation

1. Go back to the `Optimization` view by clicking on it in the side menu to see the list of optimization and evaluation runs.
2. Find the previous evaluation of the base prompt and the evaluation of the optimized prompt and click on the checkbox next to both evaluations to select them.
3. Click on `Compare` in the top right to open the comparison view.
<br>![](/exercises/ex4/images/ail04-11.png)

4. In the comparison view you can now see the results of both evaluations side by side. Compare the scores of the different metrics to see if the optimization of the prompt has improved the results.
<br>![](/exercises/ex4/images/ail04-12.png)

## Summary

You have now evaluated the optimized prompt using the provided evaluation data set and the AI Core evaluation service. You have also compared the results of your two evaluation runs to determine if the prompt has improved on additional evaluation metrics besides the one chosen for optimization. 

You have now completed all exercises in this lab. Great job!
If you want to learn more about prompt engineering and optimization, consider exploring additional resources or experimenting with different prompts and models on your own. Happy prompting!