<h1>Project description</h1>
The data is stored in three files:<br><br>
<ul><li>gold_recovery_train.csv — training dataset</li><br>
<li>gold_recovery_test.csv — test dataset</li><br>
<li>gold_recovery_full.csv — source dataset</ul></li><br>

Data is indexed with the date and time of acquisition (date feature). Parameters that are next to each other in terms of time are often similar.
  
Some parameters are not available because they were measured and/or calculated much later. That's why, some of the features that are present in the training set may be absent from the test set. The test set also doesn't contain targets.
  
The source dataset contains the training and test sets with all the features.
  
You have the raw data that was only downloaded from the warehouse. Before building the model, check the correctness of the data. For that, use our instructions.
  
<h2>Project instructions</h2>
1. Prepare the data<br><br>
1.1. Open the files and look into the data<br><br>
1.2. Check that recovery is calculated correctly. Using the training set, calculate recovery for the rougher.output.recovery feature. Find the MAE between your calculations and the feature values. Provide findings<br><br>
1.3. Analyze the features not available in the test set. What are these parameters? What is their type?<br><br>
1.4. Perform data preprocessing<br><br>
2. Analyze the data<br><br>
2.1. Take note of how the concentrations of metals (Au, Ag, Pb) change depending on the purification stage<br><br>
2.2. Compare the feed particle size distributions in the training set and in the test set. If the distributions vary significantly, the model evaluation will be incorrect<br><br>
2.3. Consider the total concentrations of all substances at different stages: raw feed, rougher concentrate, and final concentrate. Do you notice any abnormal values in the total distribution? If you do, is it worth removing such values from both samples? Describe the findings and eliminate anomalies<br><br>
3. Build the model<br><br>
3.1. Write a function to calculate the final sMAPE value<br><br>
3.2. Train different models. Evaluate them using cross-validation. Pick the best model and test it using the test sample. Provide findings<br><br>

Use these formulas for evaluation metrics:
<img src="https://github.com/UltraXman2022/DS-Integrated-Project-2/blob/main/smape_1576239058_1589899769.jpg"></img>
<img src="https://github.com/UltraXman2022/DS-Integrated-Project-2/blob/main/_smape_1_1589900649.jpg"></img>

