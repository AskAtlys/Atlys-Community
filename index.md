# Welcome to the Atlys Community Dashboard

### Overview
This is a public repository to store data contributed anonymously by citizens in an effort to crowdsource information about communities' health status and reported symptoms. Data is contributed via the [Atlys mobile app](https://play.google.com/store/apps/details?id=com.askatlys) and sent to a Mongo database before being exported to an AWS S3 bucket. New dataset files are manually exported from S3 and uploaded to this repository daily. This repository is maintained by [Atlys Networks](https://www.atlys.ca) but all data files are publicly open for researchers, analysts, and organizations to download and use.

### Acknowledgements
We want to thank all individuals who have been willing and able to anonymously contribute data about their symptoms and health status.

### Datasets

#### ext_contributions.csv
- _id
- date
- lon
- lat
- randkey
- status
- label
- count

#### agg_symptoms.csv
- _id
- date
- lon
- lat
- country
- state
- city
- postal
- label
- count

#### agg_status.csv
- _id
- date
- country
- state
- city
- postal
- status
- count


#### ref_regions
- _id
- region
- country
- state
- city
- postal
- lon
- lat


#### ref_randkeys
- _id
- date
- randkey
- country
- postal

#### ref_blacklist
- _id
- date
- randkey
- flag
