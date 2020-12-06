
# Listes : ordrées, mutables, autorisent les éléments dupliqués

## Liste vide
```python
mylist = list()
```

## Déclaration
```python
mylist = ["1", 3, True, "dada"]
```

## Récupération

### Récupération du 3ème élément
```python
mylist[2]
```

### Récupération du dernier élément
```python
mylist[-1]
```

### Récupération de l'avant dernier élément
```python
mylist[-2]
```

### Récupère les éléments de 1 à 5 (le dernier est exclu : 2, 3, 4, 5)
```python
a = mylist[1:5]
```

### Depuis le début
```python
a = mylist[:5]
```

### Jusqu'à la fin
```python
a = mylist[2:]
```

### Spécifier des intervalles

#### De l'index 1 à la fin (1, 2, 3, 4, 5, 6, 7, 8, 9)
```python
a = mylist[::1]
```

#### De l'index 1 à la fin de 2 en 2 (1, 3, 5, 7, 9)
```python
a = mylist[::2]
```

#### Dans l'ordre inverse de 1 en 1
```python
a = mylist[::-1]
```

## Pour chaque élément dans une liste
```python
for i in mylist:
    # Code
```

## Si un élément est présent dans le code
```python
if "dada" in mylist:
    # Code
```

## Taille de la Liste
```python
len(mylist)
```

## Ajout d'un élément
```python
mylist.append("new")
```

## Ajout d'un élément à une position (POUSSE LES AUTRES VALEURS)
```python
mylist.insert(2, "new")
```

## Retourne et supprime le dernier élément
```python
mylist.pop()
```

## Supprime un élément
```python
mylist.remove("element")
```

## Clear la liste
```python
mylist.clear()
```

## Reverse la liste (1,2,3 -> 3,2,1)
```python
mylist.reverse()
```

## Trie la liste (trie la liste même si dans une opération : new = mylist.sort())
```python
mylist.sort()
```

## Stocke la liste triée dans une nouvelle liste
```python
new = sorted(mylist)
```

## Ajouter 5 fois le même élément (mylist = 0,0,0,0,0 <==> mylist = [0]*5)
```python
mylist = [0] * 5
```

## Concaténation de listes
```python
new_list = mylist + mylist2
```

## Copier une liste

### Si on modifie la copie, l'originale change aussi
```python
copy = mylist
```

### Si on modifie la copie, l'originale ne change pas0

#### Méthode copy()
```python
copy = mylist.copy()
```

#### Méthode list()
```python
copy = list(mylist)
```

#### Méthode slicing
```python
copy = mylist[:]
```

### Modifier les éléments de la liste à la copie (copy = [1, 4, 9, 16, 25, 36] mylist = [1, 2, 3, 4, 5, 6])
```python
copy = [i*i for i in mylist]
```

## Création d'une liste à partir d'un tuple
```python
mylist = list(mytuple)
```

# Tuples : ordrées, immutables (ne peuvent pas changer après la création), autorisent les éléments dupliqués, Plus opti que les listes pour les grosses données (un tuple contient moins de bytes qu'une liste, environ 10x plus rapide de créer un tuple qu'une liste)

## Création (Les parenthèses sont optionnelles)
```python
mytuple = ("abab", 21, True, "Joe")
mytuple = "abab", 21, True, "Joe"
```

### Création d'un tuple à un seul élément
```python
mytuple = ("element",)
```

### Création d'un tuple à partir d'une liste
```python
mytuple = tuple(["abab", 21, True, Joe])
```

## Nombre de certains éléments dans un tuple
```python
mytuple.count('p')
```

## Premier index d'un élément (si mytuple = ('a', 'p', 'p'), alors l'index retourné sera 1)
```python
mytuple.index('p')
```

## Mettre les éléments du tuple dans des variables (le tuple doit avoir autant d'éléments que ceux déclarés)
```python
name, age, city = mytuple
```

## Mets dans i1 le premier élément, dans i3 le dernier et dans i2 tous ceux entre les deux sous forme de liste
```python
i1, *i2, i3 = mytuple
```

# Dictionnaires : Clé-valeur, pas ordonné (donc pas d'index), mutable

## Création

### Création d'un dictionnaire vide
```python
mydict = {}
```

### Méthode {}
```python
mydict = {"name": "Joe", "age": 26, "city": "New York"}
```

### Méthode dict()
```python
mydict = dict(name="Joe", age="26", city="New York")
```

## Récupération

### Récupération standard (toujours avec la clé, pas l'index)
```python
mydict["age"]
mydict[3]
```

### Obtenir toutes les clés dans un dictionnaire
```python
key in mydict.keys()
```

### Obtenir toutes les valeurs dans un dictionnaire
```python
values in mydict.values()
```

### Obtenir toutes les clés et valeurs dans un dictionnaire
```python
key, value in mydict.items()
```

## Ajout / Modification
```python
mydict["email"] = "dada@yea.aey"
```

## Suppression

### Méthode del
```python
del mydict["name"]
```

### Méthode pop()
```python
mylist.pop("name")
```

### Supprime le dernier élément ajouté
```python
mylist.popitem()
```

## Modifier un dictionnaire
```python
mydict.update(mydict2)
```

## Il est possible d'avoir un tuple comme clé (pas une liste !!)
```python
mydict = {mytuple: 15}
```

# Sets : pas ordonnés, mutables, pas de duplications

## Création

### Création d'un set vide
```python
myset = set()
```

### Création standard (myset = {1, 2, 3, 4} car 1, 3, 2 sont déjà présent dans le set)
```python
myset = {1, 2, 3, 4, 1, 3, 2}
```

### Méthode set() - myset = {e, H, o, l}
```python
myset = set("Hello")
```

### Création d'un set constant
```python
myset1 = frozenset([1, 2, 3, 4])
```

## Ajout

### Ajout d'une valeur
```python
myset.add(1)
```

## Suppression

### Méthode remove()
```python
myset.remove(3)
```

### Méthode pop() - return et enlève une valeur aléatoire du set
```python
myset.pop()
```

### Méthode discard() - pas d'erreurs si l'élément n'est pas dans le set
```python
myset.discard(3)

```
## Clear d'un set
```python
set.clear()
```

## Union de sets - myset1{1, 2, 3, 4}.union(myset2{2, 3, 4, 5}) = {1, 2, 3, 4, 5}
```python
return myset1.union(myset2)
```

## Intersection de sets - myset1{1, 2, 3, 4}.intersection(myset2{2, 3, 4, 5}) = {2, 3, 4}
```python
return myset1.intersection(myset2)
```

## Différence de sets - myset1{1, 2, 3, 4}.difference(myset2{2, 3, 4, 5}) = {5}
```python
return myset1.difference(myset2)
```

## Différence symétrique de sets - myset1{1, 2, 3, 4}.difference(myset2{2, 3, 4, 5}) = {1, 5}
```python
return myset1.symmetric_difference(myset2)
```

## Update de sets - addition de 2 sets
```python
myset1.update(myset2)
```

## Tous ceux en haut son appliquables aux updates
```python
myset1.difference_update(myset2)
```

## Vérifie si un set fait partie d'un autre - {1, 2, 3} fait partie de {1, 2, 3, 4}
```python
myset1.issubset(myset2)
```

## Vérifie si un set contient un autre set - {1, 2, 3, 4} est un superset de {1, 2, 3}
```python
myset2.issuperset(myset1)
```

## Vérifie si un set ne contient rien en lien avec un autre - {1, 2, 3} est disjoint de {4, 5}
```python
myset1.isdisjoint(myset2)
```

# Strings













































d
