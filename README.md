# Real Time Stock Market Forecasting

This repository contains an implementation of ensemble deep learning models to forecast or predict stock price. We used Alpha Vantage 
API to pull stock data(open,high,low,close,volume) and scraped news headlines from inshorts to perform sentiment analysis.

The code and the images of this repository are free to use as regulated by the licence and subject to proper attribution:
```
Shah, Raj and Tambe, Ashutosh and Bhatt, Tej and Rote, Uday, Real-Time Stock Market Forecasting using Ensemble Deep Learning and Rainbow DQN. 
Available at SSRN: https://ssrn.com/abstract=3586788 or http://dx.doi.org/10.2139/ssrn.3586788.
```
## Architecture
![](imgs/arch.PNG)


## Getting Started

It would be a better idea to create a conda environment and work in isolation 

- Create a virtual environment
```
conda create -n envname python=3.6.8 anaconda 
conda activate envname
```
Use ```conda deactivate``` to deactivate the environment
- Clone this repository
```
git clone --depth 1 https://github.com/THINK989/Real-Time-Stock-Market-Prediction-using-Ensemble-DL-and-Rainbow-DQN.git && cd Real-Time-Stock-Market-Prediction-using-Ensemble-DL-and-Rainbow-DQN
```
- Install the requirements
```
pip install -r requirements.txt
```
- Get an Alpha Vantage API key

To run ```animate.py``` you require a free [Alpha Vantage API Key](https://www.alphavantage.co/support/#api-key). 
Enter the key in ```key=''``` parameter inside the animate.py file 
``` 
ts = TimeSeries(key='',output_format='pandas')
```
- Run python script

To vizualize the forecast. Remember the data pulled by the API will not update the plot if the market is closed. 
```
python animate.py
```
To get heatmap visualization for correlation analysis on ^NSEI(Nifty50)
```
python heatmap.py
```

## License 

This repository is distributed under [MIT License](LICENSE)

and 

respective LICENSE under directories
```
forecast/LICENSE
or 
rainbow/LICENSE
```
for thier independent code usage. 

## Acknowledgements

- [@huseinzol05](https://github.com/huseinzol05/) for deep learning models
- [@sentdex](https://www.youtube.com/channel/UCfzlCWGWYyIQ0aLC5w48gBQ) for plotting tutorials
- [Vader Sentiment](https://github.com/cjhutto/vaderSentiment)
- [Alpha Vantage API](https://www.alphavantage.co/) for stock data
- [Inshorts](inshorts.com) for news headlines

