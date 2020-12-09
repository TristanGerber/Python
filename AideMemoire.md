
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

### Récupère les éléments de 1 à 5
```python
a = mylist[1:5]
# Le dernier est exclu : 2, 3, 4, 5
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

#### De l'index 1 à la fin
```python
a = mylist[::1]
# 1, 2, 3, 4, 5, 6, 7, 8, 9
```

#### De l'index 1 à la fin de 2 en 2
```python
a = mylist[::2]
# 1, 3, 5, 7, 9
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

## Trie la liste
```python
mylist.sort()
# Trie la liste même si dans une opération : new = mylist.sort()
```

## Stocke la liste triée dans une nouvelle liste
```python
new = sorted(mylist)
```

## Ajouter 5 fois le même élément
```python
mylist = [0] * 5
# mylist = 0,0,0,0,0 <==> mylist = [0]*5
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

### Si on modifie la copie, l'originale ne change pas

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

### Modifier les éléments de la liste à la copie
```python
copy = [i*i for i in mylist]
# copy = [1, 4, 9, 16, 25, 36] mylist = [1, 2, 3, 4, 5, 6]
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

### Création standard
```python
myset = {1, 2, 3, 4, 1, 3, 2}
# myset = {1, 2, 3, 4} car 1, 3, 2 sont déjà présent dans le set
```

### Méthode set()
```python
myset = set("Hello")
# myset = {e, H, o, l}
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

## Intersection de sets
```python
return myset1.intersection(myset2) 
# myset1{1, 2, 3, 4}.intersection(myset2{2, 3, 4, 5}) = {2, 3, 4}
```

## Différence de sets
```python
return myset1.difference(myset2) 
# myset1{1, 2, 3, 4}.difference(myset2{2, 3, 4, 5}) = {5}
```

## Différence symétrique de sets
```python
return myset1.symmetric_difference(myset2) 
# myset1{1, 2, 3, 4}.difference(myset2{2, 3, 4, 5}) = {1, 5}
```

## Update de sets - addition de 2 sets
```python
myset1.update(myset2)
```

## Tous ceux en haut son appliquables aux updates
```python
myset1.difference_update(myset2)
```

## Vérifie si un set fait partie d'un autre
```python
myset1.issubset(myset2) 
# {1, 2, 3} fait partie de {1, 2, 3, 4}
```

## Vérifie si un set contient un autre set
```python
myset2.issuperset(myset1) 
# {1, 2, 3, 4} est un superset de {1, 2, 3}
```

## Vérifie si un set ne contient rien en lien avec un autre
```python
myset1.isdisjoint(myset2) 
# {1, 2, 3} est disjoint de {4, 5}
```

# Strings : ordrés, immuables, texte

## Déclaration

### Déclaration standard
```python
mystring = "string"
```

### Déclaration avec \
```python
mystring = 'j\'aime'
```

### Déclaration avec " ' "
```python
mystring = "j'aime"
```

### Déclaration avec """ - peut avoir un \ pour cancel le retour à la ligne
```python
mystring = """Hello
World"""
```

## String = liste
```python
char = mystring[3]
char2 = mystring[-2]
substring = mystring[1:5]
substring2 = mystring[::-2]
```

## Addition de strings
```python
mystring3 = mystring1 + " " + mystring2
```

## Enlever les espaces inutiles
```python
mystring = mystring.strip()
```

## Mettre en majuscules
```python
mystring.upper()
```

## Mettre en minuscules
```python
mystring.lower()
```

## Teste si le string commence par
```python
mystring.startswith("Hello")
```


## Teste si le string commence par
```python
mystring.endswith("Bye")
```

## Trouve une lettre / string - la première de la liste
```python
mystring.find('ob')
```

## Nombre de lettres de type 'x'
```python
mystring.count('x')
```

## Remplace un texte par un autre
```python
mystring.replace("World", "Universe")
```

## Split un string dans une liste de string
```python
mystring.split(",")
# ["je,suis"] -> ["je", "suis"]
```

## Inverse de split - Beaucoup plus performant de faire un join qu'une boucle for avec += ou autre
```python
'XY'.join(my_list) 
# ["On", "est", "bien"] -> ["OnXYestXYbien"]
```

## Formattage de strings

### %s pour %string | %f pour float | %d pour double | %b pour bool | ...
```python
mystring = "string %s" % var
```
### %.2 pour avoir 2 nombres après la virgule
```python
mystring = "Yass %.2f" % var
```

### Méthode .format()
```python
mystring = "Yass {:.2f} and {}".format(var, var2)
mystring = f"Yass {var} and {var2}"
```

# Collections - Librairie : 

## Librairie Counter - Permet de compter diverses choses

### Importation
```python
from collections import Counter
```

### Compte le nombre d'un type d'item
```python
mycounter = Counter(mystring)
# Counter("aaaabbccccc") -> {'a': 4, 'b': 2, 'c': 5}
```

### Compte le nombre d'items
```python
mycounter.items()
# Counter("abb").items() -> [('a', 1), ('b', 2)]
```

### Différentes clés - 'a', 'b'
```python
mycounter.keys()
```

### Différentes valeurs - 1, 2
```python
mycounter.values()
```

### Clé qui revient le plus
```python
mycounter.most_common(nb_retours)
# {'b': 2, 'a': 1}
```

### Tous les éléments
```python
mycounter.elements()
```

## Librairie namedtuple - Tuple qui a un nom et auquel on peut attribuer des valeurs selon leur position

### Importation
```python
from collections import namedtuple
```

### Création
```python
Point = namedtuple('Point', 'x,y')
```

### Utilisation
```python
pt = Point(-1, 4)
```

## Librairie OrderedDict - Dictionnaire ordré par index

### Importation
```python
from collections import OrderedDict
```

### Création
```python
a = OrderedDict()
```

### Assignation
```python
a['new'] = 1
a['new2'] = 32
```

## Librairie defaultdict

### Importation
```python
from collections import defaultdict
```

### Création
```python
d = defaultdict(int)
```

### Assignation
```python
d['a'] = 1
d['b'] = 16
```

## Librairie deque

### Importation
```python
from collections import deque
```

### Création
```python
d = deque()
```

### Ajout

#### Ajout standard
```python
d.append(2)
# d[2]
```

#### Ajout à gauche
```python
d.appendleft(3)
# d[3, 2]
```

#### Méthode extend
```python
d.extend(4, 5, 6)
```

### Méthode extendleft
```python
d.extandleft(1, 2, 3)
```

###  Suppression

#### Suppression standard
```python
d.pop()
```

#### Suppression à gauche
```python
d.popleft()
```

### Méthode clear
```python
d.clear()
```

### Méthode rotate
```python
d.rotate(nb_rotates)
# d[1, 2, 3, 4] -> d[2, 3, 4, 1]
```

# Itertools - Librairie :

## Librairie product - Fais des calculs avec des tableaux

### Importation
```python
from itertools import product
```

### Addition
```python
a = [1, 2]
b = [3, 4]
prod = product(a,b, repeat=nb)
# prod = [(1, 3), (1, 4), (2, 3), (2, 4)]
```

## Librairie permutations - permet d'afficher toutes les possibilités avec une liste

### Importation
```python
from itertools import permutations
```

### Utilisation
```python
a = [1, 2, 3]
perm = permutations(a)
# perm = [(1, 2, 3), (1, 3, 2), (2, 3, 1), ...]
```

### Paramètre de taille
```python
a = [1, 2, 3]
perm = permutations(a, 2)
# perm = [(1, 2), (1, 3), (2, 3), ...]
```

## Librairie combinations - permet d'afficher toutes les possibilités de combinaison avec une liste

### Importation
```python
from itertools import combinations
```

### Utilisation
```python
a = [1, 2, 3, 4]
comb = combinations(a, 2)
# comb = [(1, 2), (1, 3), (1, 4), ...] - dans l'ordre croissant
```

## Librairie combinations_with_replacement - permet d'afficher toutes les possibilités de combinaison avec une liste, en prenant les nombres entre eux également 1-1 2-2

### Importation
```python
from itertools import combinations_with_replacement
```

### Utilisation
```python
a = [1, 2, 3, 4]
acc = accumulate(a)
# comb = [(1, 1), (1, 2), (1, 3), ...] - dans l'ordre croissant en prenant les nombres entre eux comme 1-1, 2-2
```

## Librairie accumulate

### Importation
```python
from itertools import accumulate
```

### Utilisation
```python
a = [1, 2, 3, 4]
acc = accumulate(a)
# comb = [1, 3, 6, 10] - dans l'ordre croissant
```

## Librairie groupby - teste des valeurs selons une clé

### Importation
```python
from itertools import groupby
```

### Utilisation

#### Tests
```python
a = [1, 2, 3, 4]
group_obj = groupby(a, key=lambda x: x<3)
# True [1, 2]
# False [3, 4]
```

#### Groupement
```python
a = [{'a': 1, 'b': 2}, {'a': 2, 'b': 2}, {'a': 1, 'b': 4}]
group_obj = groupby(a, key=lambda x: x['a'])
# 1 [{'a': 1, 'b': 2}, {'a': 1, 'b': 4}]
# 2 {'a': 2, 'b': 2}
```

## Librairie count - compte

### Importation
```python
from itertools import count
```

### Utilisation
```python
for i in count(10):
    # Commence à 10 et compte infiniment
```

## Librairie cycle - compte en cycle par rapport à une liste

### Importation
```python
from itertools import cycle
```

### Utilisation
```python
for i in cycle([1, 2, 3]):
    # Compte 1, 2, 3, 1, 2, 3, 1, 2, ... infiniment
```

## Librairie repeat - répète un output un nombre n de fois (si aucun paramètre, infini)

### Importation
```python
from itertools import repeat
```

### Utilisation
```python
for i in repeat(1, n):
    # Commence à 10 et compte infiniment
```

# Fonctions Lambda

## Création
```python
add10 = lambda x: x + 10
```

## Appel
```python
add10(13)
# Retourne 13 + 10 = 23
```

## Multiples arguments
```python
mult = lambda x,y: x*y
```

## Méthode embarquée
```python
sorted(array, key=lambda x: x[1])
# Trie par le deuxième index
```

# Exeptions et Erreurs

## Créer une exception
```python
raise Exception('Error')
```

## Méthode assert()
```python
assert (condition), 'message'
# Si condition est false, alors AssertionError: message
```

## Try / Except / Else / Finally
```python
try:
    #code
except ZeroDivisionError as e:
    print(e)
except ZeroDivisionError as e:
    print(e)
else:
    print("ok")
finally:
    print("cleaning up...")
```

## Création d'exceptions
```python
class ValueTooSmallError(Exception)
    def __init__(self, message, value)
    self.message = message
    self.value = value

if(value<5)
    raise ValueTooSmallError('la valeur est trop petite', value)
    
try:
    #code
except ValueTooSmallError as e:
    print(e.message, e.value)
```

# À FAIRE EN ÉCOUNTANT

# Log

## Importation
```python
import logging
```

## Variantes de logging
```python
logging.debug("message")
logging.info("message")
logging.warning("message")
logging.error("message")
logging.critical("message")
```

## Config de logging
```python
logging.basicConfig(level=logging.DEBUG, format='%(asctime)s - %(name)s - %(levelname)s - %(message)s', datfmt='%m/%d/%Y %H:%M:%S')

# level=logging.WARNING : si on veut afficher seulement les choses aussi graves qu'un warning
# format='%(asctime)s - %(name)s - %(levelname)s - %(message)s' : format du string retourné sous forme de "texte ... %(paramètre)string ... "
# datfmt='%m/%d/%Y %H:%M:%S' : format de la date en string
```

## Change logging name (root is the default one)
```python
# In a new file with the debug name wanted ex: helper.py
logger = logging.getLogger(__name__)

# In main file
import helper
```

## Log file

### StreamHandler - pour afficher

#### Création
```python
stream_h = logging.StreamHandler()
```

### FileHandler - pour stocker dans un fichier

#### Création
```python
file_h = logging.FileHandler('file.log')
```

### Formatter - format stocké sous forme de string pouvant être attribué

#### Création
```python
formatter = logging.Formatter('%(name)s . %(levelname)s - %(message)s')
```
#### Attribution
```python
stream_h.setFormatter(formatter)
file_h.setFormatter(formatter)
```

### Méthode addHandler() - permet d'ajouter au logger des handlers qui "l'écoutent"
```python
logger.addHandler(stream_h)
logger.addHandler(file_h)

# Maintenant, si on lance un message
logger.warning('warninnng')
logger.error('errrror')

# Le warning et l'erreur s'afficheront dans le log
# L'erreur sera écrite dans le fichier 'file.log'
```

## Fichier logging.conf / logging.ini

### Création : créer un fichier nommé logging.conf ou logging.ini

### Importation
```python
import logging.config
```

### Exemple de contenu du fichier (se reférer à la doc pour plus d'infos à ce sujet)
```ini
[logger_simpleExample]
level=DEBUG
formatter=simpleFormatter
args=(sys.stdout,)
```

### Attribution de la config au logger
```python
logging.config.fileConfig('logging.conf')
```

### Récupération d'un logger depuis le fichier
```python
logger = logging.getLogger('simpleExample')

# On peut maintenant simplement appeler le log et il sera formaté et aura la config définie
logger.debug('debuuuuuug')
```

## Dict Config

### Création : créer un fichier nommé logging.conf ou logging.ini

### Importation
```python
import logging.config
```

### Exemple de contenu du fichier (se reférer à la doc pour plus d'infos à ce sujet)
```ini
  file:
    class : logging.handlers.RotatingFileHandler
    formatter: precise
    filename: logconfig.log
    maxBytes: 1024
    backupCount: 3
```

## Logging des Exceptions

### Utilisation standard dans une exception
```python
except IndexError as e:
    logging.error(e)
```

### Ajout de la stack traceback
```python
except IndexError as e:
    logging.error(e, exc_info=True)
    
     # Va afficher la stack avant l'erreur
```

### Stack traceback avec une exception inconnue
```python
except:
    logging.error("L'erreur est %s", traceback.format_exc())
    
# Va logger la stack et le type d'erreur
```

## RotatingFileHandler - Crée un nouveau fichier de log après avoir atteint une certaine limite et écrase les vieux fichiers par les nouveaux - bien pour les grosses applications

### Importation
```python
from logging.handlers import RotatingFileHandler
```

### Création
```python
handler = RotatingFileHandler('app.log', maxBytes=2000, backupCount=5)

# Lorsque le fichier atteint 2kb, alors il crée un nouveau fichier
# Si beaucoup de messages, alors crée app.log, app.log.1, app.log.2, ..., app.log.5, puis les écrit à nouveau quand arrivé à la fin d'app.log.5
```

### Attribution
```python
logger.addHandler(handler)
```


## TimedRotatingFileHandler - Crée un nouveau fichier de log après une certaine intervalle et écrase les vieux fichiers - bien pour les grosses applications

### Importation
```python
from logging.handlers import TimedRotatingFileHandler
```

### Création
```python
handler = TimedRotatingFileHandler('app.log', when='m', interval=3, backupCount=7)

# Crée à toutes les 3 minutes un nouveau fichier
# Crée app.log."date actuelle", puis les écrit à nouveau quand arrivé à 7 fichiers
```

### Attribution
```python
logger.addHandler(handler)
```

# JSON

## Exemple de fichier JSON
```json
{
    "firstName": "Joe",
    "lastName": "Doe",
    "hobbies": ["running", "swimming", "singing"],
    "age": 28,
    "hasChildren": true,
    "children": [
        {
            "firstName": "Doae",
            "age": 5
        },
        {
            "firstName": "Joae",
            "age": 7
        }
    ]
}
```

## Conversion des types : JSON - Python

| Python           | JSON             |
|:---------------- | ----------------:|
| dict             | object           |
| list, tuple      | array            |
| str              | string           |
| int, long, float | number           |
| True             | true             |
| False            | false            |
| None             | null             |

## Conversion de contenu JSON / Python

### Importation
```python
import json
```

###

### De Python à JSON

#### Création d'un dict de données en Python
```python
mydata = {"nom": "Joe", "age": 25, "passions": ["Piano", "Animaux"]}
```

#### Transformer le dict en string JSON
```python
# Formate mydata en string JSON
mydataJSON = json.dumps(mydata)

# Définit le niveau d'indentation. Si pas affiché, retourne une simple ligne formattée en JSON
mydataJSON = json.dumps(mydata, indent=4)

# Les fins de lignes seront '; ' et les séparateurs de clés seront '= '
# En JSON : "nom"= "Joe";
mydataJSON = json.dumps(mydata, indent=4, separators=('; ', '= '))

# Les clés seront triées par ordre alphabétique
mydataJSON = json.dumps(mydata, indent=4, separators=('; ', '= '), sort_keys=True)
```

#### Transformer le dict en fichier json
```python
# Ouvre le fichier JSON en "write"
with open('file.json', 'w') as file:
    json.dump(mydata, file, indent=4)
```

### De JSON à Python

#### Transformer un string JSON en dict
```python
mydata = json.loads(mydataJSON)
```

#### Transformer un fichier JSON en dict
```python
# Ouvre le fichier JSON en "read"
with open('file.json', 'r') as file:
    json.load(file)
```

### Classe custom
```python
class User:
    def __init__(self, name, age):
        self.name = name
        self.age = age

mydata = User('Joe', 24)
```

Si on essaie de convertir User en JSON ou du JSON en User, une erreur s'affiche.
Pour remédier à cela, il faut créer un encodeur pour passer de User à JSON et un décodeur pour passer de JSON à User.



### Encodeur
```python
# Paramètre : user
def encoder(z):
    if isinstance(z, User):
        # Retourne un string formatté en JSON
        return {'nom': z.nom, 'age': z.age, z.__class__.__name__: True}
    else:
        raise TypeError(f"Object of type '{z.__class__.__name__}' is not JSON serializable")
        
# Va utiliser notre encodeur par défaut lors de la conversion en JSON
mydataJSON = json.dumps(mydata, default=encoder)
```

### Encodeur importé

#### Importation
```python
from json import JSONEncoder
```

#### Implémentation
```python
class Encoder(JSONEncoder)
    def default(self, o):
        if isinstance(z, User):
            # Retourne un string formatté en JSON
            return {'nom': z.nom, 'age': z.age, z.__class__.__name__: True}
        return JSONEncoder.default(self, o)
```

#### Appel avec json.dumps()
```python
mydataJSON = json.dumps(mydata, clas=Encoder)
```

#### Appel avec la méthode .encode()
```python
mydataJSON = Encoder().encode(mydata)
```

### Décodeur - passer de JSON à la classe User

#### Implémentation
```python
# Le paramètre est un dictionnaire, qui est le format de base de conversion JSON à Python
# Si le dict contient le nom de la classe User, alors il a bien été converti et on le retourne sous un format de User
# Sinon, on retourne simplement le dictionnaire
def decode(dct):
    if User.__name__ in dct:
        return User(nom=dct['nom', age=dct['age']])
    return dct
```

#### Appel avec json.loads()
```python
mydata = json.loads(mydataJSON, object_hook=decode_user)
```

# Nombres aléatoires

## Module "Random" - pseudo random, pas sécuritaire

### Importation
```python
import random
```

### Utilisation standard
```python
# Retourne un float aléatoire entre 0 et 1
a = random.random()
```

### Range spécifique

#### Float
```python
# Retourne un float aléatoire entre 1 et 10
a = random.uniform(1, 10)
```

#### Int
```python
# Retourne un int aléatoire entre 1 et 10
# 1 et 10 sont inclus
a = random.randint(1, 10)
```

#### Int - limite supérieure exclue
```python
# Retourne un int aléatoire entre 1 et 10
# 1 et 10 ne sont pas inclus
a = random.randrange(1, 10)
```

### Variante normale : f(x) = σ²  + μ
```python
# μ  : 0
# σ² : 1
a = random.normalvariante(0, 1)
```

### Élément aléatoire dans une liste
```python
# Retourne un élément de la liste aléatoire
mylist = list("GABSPEIUFS")
a = random.choice(mylist)
```

### Plusieurs éléments aléatoires dans une liste
```python
# Retourne trois éléments de la liste aléatoire
mylist = list("GABSPEIUFS")
myrandomlist = random.choices(mylist, k=3)
```

### Mélanger une liste
```python
# Retourne la liste dont les éléments sont mélangés aléatoirement
mylist = list("GABSPEIUFS")
myshuffledlist = random.shuffle(mylist)
```

### Méthode random.seed()
```python
# Set la seed
random.seed(1234)
random.random() # return 0.2651234
random.random() # return 0.7251235

# Set la seed à nouveau : les opérations seront les mêmes
random.seed(1234)
random.random() # return 0.2651234
random.random() # return 0.7251235
```

## Module "Secrets" - sécuritaire, utilisé pour mots de passes, clés, ... - plus lent que le module "Random"

### Importation
```python
import secrets
```

### Range spécifique

#### Int - limite supérieure exclue
```python
# Retourne un entier en dessous de 10, le 10 est exclu
a = secrets.randbelow(10)
```

#### Bits
```python
# Retourne un nombre entre 0 et 15
# Paramètre : nombre de bits -> 1 1 1 1 = 8 + 4 + 2 + 1 = 15
a = secrets.randbits(4)
```

### Élément aléatoire dans une liste
```python
# Retourne un élément de la liste aléatoire
mylist = list("GABSPEIUFS")
a = secrets.choice(mylist)
```

## Module "Numpy" - pratique pour les tableaux

### Importation
```python
# Le "as np" signifie qu'on peut l'appeler sous le nom de np
import numpy as np
```

### Création d'un tableau de nombres aléatoires

#### Tableau à une dimension
```python
# Retourne un tableau de 3 cases contenant des floats aléatoires entre 0 et 1
myarray = np.random.rand(3)
```

#### Tableau à deux dimensions
```python
# Retourne un tableau de 3x4 cases contenant des floats aléatoires entre 0 et 1
myarray = np.random.rand(3, 4)
```

#### Float
```python
# Retourne un tableau de 3x4 cases contenant des floats aléatoires entre 0 et 1
myarray = np.random.rand(3, 4)
```

#### Int
```python
# Retourne un tableau de 3x4 cases contenant des entiers aléatoires entre 0 et 10
myarray = np.random.randint(0, 10, (3, 4))
```

### Mélanger un tableau
```python
# Retourne un tableau mélangé
# La méthode ne mélange que l'index et pas les valeurs
np.random.shuffle(myarray)
```

### Méthode numpy.random.seed() - à utiliser à la place de random.seed()
```python
# Set la seed
np.random.rand(3,4)

# Set la seed à nouveau : les opérations seront les mêmes
np.random.seed(1234)
np.random.rand(3, 4)
```

# Décorateurs

# Générateurs

# Threading vs Multiprocessing

# Multithreading

# Multiprocessing

# Arguments de fonction

# L'astérisque(*)

# Shallow vs Deep Copying

# Context Managers

















































































































d
