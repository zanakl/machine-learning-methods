# Analiza podataka i primjena metoda strojnog učenja 

Projekt iz kolegija *Uvod u analizu podataka* koji obuhvaća primjenu različitih metoda strojnog učenja na više skupova podataka.

## O projektu

U sklopu zadaće provedene su tri vrste analize:

1. **linearna regresija** na skupu podataka Palmer Penguins
2. **klasifikacija** pomoću stabla odlučivanja na skupu Palmer Penguins
3. **klasteriranje** pomoću KMeans algoritma na skupu USArrests

Cilj je primijeniti različite metode analize podataka, validirati dobivene modele te interpretirati rezultate.

## 1. Linearna regresija – Palmer Penguins

Korišten je skup podataka **Palmer Penguins**, koji sadrži biometrijske podatke o trima vrstama pingvina:

* Adelie
* Gentoo
* Chinstrap

Analizirane su varijable poput duljine kljuna, dubine kljuna, duljine peraje, tjelesne mase i spola.

U regresijskom dijelu ispituje se odnos između:

* `flipper_length_mm` – duljina peraje
* `body_mass_g` – tjelesna masa

### Metode

* Linear Regression
* train/test split
* R²
* RMSE
* 5-fold cross-validation

Rezultati pokazuju linearnu povezanost između duljine peraje i tjelesne mase. Cross-validation dodatno se koristi za procjenu stabilnosti modela na različitim podjelama podataka.

## 2. Klasifikacija – Palmer Penguins

U drugom dijelu izrađen je klasifikacijski model koji na temelju biometrijskih značajki predviđa vrstu pingvina.

Korištene značajke su:

* `bill_length_mm`
* `bill_depth_mm`
* `flipper_length_mm`
* `body_mass_g`

Ciljna varijabla je:

* `species`

### Model

Za klasifikaciju je korišten **Decision Tree Classifier**.

Model je podijeljen na trening i testni skup, nakon čega je njegova uspješnost procijenjena pomoću:

* accuracy
* precision
* recall
* F1-score
* classification report

Također je analizirana važnost pojedinih značajki u procesu klasifikacije.

Dobiveni model ostvaruje približno **97 % točnosti** na testnom skupu.

## 3. Klasteriranje – USArrests

Za klasteriranje je korišten skup podataka **USArrests**, koji sadrži podatke za 50 saveznih država SAD-a iz 1973. godine.

Varijable uključuju:

* `Murder`
* `Rape`
* `Assault`
* `UrbanPop`

### Standardizacija

Budući da se varijable nalaze na različitim skalama, podaci su standardizirani pomoću `StandardScaler`.

### PCA

Primijenjena je analiza glavnih komponenti (PCA) radi redukcije dimenzionalnosti.

Dvije glavne komponente zadržavaju više od **85 % ukupne varijance**, što omogućuje prikaz podataka u dvodimenzionalnom prostoru uz zadržavanje većine informacija.

### KMeans

Za određivanje broja klastera korištena je **elbow metoda**.

Na temelju grafa inercije odabran je broj od **4 klastera**.

Dobiveni klasteri zatim su vizualizirani u prostoru prvih dviju glavnih komponenti zajedno s njihovim centroidima.

## Korištene tehnologije

* Python
* Jupyter Notebook
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* PyDataset

## Datoteke

* `Klasic_dz2.ipynb` – Jupyter Notebook s kompletnom analizom

