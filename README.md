# airbnb_european_cities

Quick Airbnb analysis: comparison between Rome and Berlin. Python (`pandas`/`matplotlib`) on `airbnb_european-cities.csv`, with minimal cleaning and outlier trimming. Charts: median price by `room_type`, cleanliness vs satisfaction, price vs distance from the city center using binned medians, and Superhost premium. Reproducible.

## How to run

1) Place `airbnb_european-cities.csv` in the same folder as the notebook/script.
2) Open `airbnb_european_cities.ipynb` and run the cells in order, or run:

```bash
python airbnb_european_cities.py
```

The script loads the data, applies minimal cleaning by dropping missing values, removing non-positive prices, trimming the top 1% of outliers, and generates the charts for the four sections.

## What it produces

1) Median price by `room_type` bar chart – Rome/Berlin comparison.
2) Cleanliness vs satisfaction scatter plot with regression line and correlation coefficient `r` for each city.
3) Price vs distance from the city center using a scatter plot plus binned median values.
4) Superhost premium bar chart plus percentage difference printed in the console.

Tip: to save the charts, replace `plt.show()` with `fig.savefig("name.png", dpi=150)`.

## Customizations

1) Cities: edit the list `cities = ["Rome", "Berlin"]`.
2) Robustness: use `pd.qcut` for bins with similar sample sizes or `np.log1p(realSum)` to reduce the effect of outliers.
3) Segments: filter by `room_type` or compare `guest_satisfaction_overall` for Superhosts.

## Structure

`airbnb_european_cities.ipynb` – main notebook with charts and comments.
`airbnb_european_cities.py` – same logic in script format.

# airbnb_european_cities
Analisi rapida Airbnb: confronto Roma vs Berlino. Python (pandas/matplotlib) su `airbnb_european-cities.csv`, pulizia minima e taglio outlier. Grafici: prezzo mediano per room_type, pulizia vs soddisfazione, prezzo vs distanza dal centro (mediane per bin), premium dei Superhost. Riproducibile.

Come eseguire
1) Posiziona airbnb_european-cities.csv nella stessa cartella del notebook/script.
2) Apri airbnb_european_cities.ipynb ed esegui le celle in ordine oppure:
   python airbnb_european_cities.py
Lo script carica i dati, applica una pulizia minima (drop NA, rimozione prezzi non positivi, taglio del 1% più alto degli outlier) e genera i grafici delle quattro sezioni.

## Cosa produce
1) Prezzo mediano per room_type (bar chart) – confronto Roma/Berlino. 
2) Pulizia vs soddisfazione (scatter + retta, r) per ciascuna città. 
3) Prezzo vs distanza dal centro (nuvola + mediana per bin). 
4) Superhost premium (bar chart + differenza % stampata a console). 

Suggerimento: per salvare i grafici sostituisci plt.show() con fig.savefig("nome.png", dpi=150).

## Personalizzazioni
1) Città: modifica la lista cities = ["Rome", "Berlin"]. 
2) Robustezza: usa pd.qcut per bin a numerosità simile o np.log1p(realSum) per attenuare outlier.
3) Segmenti: filtra per room_type o confronta guest_satisfaction_overall per Superhost.

## Struttura
airbnb_european_cities.ipynb – notebook principale (grafici e commenti). 
airbnb_european_cities.py – stessa logica in forma di script. 
