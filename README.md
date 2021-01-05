# COVID-datasets

Include 6 different datasets from different data sources (denoted below) for different research purposes. Basically, the datasets include information from 391 different counties in USA at a fixed time or in a series of time periods.

## Confirmed cases across counties
Clawed from [Johns Hopkins Cronavirus Resource Center](https://coronavirus.jhu.edu/map.html). Data includes confirmed cases and death from Jan. to Aug. as time series. County number is 391 in total. For each date, there would be one column for confirmed cases and the other column for death cases.


## Distance matrix across counties
Pre-processed file *sf12010countydistancemiles* from [County Distance Database](https://www.nber.org/research/data/county-distance-database). Matrix is 391 * 391, includes the distance of every county pair.


## Google Trend topics across counties
Clawed and pre-processed from [Google Trend](https://trends.google.com/trends/?geo=US). Counties are 391 in total, and daily topics' populatity scores are preserved as time series from Feb. to Oct. We utilize the popularity score of the corresponding state if the score of the specific countuy does not exist. Topics include 
| Topics     |Topics      |Topics      |
| :----------: | :-----------:  | :-----------: |
| covid     | mask    | epidemic   |
| symptom   | quarantine    | social distance    |
| corona virus    | Pandemic  | Hand hygiene  |
| Shelter-in-place order | Self-isolation  | Drive-thru testing  |
| Self-monitoring  | Anti-viral medicines   | Personal protective equipment  |
| N95 respirator | Vaccine  | Ventilator  |
| Centers for Disease Control and Prevention  |  |  |

————**Update Jan. 2021:** Google Trend data of Nov. and Dec., 2020 has been uploaded.


## Population mobility across counties
Clawed and pre-processed from [COVID19USFlows](https://github.com/GeoDS/COVID19USFlows). Counties are 391 in total, and mobility data is preserved from Feb. to Oct.  as time series.

## Toy dataset of Google Trend
Clawed and pre-processed from [Google Trend](https://trends.google.com/trends/?geo=US). Counties are 391 in total. We utilize the popularity score of the corresponding state if the score of the specific countuy does not exist. Compared with **Google Trend topics across counties**, this is a small toy dataset, which only includes topics' populatity scores of a fixed time period (). Topics include 
| Topics     |Topics      |Topics      |
| :----------: | :-----------:  | :-----------: |
| covid     | mask    | epidemic   |
| symptom   | quarantine    | social distance    |
| corona virus    | Pandemic  | Hand hygiene  |
| Shelter-in-place order | Self-isolation  | Drive-thru testing  |
| Self-monitoring  | Anti-viral medicines   | Personal protective equipment  |
| N95 respirator | Vaccine  | Ventilator  |
| Centers for Disease Control and Prevention  |  |  |


## Twitter bipartite graph
Clawed and pre-processed from [Twitter](https://twitter.com). We firstly collected 54 official accounts who have posted COVID19 related information. Then we claw top followers of them, and compute a "COVID attention score" for followers' counties. Counties are 391 in total. "COVID attention score" is computed as 
<img src="http://chart.googleapis.com/chart?cht=tx&chl= $f(\mathcal{X}) = \sum_{i=1}^{N} e^{-x}$" style="border:none;">， where N here denotes the total number of the followers in a county, and x here denotes the average post interval time (days) of a follower's recent 20 (or less) posts. We directly use 0 to denote followers with only 1 post or no post.










