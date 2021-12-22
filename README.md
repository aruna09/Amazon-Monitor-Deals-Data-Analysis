# Amazon Monitor Deals Data Analysis ☜(ﾟヮﾟ☜)

## Dataset👩‍🏫

**Story**?

Predicting House Prices is too mainstream😆

Well, it's very simple. I wanted to buy a Monitor for work, and while shortlisting one, realized that this would be a great problem to work on.
Wrote a quick script(wasn't quick at all, lol) to scrape data and saved it into the old fashioned csv.

**Content**👩‍💻👨‍💻

To start with, this is pure RAW data. It has lot's of NULL, empty and unexpected data.
So if you are looking for an intensive Data Cleaning/Preprocessing or Feature Engineering, this is the right place to start.
There are 90 columns and some of them are:

Length(In): Length in Inches

Width(In): Width in Inches

Height(In): Height in Inches

Weight: Weight in Pounds

Price: Price of the Monitor in Dollars

Brand: Brand of the Monitor

Manufacturer: Manufacturer name

Country of Origin

## Tools used ⚙

**Language**: python 3.x and selenium

**Editor**: google colab

**Visualizations**: matplotlib, seaborn

**ML Library**: scikit learn

**General preprocessing and observation**: BigQuery/Excel

## How did I start?👩

### Loading the data ofcourse!

![image](https://user-images.githubusercontent.com/25157152/146932081-2440eb59-6753-4e2a-9b70-4547a23baeb7.png)

### Observation🔎: 
A little observation reveals pretty straight forward float features and a couple of categorical values(note: these will need some kind of conversion to be used for training)

![image](https://user-images.githubusercontent.com/25157152/147081163-f334b850-e22f-45f2-8bb1-e54cd6a7f70a.png)


### Visualization📊: 
Time for some cool graphs!

![image](https://user-images.githubusercontent.com/25157152/147081425-b8de3562-1616-4832-944f-a0a026aec65b.png)

![image](https://user-images.githubusercontent.com/25157152/147081546-67009c24-b930-4107-866d-70ded5b98d03.png)


### Actual Coding begins👩‍💻: 

1. Drop **insignificant columns** like (any kind of id's or names)
2. Check for **null values/special characters** that will need trasformation
3. **General Preprocessing**:
    
![image](https://user-images.githubusercontent.com/25157152/147081328-e470828a-448c-4bec-921f-85402af827fe.png)

4. Imputing missing values and Feature Engineering for each feature was dealt with separately, on a case by case basis.
   - Length, Height and Width: missing values were imputed with group mean
   - Brand, Manufacturer: These categorical variables were Mean//Frequency Encoded with the Target feature(Price)
   -  ASIN, Item_Model_number: Label Encoded
   
### Model Building👩‍🏫

This is where we start building our classifiers which will be trained on this super clean data!

### Prediction📓

Its show time!! Check the code to find which classifier performed the best!

