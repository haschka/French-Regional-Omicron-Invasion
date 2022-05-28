# French-Regional-Omicron-Invasion
Aggregated Data Simulating French Regional Omicron Invasion

If you use this please cite ??? 

In here you find the calculated R, reproduction rates, on a regional level during SARS-CoV-2 Omicron invasions in France.

The values are calculated according to our [model](https://github.com/haschka/SIER_multivariant_epidemic): In the [regiontables folder](https://github.com/haschka/French-Regional-Omicron-Invasion/tree/main/regiontables) three files are given for
each parameterset named 
```
datasettype-generationtime-epsilon-preinfected-{rzero,error,onset}`
```
where:
### datasettype 
is either C1 in case where Omicron is indicated if the mutation E484K is absent,
or D1 if Omicron is indicated by the mutations: 
deletion of site 69/70 and/or K417N and/or S371L-S373P and/or Q493R

### generationtime 
The generation time in days for Omicron, either 3, 3.5 or 4 days.
Delta is always fixed to 5 days.

### epsilon
The cross immuity assumed between Delta and Omicron. This value indicates how much protection against an infection by the other variant is obtained by infection with one variant.

### preinfected
The fraction of the population that is assumed to be immune against Delta at the onset of the calculation.

### rzero, error, onset
The file type:
- rzero holds 4 columns, the first is the region code indicator, the second the R value for the delta variant ( intepolated from data ), the third the R value calculated for the Omicron Variant and the fourth column holds the R value of other registered variants in the timeframe (negligable)
- error holds 2 columns, the first column is the region code indicator, the second the absolute fit error. 
- onset holds 2 columns, the first column is the region code indicator, the second the number the day of december 2021 used as a start for the 20 day R calculation window.

French region codes are given as follows:
```
84      Auvergne-Rhône-Alpes
32      Hauts-de-France
93      Provence-Alpes-Côte d'Azur
44      Grand Est
76      Occitanie
28      Normandie
75      Nouvelle-Aquitaine
24      Centre-Val de Loire
94      Corse
27      Bourgogne-Franche-Comté
53      Bretagne
52      Pays de la Loire
11      Ile-de-France
1       Guadeloupe
2       Martinique
3       Guyane
4       La Réunion
6       Mayotte
5       Saint-Pierre-et-Miquelon
7       Saint-Barthélemy
8       Saint-Martin
```
