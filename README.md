# Case Disposition Inefficiency in North Carolina

The scope of this project is to observe potential factors affecting the efficency of North Carolina's judicial system and focuses primarily on criminal matters.  For the sake of data analytics, I will define efficiency as the ***case disposition efficiency***, or the ratio of the ***number of cases disposed*** to ***number of pending cases*** with respect to all felony cases of violent crimes (rape and sexual assault, robbery, assault, murder).  All data provided is county level for the 2012-2018 fiscal years (FY).  I will use several features compiled from different datasets to create a machine learning model that will perform the following tasks:

- *Detect potential attributes that could severely affect a county's case disposition efficiency*
- *Predict which counties may be of need for more resources as a result of case disposition insufficiency using machine learning*
- Store the results in a MySQL database
- Embed Tableau data visualizations into Jupyter Notebook


## Data Dictionary


| Column | Data Type | Description | 
| ----------- | ----------- | -----------|
| county | str | name of county |
| dist_judg_mag | int64 | number of district judges and magistrates |
| clerks | int64 | number of assistant and deputy clerks |
| dist_attys | int64 | number of district attorneys |
| p_def | int | indicates 1 if at least Public Defender, 0 no Public Defender |
| law_enf_ag | int64 | number of law enforcement agencies |
| avg_pop | int64 | average population (2012-2018) |
| avg_income | int64 | average income (2012-2018) |
| avg_num_divrs | float | average number of divorces (2012-2018)|
| vcr_per_100000 | float | average violent crime rate (2012-2018)|
| op_od_deaths | int64 | total number of opioid overdose deaths (2012-2018)|
| case_disp_ratio | float | ratio of disposed cases to end-pending cases |
| probability | float | probability of model prediction |
| prediction | int | indicates 1 if inefficient, 0 efficient |

## Requirements

- [Anaconda Individual Edition](https://www.anaconda.com/products/individual)
- Jupyter Notebook or Jupyter Lab within Anaconda
- [MySQL Server 8.0.21](https://dev.mysql.com/downloads/mysql/) or latest version
- [MySQL Workbench 8.0.21](https://dev.mysql.com/downloads/workbench/) or latest version
- [Tableau Desktop 2020.2](https://www.tableau.com/products/desktop/download) or latest version
- [Tableau online account](https://sso.online.tableau.com/public/idp/SSO)


## Installation

Install the following packages using the Anaconda terminal or search in Anaconda Navigator:

#### pandas, numpy, scikit-learn, pymysql
```
conda install -c anaconda pandas numpy scikit-learn pymysql 
```


## Data Websites

[N.C. Judicial Staff](https://www.nccourts.gov/judicial-directory?name=&contains=&field_judicial_group_target_id=All&field_county_target_id=All&field_district_target_id=All)

[Law Enforcement Agencies](http://www.cjin.nc.gov/Website%20Test%20-%20Law%20Enforcement%20Agencies%2001242015%20A-1.pdf)

[Population](https://www.osbm.nc.gov/demog/county-projections)

[Caseload Inventory](https://data.nccourts.gov/explore/?sort=modified)

[Median Household Income](https://www.huduser.gov/portal/datasets/il.html)

[Violent Crime Rate](https://ucr.fbi.gov/crime-in-the-u.s)

[Divorces](https://schs.dph.ncdhhs.gov/data/vital.cfm)

[Opioid Overdose Deaths](https://www.injuryfreenc.ncdhhs.gov/DataSurveillance/Poisoning.htm)


## Contributing

All pull requests and any suggestions to optimize code and/or model are greatly encouraged.
