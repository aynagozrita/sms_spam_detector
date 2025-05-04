# sms_spam_detector

## Overview
This challenge involves building an SMS text classification system to identify whether a given text message is "ham" (legitimate) or "spam." We will utilize the provided starter files to create a classification function and a Gradio web application for user interaction.


## Starter Files
The challenge begins with the following files:
  • gradio_sms_text_classification.ipynb: Your main notebook for building the Gradio application and the SMS classification function.
  • sms_text_classification_solution.ipynb: A reference notebook containing a solution for the SMS classification model.
  • SMSSpamCollection.csv: A CSV file containing labeled SMS messages for training the model.
  
## Challenge Instructions
Step 1: Create the SMS Classification Function
1. Open sms_text_classification_solution.ipynb and refer to the code to build the sms_classification function in gradio_sms_text_classification.ipynb.
2. Follow these sub-steps to implement the function:
  • Set the features variable to the text message column of the DataFrame.
  • Set the target variable to the "label" column of the DataFrame.
  • Split the data into training and testing sets, allocating 33% of the data for testing (test_size=0.33).
  • Build a pipeline to preprocess the text data and transform the test set for comparison.
  • Fit the model using the transformed training data and return the trained model.
3. Load the SMSSpamCollection.csv file into a pandas DataFrame and call the sms_classification function, storing the result in the variable text_clf.
   
Step 2: Create the SMS Prediction Function
1. Implement the sms_prediction function to predict the class of a new text message. 
2. Follow these sub-steps:
  • Create a variable to hold the prediction result.
  • Use a conditional statement to determine if the text message is classified as "ham" or "spam":
  • If the message is classified as "ham", return:  
f'The text message: "{text}", is not spam.'
  • If the message is classified as "spam", return:  
f'The text message: "{text}", is spam.'

Step 3: Create the Gradio Interface Application
1. Build a Gradio interface that includes:
  • A textbox for the user input (new text) with an appropriate label.
  • A textbox for the output displaying the classification result, also with an appropriate label.
2. Launch the Gradio application and obtain the sharing URL for your application.
3. To test your completed application, you can use the following sample text messages:
  • "You are a lucky winner of $5000!"
  • "You won 2 free tickets to the Super Bowl."
  • "You won 2 free tickets to the Super Bowl. Text us to claim your prize."
  • "Thanks for registering. Text 4343 to receive free updates on Medicare."


## Conclusion
After completing the above steps, you will have developed an SMS classification model that can be accessed through a user-friendly Gradio interface. Feel free to experiment with additional text messages to further test the robustness of your application.
