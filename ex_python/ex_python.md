
# Exercice Python : Lecture d'un fichier CSV

## Lecture

Je me permets de commencer par l'import de la librairie `pandas` plutôt de `csv`. Cette librairie est réputée pour son côté pratique et se rapproche de ce qui se fait en R.


```python
import pandas as pd

# Paramétrage de l'affichage des colonnes
pd.options.display.max_columns = 99
```

L'échantillon n'étant pas encodé dans les formats par défaut (UTF-8 avec des séparateurs `,`), je précise ces éléments à la lecture du fichier CSV.


```python
data = pd.read_csv('/Users/theyanike/Documents/DataScience/TechTest/Tech4team/sample.csv', 
                   encoding='latin-1', 
                   sep=';')
data.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Numero billet</th>
      <th>Commande</th>
      <th>Reservation</th>
      <th>Date reservation</th>
      <th>Heure reservation</th>
      <th>Cle spectacle</th>
      <th>Spectacle</th>
      <th>Cle representation</th>
      <th>Representation</th>
      <th>Date representation</th>
      <th>Heure representation</th>
      <th>Date fin representation</th>
      <th>Heure fin representation</th>
      <th>Prix</th>
      <th>Date acces</th>
      <th>Heure acces</th>
      <th>Tarif</th>
      <th>Type de client</th>
      <th>Type de produit</th>
      <th>Serie</th>
      <th>Etage</th>
      <th>Filiere de vente</th>
      <th>Nom</th>
      <th>Prenom</th>
      <th>Email</th>
      <th>Adresse</th>
      <th>Code postal</th>
      <th>Pays</th>
      <th>Age</th>
      <th>Sexe</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1400222</td>
      <td>NaN</td>
      <td>843989</td>
      <td>04/06/15 00:00</td>
      <td>16:26:04</td>
      <td>476</td>
      <td>FEMME NON-REEDUCABLE</td>
      <td>3191</td>
      <td>FEMME NON-REEDUCABLE</td>
      <td>10/10/14</td>
      <td>20:00:00</td>
      <td>10/10/14</td>
      <td>22:00:00</td>
      <td>27.0</td>
      <td>10/10/14</td>
      <td>19:49:11</td>
      <td>Abonnement mouettes</td>
      <td>Client</td>
      <td>Abonnement</td>
      <td>1er Serie</td>
      <td>CORBEILLE</td>
      <td>GUICHET</td>
      <td>KEBIR</td>
      <td>Fran_ois-Jean</td>
      <td>Fran_ois-Jean.KEBIR@mail.fr</td>
      <td>7 rue des Acinonyx jubatus</td>
      <td>69110</td>
      <td>France</td>
      <td>57.0</td>
      <td>F</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1400223</td>
      <td>NaN</td>
      <td>843990</td>
      <td>04/06/15 00:00</td>
      <td>16:26:04</td>
      <td>477</td>
      <td>G©n©rale Publique Fever</td>
      <td>3204</td>
      <td>G©n©rale Publique Fever</td>
      <td>05/11/14</td>
      <td>20:00:00</td>
      <td>05/11/14</td>
      <td>21:30:00</td>
      <td>27.0</td>
      <td>05/11/14</td>
      <td>19:52:17</td>
      <td>Abonnement mouettes</td>
      <td>Client</td>
      <td>Abonnement</td>
      <td>1er Serie</td>
      <td>CORBEILLE</td>
      <td>GUICHET</td>
      <td>KEBIR</td>
      <td>Fran_ois-Jean</td>
      <td>Fran_ois-Jean.KEBIR@mail.fr</td>
      <td>7 rue des Acinonyx jubatus</td>
      <td>69110</td>
      <td>France</td>
      <td>57.0</td>
      <td>F</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1400225</td>
      <td>NaN</td>
      <td>843991</td>
      <td>04/06/15 00:00</td>
      <td>16:26:04</td>
      <td>479</td>
      <td>L'HISTOIRE TERRIBLE... 2e EPOQUE</td>
      <td>3218</td>
      <td>L'HISTOIRE TERRIBLE... 2e EPOQUE</td>
      <td>28/11/14</td>
      <td>20:00:00</td>
      <td>28/11/14</td>
      <td>23:30:00</td>
      <td>27.0</td>
      <td>28/11/14</td>
      <td>19:52:07</td>
      <td>Abonnement mouettes</td>
      <td>Client</td>
      <td>Abonnement</td>
      <td>1er Serie</td>
      <td>CORBEILLE</td>
      <td>GUICHET</td>
      <td>KEBIR</td>
      <td>Fran_ois-Jean</td>
      <td>Fran_ois-Jean.KEBIR@mail.fr</td>
      <td>7 rue des Acinonyx jubatus</td>
      <td>69110</td>
      <td>France</td>
      <td>57.0</td>
      <td>F</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1400228</td>
      <td>NaN</td>
      <td>843992</td>
      <td>04/06/15 00:00</td>
      <td>16:26:04</td>
      <td>482</td>
      <td>LE ROI LEAR</td>
      <td>3257</td>
      <td>LE ROI LEAR</td>
      <td>14/01/15</td>
      <td>20:00:00</td>
      <td>14/01/15</td>
      <td>21:40:00</td>
      <td>27.0</td>
      <td>14/01/15</td>
      <td>19:57:08</td>
      <td>Abonnement mouettes</td>
      <td>Client</td>
      <td>Abonnement</td>
      <td>1er Serie</td>
      <td>ORCHESTRE</td>
      <td>GUICHET</td>
      <td>KEBIR</td>
      <td>Fran_ois-Jean</td>
      <td>Fran_ois-Jean.KEBIR@mail.fr</td>
      <td>7 rue des Acinonyx jubatus</td>
      <td>69110</td>
      <td>France</td>
      <td>57.0</td>
      <td>F</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1400229</td>
      <td>NaN</td>
      <td>843986</td>
      <td>04/06/15 00:00</td>
      <td>16:26:04</td>
      <td>483</td>
      <td>JE SUIS</td>
      <td>3268</td>
      <td>JE SUIS</td>
      <td>16/01/15</td>
      <td>20:00:00</td>
      <td>16/01/15</td>
      <td>21:30:00</td>
      <td>15.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Abonnement mouettes</td>
      <td>Client</td>
      <td>Abonnement</td>
      <td>Serie unique</td>
      <td>NaN</td>
      <td>GUICHET</td>
      <td>KEBIR</td>
      <td>Fran_ois-Jean</td>
      <td>Fran_ois-Jean.KEBIR@mail.fr</td>
      <td>7 rue des Acinonyx jubatus</td>
      <td>69110</td>
      <td>France</td>
      <td>57.0</td>
      <td>F</td>
    </tr>
  </tbody>
</table>
</div>



La variable `Date reservation` que nous utiliserons plus tard doit être revue pour avoir un format correct à la lecture.


```python
# Conversion en format date
data['Date sell'] = data['Date reservation'].apply(pd.to_datetime, format='%d/%m/%y %H:%M')

# Retour en 'object' avec format unlisible
data['Date sell'] = data['Date sell'].apply(lambda date: date.strftime('%d %B% %Y'))
```

## Exploration

### Général

Voici quelques informations qui me permettront d'en savoir plus sur la donnée.


```python
print("Le dataset contient", data.shape[0], "lignes et", data.shape[1], "colonnes.")
```

    Le dataset contient 99 lignes et 31 colonnes.



```python
print("Il y a eu un total de", len(data['Reservation'].unique()), "réservations uniques.")
```

    Il y a eu un total de 73 réservations uniques.


### Âge des clients


```python
# Mémorisation des informations
age_desc = data['Age'].describe()

# Création d'un résumé sous la forme d'un dataframe 
age_summary = pd.DataFrame(index=["Moyenne", "Médiane", "Valeur max", "Valeur min", "Q1", "Q3"]) 
age_summary['Âge des clients'] = [ageDesc['mean'], 
                                  ageDesc['50%'], 
                                  ageDesc['max'], 
                                  ageDesc['min'], 
                                  ageDesc['25%'], 
                                  ageDesc['75%']]
```

Voici les **données descriptives concernant l'âge des clients**.


```python
age_summary
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Âge des clients</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Moyenne</th>
      <td>68.514286</td>
    </tr>
    <tr>
      <th>Médiane</th>
      <td>66.000000</td>
    </tr>
    <tr>
      <th>Valeur max</th>
      <td>81.000000</td>
    </tr>
    <tr>
      <th>Valeur min</th>
      <td>50.000000</td>
    </tr>
    <tr>
      <th>Q1</th>
      <td>57.000000</td>
    </tr>
    <tr>
      <th>Q3</th>
      <td>81.000000</td>
    </tr>
  </tbody>
</table>
</div>



### Spectacles


```python
print("La donnée concerne", len(data['Spectacle'].unique()), "représentations.")
```

    La donnée concerne 25 représentations.


J'importe la deuxième librairie dont j'ai besoin, `numpy`.


```python
import numpy as np
```

Nous créons un dataframe ne contenant que trois des variables de `data`. La donnée est manipulée afin de mettre en valeur la moyenne des prix selon le spectacle.


```python
spect = pd.concat([data['Spectacle'], data['Cle spectacle'], data['Prix']], axis=1)

# Paramétrage des élements à aggréger
aggregations = {
    'Prix': {
        # Calcul de la moyenne arrondie au 100è
        'Moyenne': lambda prix: np.round(np.mean(prix), 2),
        # Affichage de la longueur de la liste des prix uniques
        'Nb. prix différents': lambda nb: len(set(nb))
    },
    'Cle spectacle': {
        'Nb. spectateurs': 'count'
    }
}

# Tri et aggrégation
spect_group = spect.groupby('Cle spectacle').agg(aggregations)
spect_group.head(20)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th colspan="2" halign="left">Prix</th>
      <th>Cle spectacle</th>
    </tr>
    <tr>
      <th></th>
      <th>Nb. prix différents</th>
      <th>Moyenne</th>
      <th>Nb. spectateurs</th>
    </tr>
    <tr>
      <th>Cle spectacle</th>
      <th></th>
      <th></th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>476</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>1</td>
    </tr>
    <tr>
      <th>477</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>1</td>
    </tr>
    <tr>
      <th>479</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>1</td>
    </tr>
    <tr>
      <th>482</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>1</td>
    </tr>
    <tr>
      <th>483</th>
      <td>1.0</td>
      <td>15.00</td>
      <td>1</td>
    </tr>
    <tr>
      <th>485</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>1</td>
    </tr>
    <tr>
      <th>490</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>1</td>
    </tr>
    <tr>
      <th>497</th>
      <td>2.0</td>
      <td>16.00</td>
      <td>16</td>
    </tr>
    <tr>
      <th>498</th>
      <td>2.0</td>
      <td>18.33</td>
      <td>9</td>
    </tr>
    <tr>
      <th>499</th>
      <td>1.0</td>
      <td>31.00</td>
      <td>1</td>
    </tr>
    <tr>
      <th>537</th>
      <td>2.0</td>
      <td>26.00</td>
      <td>5</td>
    </tr>
    <tr>
      <th>538</th>
      <td>2.0</td>
      <td>28.00</td>
      <td>10</td>
    </tr>
    <tr>
      <th>539</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>4</td>
    </tr>
    <tr>
      <th>543</th>
      <td>2.0</td>
      <td>24.50</td>
      <td>2</td>
    </tr>
    <tr>
      <th>545</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>3</td>
    </tr>
    <tr>
      <th>546</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>2</td>
    </tr>
    <tr>
      <th>548</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>4</td>
    </tr>
    <tr>
      <th>549</th>
      <td>1.0</td>
      <td>27.00</td>
      <td>10</td>
    </tr>
    <tr>
      <th>551</th>
      <td>2.0</td>
      <td>26.29</td>
      <td>7</td>
    </tr>
    <tr>
      <th>552</th>
      <td>1.0</td>
      <td>15.00</td>
      <td>4</td>
    </tr>
  </tbody>
</table>
</div>



Le **prix moyen par spectacle** est disponible dans la colonne **Moyenne**.

### Dates et heures d'achat

Je fais appel à la troisième librairie `matplotlib` afin de pouvoir réaliser des graphiques.


```python
# Affichage des graphiques
%matplotlib inline 

import matplotlib.pyplot as plt
# Paramétrage du style des graphiques
plt.style.use('ggplot')
```

Pour en revenir à la date, nous devons la transformer une fois de plus pour la reconvertir en type `Date` pour notre nouvelle variable `Datetime sell`.


```python
# Conversion en format date
data['Datetime sell'] = data[['Date sell', 'Heure reservation']].apply(lambda x: ' '.join(x), axis=1)

# Retour en 'object' avec format unlisible
data['Datetime sell'] = data['Datetime sell'].apply(pd.to_datetime, format='%d %B %Y %H:%M:%S')
```

Nous avons séparé la date de l'achat à la date complète contenant également l'heure.


```python
resa = pd.concat([data['Reservation'], data['Date sell'], data['Datetime sell']], axis=1)
resa.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Reservation</th>
      <th>Date sell</th>
      <th>Datetime sell</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>843989</td>
      <td>04 June 2015</td>
      <td>2015-06-04 16:26:04</td>
    </tr>
    <tr>
      <th>1</th>
      <td>843990</td>
      <td>04 June 2015</td>
      <td>2015-06-04 16:26:04</td>
    </tr>
    <tr>
      <th>2</th>
      <td>843991</td>
      <td>04 June 2015</td>
      <td>2015-06-04 16:26:04</td>
    </tr>
    <tr>
      <th>3</th>
      <td>843992</td>
      <td>04 June 2015</td>
      <td>2015-06-04 16:26:04</td>
    </tr>
    <tr>
      <th>4</th>
      <td>843986</td>
      <td>04 June 2015</td>
      <td>2015-06-04 16:26:04</td>
    </tr>
  </tbody>
</table>
</div>




```python
# Paramétrage des élements à aggréger
date_agg = {
    'Reservation': {
        'Nb. billets vendus/jour': 'count'
    }
}

# Tri et aggrégation
resa_group = resa.groupby('Date sell').agg(date_agg)
resa_group
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th>Reservation</th>
    </tr>
    <tr>
      <th></th>
      <th>Nb. billets vendus/jour</th>
    </tr>
    <tr>
      <th>Date sell</th>
      <th></th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>02 June 2015</th>
      <td>91</td>
    </tr>
    <tr>
      <th>04 June 2015</th>
      <td>8</td>
    </tr>
  </tbody>
</table>
</div>



Nous observons le fait que cet échantillon contient des données sur deux jours. 


```python
plt.figure()
resa_plot = resa_group.plot(kind='bar')

# Légende retirée
resa_plot.get_legend().remove()

# Personnalisation des labels
plt.xlabel("Date de réservation")
plt.ylabel("Nb. de clients")
plt.title("Nombre de billets vendus par jour")
plt.xticks(rotation="horizontal")
```




    (array([0, 1]), <a list of 2 Text xticklabel objects>)




    <matplotlib.figure.Figure at 0x1209b1f98>



![png](output_33_2.png)


La date contenant l'heure est découpée de manière à pouvoir bénéficier de toutes les informations que peut nous donner une date.


```python
datetime = pd.DatetimeIndex(resa['Datetime sell'])
```

Nous reproduisons le même exercice que précédemment en y ajoutant l'information sur le temps en heure pour le fun.


```python
# Paramétrage des élements à aggréger
hour_agg = {
    'Reservation': {
        'Nb. billets vendus/heure': 'count'
    }
}

# Tri et aggrégation
resa_hour_group = resa.groupby([datetime.date, datetime.hour]).agg(hour_agg)
resa_hour_group.head(100)
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr>
      <th></th>
      <th></th>
      <th>Reservation</th>
    </tr>
    <tr>
      <th></th>
      <th></th>
      <th>Nb. billets vendus/heure</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th rowspan="2" valign="top">2015-06-02</th>
      <th>10</th>
      <td>30</td>
    </tr>
    <tr>
      <th>12</th>
      <td>61</td>
    </tr>
    <tr>
      <th>2015-06-04</th>
      <th>16</th>
      <td>8</td>
    </tr>
  </tbody>
</table>
</div>



Les données ont été triées de sorte à pouvoir dire à quelle heure les billets ont été achetés. 


```python
plt.figure()
hour_plot = resa_hour_group.plot(kind='bar')

# Légende retirée
hour_plot.get_legend().remove()

# Personnalisation des labels
plt.xlabel("Date et heure de réservation")
plt.ylabel("Nb. de clients")
plt.title("Nombre de billets vendus par jour et heure")
plt.xticks(rotation="horizontal")
```




    (array([0, 1, 2]), <a list of 3 Text xticklabel objects>)




    <matplotlib.figure.Figure at 0x12061dc50>



![png](output_39_2.png)


## Algorithme

### Mise en situation


```python
data.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Numero billet</th>
      <th>Commande</th>
      <th>Reservation</th>
      <th>Date reservation</th>
      <th>Heure reservation</th>
      <th>Cle spectacle</th>
      <th>Spectacle</th>
      <th>Cle representation</th>
      <th>Representation</th>
      <th>Date representation</th>
      <th>Heure representation</th>
      <th>Date fin representation</th>
      <th>Heure fin representation</th>
      <th>Prix</th>
      <th>Date acces</th>
      <th>Heure acces</th>
      <th>Tarif</th>
      <th>Type de client</th>
      <th>Type de produit</th>
      <th>Serie</th>
      <th>Etage</th>
      <th>Filiere de vente</th>
      <th>Nom</th>
      <th>Prenom</th>
      <th>Email</th>
      <th>Adresse</th>
      <th>Code postal</th>
      <th>Pays</th>
      <th>Age</th>
      <th>Sexe</th>
      <th>Date sell</th>
      <th>Datetime sell</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1400222</td>
      <td>NaN</td>
      <td>843989</td>
      <td>04/06/15 00:00</td>
      <td>16:26:04</td>
      <td>476</td>
      <td>FEMME NON-REEDUCABLE</td>
      <td>3191</td>
      <td>FEMME NON-REEDUCABLE</td>
      <td>10/10/14</td>
      <td>20:00:00</td>
      <td>10/10/14</td>
      <td>22:00:00</td>
      <td>27.0</td>
      <td>10/10/14</td>
      <td>19:49:11</td>
      <td>Abonnement mouettes</td>
      <td>Client</td>
      <td>Abonnement</td>
      <td>1er Serie</td>
      <td>CORBEILLE</td>
      <td>GUICHET</td>
      <td>KEBIR</td>
      <td>Fran_ois-Jean</td>
      <td>Fran_ois-Jean.KEBIR@mail.fr</td>
      <td>7 rue des Acinonyx jubatus</td>
      <td>69110</td>
      <td>France</td>
      <td>57.0</td>
      <td>F</td>
      <td>04 June 2015</td>
      <td>2015-06-04 16:26:04</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1400223</td>
      <td>NaN</td>
      <td>843990</td>
      <td>04/06/15 00:00</td>
      <td>16:26:04</td>
      <td>477</td>
      <td>G©n©rale Publique Fever</td>
      <td>3204</td>
      <td>G©n©rale Publique Fever</td>
      <td>05/11/14</td>
      <td>20:00:00</td>
      <td>05/11/14</td>
      <td>21:30:00</td>
      <td>27.0</td>
      <td>05/11/14</td>
      <td>19:52:17</td>
      <td>Abonnement mouettes</td>
      <td>Client</td>
      <td>Abonnement</td>
      <td>1er Serie</td>
      <td>CORBEILLE</td>
      <td>GUICHET</td>
      <td>KEBIR</td>
      <td>Fran_ois-Jean</td>
      <td>Fran_ois-Jean.KEBIR@mail.fr</td>
      <td>7 rue des Acinonyx jubatus</td>
      <td>69110</td>
      <td>France</td>
      <td>57.0</td>
      <td>F</td>
      <td>04 June 2015</td>
      <td>2015-06-04 16:26:04</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1400225</td>
      <td>NaN</td>
      <td>843991</td>
      <td>04/06/15 00:00</td>
      <td>16:26:04</td>
      <td>479</td>
      <td>L'HISTOIRE TERRIBLE... 2e EPOQUE</td>
      <td>3218</td>
      <td>L'HISTOIRE TERRIBLE... 2e EPOQUE</td>
      <td>28/11/14</td>
      <td>20:00:00</td>
      <td>28/11/14</td>
      <td>23:30:00</td>
      <td>27.0</td>
      <td>28/11/14</td>
      <td>19:52:07</td>
      <td>Abonnement mouettes</td>
      <td>Client</td>
      <td>Abonnement</td>
      <td>1er Serie</td>
      <td>CORBEILLE</td>
      <td>GUICHET</td>
      <td>KEBIR</td>
      <td>Fran_ois-Jean</td>
      <td>Fran_ois-Jean.KEBIR@mail.fr</td>
      <td>7 rue des Acinonyx jubatus</td>
      <td>69110</td>
      <td>France</td>
      <td>57.0</td>
      <td>F</td>
      <td>04 June 2015</td>
      <td>2015-06-04 16:26:04</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1400228</td>
      <td>NaN</td>
      <td>843992</td>
      <td>04/06/15 00:00</td>
      <td>16:26:04</td>
      <td>482</td>
      <td>LE ROI LEAR</td>
      <td>3257</td>
      <td>LE ROI LEAR</td>
      <td>14/01/15</td>
      <td>20:00:00</td>
      <td>14/01/15</td>
      <td>21:40:00</td>
      <td>27.0</td>
      <td>14/01/15</td>
      <td>19:57:08</td>
      <td>Abonnement mouettes</td>
      <td>Client</td>
      <td>Abonnement</td>
      <td>1er Serie</td>
      <td>ORCHESTRE</td>
      <td>GUICHET</td>
      <td>KEBIR</td>
      <td>Fran_ois-Jean</td>
      <td>Fran_ois-Jean.KEBIR@mail.fr</td>
      <td>7 rue des Acinonyx jubatus</td>
      <td>69110</td>
      <td>France</td>
      <td>57.0</td>
      <td>F</td>
      <td>04 June 2015</td>
      <td>2015-06-04 16:26:04</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1400229</td>
      <td>NaN</td>
      <td>843986</td>
      <td>04/06/15 00:00</td>
      <td>16:26:04</td>
      <td>483</td>
      <td>JE SUIS</td>
      <td>3268</td>
      <td>JE SUIS</td>
      <td>16/01/15</td>
      <td>20:00:00</td>
      <td>16/01/15</td>
      <td>21:30:00</td>
      <td>15.0</td>
      <td>NaN</td>
      <td>NaN</td>
      <td>Abonnement mouettes</td>
      <td>Client</td>
      <td>Abonnement</td>
      <td>Serie unique</td>
      <td>NaN</td>
      <td>GUICHET</td>
      <td>KEBIR</td>
      <td>Fran_ois-Jean</td>
      <td>Fran_ois-Jean.KEBIR@mail.fr</td>
      <td>7 rue des Acinonyx jubatus</td>
      <td>69110</td>
      <td>France</td>
      <td>57.0</td>
      <td>F</td>
      <td>04 June 2015</td>
      <td>2015-06-04 16:26:04</td>
    </tr>
  </tbody>
</table>
</div>



Nous allons sélectionner quelques variables pour entraine un modèle d'algorithme de Mahcine learning. Ceci reste dans le cadre de l'exercice et n'utilise pas de méthode mathématique de sélection de variables.

Pour le bonus, nous voulons étudier de plus près la variable `Etage` qui contient cinq valeurs manquantes. Nous allons tenter de les déterminer.


```python
data['Etage'].value_counts()
```




    ORCHESTRE    63
    CORBEILLE    22
    BALCON        6
    GRADIN        2
    PARTERRE      1
    Name: Etage, dtype: int64



Je sélectionne quatorze variables en favorisant les identifiants (clés) de spectacles, réservations, etc.


```python
sub_data = pd.concat([data['Numero billet'], 
                      data['Reservation'],
                      data['Cle spectacle'],
                      data['Cle representation'],
                      data['Prix'],
                      data['Tarif'],
                      data['Type de produit'],
                      data['Serie'],
                      data['Filiere de vente'],
                      data['Nom'],
                      data['Code postal'],
                      data['Sexe'],
                      data['Datetime sell'],
                      data['Etage']],
                     axis=1)

# Séparation du timestamp en heure et en jour de l'année
sub_data['hour'] = sub_data['Datetime sell'].dt.hour
sub_data['day'] = sub_data['Datetime sell'].dt.dayofyear
sub_data = sub_data.drop('Datetime sell', axis=1)
```

### Pré-processing

J'importe les éléments nécessaires au pré-processing de la librairie `scikit-learn`.


```python
from sklearn import preprocessing
from sklearn.preprocessing import LabelEncoder
```

Les variables ont besoin d'être retravaillées afin d'avoir le format correct pour entraîner un modèle.


```python
le_tarif = preprocessing.LabelEncoder()
le_tarif.fit(sub_data['Tarif'])

le_product_type = preprocessing.LabelEncoder()
le_product_type.fit(sub_data['Type de produit'])

le_serie = preprocessing.LabelEncoder()
le_serie.fit(sub_data['Serie'])

le_branch = preprocessing.LabelEncoder()
le_branch.fit(sub_data['Filiere de vente'])

le_name = preprocessing.LabelEncoder()
le_name.fit(sub_data['Nom'])
```




    LabelEncoder()



D'autre part, j'observe les niveaux de facteurs de la variable `Sexe`...


```python
sub_data['Sexe'].unique()
```




    array(['F', 'H', nan], dtype=object)



... et de la variable `Etage`.


```python
sub_data['Etage'].unique()
```




    array(['CORBEILLE', 'ORCHESTRE', nan, 'PARTERRE', 'BALCON', 'GRADIN'], dtype=object)



Notons que les valeurs manquantes dans `Etage` sont converties en -1.


```python
sub_data['Tarif'] = le_tarif.transform(sub_data['Tarif'])
sub_data['Type de produit'] = le_product_type.transform(sub_data['Type de produit'])
sub_data['Serie'] = le_serie.transform(sub_data['Serie'])
sub_data['Filiere de vente'] = le_branch.transform(sub_data['Filiere de vente'])
sub_data['Nom'] = le_name.transform(sub_data['Nom'])
sub_data['Sexe'] = sub_data['Sexe'].factorize()[0]
sub_data['Etage'] = sub_data['Etage'].factorize()[0]

sub_data.head()
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Numero billet</th>
      <th>Reservation</th>
      <th>Cle spectacle</th>
      <th>Cle representation</th>
      <th>Prix</th>
      <th>Tarif</th>
      <th>Type de produit</th>
      <th>Serie</th>
      <th>Filiere de vente</th>
      <th>Nom</th>
      <th>Code postal</th>
      <th>Sexe</th>
      <th>Etage</th>
      <th>hour</th>
      <th>day</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>0</th>
      <td>1400222</td>
      <td>843989</td>
      <td>476</td>
      <td>3191</td>
      <td>27.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>12</td>
      <td>69110</td>
      <td>0</td>
      <td>0</td>
      <td>16</td>
      <td>155</td>
    </tr>
    <tr>
      <th>1</th>
      <td>1400223</td>
      <td>843990</td>
      <td>477</td>
      <td>3204</td>
      <td>27.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>12</td>
      <td>69110</td>
      <td>0</td>
      <td>0</td>
      <td>16</td>
      <td>155</td>
    </tr>
    <tr>
      <th>2</th>
      <td>1400225</td>
      <td>843991</td>
      <td>479</td>
      <td>3218</td>
      <td>27.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>12</td>
      <td>69110</td>
      <td>0</td>
      <td>0</td>
      <td>16</td>
      <td>155</td>
    </tr>
    <tr>
      <th>3</th>
      <td>1400228</td>
      <td>843992</td>
      <td>482</td>
      <td>3257</td>
      <td>27.0</td>
      <td>1</td>
      <td>0</td>
      <td>0</td>
      <td>1</td>
      <td>12</td>
      <td>69110</td>
      <td>0</td>
      <td>1</td>
      <td>16</td>
      <td>155</td>
    </tr>
    <tr>
      <th>4</th>
      <td>1400229</td>
      <td>843986</td>
      <td>483</td>
      <td>3268</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>12</td>
      <td>69110</td>
      <td>0</td>
      <td>-1</td>
      <td>16</td>
      <td>155</td>
    </tr>
  </tbody>
</table>
</div>



Les valeurs manquantes sont regroupées dans notre échantillon de test final.


```python
test = sub_data[sub_data['Etage'] == -1]
test_features = test.drop('Etage', axis=1)
test
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Numero billet</th>
      <th>Reservation</th>
      <th>Cle spectacle</th>
      <th>Cle representation</th>
      <th>Prix</th>
      <th>Tarif</th>
      <th>Type de produit</th>
      <th>Serie</th>
      <th>Filiere de vente</th>
      <th>Nom</th>
      <th>Code postal</th>
      <th>Sexe</th>
      <th>Etage</th>
      <th>hour</th>
      <th>day</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>1400229</td>
      <td>843986</td>
      <td>483</td>
      <td>3268</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>12</td>
      <td>69110</td>
      <td>0</td>
      <td>-1</td>
      <td>16</td>
      <td>155</td>
    </tr>
    <tr>
      <th>50</th>
      <td>1491917</td>
      <td>838748</td>
      <td>552</td>
      <td>3694</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>1</td>
      <td>69004</td>
      <td>1</td>
      <td>-1</td>
      <td>12</td>
      <td>153</td>
    </tr>
    <tr>
      <th>51</th>
      <td>1491918</td>
      <td>838748</td>
      <td>552</td>
      <td>3694</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>1</td>
      <td>69004</td>
      <td>1</td>
      <td>-1</td>
      <td>12</td>
      <td>153</td>
    </tr>
    <tr>
      <th>62</th>
      <td>1491929</td>
      <td>838779</td>
      <td>552</td>
      <td>3694</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>10</td>
      <td>69004</td>
      <td>1</td>
      <td>-1</td>
      <td>12</td>
      <td>153</td>
    </tr>
    <tr>
      <th>70</th>
      <td>1491937</td>
      <td>838788</td>
      <td>552</td>
      <td>3694</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>10</td>
      <td>69004</td>
      <td>1</td>
      <td>-1</td>
      <td>12</td>
      <td>153</td>
    </tr>
  </tbody>
</table>
</div>



Les autres observations constituent notre échantillon d'entraînement.


```python
train = sub_data[sub_data['Etage'] != -1]
train_outcome = train['Etage']
train_features = train.drop('Etage', axis=1)
```

### Cross-validation


```python
from sklearn import cross_validation
from sklearn.ensemble import RandomForestClassifier
from sklearn.metrics import accuracy_score
from sklearn.metrics import confusion_matrix

# Choix d'une référence pour les résultats aléatoires
np.random.seed(2016)
```

Je choisis de procéder à une cross-validation manuelle dans le cadre de l'exercice au sein des données `train`. Je les divise en 80% pour entraîner et 20% pour tester. 


```python
sub_train, sub_test, sub_train_outcome, sub_test_outcome = cross_validation.train_test_split(train_features, 
                                                                                             train_outcome, 
                                                                                             test_size=0.2, 
                                                                                             random_state=0)
```

Dans le cadre de l'étude de la variable `Etage`, nous cherchons à déterminer des résultats sous forme de catégories. Nous sommes donc dans une optique de classification et utilisons donc l'algorithme Random Forest.

### Application


```python
clf = RandomForestClassifier(n_estimators=10)
clf = clf.fit(sub_train, sub_train_outcome)
```

J'entraîne mon modèle et l'applique sur mon ensemble de sous-test.


```python
rf_sub_test_results = clf.predict(sub_test)
```


```python
accuracy_score(sub_test_outcome, rf_sub_test_results)
```




    0.89473684210526316



La pertinence atteint 89.47%.
J'étudie les particularités de l'algorithme et notamment des variables les plus importantes.


```python
importances = clf.feature_importances_
std = np.std([tree.feature_importances_ for tree in clf.estimators_], axis=0)
indices = np.argsort(importances)[::-1]

# Affichage du top des variables
print("Top des variables:")

col_labels = sub_test.columns.values.tolist()
for var in range(0, len(col_labels)):
    print("%d. %s (%f)" % (var, col_labels[var], importances[indices[var]]))
```

    Top des variables:
    0. Numero billet (0.244537)
    1. Reservation (0.136839)
    2. Cle spectacle (0.120432)
    3. Cle representation (0.097015)
    4. Prix (0.096528)
    5. Tarif (0.063797)
    6. Type de produit (0.061605)
    7. Serie (0.041001)
    8. Filiere de vente (0.040456)
    9. Nom (0.026068)
    10. Code postal (0.025139)
    11. Sexe (0.019568)
    12. hour (0.019457)
    13. day (0.007557)


Je réalise un graphique afin de visualiser leur importance.


```python
plt.figure()
plt.title("Importance des variables")
plt.bar(range(0, len(col_labels)), importances[indices], yerr=std[indices], align='center')
plt.xticks(range(0, len(col_labels)), col_labels, rotation='vertical')
plt.xlim([-1, len(col_labels)])
plt.show()
```


![png](output_75_0.png)



```python
cm = confusion_matrix(sub_test_outcome, np.around(rf_sub_test_results))
```


```python
def plot_confusion_matrix(cm, title="Matrice de confusion", cmap=plt.cm.Blues):
    plt.imshow(cm, interpolation='nearest', cmap=cmap)
    plt.title(title)
    plt.colorbar()
    plt.tight_layout()
    plt.ylabel("Valeurs réelles")
    plt.xlabel("Prédictions")

plt.figure()
plot_confusion_matrix(cm)
```


![png](output_77_0.png)


### Prédiction

J'applique l'algorithme sur l'ensemble de test final.


```python
rf_test_results = clf.predict(test_features)
rf_test_results
```




    array([0, 1, 1, 1, 1])




```python
etages = data['Etage'].unique()

# Création d'un dataframe contenant les valeurs finales
valid_etages = []
for key in np.nditer(rf_test_results):
    valid_etages.insert(key, etages[key])
```


```python
final_etage = pd.DataFrame(validEtages, index=test.index, columns=['Etage'])
final_etage
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Etage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>CORBEILLE</td>
    </tr>
    <tr>
      <th>50</th>
      <td>ORCHESTRE</td>
    </tr>
    <tr>
      <th>51</th>
      <td>ORCHESTRE</td>
    </tr>
    <tr>
      <th>62</th>
      <td>ORCHESTRE</td>
    </tr>
    <tr>
      <th>70</th>
      <td>ORCHESTRE</td>
    </tr>
  </tbody>
</table>
</div>




```python
test_features['Etage'] = final_etage['Etage']
```

D'après l'algorithme, voici les résultats que nous devrions avoir pour la variable `Etage` sur les cinq valeurs manquantes.


```python
test_features
```




<div>
<table border="1" class="dataframe">
  <thead>
    <tr style="text-align: right;">
      <th></th>
      <th>Numero billet</th>
      <th>Reservation</th>
      <th>Cle spectacle</th>
      <th>Cle representation</th>
      <th>Prix</th>
      <th>Tarif</th>
      <th>Type de produit</th>
      <th>Serie</th>
      <th>Filiere de vente</th>
      <th>Nom</th>
      <th>Code postal</th>
      <th>Sexe</th>
      <th>hour</th>
      <th>day</th>
      <th>Etage</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>4</th>
      <td>1400229</td>
      <td>843986</td>
      <td>483</td>
      <td>3268</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>12</td>
      <td>69110</td>
      <td>0</td>
      <td>16</td>
      <td>155</td>
      <td>CORBEILLE</td>
    </tr>
    <tr>
      <th>50</th>
      <td>1491917</td>
      <td>838748</td>
      <td>552</td>
      <td>3694</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>1</td>
      <td>69004</td>
      <td>1</td>
      <td>12</td>
      <td>153</td>
      <td>ORCHESTRE</td>
    </tr>
    <tr>
      <th>51</th>
      <td>1491918</td>
      <td>838748</td>
      <td>552</td>
      <td>3694</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>1</td>
      <td>69004</td>
      <td>1</td>
      <td>12</td>
      <td>153</td>
      <td>ORCHESTRE</td>
    </tr>
    <tr>
      <th>62</th>
      <td>1491929</td>
      <td>838779</td>
      <td>552</td>
      <td>3694</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>10</td>
      <td>69004</td>
      <td>1</td>
      <td>12</td>
      <td>153</td>
      <td>ORCHESTRE</td>
    </tr>
    <tr>
      <th>70</th>
      <td>1491937</td>
      <td>838788</td>
      <td>552</td>
      <td>3694</td>
      <td>15.0</td>
      <td>1</td>
      <td>0</td>
      <td>3</td>
      <td>1</td>
      <td>10</td>
      <td>69004</td>
      <td>1</td>
      <td>12</td>
      <td>153</td>
      <td>ORCHESTRE</td>
    </tr>
  </tbody>
</table>
</div>




```python

```
