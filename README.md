# ISDS_G9
Introduction to Social Data Science (Group 9)

Last updated: 15-08-2022

To do list:

1. Latex dokument

2. Datarens
	- Nævne inflationsjusteringen og muligvis gå med data fra '09 og frem grundet paradigmskfite på boligmarkedet
	- Lav en tabel med NaN's for hver variable (bindestreg benyttes i data som NaN). Lav det derudover som andele af totalen
	- Vi kan muligvis interpolere over variable, hvis der er NaN's i variabel vi gerne vil bruge
	- Kig på dupliketter. Dette er relevant for adresse-variablen (70 stks ca.)

Ekstra data:
	- CPI data skal merges ind i main-data (2022-justeret). Data fra 1980-2022
		- left merge på måned og år

3. Deskriptiv
    - Density plot huspriser (normalfordeling der højst ssh. er højreskæv)
    - Boxplot af outliers
    - Geo map for priser baseret på område
    - Korrelation plots (for alle variable [10 variable på nuværende tidspunkt er relevante])

4. Analyse:
    - Lav measures på 
            - metro
            - ladestationer
            - afstande til kyst
            - parker
            - vurdering af skoler (karaktergennemsnit) 
            - Støjniveau
            - luftforurening
            - restaurenter, fastfood/take-away
            - grønne arealer (træer)
            - (overvej om andre er relevante)
    - Lave pandas 'bins' til at kategorisere de forskellige variable indenfor de respektive geografiske områder

Fremgangsmetode:
    - Baseline model (uden geografiske features)
        - OLS, lasso, Rainforest og SGBOOST
    - Udvidet model (f.eks. afstanden til ladestandere og vand om hvorvidt det kan påvirke pris)

Grundlag for data:
    - Boliga.dk
    - Københavns kommunes open data
    - Danmarks Statistik

Arbejdsfordeling:
    - HC: Geodata
    - Julius: ML
    - Kerem: Datarens