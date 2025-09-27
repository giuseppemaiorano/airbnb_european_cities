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
