# Pandas
![img1](https://i.guim.co.uk/img/media/54e2b9530919ffe21b006f21cdd192d097745f7e/0_54_2560_1536/master/2560.jpg?width=700&quality=85&auto=format&fit=max&s=137c244ec11a9cfb40ca25fe00fcf857)

## Joining Data with pandas

Inner join : pour une simple jointure, on choisit juste la colonne de jointure

left join ou right join : on choisit la table où on souhaite faire une jointure à gauche ou à droite par un suffixe
```python
import pandas as pd

maisons = pd.read_csv('maisons.csv')
proprio = pd.read_csv('propriotaires.csv')

maisons_proprio = proprio.merge(maisons , on='vid', suffixes=('_own','_veh'))

# Print the value_counts to find the most popular fuel_type
# print(taxi_own_veh['fuel_type'].value_counts())

```
