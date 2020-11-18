# Review of the Use of Wearables in Personalized Medicine

[![Check Report](https://github.com/cybertraining-dsc/fa20-523-302/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-302/actions)
[![Status](https://github.com/cybertraining-dsc/fa20-523-302/workflows/Status/badge.svg)](https://github.com/cybertraining-dsc/fa20-523-302/actions)
Status: in progress

Adam Martin, [fa20-523-302](https://github.com/cybertraining-dsc/fa20-523-302), [Edit](https://github.com/cybertraining-dsc/fa20-523-302/blob/main/project/project.md)


{{% pageinfo %}}

## Abstract


Contents

{{< table_of_contents >}}

{{% /pageinfo %}}

**Keywords:** Wearables, Classification, Descriptive Analysis, Healthcare, Movement Tracking, Precision Health

## 1. Introduction

Wearables have been on the market for years now, gradually improving and providing increasingly insightful data on user health metrics. Most wearables contain an array of sensors allowing the user to track aspects of their physical health. This includes heart rate, motion, calories burned, and some devices now support ECG and BMI measurements. This vast trove of data is valuable to consumers, as it allows for the measurement and gamification of key health metrics. But can this data also be useful for health professionals in determining a patient’s activity levels and tracing important events in their health history?


## 2. Background Research and Previous Work

Previous work exists on the use of sensors and wearables in assisted living environments.  Consumer wearables are commonplace and have been used primarily for tracking individual activity metrics.  This research attempts to establish the efficacy of these devices in providing useful data for user activity, and how this information could be useful for healthcare workers.  This paper examines the roadblocks in making this information available to healthcare professionals and examines what wearable information is currently being used in healthcare.

Existing research focuses on a wide variety of inputs [^2][^1].  Sensors including electrodes, chemical probes, microphones, optical detectors, and blood glucose sensors are referenced as devices used for gathering healthcare information.  This research will focus on data that can be gathered with a modern smartphone or smartwatch.  Most of the sensors described are not as ubiquitous as consumer items like FitBits or Apple Watches.  

Previous studies have indicated the significance of precision health and the need for patient-specific data from wearables to be integrated into a patient's care strategy [^4].  Wearable data outlining a patient's sleep, motion habits, heart rate, and other metrics can be invaluable in diagnosing or predicting conditions.  Increased sedentary activity could indicate depression, and could predict future heart problems.  A patient's health could be graphed and historical trends could be useful to determine potential causes for a diagnosis.  
It is often asserted that a person's environmental factors are better predictors for their health than their genetic makeup [^4].  Linking behavioral and social determinants with biomedical data would allow professionals to better target certain conditions. 

## 3. Choice of Data-sets

The dataset used for this project contains labeled movement data from wearable devices.  The goal is to establish the potential for wearable devices to provide high-quality data to users and healthcare professionals.  

A dataset gathered from 24 individuals with Apple devices measuring attitude, gravity, acceleration, and rotation rate, will be used to determine user states.  The dataset is labeled with six states (walking downstairs, walking upstairs, sitting, standing, walking and jogging) and each gyroscopic sensor has several attributes describing its motion.  

If successful, this will establish that wearables have a high potential for providing relevant information beyond exercise metrics.  

## 4. Methodology

The analysis of relevant wearable data is undertaken to determine the accuracy of activity information.  This analysis will consist of a brief descriptive analysis of the motion tracking data, and will proceed with attempts to classify the labeled data using various classification methods (K-nearest neighbors, random forest).

First, the data has to be downloaded from the MotionSense project GitHub.  A basic descriptive analysis will be performed, visualizing the sensor values for each movement class over time.  

A SciKit pipeline is set up for each classifier.  After obtaining a train/test split the pipeline applies a standard scaler to normalize the data, and then fits the classifier on the training data.  Each classifier is then scored using the testing dataset.

If a classification strategy of sufficient accuracy is possible, it will be determined that wearable data can potentially serve as a useful supplementary source of information to aid in establishing a patient's medical history.

Reviewing relevant literature is important to determine the current state of wearables research regarding usefulness to healthcare workers and user well-being.  Much of this research will be focused on determining the state of wearables in the healthcare industry and determining if there is a need for streamlined data transfer to healthcare professionals.  
 

## 5. Discussion

The dataset is comprised of six discrete classes of movement.  Below is a sample of the dataset.  

![Figure 1](https://raw.githubusercontent.com/cybertraining-dsc/fa20-523-302/main/project/images/dataframe.png)

**Figure 1:** Pandas data frame snippet

There is an imbalance in the number of datapoints for each class, which could lead to classification errors.

![Figure 2](https://raw.githubusercontent.com/cybertraining-dsc/fa20-523-302/main/project/images/occurence.png)

**Figure 2:** Data distribution per movement class.

Below is an example of the data's representation of a class of movement.  In this instance it's that of a male jogging.

![Figure 3](https://raw.githubusercontent.com/cybertraining-dsc/fa20-523-302/main/project/images/timeseries_run.png)

**Figure 2:** 10 second sensor readout of a jogging male.



## 6. Conclusion


## 7. Acknowledgements 


## 8. References

[^1]: Piwek L, Ellis DA, Andrews S, Joinson A. (2016, February 02).  I Retrieved November 11, 2020 from <https://journals.plos.org/plosmedicine/article?id=10.1371/journal.pmed.1001953>  

[^2]: Yetisen, Ali K. (2018, August 16).  I Retrieved November 15, 2020 from <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6541866/>  

[^3]: Loncar-Turukalo, Tatjana, Literature on Wearable Technology for Connected Health: Scoping Review of Research Trends, Advances, and Barriers (2019, September 21). I Retrieved November 02, 2020 from <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6818529/>

[^4]: Glasgow, Russell E. Realizing the full potential of precision health: The need to include patient-reported health behavior, mental health, social determinants, and patient preferences data (2018, September 13). I Retrieved November 15, 2020 from <https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6202010/>




