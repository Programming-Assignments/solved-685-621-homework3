Download Link: https://assignmentchef.com/product/solved-685-621-homework3
<br>
<ol>

 <li><strong>Problem 1</strong></li>

</ol>

In this problem, develop code to analyze the Iris data sets using the test statistics listed in Table 1. Table 1: Data Analysis Statistics

<table width="378">

 <tbody>

  <tr>

   <td width="130"><strong>Test Statistics</strong></td>

   <td width="249"><strong>Statistical Function </strong><em>F</em>(·)</td>

  </tr>

  <tr>

   <td width="130">Standard Deviation</td>

   <td width="249"></td>

  </tr>

 </tbody>

</table>

The analysis should be done by feature followed by class of flower type. This analysis should provide insight into the Iris data set.

Note: The trimmed mean is a variation of the mean which is calculated by removing values from the beginning and end of a sorted set of data. The average is then taken using the remaining values. This allows any potential outliers to be removed when calculating the statistics of the data. Assuming the data in <strong>x</strong><em><sub>s </sub></em>= [<em>x</em><sub>1<em>,s</em></sub><em>,x</em><sub>2<em>,s</em></sub><em>,</em>··· <em>,x<sub>n,s</sub></em>] is sorted, the resulting <strong>x</strong><em><sub>s,p </sub></em>= [<em>x</em><sub>1+<em>p,s</em></sub><em>,x</em><sub>2+<em>p,s</em></sub><em>,</em>··· <em>,x<sub>n</sub></em><sub>−<em>p,s</em></sub>]. the trimmed mean allows the removal of extreme values influencing the mean of the data.

<ol start="2">

 <li><strong>Problem 2 Parts a and b</strong></li>

</ol>

In this problem we will begin to analyze Iris data based on the class of flower type using linear discriminant analysis.

<ul>

 <li>Implement the two class linear discriminant based on the Fisher’s Linear Discriminant (FLD) two-class separability (Fisher, 1936) described below. This is also shown in the two class linear discriminant function presented in (Bishop, 2006) Section 4.1.1 Two classes. For this exercise you will want to separate your Iris data into three sets and focus on any two class combination. For example, from the iris data take the first 50 observations for class 1, the next 50 as class 2 and the final 50 as class 3. Using the two class linear discriminant function compare class 1 verses class 2, class 1 verses class 3 and finally compare class 2 versus class 3.</li>

 <li>For this problem you will want to expand the two class case from part a to a three class case as presented in (Bishop, 2006) from Section 4.1.2 Multiple classes.</li>

</ul>

Now that we have our statistic set up let look a the mean and standard deviation between the classes (Iris flower types) and within the classes let’s consider the Fisher’s Linear Discriminant (FLD) to quantify two-class separability of features (Fisher, 1936). FLD is a simple technique which measures the discrimination of sets of real numbers. Without going into all of the theory of the FLD lets focus on the primary components assuming we have a two class problem, equal class sample and a covariance matrix that is generated from normal distributions. The within-class scatter matrix is defined as

<table width="556">

 <tbody>

  <tr>

   <td width="457"><em>S</em><em>W </em>= X<em>P</em><em>CS</em><em>C</em><em>C</em>where <em>S<sub>C </sub></em>is the covariance matrix for class <strong>C </strong>∈ {−1<em>,</em>+1}</td>

   <td width="99">(1)</td>

  </tr>

  <tr>

   <td width="457"><em>l</em><em>C</em><em>S<sub>C </sub></em>= <sup>X</sup>(<strong>x </strong>− <em>µ<sub>C</sub></em>)(<strong>x </strong>− <em>µ<sub>C</sub></em>)<em><sup>T</sup></em></td>

   <td width="99">(2)</td>

  </tr>

 </tbody>

</table>

<em>i</em>=1<em>,</em>

<em>i</em>∈<em>C</em>

and <em>P<sub>C </sub></em>is the <em>a priori </em>probability class <strong>C</strong>. That is, <em>P<sub>C </sub></em>≈ <em>k<sub>C</sub>/k</em>, where <em>k<sub>C </sub></em>is the number of samples in class <strong>C</strong>, out of a total of <em>k </em>samples. The between-class smatter matrix is defined as

<table width="556">

 <tbody>

  <tr>

   <td width="539"><em>S</em><em>B </em>= X(<em>µ</em>−1 − <em>µ</em>+1)(<em>µ</em>−1 − <em>µ</em>+1)<em>T</em><strong>C</strong>where <em>µ </em>is the global mean vector</td>

   <td width="17">(3)</td>

  </tr>

 </tbody>

</table>

(4)

and the class mean vector <em>µ<sub>C </sub></em>is defined as

(5)

Now lets look at the criterion function <em>J</em>(·) written as follows:

<strong>w</strong><em>TS</em><em>B</em><strong>w</strong>

<em>J</em>(<strong>w</strong>) =            (6) <strong>w</strong><em>TS</em><em>W</em><strong>w</strong>

where <strong>w </strong>is calculated to optimize <em>J</em>(·) as follows:

<strong>w </strong>)                                                                   (7)

<em>w </em>for the Fisher Linear Discriminant has been obtained, which will allow for the linear function to yield the maximum ratio between of the between-class scatter and the within-class scatter. Now let’s determine a threshold <em>b </em>that will allow us to determine which class a new observation will belong to. The optima decision boundary assuming each class has the same number of samples can be calculated as follows:

<em>b </em>= −0<em>.</em>5(<strong>w</strong><em>µ</em><sub>−1 </sub>+ <strong>w</strong><em>µ</em><sub>+1</sub>)                                                                   (8)

Now, if we have a new input observation <em>x </em>we can determine which class the new observation belongs to based on the following

<em>y </em>= <strong>w</strong><em>x </em>+ <em>b                                                                              </em>(9)

where <em>y &lt; </em>0 is class −1 and <em>y </em>≥ 0 is class +1.

The previous discussion is based on the FLD and is simplified as a two class linear discriminant function presented in (Bishop, 2006) Section 4.1.1 Two classes. Credit is given to Fisher for his work in this area of linear discrimination.

<ol start="3">

 <li><strong>Problem 3 </strong><em>Note this is a Collaborative Problem</em></li>

</ol>

25 Points Total

In this problem the Iris data set is to be expanded with synthetic data so that 100 additional observations are generated for each flower class resulting in 300 additional observations. Once the data is generated make similar figure as provided in Figure 1 (a) for each set of paired features and classes.

So let’s take the first 50 observations, the first feature (sepal length) and fourth feature (petal width) shown in red as observed in Figure 1. The 100 additional observations generated are show in blue. In this example the data has similar covariance matrix, mean, minimum and maximum. The synthetic data was generated using the covariance matrix, mean, minimum and maximum of the data. Random data was generated that contained 100 observations and 4 features. The random data was multiplied by the covariance matrix, normalized to fit the original Iris data in terms of minimum and maximum values then the mean of the data was set based on the Iris mean.

<ul>

 <li>Synthetic Data (blue) vs Iris Data (red)</li>

 <li>Distributions</li>

</ul>

Figure 1: Synthetic Data vs Iris Data (a) shows the synthetic data in blue and the original Iris in red, (b) the distributions of the data are shown for context.

<ol start="4">

 <li><strong>Problem 4 </strong><em>Note this is a Collaborative Problem</em></li>

</ol>

In some application areas of data science, data retrieval and data cleansing are critical to the entire analysis process. One example is portfolio analysis. Elsevier’s Scopus <a href="https://www.scopus.com/">(https://www.scopus.com) </a>is the largest abstract and citation database of peer reviewed literature: scientific journals, books and conference proceedings. It covers nearly 36,377 titles from approximately 11,678 publishers, of which 34,346 are peer-reviewed journals in top-level subject fields: life sciences, social sciences, physical sciences and health sciences.

<ul>

 <li>Go to the Scopus website and search for data science and machine learning related documents. Plot the distribution of the number of documents by year from at least the last 10 years. What is the story that the plot tells you?</li>

 <li>Limit the search to 2016 and 2017. List the possible data fields/columns you may need to export in order to answer the question of author and/or institution collaborations in this scientific area during this timeframe.</li>

 <li>Within the possible fields you suggest to export, which fields need data cleansing and why, in order to provide robust input for performing portfolio analysis?</li>

</ul>

<ul>

 <li></li>

</ul>