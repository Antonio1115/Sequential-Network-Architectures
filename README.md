# Sequential Network Architectures for Sentiment Analysis

This project explores and compares multiple sequential neural network architectures (CNN, LSTM, and Transformer) for text sentiment classification on the IMDB movie review dataset. Originally developed as part of a university machine learning course, the project emphasizes rigorous evaluation, architectural comparison, and statistical analysis.

## Contents

- `Lab_7.ipynb`: End-to-end implementation, training, evaluation, and analysis of sequential neural network models.
- `Lab_7.html`: HTML export of the notebook for easy viewing without Jupyter.

## Objective

The objective of this lab is to explore and implement sequential neural network architectures, such as those used for time series, sequence prediction, or natural language processing tasks. The notebook guides you through data preparation, model building, training, evaluation, and analysis.


## What Was Done & Results

### Project Overview

This project performs sentiment analysis on the IMDB movie review dataset using several sequential neural network architectures: CNN, LSTM, and Transformer models. The goal is to classify reviews as positive or negative and compare the effectiveness of different deep learning models.

### Steps and Methods

- **Data Preparation:** Loaded the IMDB dataset, checked for missing values and duplicates, and described the dataset features (`review` and `sentiment`).
- **Evaluation Metric:** Used the F1 Score as the main metric, since both false positives and false negatives are equally important.
- **Data Splitting:** Used Stratified 10-Fold Cross-Validation to ensure balanced representation of positive and negative reviews in each fold.
- **Text Preprocessing:** Tokenized and padded review texts for input into neural networks.
- **Model Architectures:**
	- *CNN Model*: Used convolutional and pooling layers to extract local features from text.
	- *LSTM Model*: Used LSTM layers to capture sequential dependencies in the text.
	- *Transformer Model*: Used multi-head self-attention to model complex relationships in the sequence.
	- *Dual-Attention Transformer*: Experimented with stacked attention layers.
- **Training and Evaluation:** Trained each model on the training folds and evaluated on the test fold. Collected F1 scores and training times. Plotted training/validation accuracy and loss for each model.
- **Statistical Analysis:** Used statistical tests (Friedman, Wilcoxon, paired t-test) to determine if differences in model performance were significant. Created a Critical Difference Diagram to visualize significant differences.
- **Additional Analysis:** Analyzed how review length affected prediction accuracy, finding that shorter reviews were generally classified more accurately.

### Results

- **Performance:** All models achieved similar F1 scores (around 0.82–0.83). The CNN model was the fastest to train, while the Transformer with 4 heads was the slowest.
- **Best Model:** The LSTM model slightly outperformed others in average F1 score, but differences were small.
- **Statistical Significance:** Some improvements (e.g., dual-attention Transformer) were statistically significant, as shown by the paired t-test.
- **Review Length:** Shorter reviews had higher prediction accuracy, while longer reviews were more challenging for the models.

### Conclusion

This project compared several sequential neural network architectures for sentiment analysis, using robust evaluation and statistical methods. The results show that while all models perform well, LSTM and CNN are strong choices for this task, and model selection can be guided by training time and specific use-case needs. The analysis also highlighted areas for improvement, such as handling longer reviews.

## Usage

1. **Open the Notebook**: Launch `Lab_7.ipynb` in Jupyter Notebook or JupyterLab.
2. **Run the Cells**: Execute each cell in order to reproduce the results and visualizations.
3. **View Results**: Alternatively, open `Lab_7.html` in your web browser to view the completed notebook.

## Requirements

- Python 3.x
- Jupyter Notebook or JupyterLab
- Common machine learning libraries (e.g., TensorFlow or PyTorch, NumPy, pandas, matplotlib, etc.)

Install requirements with:

```bash
pip install -r requirements.txt
```

*(If a `requirements.txt` is not provided, install the necessary packages as you encounter ImportErrors.)*

## Author

- Antonio F.

## License

This project was developed for educational purposes as part of academic coursework.
