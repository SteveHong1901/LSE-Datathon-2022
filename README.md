# LSE-Datathon-2022


## Inspiration
We were fascinated to find out that network theory, a concept that we were only exposed to in Maths class as graph theory, could be used for financial stability and data science. We centred our data processing such that the data provided was structured like networks. We tried to incorporate as many properties of networks as possible in our analysis.

## What it does
A full project (data processing to evaluation of models) with evaluations and observations in between. Processes and cleans the data provided, transforms the data to improve performance of the model. Employs 2 different anomaly detection algorithms, mainly to be used as a preliminary study in fine tuning and designing an effective model. Also included evaluations and visualisations of the models, along with possible areas of improvement.

## How we built it
We leveraged upon the network model by restructuring the long dataframe into a symmetric matrix, which led to various interesting applications. A range of powerful libraries for dataframe manipulation, data visualisation and machine learning algorithms had been utilised, such as Pandas, Matplotlib and Sklearn. We also researched extensively on the available unsupervised learning models for anomaly detection, and carefully evaluated them statistically so that we can avoid any major biases when it came to model selection and implementation. The final models included are  Histogram-based Outlier Detection (HBOS) and Isolation Forest.


## Challenges we ran into
The first challenge we needed to deal with was to transform the data we gave to matrices. We decided to sort the data using the date given (net_id in the “bis_arcs-1 file'') and an adjacency matrix from network theory was used to transform data. We found out that not all the countries having foreign claims data recorded in the “bis_arcs-1 file”, we used code["vertex_id"].unique()to retrieve id of all countries, so that we can form matrices between every countries and for data not recorded in the dataframe we have 0 instead. Moreover, in order to use the outlier detection model, we have to modify the data, so we flattened and reshaped the data to make it fit into the model we chose to use.

## Accomplishments that we're proud of
Despite the lack of theoretical knowledge behind network theory nor much of financial theory needed to judge financial stability, we managed to come up with a data processing and modelling technique that managed to identify some anomalies during the European sovereign debt crisis. We are proud of the fact that we came up with a way to structure the data into an adjacency matrix (without knowledge of its existence before). Although some limitations were identified, it was seen that it was still competent in identifying some signals regarding the crisis and also managed to identify which country had the anomalous change. As such, we are satisfied with the overall performance of this project, although we essentially started from scratch in terms of theoretical knowledge.



## What we learned
This 24-hour project gave ample opportunities for us to research deeply in how unsupervised learning models function. We were introduced to many new statistical and ML concepts, to not only make sure that the model had been implemented correctly, but also to evaluate whether its results made sense and could be interpreted. 

This project also helps to refine substantially our data processing and manipulation skills. We realised that this had been one of the most demanding parts of the process, which required a high fluency in various libraries. We were also very surprised by how useful mathematical and spatial reasoning had been, especially when we tried to locate the quarter and the order that a country was in given its location on the bigger array.
 
Also, it was very surprising to see that the more the problem was examined, the more complicated it became. There seemed to be an endless amount of factors that could be considered. Meanwhile, it was a huge challenge trying to change our original data, let alone trying to incorporate other signals into the network. As such, we learned that many problems tend to be more complex than they seem and as such require more inspection along with trial and error. We learned that we will need to keep this fact in mind when partaking in other interesting projects in the future.

## What's next for FNA: Anomaly Detector
There are many areas of improvement for this project. The first priority would be to find a way to incorporate other signals into the network. For example, the network could incorporate other macroeconomic data such as GDP and other ratios to create a more robust anomaly detection algorithm. As the priority would be to give reliable predictions to financial instability for a safer and more efficient system, the model would have to be fine tuned so that less false signals can be given. A false signal may be highly detrimental to the financial system as costly actions may be taken based on a bad signal. Finally, more theoretical knowledge in applying network theory to financial stability would be helpful to the project. 
