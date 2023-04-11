# Finance & Quantitative Modeling for Analysts Specialisation
This course is available on Coursera, and here is my own note about this course. Also, this course is made up of 4 mini courses: ***Fundamentals of Quantitative Modeling***, ***Introduction to Spreadsheets and Models***, ***Financial Acumen for Non-Financial Managers*** and ***Introduction to Corporate Finance***.

## Fundamentals of Quantitative Modeling

### Module 1 

#### What is a model?

* A formal ***description*** of a business process.
* It typically involves ***mathematical equations*** and random variables.
* It is almost always a ***simplification*** of a more complex structure.
* It typically relies upon a set of ***assumptions***.
* It is usually implemented in a ***computer program*** or using a spreadsheet.

#### Examples of models

* The price of a diamond as a function of its weight.
* The spread of an epidemic over time.
* The relationship between demand for, and price of a product.
* The uptake of a new product in a market.

#### Diamonds and weight

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230770325-99d91daa-a7bf-4379-973e-083e45a9f46f.png>

#### Spread of an epidemic


<img width = 50% height = 50% src =https://user-images.githubusercontent.com/128298224/230770391-33370d55-acce-40c6-a60e-d8fc2ba69c62.png>

#### Demand models

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230770433-138a7431-3099-4200-b20f-283a4b8c885f.png>

#### The uptake of a new product

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230770481-ea47ee27-c42d-40ce-96d5-8a15015527dc.png>


#### Ways to use models in practice

* Prediction: Calculating a single output: What's the expected price of a diamond ring that weighs 0.2 carats?
* Forecasting (time series): How many people are expected to be infected in 6 weeks?
* Optimisation: What price maximises profit?
* Ranking and targeting: Given limited resources, which potential diamonds for sale should be targeted first for potential purchase?
* Exploring what-if scenarios: If the growth rate of the epidemic increased to 20% per week, then how many infections would we expect in the next 10 weeks?
* Interpreting coefficients in model: What do we learn from the coefficient -2.5 in the price/demand model?
* Assessing how sensitive the model is to key assumptions.

#### Benefits of modeling

* Identify gaps in current understanding
* Make assumptions explicit
* Have a well-defined description of the business process
* Create an institutional memory
* Used as a decision support tool
* Serendipitous insight generator

#### Modeling Process Workflow

<img width = 75% height = 75% src = https://user-images.githubusercontent.com/128298224/230773640-82f4dcd2-f996-419d-8c74-61891071cf5e.png>

#### What if the model doesn't always work

* When the observed outcome differs greatly from the model's predicition, then there is the possibility of learning from thies event if we can understand why the difference occurs.
* Modeling is a continuous and evolutionary process
* We identify the weaknesses and limitations and iterate the modeling process to overcome them.


#### Data driven vs. theory driven

* ***Theory***: Given a set of assumptions and relations, then what are the logical consequences? E.g. If we assume that markets are efficient, then what should the price of a stock option be?
* ***Data***: Given a set of observations, how can we approximate the underlying process that generated them? E.g. I've separated out my profitable customers from the unprofitable ones. Now, what features are able to differentiate them?

#### Deterministic vs. probabilistic/stochastic

* ***Deterministic***: Given a fixed set of inputs, the model always gives the same output. E.g. Invest $1000 at 4% annual compound interest for 2 years. After 2 years the initial $1000 will always be worth $1081.60.
* ***Probabilistic***: Evven with identical inputs, the model output can vary from instance to instance. E.g. A person spends $1000 on lottery tickets. After the lottery is drawn how much they are worth dependes on a random variable, whether or not they won the lottery.

#### Discrete vs. continuous variables

* Watches can be digital or analog
* Likewise models can involve discrete or continuous variables. ***Discrete***: characterised by jumps and distinct values; ***Continuous***: a smooth process with an infinite number of potential values in any fixed interval.

#### Static vs. dynamic

* ***Static***: the model captures a single snapshot of the business process. E.g. Given a website's installed software base, what are the chances that it is compromised today?
* ***Dynamic***: the evolution of the process itself is of interest. The model describes the movement from state to state. E.g. Given a person's participation in a job training program, how long will it take until he/she finds a job and then, if they find one, for how long will they keep it?


#### Linear function

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230774475-7ea3b045-9502-4053-ac08-643c29a9e670.png>

* $y = mx + b$
* Essential characteristic: the slope is constant.

#### The power function for various powers of $x$

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230774533-708c55d7-d1d4-4d49-8f11-d7726f694a73.png>

* $y = x^{m}$.
* Essential characteristic: A one ***percent*** (proportionate) change in $x$ corresponds to an approximate $m$ ***percent*** (proportionate) change in $y$.

#### The exponential function

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230774713-d46dae68-b138-4488-89d0-9556fdb9ac38.png>

* $y = e^{mx}$.
* Essential characteristic: the rate of change of $y$ is proportional to $y$ itself.

#### The log function

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230774914-56ce0522-ab48-46b2-bf60-4073c0f41c05.png>

* $y = \log_{b}(x)$.
* $\log(xy) = \log(x)+\log(y)$.
* The log function is very useful for modeling processes that exhibit ***diminishing returns to scale***.
* There are processes that increase but at a decreasing rate.
* Essential characteristic: A constant proportionate change in $x$ is associated with the same absolulte change in $y$.

### Module 2


#### Deterministic models

* There are no random/uncertain components in these models.
* If the inputs to the model are the same then the outputs will always be the same.
* The downside of deterministic models: it is hard to assess uncertainty in the outputs.

#### A linear cost function

* Call the number of units produced $q$, and the total cost of producing $q$ units $C$.
* Define $$C = 100+30q.$$ 
<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230897263-cf6354bb-804c-4dee-98e2-52b98f4547a8.jpg>

#### Interpretation 

* The two coefficients in the line are the intercept and slope: $b$ and $m$ in general, 100 and 30 in this particular instance.
* $b$: the total cost of producing 0 units. That part of total cost that doesn't depend on the quantity produced: the ***fixed*** cost.
* $m$: the slope of the line: the change in total cost for an incremental unit of production: the ***variable*** cost.

#### Example with a 'time-to-produce' function

* It takes 2 hours to set up a production run, and each incremental unit produced always takes an additional 15 minutes (0.25 hours); always here means constant slope.
* Call $T$ the time to produce $q$ unites, then $$T = 2+0.25q$$
* Interpretation: $b$ is the ***setup*** time; $m$ is the ***work rate*** (15 minutes per additional item).

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230898112-9301e0b9-6cdf-44e3-9469-9673aadd56ae.jpg>


#### Linear programming

* One of the key uses of linear models is in ***Linear Programming (LP)***, which is a techinique to solve certain ***optimisation*** problems.
* These models incorporate ***constraints*** to make them more realistic.
* Linear programming problems can be solved with add-ins for common spreadsheet programs.


#### Growth in discrete time

* Growth is a fundamental business concept: the number of customer at time $t$; the revenue in quarter $q$; the value of an investment at some time $t$ in the future.
* Sometimes a linear model may be appropraite for a growth process, but an alternative to a ***linear growth*** model is a ***proportionate*** one.
* Proportionate growth: a constant percent increase (decrease) from one period to the next.

#### Simple interest

* Start off with $100 (***principal***) and at the end of every year earn 10% of ***simple interest*** on the initial $100.
* Simple interest means that interest is only earned on the principal investment.
* Every year the investment grows by the same amount.

#### Compound interest

* Start off with $100 (***principal***) and at the end of every year earn 10% of ***compound interest*** on the initial $100.
* Compound interest means that the interest itself earns interest in subsequent years.
* Notice that the growth is no longer the same absolute amount each year, but it is the same proportionate amount (10%).

#### Comparison between two interest

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230899107-b332ea49-a986-404b-8bec-218ed6176348.jpg>


#### Constant proportionate growth

* Denote the initial amount as $P_{0}$.
* Denote the constant proportionate growth factor by $\theta$.
* The growth progression is $$P_{0},P_{0}\theta,P_{0}\theta^{2},...,$$
* $\theta > 1$ means the process is growing.
* $\theta < 1$ means the progress is decaying.
* The type of progression is called ***geometric progression***.

#### The constant multiplier

* For the catch to fall by 5% each year, means that the multiplier is $\theta = 0.95$.
* In general, if the process is changing by $R$% in each time period, then the multiplier is $$\theta = 1+\frac{R}{100}.$$

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230900037-d3f62edd-2554-4810-8a24-dabcfb4ea20c.jpg>

#### The sum of the geometric series

* If we denote the sum up to time $t$ as $S_{t}$, then $$S_{t} = P_{0}\frac{1-\theta^{t+1}}{1-\theta}.$$
* More efficient than spreadsheet.

#### Present and future value

* If there is no inflation and the prevailing interest rate is 4%, then which of the following options would you prefer?
* $1000 today or $1500 in ten years?
* Either look at how $1000 will be worth in ten years or calculate how much you would have to invest today to get $1500 ten years from now.
* The latter approach relies on the concept of ***present value***.

#### The present value calculation

* We know that $P_{t} = P_{0}\theta^{t}$ and making $P_{0}$ the subject of the formula means that $P_{0} = P_{t}\theta^{-t}$.
* Therefore, 1500 dollars in ten years time in a 4% interest rate environment is worth $1500(1+0.04)^{-10}$ in today's money, which is $1013.346, which is more than $1000, so you should prefer the second investment of $1500 received in ten years.
* This straightforward proportionate increase model allows for a simple discounting formula.

#### Use of present value

* A primary use in discounting investments to the present time.
* An ***annuity*** is a schedule of fixed payments over a specified and finite time period.
* The present value of an annuity is the ***sum*** of the present values of each separate payment.
* Present value is also used in ***lifetime customer value*** calculations.

#### Continuous compounding

* The compounding period for an investment can be yearly, monthly, weekly, daily etc.
* As the compounding period gets shorter and shorter, in the limit, the process is said to be ***continuously compounded***.
* If a principal amount $P_{0}$ is continuously compounded at a nominal annual interest rate of R%, then at year $t$, $$P_{t} = P_{0}e^{rt}$$ where $r = \frac{R}{100}$.

#### Modeling an epidemic

* The model $P_{t} = P_{0}e^{rt}$ doesn't just describe money growing, it is called ***exponential growth*** or ***decay*** depending on whether $r$ is positive or negative respectively.
* A continuous time model for the initial stages of an epidemic states that the number of cases at week $t$ is $15e^{0.15t}$, halfway through week 7, how many cases do you expect?

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230902097-804a13c1-a895-438c-89dc-c0dcd1554a88.jpg>

#### Calculating the expected number of cases

* Interpretation of the 0.15 coefficient: There is an approximate 15 weekly growth rate in cases.
* Continuous models allow calculations at any value of $t$, not just a set of discrete values.

#### Using a model for optimisation

* A common modeling objective is to perform a subsequent optimisation.
* The objective of the optimisation is to find the value of an input that maximises/minimises an output.

#### Demand model

* Consider the demand model: $$Q = 60000P^{-2.5}.$$
* If the price of production is constant at $C=2$ for each unit, then at what price is profit maximised?
* Profit = Revenue - Cost
* Revenue = $P\times Q$.
* Profit = $PQ-CQ = Q(P-C) =60000P^{-2.5}(P-2).$
* Goal: Choose $p$ to maximise this equation.

#### Brute force approach

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230902960-0a16a87d-c4b0-4217-869e-563e34157d4c.jpg>

#### Calculus approach

* Profit is maximised when the ***derivatie*** or profit with respect to price equals to 0.
* Through calculus one obtains the optimal value of price as $$p_{\text{opt}} = \frac{cb}{1+b}$$, where $c$ is the production cost and $b$ is the exponent in the power function.
* The value (-b) is known as ***the price elasticity of demand***.

#### Visualising the calculus solution

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/230903553-a380f0ec-0d77-463b-b4c4-df444e55d10d.jpg>

### Module 3

#### Probabilistic models

* These are models that incorporate ***random variables*** and ***probability distributions***.
* Random variables represent the potential outcomes of an uncertain event.
* Probability distribution assign probabilities to the various potential outcomes.
* We use probabilistic models in practice because realistic decision making often necessitates recognising uncertainty in the intpus and outputs of a process.

#### Key features of a probabilistic model

* By incorporating ***uncertainty*** explicitly in the model we can measure the uncertainty associated with the outputs, for example by giving a range to a forecast, which is a more realistic goal.
* In a business setting incorprating ***uncertainty*** is synonymous with understanding and quantifying in the ***risk*** in a business process, and ideally leads to better management decisions.

#### Valuing a drug development company

* A company has 10 drugs in a development portfolio.
* Given a drug has been approved, you have predicted its revenue.
* But whether a drug is approved or not is an uncertain future event (a random variable). You have estimated the probability of approval.
* You only wish to invest in the company if the company's expected total revenue for the portfolio is over $10B in 5 years time.
* You need to calculate the ***probability distribution*** of the total revenue to understand the investment risk.

#### Some examples of probabilistic models

* Regression models
* Probability trees
* Monte Carlo simulation
* Markov models

#### Regression models

* $E(Price|Carats) = -259.6 + 3721\times Carats$.
* The gray band gives a prediction interval for the price of a diamond taken from this population.
<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/231178439-c4315006-1c48-4f10-8312-979bee01a70c.png>

* Regression models use data to estimate the relationship between the mean value of the outcome (Y) and a predictor variable (X).
* The intrinsic variation in the raw data is incorporated into forecasts from the regression model.
* The less noise in the underlying data the more precise the forecasts from the regression model will be.

#### Probability tress

* Probability tress allow you to propagate probabilities through a sequence of events.
* $P(\text{Stop infringing}) = 0.1+0.9\times 0.15+0.9\times 0.85\times 0.2 = 0.388.$

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/231179458-2832faa8-551a-4680-9239-35d69b26b9ff.png>

#### Monte Carlo simuation

* From the demand model $$Q = 60,000P^{-2.5}.$$
* The optimal price was $p_{opt} = \frac{cb}{1+b}$ where $b = -2.5$, $c$ is the cost, $c=2$ and $p_{opt}\approx 3.33$.
* What if $b$ is not known exactly?
* Monte Carlo simulation replaces the number -2.5 with a random variable, and recalculates $p_{opt}$ using different realisations of this random variable from some stated probability distribution.

#### Input and output from a MC simulation

* Input: $b$ from a uniform distribution between $-2.9$ and $-2.1$.
* Output: $p_{opt} = \frac{cb}{1+b}.$
* 100,000 replications
* Interval $= (3.1,3.7)$.

<img width = 50% height = 50% src = https://user-images.githubusercontent.com/128298224/231181300-1ba328c8-00ed-420d-9be8-65a455172251.png>
