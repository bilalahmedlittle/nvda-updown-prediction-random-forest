# nvda-updown-prediction-random-forest
Predicting NVDA stock price direction (up/down) using a Random Forest model trained on historical data.

This is a short project with the main purpose of experimenting with different steps in machine learning model building and gaining an understanding of NVDA data before my main project *( predicting NVDA daily returns using LGBM to develop a market strategy)*.

It follows these clear steps:

- Import data
- Add features to data [Link Text](NVDA_rf.ipynb#adding-basic-features-to-the-dataset-to-use-in-our-ML-models)
- Feature engineering via:
  1) Correlation Analysis, Permutation Importance, SHAP Analysis [Link Text](NVDA_rf.ipynb#feature-importance-analysis)
  2) Forward Selection [Link Text](NVDA_rf.ipynb#Forward-Selection)
- Hyperparameter tuning [Link Text](NVDA_rf.ipynb#hyperparameter-tuning)

---

### Results 
[Link Text](NVDA_rf.ipynb#results)

Our final model produced these results:
  'Mean train accuracy: 0.6901
   Mean validation accuracy: 0.5300
   Std validation accuracy: 0.0308'

And as stated in the summary in our notebook:
    
  Our model achieved a 53.00% up/down accuracy, which is sufficiently above randomness to suggest it is not merely producing noise and could form the basis of a profitable trading strategy with the right infrastructure. There is also roughly a 16% gap between training and validation accuracy, which is acceptable and significantly lower than our original figures.

### Improvements for the next NVDA project *( details above)*:
- Add more features, particularly market features and regime indicators
- Create a reusable model training function to improve code quality
- Add visuals for model performance evaluation
- Possibly avoid permutation importance / SHAP analysis due to incompatibility; instead, move straight to forward/backward selection after initial feature trimming
