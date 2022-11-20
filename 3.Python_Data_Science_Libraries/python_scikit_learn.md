# scikit-learn

- Has many submodules, each with its own specific functionality.
- May only need to import a specific submodule for a particular task (eg. sklearn.model_selection)

## Installation

```console
$ pip install sklearn
```

## train_test_spilt()

- Split the data with proportion.

```Python

from sklearn.model_selection import train_test_split

datatrain = df["column1"].values
datatest = df["conlumn2"].values

train_x, test_x, train_y, test_y = train_test_split(datatrain, datatest, test_size=0.2, random_state=500)
```

- test size is used to controle the proportion of the test dataset from the main dataset.
- 0.2 means 20 percent.
- Therefore, this split will split 20 percent of the main dataset into test dataset.

- random_state is used to randomly split up the data.

## Transforming Text into Numerical Feature Vectors

- text needs to be turn into vectors in order to be used to train model.


```Python

from sklearn.feature_extraction.text import CountVectorizer

text = ["today is a windy day", "omg the weather is so nice", "wow I love winter"]

traindata = ["windy is a weather", "winter is so nice", "I love today"]
testdata = ["omg winter is so windy", "the weather today is so nice", "wow winter"]


vectorizer = CountVectorizer()
vectorizer.fit(text)

X_train = vectorizer.transform(traindata)
X_test = vectorizer.transform(testdata)

print("X_train:")
print(X_train)
print("\nX_test:")
print(X_test)

print("\nvectorizer_dict: ")
print(vectorizer.vocabulary_)
```

```
Output:

X_train:
  (0, 0)	1
  (0, 7)	1
  (0, 8)	1
  (1, 0)	1
  (1, 2)	1
  (1, 4)	1
  (1, 9)	1
  (2, 1)	1
  (2, 6)	1

X_test:
  (0, 0)	1
  (0, 3)	1
  (0, 4)	1
  (0, 8)	1
  (0, 9)	1
  (1, 0)	1
  (1, 2)	1
  (1, 4)	1
  (1, 5)	1
  (1, 6)	1
  (1, 7)	1
  (2, 9)	1
  (2, 10)	1

vectorizer_dict: 
{'today': 6, 'is': 0, 'windy': 8, 'omg': 3, 'the': 5, 'weather': 7, 'so': 4, 'nice': 2, 'wow': 10, 'love': 1, 'winter': 9}
```

## Training and Evaluating the Model

- There are many classifiers in the library.

For instance: LogisticRegression()

```Python
from sklearn.linear_model import LogisticRegression

classifier = LogisticRegression()

# Train the classifier and train data
clssifier.fit(X_train, y_train)

# Test the classifier accuracy
acc = classifier.score(X_test, y_test)
print("Accuracy:", acc)
# Instance output:
#   Accuracy: 0.81
#   This means that the model achieved a 81% accuracy.

# Use the classifier to predict new data
text = ["today is windy", "omg the weather is so nice", "wow I love winter"]
new_text = ["windy, winter, omg", "wow today is a nice day", "I love windy winter"]
X_new = vectorizer.transform(new_text)
print(classifier.predict(X_new))
# Gives prediction depends what you trained
# If you trained a good or bad classifier, it might return [0, 1, 1] (0 is bad, 1 is a good)
# If you trained a coldness classifier, it might return [0.82, 0.15, 0.73] (82% percent it is cold, 15% it is not that cold, 73% it is cold; higher percentage means colder)
```
