# Welcome to the Atlys Community Dashboard

### Overview
This is a public repository to store data contributed anonymously by citizens in an effort to crowdsource information about communities' health status and reported symptoms. Data is contributed via the [Atlys mobile app](https://play.google.com/store/apps/details?id=com.askatlys) and sent to a Mongo database before being exported to an AWS S3 bucket. New dataset files are manually exported from S3 and uploaded to this repository daily. This repository is maintained by [Atlys Networks](https://www.atlys.ca) but all data files are publicly open for researchers, analysts, and organizations to download and use.

### Acknowledgements
We want to thank all individuals who have been willing and able to anonymously contribute data about their symptoms and health status.

### Datasets

#### ext_contributions.csv


column | type | notes
------------ | ------------- | -------------
_id | objectid |
date | date | 
postal | string | 
randkey | string |
status | string |
label | string |
count | integer |


#### agg_symptoms.csv

column | type | notes
------------ | ------------- | -------------
_id | objectid |
date | date | 
lon | double | 
lat | double | 
country | string | 
city | string | 
postal | string | 
label | string |
count | integer |


#### agg_status.csv

column | type | notes
------------ | ------------- | -------------
_id | objectid |
date | date | 
lon | double | 
lat | double | 
country | string | 
city | string | 
postal | string | 
status | string |
count | integer |


#### ref_regions

column | type | notes
------------ | ------------- | -------------
_id | objectid |
region | string | 
country | string | 
state | string |
city | string | 
postal | string | 
lon | double |
lat | double |

* The 'lon' and 'lat' is currently set according to:                               
  * United States: postal
  * Canada: state
  * Everywhere Else: country


#### ref_randkeys
column | type | notes
------------ | ------------- | -------------
_id | objectid |
date | date | 
randkey | string | 
country | string | 
postal | string | 


#### ref_blacklist
column | type | notes
------------ | ------------- | -------------
_id | objectid |
date | date | 
randkey | string | 
flag | string | 

* These randkeys are excluded from aggregated data sets and flagged as spam or obsolete.
