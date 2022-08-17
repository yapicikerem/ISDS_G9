# ISDS_G9
Introduction to Social Data Science (Group 9)

Last updated: 17-08-2022

To do list:

1. Latex dokument
	- Ift. hvordan vi skal skrive - short and to the point --> vi skal ikke skrive ligesom de gør i exam project, som Tobias har lagt op.
	- Fiks titel
	- Fiks sprog til engelsk, så der kommer til at stå abstract i stedet for resumé, og contents i stedet for indholdsfortegnelse
	- Vi skal have abstract :D (jeg skal nok skrive et lynhurtigt)
	- Jeg synes vi skal have gruppemedlemmer for forside (med eksamensnumre) - hvad tænker I?

2. Datarens
	- Nævne inflationsjusteringen og muligvis gå med data fra '09 og frem grundet paradigmskfite på boligmarkedet
	- Lav en tabel med NaN's for hver variable (bindestreg benyttes i data som NaN). Lav det derudover som andele af totalen
	- Kig på dupliketter. Dette er relevant for adresse-variablen (70 stks ca.)
	- Kategoriske variable skal justeres, så de passer til ML algoritmer.
	- JUSTER SQMPRICES MED CPI FØR VI FJERNER OUTLIERS!
	- Bliv lige sikker på, at de laveste salgspriser vi inkluderer er reasonable - tjek husspecfikiation for nogle af de billigste huse

Ekstra data:
	- CPI data skal merges ind i main-data (2022-justeret). Data fra 1980-2022
		- left merge på måned og år

3. Deskriptiv
    - TAG LOG AF SQMPRICES FØR DER LAVES SCATTER PLOTS OG KORRELATION PLOTS
    - Missing value plots a la Kaggle plot, som et bar-plot! Link: https://www.kaggle.com/code/donaldst/stackingandensembling
    - Scatter plots i lower triangle form, hvor yderste plot er et density plot (gerne med density curve udover bins'ene i histogrammet)
    - Boxplot af outliers (synes måske vi skal droppe det her når vi har så mange datapunkter - tror ikke det er super egnet)
    - Heat-Geo map for priser baseret på område
    - Correlation plots (se, om det også virker med kategoriske variable)
    - Yearly avg. of sqmPrice over time (both with and without adjusted for CPI) - plot after outliers have been removed.

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
            - renter (optional)
    - Lave pandas 'bins' til at kategorisere de forskellige variable indenfor de respektive geografiske områder

Machine Learning - OLS, LASSO, Ridge, Random forest og XGBOOST:
    - Feature selection for baseline model by correlation plots (uden geografiske features)
    - Polynomial feature selection by scatter plots (for OLS, LASSO, Ridge)
    - Train/validation/test split with test data being most recent (overvej at undersøge backtesting)
    - Standardize data wrt. training data for LASSO and Ridge to prevent data leakage
    - Find reference article for rule of thumb for train/test split depending on no. of observations
    - Smid reference til 'Statistical paradises and paradoxes' ift. sample selection
    - Smid reference om importance af i.i.d. assumption i relation til theory of generalization --> Vapnik–Chervonenkis theory (dette er den mest kendte teori der basically stater assumptions, hvorunder supervised ML algoritmer kan generalisere, i.e. have god out-of-sample performance)
    - Overvej train/validation/test split for Lasso og Ridge ift. at finetune hyperparameters (find referencer ift. rule of thumbs).
    - Repeat above med udvidet model including geospatial measures

Grundlag for data:
    - Boliga.dk
    - Københavns kommunes open data
    - Danmarks Statistik

Arbejdsfordeling:
    - HC: Geodata
    - Julius: ML
    - Kerem: Datarens
