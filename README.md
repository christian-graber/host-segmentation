<h1 align="center">This is why hosting on Airbnb doesn't have to be a fit for you.</h1>

## Table of contents

- [Installations](#installations)
- [Project Motivation](#project-motivation)
- [File Descriptions](#file-descriptions)
- [Summary of Results](#summary-of-results)
- [Acknowledgement](#acknowledgement)

## Installations

- numpy
- pandas
- matplotlib
- seaborn
- scikit-learn
- pyclustertend

## Project Motivation

I like the idea of sharing your home by short-term rental services like Airbnb. Unfortunately, my personal experience is ambiguous. Airbnb's service has allowed me to make good money and I've met a lot of great people. Unfortunately, I found the support from Airbnb to be very excessive. I didn't have the feeling that my person or rather my use case was in demand and I therefore decided to use another service. A brief research on the internet showed that it's not just me, but that there are other hosts who have had similar experiences. This analysis isn’t sufficient and therefore it can't be conclusively. It's meant to be food
for thought that customers aren't only the people looking for a stay, but
also the hosts of such services. Furthermore, I wanted to show that there is no one perfect host, but that there are many different types of hosts, all of which are valued.


## File Descriptions

Within the project you'll find the following files:

<details>
  <summary>Contents</summary>

  ```text
  host-segmentation/
  ├── README.md
  └── 221209_Project_Host-Segmentation.ipynb: Jupyter notebook used for Gathering, Assessment, Cleaning, Explorative Data Analysis and Visualization.

  ```
</details>


## Summary of Results

- Data Gathering.
    - Boston: https://www.kaggle.com/datasets/airbnb/boston
    - Seattle: https://www.kaggle.com/datasets/airbnb/seattle
- Data Assessment.
    - Datasets 'listings.csv' contains all necessary features and is therefore sufficient for data analysis.
    - The dataset is messy and contains untidy data (see 221209_Project_Host-Segmentation.ipynb).
- Data Cleaning (see 221209_Project_Host-Segmentation.ipynb).
- Data Modelling.
    - Dimensionality reduction by means of principal components analysis from 25 features to 12 components by keeping ~96% of explained variance.
    - Assessing Clustering Tendency.
        - Hopkins Statistic: Positiv test result (a hopkins score of 0.03), that means ...
            - The data isn't randomly/uniformly distributed.
            - Clustering can be meaningful for grouping the observations. 
        - Determination of Number of Clusters by Elbow Method.
            - No distinct elbow.
            - Number of clusters for further analysis: 9.
    - Clustering by k-means algorithm.
      <table>
      <tbody>
      <tr>
      <td>Cluster ID</td>
      <td>Proportion of Observations [%]</td>
      </tr>
      <tr>
      <td>0</td>
      <td>10.6</td>
      </tr>
      <tr>
      <td>1</td>
      <td>9.5</td>
      </tr>
      <tr>
      <td>2</td>
      <td>9.5</td>
      </tr>
      <tr>
      <td>3</td>
      <td>8.2</td>
      </tr>
      <tr>
      <td>4</td>
      <td>9.9</td>
      </tr>
      <tr>
      <td>5</td>
      <td>10.4</td>
      </tr>
      <tr>
      <td>6</td>
      <td>14.8</td>
      </tr>
      <tr>
      <td>7</td>
      <td>15.1</td>
      </tr>
      <tr>
      <td>8</td>
      <td>12.0</td>
      </tr>
      </tbody>
      </table>
    - Explorative Data Analysis
        - It exist meaningful groups within the available data with different properties.
        - Review Scores Rating by customers isn't significantly affected by these differences. That means, there is no one perfect host.


## Acknowledgements

- Airbnb: for providing listings data.
- Udacity: for teaching data analytics.
