# French-Regional-Omicron-Invasion
Aggregated Data Simulating French Regional Omicron Invasion

If you use this please cite ??? 

In here you find the calculated R-zero values on a regional level during SARS-CoV-2 Omicron invasions in France.

The values are calculated according to our [model](https://github.com/haschka/SIER_multivariant_epidemic): Three files are given for
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
The generation time in days for Omicron, either 3, 3.5 or 4. Delta is always fixed to 5.

### epsilon
The inferred cross immuity assumed between Delta and Omicron. This value indicated how much protection against an infection by the other variant is obtained by infection with one variant.

### preinfected
The fraction of the population that is assumed to be immune against delta at the onset of the calculation

### rzero, error, onset
The file type:
- rzero holds 4 columns, the first is the region code indicator, the second the R_zero value for the delta variant ( intepolated from data ), the third the R_zero value calculated for the Omicron Variant.
- error holds 2 columns, the first column is the region code indicator, the second the absolute fit error. 
- onset holds 2 columns, the first column is the region code indicator, the second the number the day of december 2021 used as a start for the 20 day R_zero calculation window.
