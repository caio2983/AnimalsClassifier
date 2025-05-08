<h1 align="center">Animals Classifier</h1>

<p>Machine Learning Project where I developed an image classifier to distinguish between dogs, ducks, and foxes using Logistic Regression. The images were obtained through public APIs specific to each category. I performed data cleaning and organization using the Pandas library, and used Scikit-learn for model building and evaluation. Matplotlib was also used to generate visualizations that supported the analysis of results.</p>

<h2>📁 Dataset Generation</h2>

<p>The script automatically creates an images/ folder with three subdirectories:</p>
<code>images/
├── dogs/
├── foxes/
└── ducks/
</code>

##
It then downloads 1000 images from the following public APIs:

- 🐶 Dogs: [https://random.dog/woof.json](https://random.dog/woof.json)  
- 🦊 Foxes: [https://randomfox.ca/floof/](https://randomfox.ca/floof/)  
- 🦆 Ducks: [https://random-d.uk/api](https://random-d.uk/api)

Each image is resized to 64x64 pixels and represented as a 3-dimensional array with the shape (64, 64, 3), where the third dimension corresponds to the RGB color channels.
All images are stored in the feature array X, with their corresponding labels placed in y. The dataset is then split into 80% for training and 20% for testing.


Logistic Regression is applied to the data:

![image](https://github.com/user-attachments/assets/12673ded-9280-4683-89db-844208bb5740)

## Performance Measures
<h3>Accuracy</h3>
<code>from sklearn.metrics import accuracy_score
accuracy = accuracy_score(y_test, y_pred</code>

Accuracy on the test set: 0.91

This means that 91% of the predictions made by the model on the test set were correct. In other words, the model correctly classified 91% of the images from the test set.

## 
<h3>Classification Report</h3>

![image](https://github.com/user-attachments/assets/b872d495-cc68-41e3-afe2-615233b114ce)

<h4>Precision</h4>
![image](https://github.com/user-attachments/assets/683c6489-eaa3-459d-ab4e-6a26748b9bed)
Precision measures the proportion of correctly predicted positive instances for each class, relative to all instances the model predicted as positive. For example, a precision of 93% for the 'dog' class means that, in 93% of the cases where the model predicted 'dog', the prediction was correct.

<h4>Recall</h4>
<img src="https://github.com/user-attachments/assets/ee5dcbe9-5ea1-46d1-9249-8c832307ad75"/>
Recall measures the proportion of correctly predicted positive instances for each class, relative to all instances that actually belong to that class.

<h4>F1-Score</h4>
<img src="https://github.com/user-attachments/assets/54b73361-c44c-4f28-a4b0-3b28c1e93f59"/>

<p>The F1-score is the harmonic mean of precision and recall, providing a single metric that balances both. Unlike the arithmetic mean, the harmonic mean emphasizes lower values, meaning the F1-score will only be high if both precision and recall are high. It ranges from 0 to 1, where values closer to 1 indicate that the model has achieved a good balance between correctly identifying positive instances (recall) and minimizing false positives (precision).</p>

<h4>Confusion Matrix</h4>
<img src="https://github.com/user-attachments/assets/7560507f-6c9a-41f5-b408-4a6bddea332f"/>
<p>The confusion matrix is a table that shows how well a classification model performs. It compares the model’s predicted labels with the true labels, displaying:

True Positives (TP): correctly predicted positives

True Negatives (TN): correctly predicted negatives

False Positives (FP): incorrect positive predictions

False Negatives (FN): incorrect negative predictions






