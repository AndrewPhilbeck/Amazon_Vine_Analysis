# Amazon_Vine_Analysis

# Amazon Vine Review

Analyzing the reviews of the Amazon Vine program to check for bias

## Overview

I chose to analyze a large dataset of book reviews through with PySpark and Pandas to determine if there was any bias based on the number of favorable reviews published by Vine members. 

In order to best study the dataset I created four different tables by connecting Amazon Web Services to PySpark and then to pgAdmin4. 

### Customer Table
(First twenty rows)

<img width="198" alt="customer table" src="https://user-images.githubusercontent.com/115502048/219958231-eef3645b-66be-48bd-9d3d-aec7d7c0c1c5.png">

### Products Table
(First twenty rows)

<img width="482" alt="products table" src="https://user-images.githubusercontent.com/115502048/219958243-94518b70-1a76-4fa1-b208-8507abc25984.png">

### Review ID Table
(First twenty rows)

<img width="353" alt="review id table" src="https://user-images.githubusercontent.com/115502048/219958251-fedad7ea-c216-4c20-840d-af52f90bd44f.png">

### Vine Table
(First twenty rows)

<img width="457" alt="vine table" src="https://user-images.githubusercontent.com/115502048/219958278-786cfdf9-b993-4067-8cd3-b54f6f84ef97.png">

I then created a Data Frame using Pandas to implement further analysis just on the Vine Table.  

## Results of Analysis

I then created a Data Frame using Pandas to implement further analysis just on the Vine Table. The results of the analysis were quite surprising. 

* For the reviews which garnered at least 20 votes or higher and where the percentage of helpful votes divided by total votes was at least 50% there were a total of “0” from those who participated in the Vine program.

<img width="606" alt="first post d2" src="https://user-images.githubusercontent.com/115502048/219958287-59e39d05-8b4d-42ec-ba4e-beaa551594f0.png">

* This means (with the same parameters in place) there were a total of “403897” from those not participating in the Vine program.

<img width="648" alt="second d2" src="https://user-images.githubusercontent.com/115502048/219958297-966253c0-ed07-436c-bbc0-3541d9944ca8.png">

* Of those not participating in the Vine program there were a total of “242889” five-star reviews given.

<img width="653" alt="third d2" src="https://user-images.githubusercontent.com/115502048/219958311-54e1d5fc-c988-4667-9e98-c5a3f5092ff8.png">

* The percentage of five-star reviews given by non Vine participants was 60.15%

<img width="648" alt="fourth d2" src="https://user-images.githubusercontent.com/115502048/219958325-492b0e1f-6c60-4b20-9935-f80b1fd1cc9a.png">

### Because those participating in the Vine program did not even pass the bar set to be analyzed my conclusion is _No Bias_. 

Given the clarity of the results I do not recommend any other analysis. 

If some must be done however the first thing would be to lessen the expectations for being analyzed. Simply look at the total number of five-star reviews for those in the vine program vs. those who are not, regardless of how many votes they received or if the helpful votes divided by total votes were above 50%.
