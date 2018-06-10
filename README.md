
# README #

#### Note: If you have issues viewing the notebooks copy/paste the nb link into nbviewer.jupyter.org

### What is this repository for? ###

The primary goal of this repo is to demonstrate the workflow between research of a quantitative idea or theory to implementation as a potential live trading strategy. Unlike other finance based tutorials the results will not be cherry picked to show only the best of the best examples. Sometimes results are counterintuitive, sometimes they are conflicting. Real strategy development is often dirty, complex, full of starts and stops and requires us to use all of our skills to extract the signal from the noise. With that said I welcome interactive engagement, ideas, insight, and constructive criticism, especially if errors or bugs are found. **(IN-PROGESS...)**

The strategy development focuses on using mixture models as a method for market timing. Types of mixtures to be covered include:

* gaussian mixtures **(in-progress...)**
* bayesian mixtures **(not-started)**
* nonparametric mixtures **(not-started)**
* gaussian processes **(not-started)**


#### There are some challenges to implementation ####

* This repo will attempt to make use of the [QuantConnect](https://www.quantconnect.com/) platform. It is built in `C#` with `python` integrated as a first class citizen on the platform. However, for those of us who are migrating to this platform from `Quantopian`, there is a non-trivial learning curve. 
* The `python` infrastructure is more flexible i.e. there are less restrictions on packages and which classes can be imported, there are more securities available for testing and trading.
* The `python` infrastructure is more immature however i.e. there is no interactive debugger `(as of Dec. 11, 2017)`, the error stack traces are not as informative and do not point to which lines caused particular errors, so testing can be a pain.
* The owner of the platform `Jared Broad` is very responsive and the team is active in communicating with the users and working with us to improve the platform
 
### Chapter (Notebook) Outlines ###

1. **Motivation: (Completed-Editing...)**
	- this chapter goes through a demo of challenges to time series prediction using real market data
	- what is stationarity?
	- why one distribution isn't enough?
	- how can multiple distributions help?
2. **Gaussian mixtures: (Completed-Editing...)**
	- In this chapter we explore the underlying intuition behind gaussian mixtures
	- We will construct a simple implementation of the expectation-maximization algorithm
	- We apply a gaussian mixture model to predict an asset's return distribution using sklearn
3. **Designing the strategy: (Completed-Editing...)**
	- In this chapter we will use what we have learned to construct a strategy idea
	- We rapidly prototype the idea using the data we have to decide if the idea is worth further testing
4. **Implementation: (Completed-Editing...)**
	- In this chapter we will implement the idea into a strategy using the Quantconnect platform IDE.
	- We will implement the simplified components of an automated strategy including:
		* slippage/fees		
		* order management, 
		* inventory management, 
		* indicator construction,
		* task scheduling
5. **Evaluation: (Completed-Editing...)**
	- Backtest the strategy.
	- Download backtest portfolio equity
	![quantconnect algo equit download](https://raw.githubusercontent.com/BlackArbsCEO/mixture_model_trading_public/master/visuals/05_Algorithm_Evaluation/Quantconnect-download-data-gif-Peek%202018-02-19%2010-42.gif)
	- Read in Algorithm Portfolio Equity
	- Choose the Best Algorithm Among 4 Variants
	- Choose Best Bayesian Model of Algorithm Returns
	- Compare Bayesian Cones for all Algos and all Return Models
	- Compare Best Algo Predicted Portfolio Ending Values
	- Compare Best Algo Predicted CAGR Distributions
	- Model Averaging

### QuantConnect Links/Resources for Python Users ###

* [How to use the api?](https://www.quantconnect.com/docs)
* [Github repo full of Python Algo Examples](https://github.com/QuantConnect/Lean/tree/master/Algorithm.Python)
* [Forum discussion-migrating from Quantopian to Quantconnect](https://www.quantconnect.com/forum/discussion/2317/migrating-from-quantopian-to-quantconnect/p2)
* [Tutorials](https://www.quantconnect.com/tutorials/)


### Who do I talk to about this repo? ###

* blackarbsceo | [blackarbs.com](www.blackarbs.com)
* bcr@blackarbs.com

