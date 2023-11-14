# Spam Classification Using Ensemble Learning

## Project Description

This project is an exploration of ensemble learning methods for classifying email messages as spam or ham (non-spam). Various ensemble classifiers, including Random Forest, AdaBoost with logistic regression, and AdaBoost with a Decision Tree base learner, are trained and evaluated on their accuracy and per-class classification performance.


## Dataset

The spam dataset is loaded from a CSV file. It's split into training and testing sets, with the training set used to fit the models and the testing set used to evaluate performance.

## Models and Training

The following classifiers are implemented and trained:

- **Random Forest Classifier**: Evaluated with different numbers of base learners (`n_estimators`) and max features parameters.
- **AdaBoost with Logistic Regression**: Tested with varying numbers of base learners.
- **AdaBoost with Decision Tree**: Also examined with a different count of base learners.

## Results

The models' performance was assessed based on accuracy and per-class accuracy for 'ham' and 'spam' classes. The highest performing configurations were identified as:

- **Random Forest**: Achieved the best overall accuracy and per-class accuracy for 'ham'.
- **AdaBoost with Logistic Regression**: Showed consistent accuracy across different numbers of base learners.
- **AdaBoost with Decision Tree**: Reached comparable accuracy to the Decision Tree classifier with the highest number of base learners.

## Observations

- The accuracy generally increased with more base learners.
- The Random Forest classifier with `n_estimators=1000` and `max_features='auto'` achieved the highest accuracy.
- The AdaBoost Ensemble with Decision Trees as base learners produced similar results to the Decision Tree Classifier, suggesting limited benefit from the ensemble approach in this case.

## Fusion Classifier Comparison

- A fused classifier outperformed the AdaBoost Ensemble with Decision Tree as the base learner, suggesting the effectiveness of classifier ensembles.

## Impact of Training Sample Size

- The accuracy of both the fused classifier and the AdaBoost Ensemble varied with the training-test split, with the fused classifier generally performing better except for certain split ratios.

## Conclusion

The Random Forest classifier yielded the best results among the tested classifiers, with the AdaBoost Ensemble with Logistic Regression providing the best balance between complexity and performance.
