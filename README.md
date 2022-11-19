# A Learnheuristic Approach to A Constrained Multi-Objective Portfolio Optimisation Problem
## Project Description:
Multi-objective portfolio optimisation is an important problem researched across various fields of study as it achieves the objective of maximising the expected return while minimising the risk of a given portfolio at the same time. However, many studies fall short of including realistic constraints into the model, which poses as a limitation to practical trading strategies. In this research, we introduce realistic constraints, such as transaction costs as well as holding costs, into an optimisation model. Due to the non-convex nature of this problem, metaheuristic algorithms, such as NSGA-II, R-NSGA-II, NSGA-III and U-NSGA-III, will play a vital role in solving the problem. Furthermore, a learnheuristic approach is taken as surrogate models are used to enhance the metaheuristics employed. These algorithms are then compared to the baseline metaheuristic algorithms, which solve a constrained, multi-objective optimisation problem without the use of learnheuristics. The results of this research show that, despite taking significantly longer to run to completion, the learnheuristic algorithms outperform the baseline algorithms in terms of hypervolume and rate of convergence. Furthermore, the backtesting results indicate that utilising learnheuristics to generate weights for asset allocation leads to a lower risk percentage, higher expected return and higher Sharpe ratio compared to backtesting without the use of learnheuristics. This leads us to conclude that using learnheuristics to solve a constrained, multi-objective portfolio optimisation problem produces superior and more preferable results compared to solving the problem without the use of learnheuristics.

## Summary of The Methodology Followed:
<p align="center">
<img width="505" alt="Screenshot 2022-11-14 at 00 18 27" src="https://user-images.githubusercontent.com/81515681/201547368-709af1d2-3c89-4c38-a3cb-a419a5900860.png">
</p>

## Results:
### Genetic algorithms without surrogate variants
<p align="center">
<img width="500" alt="Screenshot 2022-11-14 at 00 25 09" src="https://user-images.githubusercontent.com/81515681/201547802-334f23b7-bd7a-495c-80b5-4647090bd096.png">
</p>

<p align="center">
<img width="582" alt="Screenshot 2022-11-14 at 00 25 23" src="https://user-images.githubusercontent.com/81515681/201547836-09996a2c-190e-4b49-b825-b3048dbf8ac7.png">
</p>

Based on the results from Table I, it is evident that the NSGA-II algorithm takes the longest time to run, however, given that it produces the highest hypervolume, it suggests that the best performing algorithm is NSGA-II. Based on Fig. 1, it can be seen that the NSGA-II algorithm is the first to converge.

### Learnheuristic algorithms
<p align="center">
<img width="500" alt="Screenshot 2022-11-20 at 01 56 49" src="https://user-images.githubusercontent.com/81515681/202876200-3eec3e0d-5d59-48fb-8d49-f42cd57de7ca.png">
</p>

<p align="center">
<img width="816" alt="Screenshot 2022-11-19 at 17 47 40" src="https://user-images.githubusercontent.com/81515681/202859315-236fe231-a455-4f58-97d3-f74d4411539a.png">
</p>

Table II indicates that, similar to the non-surrogate variant, the NSGA-II algorithm yields the highest hypervolume, thus making it the most efficient algorithm. Fig. 2-5 each indicate that the learnheuristic algorithms produce higher hypervolumes and converge sooner compared to the baseline algorithms, despite taking significantly longer to run to completion.

### Backtesting
<p align="center">
<img width="500" alt="Screenshot 2022-11-19 at 17 47 25" src="https://user-images.githubusercontent.com/81515681/202859321-13b1db08-86d6-44c4-950d-1003c3ba3b6f.png">
</p>

From Table III above, we see that each of the four learnheuristic algorithms outperform the backtest run without a learnheuristic algorithm. The portfolios that run by utilising the surrogate-assisted genetic algorithms to find the optimal weights for asset allocation yield higher returns for a lower percentage of risk and also produce greater Sharpe ratios.

## Recommendations for Future Work:
The parameters of the learnheuristic algorithms are incredibly sensitive. Therefore, in future research, implementing a search algorithm, such as a random search or a grid search, to tune the parameters would be beneficial. This, in turn, may also assist with allowing the learnheuristic algorithms to consider portfolios with more than ten assets and still produce optimal results. 

## Installation Guide:
1. Download the full project and unzip the 'Dataset' folder.
2. Ensure that the latest versions of the *PyPortfolioOpt*, *Pymoo*, *Pysamoo* and *portfolio-backtest* frameworks are installed on the machine. Links to the documentation of these libraries can be found in the research report above.
3. Run the Jupyter Notebook code from the top.
