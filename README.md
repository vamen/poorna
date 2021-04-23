# highway
Data platform that supports fast streaming of mini batches  and  fast generating reports on macro batches

**Need for the project**

Every modren day company needed a solution that allows them to pool the data from all client facing application into a wharehouse.(which grows to become bigdata) and then run  jobs on these data to generates the reports that drives the decisioning.

The typical end to end time of above mentioned process was 24hrs.

Frameworks like spark were built and pltforms like glue/hudi etc were build on top of these for this use case.Lots of independent systems intracted between each other to validate,format,clean etc and pass on data between them.

handling huge volume of data was higgher priority then the turn arround time for the report.

Days passed. decision makers were happy about the reports that helped them to make good reports, and as a natural next state decision makers become restless and they wants updated report faster with turn arround time of half an hour. 
Currents frameworks can not handle near realtimes,but engineers are worked up to achive it to save there asses. some of the folks decided to bring streming solutions on existing systems which are quite broke at the time of this writting.

The Idea of this project is to reduce **TOT** (turn arround time) by 
- Reduce independent componet.(queues,schedulers,etl jobs) and combine them into single modular project, 
- switch between Distributed computing and single system computing. (whats the point running a job in cluster with 20 nodes when data is in kbs. (this happens a lot with ancillary data associated with main data)).
- Still thinking. (Ideas are welcome and appriciated).



