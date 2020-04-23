# How does medicines travel around the world

**Please read my [blog post](https://medium.com/@soniyajain_40637/how-medicines-travel-around-the-world-e797afd0c17b) for the detailed analysis and conclusions about this project. I am giving below a short snippet from my blog post.**

Have you ever wondered where does your medicines comes from? Who else consumes the same branded medicines as you do? Well, I had!  

In this project, I am analysing how diverse is the market concentration of importing countries for the medicines exported by each country. 

About dataset:

I sourced the 2019 dataset from Trademap for my analysis. The dataset contains 9 different export related variables for 207 countries.  I am using 3 variables listed below:

1.	Share in world exports (%): Share of each country in worldwide exports for 2019. There were 155 countries having zero share in exports. Thus, these countries were removed to reduce noise, thereby leaving 52 countries for accurate analysis.

2.	Market concentration of importing countries: It represents the distribution of market share of medicines among importers. The concentration index is ranged between 0 and 1. Higher index indicates that imports are focused in fewer countries whereas lower index indicates more fair distribution of market share among importers. 

For example, Denmark has 0.74 market concentration of importing countries. This mean Denmark exports medicines to fewer countries. On the contrary, Germany has 0.07 market concentration of importing countries. This means Germany exports its medicines to many countries, enabling its importers to have a fair market share of medicines.

3.	Exporters [ values]: Export Country names.

Analysis:

For my analsysis, I am running linear regression model to see relationship between Market concertation (dependent variable) and World share (independent variable). Detailed analysis is done in this [notebook](https://github.com/jainsoniya/How-does-medicines-travel-around-the-world/blob/master/data_preprocessing_and_analysis.ipynb)

Conclusion:

Overall, the market concentration is low among importing companies for exported medicines. This means the medicines exported are fairly distributed among the importing countries. However, if we segregate the countries to large and small exporters, the market concentration tends to increase with the increase in export share. It means that the exported medicines are distributed to fewer countries.

Further, the large exporters fairly distribute their medicines to the whole world. However, small exporters exports to limited regions. This is a matter of concern as the fate of these small exporters are dependent on those limited importers. One way of reducing such dependency is promote export diversification. [This](https://www.undp.org/content/dam/undp/library/Poverty%20Reduction/Inclusive%20development/Towards%20Human%20Resilience/Towards_SustainingMDGProgress_Chapter1.pdf) research paper explains beautifully the interaction between export dependence and export concentration, and ways to reduce export dependency

Now that you know how medicines travel around the world, fell free to visit my [interactive dashboard](https://public.tableau.com/profile/soniya4758#!/vizhome/Wheredoesyourmedicinecomesfrom/Dashboard2) to see how medicines traveled from your country.

Source:
1.[trademap](https://www.trademap.org/Country_SelProduct.aspxnvpm=1%7c%7c%7c%7c%7cTOTAL%7c%7c%7c2%7c1%7c1%7c2%7c1%7c%7c2%7c1%7c)
2.[howto](https://howmuch.net/articles/world-map-of-drug-exports-2016)

Resources:
1. [wikipedia](https://en.wikipedia.org/wiki/Market_concentration)
2. [World Bank](https://datacatalog.worldbank.org/import-product-concentration-index)
3. [unctad](https://unctadstat.unctad.org/EN/IndicatorsExplained.html)
