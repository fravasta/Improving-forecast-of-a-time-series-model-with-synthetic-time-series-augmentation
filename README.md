# Improving-forecast-of-a-time-series-model-with-synthetic-time-series-augmentation
using LSTM model to make predictions and trying to overcome the lack of extrapolation through GAN generated stock prices


Tools used: LSTM Neural Networks, XGBOOST and TimeGAN (specifically introduced for Time Series)

## Proposed Methodology
The methodology is divided into three main parts:

**Part 1: Training a forecasting model on Real Data**
- Training Phase: Train a forecasting model using only the original (real) training dataset.
- Prediction and Evaluation: Apply the trained forecasting model to unseen test data to make predictions. Evaluate the model's performance using metrics such as Mean Absolute Error (MAE).

**Part 2: Augmenting the Dataset with Synthetic Data and Training a New LSTM Model**
- Synthetic Data Generation: Build and train a TimeGAN (Time-series Generative Adversarial Network) to generate synthetic time-series data. Combine the synthetic data with the original training dataset to create an augmented training dataset.
- Training Phase: Train a new forecasting model on the augmented training dataset.
- Prediction and Evaluation: Apply the new forecasting modelto the same unseen test data to make predictions. Evaluate its performance using the same metrics (MAE).

**Part 3: Comparison and Analysis**
- Compare the performance of the two forecasting models: The first model, trained only on real data. The second model, trained on the augmented dataset (real + synthetic data) Measure whether the inclusion of synthetic data leads to an improvement in performance.


**Expected Outcomes**
The comparison will reveal whether the augmented dataset (real + synthetic data) leads to better performance compared to using only real data.
If the synthetic data is of high quality and captures the underlying patterns of the real data, the second model is expected to achieve lower MAE on the test set.