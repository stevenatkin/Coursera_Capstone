# Business Trends in Areas Surrounding Community Colleges

## Introduction

With the rising cost of tuition many students are gravitating to community colleges and 
certificate based learning programs that are more affordable than traditional four year programs. With this in mind, many students are relocating to some of the fastest growing cities to both meet long term career goals and improve their short term job prospects as many students frequently require a source of income during their studies.

This shift in learning and migration represents opportunities for businesses to provide goods and services that are in close proximity to community colleges to meet the needs of students. Many of these needs are similar to students in traditional college programs, though some may be more specifically aligned to community college students and part-time students. To identify these potential business opportunities the three fastest growing US cities<sup>[1](#uscensus)</sup> (Phoenix Arizona, San Antonio Texas, and Dallas Fort Worth Texas) and associated community colleges are studied.

Each of the surrounding areas in close proximity to community colleges within these cities are analyzed to discern the types of businesses that have been established, and the demographics of the students attending these schools. This analysis reveals the types of businesses that may be suitable in other cities that are in close proximity to community colleges that have yet to experience the same level of rapid growth.

## Intended Audience
This paper's research is intended for small to medium size business owners looking to identify and establish suitable types of business venues in areas that are in close proximity to community colleges.

## Data and Research Methodology

This paper uses data from Foursquare<sup>[2](#foursquare)</sup>, Mapbox<sup>[3](#mapbox)</sup>, and The National Center for Education and Statistics<sup>[4](#nces)</sup> 
to generate insights, identify patterns, and uncover business trends in close proximity to community colleges within Phoenix Arizona, San Antonio Texas, and Fort Worth Texas. Clustering techniques and map visualization is applied to segment and cluster businesses within each of the surrounding community college areas to better understand their similarities and differences. 

### Sample Foursquare Data
Some of the types of data from Foursquare that will be analyzed include restaurants as shown in Fig. 1.

![alt text](https://github.com/stevenatkin/Coursera_Capstone/blob/master/venue_data.png?raw=true)

*Fig. 1: Foursquare restaurants near campus*

## Data Analyzed

#### Community College Data

To identify the list of community colleges, geographic locations, enrollment data, and demographic information the Integrated Postsecondary Education System (IPEDS) from the National Center for Education and Statistics data set for 2018-2019 was examined and filtered by respective location. To identify the neigborhoods that each school was located in the Mapbox service was used to geolocate the school's physical neigborhood. When such data was unavailable the name of the city was used instead. The list of schools for each city can be found in Fig. 2, Fig. 3, and Fig. 4 with their respective locations and student demographic data. 

![san_antonio_schools](https://github.com/stevenatkin/Coursera_Capstone/blob/master/san_schools.png?raw=true)

*Fig. 2: San Antonio Schools*

![phx_schools](https://github.com/stevenatkin/Coursera_Capstone/blob/master/phx_schools.png?raw=true)

*Fig. 3: Phoenix Schools*

![dfw_schools](https://github.com/stevenatkin/Coursera_Capstone/blob/master/dfw_schools.png?raw=true)

*Fig. 4: Dallas Fort Worth Schools*

#### Surrounding Venue Data

To determine the surrounding venues for each school the Foursquare service was used to locate the 50 nearest businesses within a 5,000 meter radius. Sample data of the venues are shown in Fig. 5, Fig 6, and Fig 7.

  ![san_venues](https://github.com/stevenatkin/Coursera_Capstone/blob/master/san_venues.png?raw=true)

*Fig. 5: San Antonio Venues*

![phx_venues](https://github.com/stevenatkin/Coursera_Capstone/blob/master/phx_venues.png?raw=true)

*Fig. 6: Phoenix Venues*

![dfw_venues](https://github.com/stevenatkin/Coursera_Capstone/blob/master/dfw_venues.png?raw=true)

*Fig. 7: Dallas Fort Worth Venues*

## Research Methodology

#### Student Enrollment and Demographic Analysis

To get a better sense of the demographic distribution of the students in each city, simple bar charts were constructed that aggreagated all student enrollment data in each respective city as shown in Fig. 8, Fig 9, and Fig 10.

 ![san_enrollment](https://github.com/stevenatkin/Coursera_Capstone/blob/master/san_enrollment.png?raw=true)

*Fig. 8: San Antonio Enrollment*



![phx_enrollment](https://github.com/stevenatkin/Coursera_Capstone/blob/master/phx_enrollment.png?raw=true)

*Fig. 9: Phoenix Enrollment*

![dfw_enrollment](https://github.com/stevenatkin/Coursera_Capstone/blob/master/dfw_enrollment.png?raw=true)

*Fig. 10: Dallas Fort Worth Enrollment*

#### Venue Grouping and Preparation for Clustering

To aid in identfying similarities and differences in the types of venues surrounding community colleges clustering analysis was performed. Unsupervised learning using the K-means algorithm was utilized to cluster the venues. The K-Means algorithm is one of the most frequently used methods of unsupervised learning. 

To properly cluster the venues they needed to be one hot encoded as the venues represented categorical data. After the data was one hot encoded it was grouped in preparation for clustering analysis, as shown in Fig. 11, Fig. 12, and Fig. 13.

![san_grouping](https://github.com/stevenatkin/Coursera_Capstone/blob/master/san_grouping.png?raw=true)

*Fig. 11: San Antonio Venues One Hot Encoded and Grouped*

![phx_grouping](https://github.com/stevenatkin/Coursera_Capstone/blob/master/phx_grouping.png?raw=true)

*Fig. 12: Phoenix Venues One Hot Encoded and Grouped*

![dfw_grouping](https://github.com/stevenatkin/Coursera_Capstone/blob/master/dfw_grouping.png?raw=true)

*Fig. 13: Dallas Fort Worth Venues One Hot Encoded and Grouped*

#### Determining Optimal Cluster Sizes

Prior to performing clustering of the venue data the data had to be analyzed using the sillhouette method to determine the optimal cluster sizes. The cluster sizes and their respective scores were plotted to easily identify the optimal number of clusters for each city as shown in Fig. 14, Fig. 15, and Fig. 16.

![san_score](https://github.com/stevenatkin/Coursera_Capstone/blob/master/san_score.png?raw=true)

*Fig. 14: San Antonio Optimal Cluster Size*

![phx_score](https://github.com/stevenatkin/Coursera_Capstone/blob/master/phx_score.png?raw=true)

*Fig. 15: Phoenix Optimal Cluster Size*

![dfw_score](https://github.com/stevenatkin/Coursera_Capstone/blob/master/dfw_score.png?raw=true)

*Fig. 16: Dallas Fort Worth Optimal Cluster Size*

### Results and Discussion

#### Clustering

To cluster the venues the cluster sizes obtained from the silhouette method for each city was used as input to K-Means clustering. The data was then grouped by cluster and the top 5 venue categories were displayed as shown in Fig. 17, Fig. 18, and Fig. 19.

![san_clusters](https://github.com/stevenatkin/Coursera_Capstone/blob/master/san_clusters.png?raw=true)

*Fig. 17: San Antonio Clusters*

![phx_clusters](https://github.com/stevenatkin/Coursera_Capstone/blob/master/phx_clusters.png?raw=true)

*Fig. 18: Phoenix Clusters*

![dfw_clusters](https://github.com/stevenatkin/Coursera_Capstone/blob/master/dfw_clusters.png?raw=true)

*Fig. 16: Dallas Fort Worth Clusters*

Examing the results of clustering reveals four distinct clusters in San Antonio and Phoenix and eight clusters in Dallas Fort Worth. When examining the clusters for each city more closely some obvious similarities emerge. 

We find that in the case of community colleges in San Antonio the clusters are largely defined by the venue categories Coffee Shops and Mexican Restaurants. When we look at Phoenix we see a similiar pattern especially for Mexican Resturants, but the other clusters are not as distinct as what was observed in San Antonio and certainly there is no cluster that is uniquely defined by the presense of Coffee Shops. When we examine the community colleges in the Dallas Fort Worth area we find a greater number of clusters some of which are different from what was observed in San Antonio and Phoenix. Specifically, the clusters that are defined by Breweries and Burger Joints, yet we do see clusters that are defined by the presense of Mexican Resturants as was observed in San Antonio.

#### Geospatial Locations of Colleges

To gain additional insight and to better undertsnad the clusters each community college was placed on a map with its assigned cluster, as shown in Fig. 17, Fig. 18, and Fig. 19.

![san_map](https://github.com/stevenatkin/Coursera_Capstone/blob/master/san_map.png?raw=true)

*Fig. 17: San Antonio Map*

![phx_map](https://github.com/stevenatkin/Coursera_Capstone/blob/master/phx_map.png?raw=true)

*Fig. 18: Phoenix Map*

![dfw_map](https://github.com/stevenatkin/Coursera_Capstone/blob/master/dfw_map.png?raw=true)

*Fig. 16: Dallas Fort Worth Map*

Examing the locations of each of the schools in relation to each other explains some of the diversity of the clusters across these cities. Clearly, as schools become physically closer to each other some amount of natural overlap occurs as well as these locations becoming hubs for more businesses to operate given the much larger density of students. Additionally, some of the specific types of clusters are possibly more closely aligned to the demographic preferences of both the students and the region in general. In this case two of the cities are located in Texas and one in Arizona so the results may be somewhat skewed towards general trends of the US Southwest.  

### Conclusion

Examing the types of businesses in close proximity to community colleges reveals that businesses catering to providing meals such as Mexican Resturants and places where students can study such as Coffee Shops and Cafes are highly popular businesses. In some regions there could be some amount of oversaturation of certain venue types in highly competitive markets and may not represent an opportunity for investment, while other types of venues may offer better opportunities with less competition. 

More study is still required to better determine which businesses have a high likelyhood of success around community college campuses. Other factors that would need to be explored include: construction and leasing costs, labor rates, and the general socio-economic conditions of the perspective markets.  

### Jupyter Notebook

To see the complete data, algorithms, and code used to complete this analysis see the live notebook on [Nbviewer](https://nbviewer.jupyter.org/github/stevenatkin/Coursera_Capstone/blob/master/capstone.ipynb) and [GitHub](https://github.com/stevenatkin/Coursera_Capstone).

### References 

<a name="uscensus" href="https://www.census.gov/newsroom/press-releases/2019/subcounty-population-estimates.html">
1: US Census &mdash; Fastest-Growing Cities</a>  

<a name="foursquare" href="https://foursquare.com/city-guide">
2: Foursquare City Guide</a>

<a name="mapbox" href="https://www.mapbox.com">
3: Mapbox Location Data</a>

<a name="nces" href="https://nces.ed.gov">
4: National Center for Education and Statistics</a>


