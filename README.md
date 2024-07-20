# Smart_Lavatory_Management_System
# Smart Lavatory System Cleanliness Prediction

This project involves predicting the cleanliness of a lavatory system using various environmental and usage data. The model used is a Long Short-Term Memory (LSTM) neural network.

## Dataset

The dataset used in this project is `Smart Lavatory System.csv`, which contains the following features:

- `Gas Sensor(MQ137)-ppm`
- `Gas Sensor(MQ4)-ppm`
- `Gas Sensor(MQ8)-ppm`
- `VOC`
- `Temperature(DHT22)(in deg. celsius)`
- `Humidity(RH)%`
- `No. of Users(IR)`

## Data Preprocessing

1. **Label Encoding**: The `VOC` feature is encoded using a Label Encoder.
2. **Feature Selection**: The following features are selected for training the model:
   - `Gas Sensor(MQ137)-ppm`
   - `Gas Sensor(MQ4)-ppm`
   - `Gas Sensor(MQ8)-ppm`
   - `VOC`
   - `Temperature(DHT22)(in deg. celsius)`
   - `Humidity(RH)%`
3. **Target Variable**: The target variable `Cleanliness` is created based on certain conditions on the features.

## Model Training

1. **Data Scaling**: The features are scaled using `StandardScaler`.
2. **Data Reshaping**: The data is reshaped to fit the LSTM model input requirements.
3. **LSTM Model**: A Sequential LSTM model is defined with one LSTM layer and one Dense layer with a sigmoid activation function.
4. **Compilation**: The model is compiled using the Adam optimizer and binary cross-entropy loss function.
5. **Training**: The model is trained for 300 epochs with a batch size of 20 and a validation split of 0.2.

## Model Evaluation

1. **Accuracy**: The accuracy of the model on both the training and test datasets is calculated.
2. **Predictions**: The model predictions on the test dataset are compared with the actual values.
3. **Root Mean Squared Error (RMSE)**: The RMSE of the predictions is calculated.
4. **Confusion Matrix**: A confusion matrix is plotted to visualize the performance of the model.
5. **Classification Report**: A classification report is printed to show precision, recall, and F1-score.

## Visualization

1. **Accuracy Plot**: A plot of the training and validation accuracy over epochs.
2. **Actual vs Predicted Values**: A scatter plot comparing the actual and predicted cleanliness values.
3. **Confusion Matrix**: A heatmap of the confusion matrix.

## How to Run

1. Ensure you have the necessary libraries installed:
    ```bash
    pip install pandas numpy sklearn tensorflow matplotlib seaborn
    ```

2. Place the `Smart Lavatory System.csv` file in the same directory as the script.

3. Run the script:
    ```bash
    python script_name.py
    ```

## Example Output

- **Train Accuracy**: 
- **Test Accuracy**: 
- **RMSE**: 
- **Confusion Matrix**: 

## Visualizations

1. **Accuracy Plot**:
    ![Accuracy Plot](accuracy_plot.png)

2. **Actual vs Predicted Cleanliness**:
    ![Actual vs Predicted](actual_vs_predicted.png)

3. **Confusion Matrix**:
    ![Confusion Matrix](confusion_matrix.png)

## Author

[Your Name]

## License

This project is licensed under the MIT License.
