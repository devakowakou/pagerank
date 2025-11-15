Voici un README.md clair et professionnel pour votre projet PageRank :

```markdown
# PageRank Algorithm Implementation

Implémentation Python de l'algorithme PageRank utilisé par les moteurs de recherche pour classer l'importance des pages web.

## 📋 Description

Ce projet implémente deux méthodes pour calculer le PageRank :
1. **Méthode d'échantillonnage** : Simulation d'un "surfeur aléatoire" suivant les liens entre les pages
2. **Méthode itérative** : Calcul mathématique direct utilisant la formule de PageRank

## 🚀 Installation et Exécution

### Prérequis
- Python 3.6 ou supérieur

### Utilisation

```bash
# Cloner le repository
git clone <votre-repo>
cd pagerank

# Exécuter avec un corpus de pages web
python pagerank.py corpus0
python pagerank.py corpus1
python pagerank.py corpus2
```

### Structure des corpus
Chaque corpus doit contenir :
- Des fichiers HTML (`.html`)
- Des liens entre les pages via des balises `<a href>`

## 📊 Exemple de Résultat

```
PageRank Results from Sampling (n = 10000)
  1.html: 0.2223
  2.html: 0.4303
  3.html: 0.2145
  4.html: 0.1329

PageRank Results from Iteration
  1.html: 0.2202
  2.html: 0.4289
  3.html: 0.2202
  4.html: 0.1307
```

## 🧠 Fonctionnalités Implémentées

### 1. `transition_model(corpus, page, damping_factor)`
Retourne la distribution de probabilité pour la prochaine page visitée par un surfeur aléatoire.

### 2. `sample_pagerank(corpus, damping_factor, n)`
Calcule le PageRank par échantillonnage de chaîne de Markov.

### 3. `iterate_pagerank(corpus, damping_factor)`
Calcule le PageRank par itération de la formule mathématique jusqu'à convergence.

## ⚙️ Paramètres

- **`DAMPING = 0.85`** : Facteur d'amortissement (probabilité de suivre un lien)
- **`SAMPLES = 10000`** : Nombre d'échantillons pour la méthode Monte Carlo
- **`THRESHOLD = 0.001`** : Seuil de convergence pour la méthode itérative

## 📁 Structure du Projet

```
pagerank/
├── pagerank.py          # Code principal
├── README.md            # Ce fichier
├── corpus0/             # Corpus de test 1
│   ├── 1.html
│   ├── 2.html
│   ├── 3.html
│   └── 4.html
├── corpus1/             # Corpus de test 2
└── corpus2/             # Corpus de test 3
```

## 🧪 Tests

```bash
# Vérifier la correction du code
check50 ai50/projects/2024/x/pagerank

# Vérifier le style du code
style50 pagerank.py
```

## 📚 Contexte Théorique

L'algorithme PageRank est basé sur le modèle du "surfeur aléatoire" :
- Un surfeur commence sur une page aléatoire
- À chaque étape, il suit un lien avec probabilité `d`
- Ou saute à une page aléatoire avec probabilité `1-d`
- Le PageRank d'une page est la probabilité stationnaire que le surfeur s'y trouve

## 👨‍💻 Auteur

Développé dans le cadre du cours d'Intelligence Artificielle.

## 📄 Licence

Ce projet est destiné à un usage éducatif.
```

## Pour créer et utiliser ce README :

1. **Créez le fichier** :
```bash
nano README.md
```

2. **Copiez-collez le contenu ci-dessus**

3. **Ajoutez-le à Git** :
```bash
git add README.md
git commit -m "Add comprehensive README file"
```

4. **Vérifiez le rendu** :
```bash
cat README.md
```

