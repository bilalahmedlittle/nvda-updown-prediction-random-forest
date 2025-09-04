# nvda-updown-prediction-random-forest
Predicting NVDA stock price direction (up/down) using a Random Forest model trained on historical data.

This is a short project with the main purpose of experimenting with different steps in machine learning model building and gaining an understanding of NVDA data before my main project *( predicting NVDA daily returns using LGBM to develop a market strategy)*.

It follows these clear steps:

- Import data
- Add features to data (Cell 2-5)
- Feature engineering via: 
  1) Correlation Analysis, Permutation Importance, SHAP Analysis (Cell 6-10)
  2) Forward Selection (Cell 11-12)
- Hyperparameter tuning (Cell 13)

---

### Results 
(Cell 14)

Our final model produced these results:
  Mean train accuracy: 0.6443
  Mean validation accuracy: 0.5410
  Std validation accuracy: 0.0202

And as stated in the summary in our notebook:
    
  Our model achieved a 53.10% up/down accuracy, which is sufficiently above randomness to suggest it is not merely producing noise and could form the basis of a profitable trading strategy with the right infrastructure. There is also roughly a 10% gap between training and validation accuracy, which is acceptable and significantly lower than our original figures.

### Improvements for the next NVDA project *( details above)*:
- Add more features, particularly market features and regime indicators
- Create a reusable model training function to improve code quality
- Add visuals for model performance evaluation
- Possibly avoid permutation importance / SHAP analysis due to incompatibility; instead, move straight to forward/backward selection after initial feature trimming
