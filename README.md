Title: Annual Greenhouse Gas Emissions Research
Aim: To research the annual greenhouse gas emissions in the United Kingdom and produce a
model to Visualise its Data, and predict annual emissions for the next five(5) years using
Python and Excel.
Summary: Using the Office of National Statistics “Atmospheric emissions: greenhouse gases
by industry and gas” data set I visualised the current trend of greenhouse gas emissions as
well as creating a model to predict the emissions for the next 5 years. I will explain the step
by step process below;
a. ONS Data: Data Cleaning and Preparation: The ONS dataset was provided in a
xlsx format which included multiple spreadsheets. These spreadsheets
contained information on the annual greenhouse gas emission by sector and
section as well as each individual gas emission in the UK indexed by the year.
I edited the data in an excel workbook, removing the spreadsheets
containing individual gas data and worked on the annual greenhouse gas
spreadsheet. I decided to remove the table which contains individual sector
annual gas emissions and only retained the table showing emissions by sector
and section indexed by year and. I made this decision because I wanted to
retain as much information as possible for our model to be robust and
accurate.
I changed the format from xlsx to csv, imported it into my jupyter
notebook, dropped the sectors and retained the sections using pandas and
transposed it, so sections were the columns and years were the rows. The
total greenhouse emissions was designated to be our target column. The data
type of the figures in the table were objects which I changed to integers using
functions in the pandas library.
b. Exploratory Data Analysis: The greenhouse gas emissions in the United
Kingdom have been on a steady decline since 1990.
name: DAVID AMUSAN
Email: davidamusan16@gmail.com
The graph shows greenhouse emissions have been on a steep decline with a
rather large drop between 2015 and 2020. Investigating that further in the
figure below shows that between 2019 and 2020 there has been a huge
decline in the greenhouse gas emissions.
This could be attributed to the COVID-19 impact that hit. During our
prediction we will determine if this was an anomaly due to the rise to the
predicted figures of the year 2021 and 2022.
c. Modelling: Our data had 100+ and 32 rows. To reduce these dimensions and
still retain as much information as possible Principal Component Analysis
was applied to our data. This was applied on the columns in each sector by
first scaling them relative to each other and then applying PCA to reduce each
sector's number of dimensions to one(1).
After this was applied the number of columns were reduced from
100+ to 22, while still retaining the information of each section.
name: DAVID AMUSAN
Email: davidamusan16@gmail.com
Scaled and Compiled Table showing Sections against Years.
d. Modelling Technique: After plotting the data available and deliberating on the
problem statement. A multiple linear regression model was chosen to be our
model. A close second would have been Recurrent Neural Networks which
would have been able to generate good predictions but was decided against
because of major drawbacks as well as limitations. The output of the linear
regression model will enable predictions to be made of the incoming years by
supplying hypothetical rows to the model for each sector so a total can be
predicted.
e. Model Output: Our multiple linear regression model has an accuracy of
0.9902725906857217. We split our data set into training and test random
data sets, after which we fit, learnt and began making predictions.
Our hypothesis on the huge drop being as a result of the
pandemic was correct. Our model predicted a huge increase in the following
year due to previous occurrences of sharp drops in greenhouse gas emissions.
Our graph below shows the prediction of the next 5 years against the
previous 2 years in the dataset.
name: DAVID AMUSAN
Email: davidamusan16@gmail.com
Predictions of greenhouse gas emissions over the next 5 years.
f. Conclusion: The United Kingdom's aim for net zero greenhouse gas emissions
by 2050 does not seem feasible due to unforeseen circumstances like a
pandemic or natural disaster. The other half of the spectrum is an
astronomical increase in technological prowess which would in turn prevent a
huge spike in GHG emissions and exponentially reduce the current emissions
each year up until 2050. But at the current rate, 2050 does not seem feasible.
g. Limitations
● Outliers have a huge effect on Linear regression. Due to time
constraints I wasn't able to completely curb this issue.
● Linear regression assumes all variables are independent of each other,
this might not be the case when dealing with dependent industries
which have directly proportional GHG emissions.
