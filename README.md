# Solar Irradiance Forecasting Using Deep Learning Techniques

This repository contains a comparative analysis of deep learning techniques for solar irradiance forecasting using a dataset from Karachi, our local city. The goal of this research is to determine the most effective algorithm among four different models for predicting solar irradiance.

The dataset and code files are included in this repository. The code was originally executed on Kaggle but has been uploaded through Google Colab for easier access, viewing, and experimentation by others. To run the code in Google Colab, simply replace all instances of the path '/kaggle/working' with '/content/' in the code file. After making these changes, you can execute the entire code using the 'Run All' option.

The link to the research paper: [Solar Irradiance Forecasting Using Deep Learning Techniques](https://www.mdpi.com/2673-4591/46/1/15)

*This work was done as a Complex Engineering Problem (CEP)-based end-of-semester project for EE-412 Alternate Energy Systems (Spring 2023) as part of BE-Electrical Engineering at NEDUET. The following section summarizes the key findings from this CEP.*

# AES-CEP Summary

## Project Report
Details of the project can be found in the [Project Report](https://github.com/moeed17/Solar-Irradiance-Forecasting-Using-Deep-Learning-Techniques/blob/main/AES%20CEP.pdf).

## Group Members
Hassan Ali Rizvi EE-135: Performed comprehensive literature review.

[Hammad Ali Khan EE-139](https://github.com/hammaad2002): Performed the main experimentation.

Iqra Asif EE-147: Writing and Formatting Report, and PPT Slides.

[Abdul Moeed EE-170](https://github.com/moeed17): Performed comprehensive literature review, Writing and Formatting Report, deducing final results, and PPT Slides.

## Deliverables
### 1) Significance
The increasing awareness of the need to find alternative means of electric power generation without depleting Earth's natural resources has led to the rise of alternative energy. Renewable energy sources, a subset of alternative energy, exhibit a relatively lower carbon footprint. One such renewable energy source is solar power, which harnesses sunlight to generate electricity, serving as a clean and sustainable alternative to finite fossil fuels.

Solar irradiance, the power of sunlight received on a given surface area during a specific time, is crucial in determining the efficiency and performance of 
solar power systems. Accurate forecasting of solar irradiance holds great significance in various applications, it aids in optimizing the use of solar energy and managing its integration into power grids.

In this context, our research/work presents a comparative study of various deep learning models—Recurrent Neural Network (RNN), Gated Recurrent Unit (GRU), Long-short term memory (LSTM), and Temporal Convolution Network (TCN)—for solar irradiance forecasting, aiming to identify the most effective model for this specific purpose. Notably, our work involves conducting a comparative analysis of these models on the **Karachi, Pakistan** (our local city) dataset.

### 2) Deep Learning Models used
1. RNN
A recurrent neural network (RNN) is a powerful neural network architecture that uses its hidden layer to capture and remember information from previous data points, making it effective for tasks involving sequences.

2. LSTM
Long Short-Term Memory (LSTM) networks are a type of Recurrent Neural Network (RNN) architecture consisting of a forget gate, candidate layer (tanh), input gate, output gate, hidden state, and memory state.

3. GRU
The (GRU) is a specialized type of RNN designed for sequential data. It tries to solve the issue of exploding and vanishing gradients by incorporating two gate mechanisms: the first is the update gate and the second is the reset gate. Using these gates, it remembers relevant information needed and discards the rest.

![Image](https://miro.medium.com/v2/resize:fit:1400/format:webp/1*B0q2ZLsUUw31eEImeVf3PQ.png)
*Picture Credits -> Medium*

You can find more details on the discussed models [here](https://towardsdatascience.com/a-brief-introduction-to-recurrent-neural-networks-638f64a61ff4).

4. TCN
A Temporal Convolutional Network (TCN) is an advanced type of neural architecture that has evolved from a 1-D Convolutional Neural Network (CNN).
This method uses stacked convolutions with causal padding, dilation, and residual or skip connections to get a much larger receptive field.
More details on TCN can be found comprehensively [here](https://towardsdatascience.com/temporal-convolutional-networks-the-next-revolution-for-time-series-8990af826567).

### 3) Dataset
The Karachi dataset of 2019, acquired from the NSRDB, provides solar irradiance readings at a time resolution of 15 minutes. The dataset covers a period of one year, consists of 35,040 samples. The  last ten days of data were used exclusively for testing, while the remaining dataset served as the training data. Notably, no portion of the dataset was allocated for validation. The data used to support the findings of this study are available [here](https://nsrdb.nrel.gov/data-viewer).

### 4) Results
After training for 500 epochs, graphs/results conclude that LSTM was the most accurate model among the four. The plots below clearly demonstrate the superiority in terms of forecasting of the LSTM model when comparing it to the other neural network models.
![My Image](https://github.com/moeed17/Solar-Irradiance-Forecasting-Using-Deep-Learning-Techniques/blob/main/Results.png)

The model's accuracy was assessed after training the models on the entire year's data, excluding the last 10 days designated as the test set. The LSTM model achieved the highest R-squared value equal to 0.993406, indicating it outperformed the others. All model’s RMSE values are as follows: 

<p align="center">
𝐿𝑆𝑇𝑀: 0.020051
<p align="center">
𝐺𝑅𝑈: 0.021371
<p align="center">
𝑇𝐶𝑁: 0.021519
<p align="center">
𝑅𝑁𝑁: 0.02217
</p>

All models R-squared values are as follows:
<p align="center">
𝐿𝑆𝑇𝑀: 0.993406 
<p align="center">
𝐺𝑅𝑈: 0.992509
<p align="center">
𝑇𝐶𝑁: 0.992405 
<p align="center">
𝑅𝑁𝑁: 0.991935 

that is the models have an accuracy of 99%.

### 5) Conclusions & Future Work
This study and work present a comparative analysis of various neural network models for very short-term solar irradiance forecasting using the Karachi dataset. The key findings indicate that the LSTM model outperforms the other models, achieving the highest and lowest R-squared and RMSE values, respectively.

Future work could explore feature extraction techniques like time series decomposition to further enhance forecasting model performance. Additionally, the exploration of Liquid Neural Networks, which aim to achieve powerful predictions with fewer neurons and connections inspired by C. Elegans, shows promise. These approaches have the potential to offer more efficient and effective forecasting models. Examining these techniques and alternative architectures can expand and enhance the proposed forecasting models' applicability and generalizability.
