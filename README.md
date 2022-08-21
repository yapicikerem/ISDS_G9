# ISDS_G9
Introduction to Social Data Science (Group 9)

Last updated: 17-08-2022

To do list:

FIND LØSNING PÅ HVORDAN VI SÆTTER JUPYTER NOTEBOOK OP IFT. INDLÆSNING AF FILER - der må være en smart måde at gøre det på.

Hvis vi har tid:
	- Dokumenter koden
	- Diskussion - nævne makroøkonomiske variable, der kan være relevante for at prædiktere husprisen

1. Latex dokument
	- Ift. hvordan vi skal skrive - short and to the point --> vi skal ikke skrive ligesom de gør i exam project, som Tobias har lagt op.
	- Fiks titel
	- Fiks sprog til engelsk, så der kommer til at stå abstract i stedet for resumé, og contents i stedet for indholdsfortegnelse
	- Vi skal have abstract :D (jeg skal nok skrive et lynhurtigt)
	- Jeg synes vi skal have gruppemedlemmer for forside (med eksamensnumre) - hvad tænker I? (done (KY) - 18-08-2022)


3. Deskriptiv
    - TAG LOG AF SQMPRICES OG DEFLATÉR FØR DER LAVES SCATTER PLOTS OG KORRELATION PLOTS - NÆVN I OPGAVE

5. Machine Learning - OLS, LASSO, Ridge, Random forest og XGBOOST:
    - Feature selection for baseline model by correlation plots (uden geografiske features)
    - Polynomial feature selection by scatter plots (for OLS, LASSO, Ridge)
    - Train/validation/test split with test data being most recent (overvej at undersøge backtesting)
    - Standardize data wrt. training data for LASSO and Ridge to prevent data leakage
    - Find reference article for rule of thumb for train/test split depending on no. of observations
    - Smid reference om importance af i.i.d. assumption i relation til theory of generalization --> Vapnik–Chervonenkis theory (dette er den mest kendte teori der basically stater assumptions, hvorunder supervised ML algoritmer kan generalisere, i.e. have god out-of-sample performance)
    - Smid reference til 'Statistical paradises and paradoxes' ift. sample selection
    - Overvej train/validation/test split for Lasso og Ridge ift. at finetune hyperparameters (find referencer ift. rule of thumbs).
    - Repeat above med udvidet model including geospatial measures
    - Lav learning curves for at vurdere vigtighed af sample length.
    - Find ud af hvilken løsningsform sklearn package bruger til OLS - SGD eller closed-form eller tredje? Skriv om det i opgave
    - Page 329 ift. inverse_transform efter standardisering - anvend evt. exp() funktion på log(sqmPrices) for original skala.

Grundlag for data:
    - Boliga.dk
    - Københavns kommunes open data
    - Danmarks Statistik

Arbejdsfordeling:
    - HC: Geodata
    - Julius: ML
    - Kerem: Datarens
