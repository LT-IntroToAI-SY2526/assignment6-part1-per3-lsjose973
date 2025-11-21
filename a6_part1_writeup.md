# Assignment 6 Part 1 - Writeup

**Name:** _______________  
**Date:** _______________

---

## Part 1: Understanding Your Model

### Question 1: R² Score Interpretation
What does the R² score tell you about your model? What does it mean if R² is close to 1? What if it's close to 0?

**YOUR ANSWER:**
The R² score tells us how well the data is explained by the model we created. In the context of this assignment, the R² value would represent how well the test score that a student received correlates with the amount of hours they studied. If the R² value is close to 1, it means that the model explains the data very well (meaning that the two variables have a strong correlation), and if the R² value is close to 0, it means that the the data isn't explained well by the model. This means that the two variables are likely unrelated, meaning that there's no correlation. 

---

### Question 2: Mean Squared Error (MSE)
What does the MSE (Mean Squared Error) mean in plain English? Why do you think we square the errors instead of just taking the average of the errors?

**YOUR ANSWER:**
The Mean Squared Error gives us an average of how inaccurate our model is when predicting values. A lower MSE is better than a high MSE because it means that on average, our model predicts values closer to the actual value. There are two main reasons as to why we square the errors instead of just taking the average. One reason is to make sure all of the errors are positive; if the errors were both negative and positive, they would cancel out and lead to a very low MSE even it's supposed to be high. The other reason that we square the errors is to punish bigger mistakes instead of every mistake. For example if your error is small, like 1, the square of 1 is only 1. But if your error is bigger like 10, the square of that becomes 100.

---

### Question 3: Model Reliability
Would you trust this model to predict a score for a student who studied 10 hours? Why or why not? Consider:
- What's the maximum hours in your dataset?
- What happens when you make predictions outside the range of your training data?

**YOUR ANSWER:**
I don't think I would trust this model to predict a score for a student who studied 10 hours. This is because the maximum hours in my dataset is 9.6 hours, and although it's close to 10, 10 is still outside of the data range. If I were to try and predict a score for a data outside of the range that it was trained on, the data would be an extrapolation of the model. 
---

## Part 2: Data Analysis

### Question 4: Relationship Description
Looking at your scatter plot, describe the relationship between hours studied and test scores. Is it:
- Strong or weak?
- Linear or non-linear?
- Positive or negative?

**YOUR ANSWER:**
The relationship is fairly strong. Although there is some variation, most of the data points cluster around the line of best fit. Additionally, the trend seems to form a linear line with a positive slope, indicating that the two variables have a positive correlation. This means that as the hours spent studying increases, the test score that a student receives increases as well.



---

### Question 5: Real-World Limitations
What are some real-world factors that could affect test scores that this model doesn't account for? List at least 3 factors.

**YOUR ANSWER:**
1. Sleep -- even if a person studied a lot, for example pulling an all nighte before the exam, they could be tired while taking the exam leading to a worsened performance.
2. Test Anxiety -- some people are more anxious than others when it comes to taking tests, so even if some people studied more, people with lower hours spent studying could score higher because they are less anxious when they take tests.
3. Studying efficiency -- there are various methods of studying, with some being objectively better than others. in the data set, there are bound to be some people who are able to study for less hours than others, but score higher because they are more efficient when they are studing. 


---

## Part 3: Code Reflection

### Question 6: Train/Test Split
Why do we split our data into training and testing sets? What would happen if we trained and tested on the same data?

**YOUR ANSWER:**
We split our data into training and testing sets because we want to see if the model we create is actually generalizable and useable. The training set is used to teach the model how to predict data, and the testing set is used to see if the model we create is actually accurate. If we trained and tested on the same data, the model would perform better than it actually should, giving a false sense of accuracy. Instead of learning how to actually see the pattern in the data trends, it instead memorizes the different points. If we tried to predict a score for an hour that wasn't on the data we tested and trained on, it would product a result that is more inaccurate than it actually should be.
---

### Question 7: Most Challenging Part
What was the most challenging part of this assignment for you? How did you overcome it (or what help do you still need)?

**YOUR ANSWER:**
I think the most challenging part of this assignment was understanding why we put the independant variable as a list. I began to understand it after we went over it in class, as I now know that there could be graphs where there are multiple independant variables. For example, in the context of this assignment we could have put Hours Studied, Hours Slept, etc, because these are all factors that influence the test scores. 



---
## Part 4: Extending Your Learning

### Question 8: Future Applications
Describe one real-world problem you could solve with linear regression. What would be your:
- **Feature (X):** 
- **Target (Y):** 
- **Why this relationship might be linear:**

**YOUR ANSWER:**
One real-world problem that I could solve with linear regression would likely be the amount of calories burned in a day based on how much exercise you do. My independant X values could be time spent running, time spent walking, time spent doing yoga, etc. My dependant Y value would be the amount of calories burned. I think that this relationship would be linear because the amount of calories you burn tends to increase proportionally with how much cardio you do. The amount of calories you burn on average in the first 10 minutes of exercising is the same amount of calories you burn on average in a 10 minute interval later in the same  session (ex: 30-40 mins).



---

## Grading Checklist (for your reference)

Before submitting, make sure you have:
- [X] Completed all functions in `a6_part1.py`
- [X] Generated and saved `scatter_plot.png`
- [X] Generated and saved `predictions_plot.png`
- [X] Answered all questions in this writeup with thoughtful responses
- [X] Pushed all files to GitHub (code, plots, and this writeup)

---

## Optional: Extra Credit (+2 points)

If you want to challenge yourself, modify your code to:
1. Try different train/test split ratios (60/40, 70/30, 90/10)
2. Record the R² score for each split
3. Explain below which split ratio worked best and why you think that is

**YOUR ANSWER:**
