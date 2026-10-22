# French Crosswordese Dictionary

**English first, version française complète plus bas.**

## The Short Words Of French Crosswords

Anyone who does crosswords in English knows OREO, ERA and EPEE. They show up again and again, not because people use them every day, but because their letters fit almost anywhere. Puzzle fans call this crosswordese.

French grids have their own set. ERG, ÉMEU, OSÉ, ÉPÉE, ÊTA, ÉTÉ, NOPAL, ORSEC... A *mots fléchés* regular meets them every week, often with the same clues. « Dune désert » gives ERG, « Rapide ratite vivant en Australie » gives ÉMEU, « Entre zêta et thêta » gives ÊTA.

This dataset lists the **2,000 short answers (2 to 5 letters) that come up most often** across tens of thousands of French clues. For each word you get how many distinct clues it answers and up to three real example clues. It is a small, clean word list that you can use in a game, a grid generator, a language course or a linguistics project.

The data comes from [La Petite Case](https://www.lapetitecase.fr), a free French website that helps people solve *mots fléchés* and *mots croisés*. Each clue there has its own page with every possible answer sorted by number of letters.

### What Is In The File

| | |
|---|---|
| Words | 2,000 |
| Length | 2 to 5 letters |
| Example clues | up to 3 per word, each one with a verified answer |
| Language | French |

| word_display | clue_count | example clues |
|---|---|---|
| BLEU | 68 | Couleur d'iris · Nouvel arrivé |
| NIAIS | 62 | Zozo · Serins |
| AS | 56 | Un cador · Personne douée · Boss des maths |
| DON | 51 | Chef de la mafia · Prêtre italien · Monsieur en espagnol |
| ÉMEU | 34 | Symbole de l'Australie |
| ERG | 29 | Paysage désert · Zone désertique |
| ORSEC | 5 | Plan d'urgence · Plan de sauvetage |

The top of the list is made of short, very polysemous words. BLEU can be a colour, a bruise, a rookie or a cheese. AS can be a playing card, an expert or a pilot. Further down you find the real grid specialists, such as animals from far away, Greek letters, rivers, chemical symbols, old units, Pyrenean valleys (OSSAU) and emergency plans (ORSEC).

### Columns

| column | description |
|---|---|
| `rank` | Rank by `clue_count`, 1 being the most frequent |
| `word` | Grid form, capitals A to Z, no accents |
| `word_display` | Correct spelling with accents (ÉMEU, GÊNÉ). Two spellings with the same grid form are two rows (GÊNE and GÊNÉ) |
| `length` | Number of letters, which is the number of cells |
| `clue_count` | Number of distinct clues for which the word is a strong answer |
| `example_clue_1` to `example_clue_3` | Real clues whose answer was checked by hand (can be empty) |

Read it with `pd.read_csv(path, keep_default_na=False)`. Otherwise pandas reads the word `NA` as a missing value.

### How It Was Built

We counted the strong, ranked answers of every clue published on La Petite Case and kept words of 2 to 5 letters. Example clues were kept only when a person had verified their answer. Words with fewer than two verified example clues were dropped, which removes most noise. Accents matter in French, so the list keeps them. GÊNE (the noun) and GÊNÉ (the participle) are two separate rows, even though they fill the same four cells.

### Ideas

- **Get better at mots fléchés.** Learn the first few hundred words and a large part of the short entries in a typical grid will look familiar.
- **Feed a grid generator.** Short fill words are the hardest part of building a grid. This list gives you correct spellings and real clue ideas.
- **Make word games.** Wordle-like games, quizzes, flash cards for French learners.
- **Do linguistics.** What makes a word grid-friendly? Look at vowel ratios, letter frequencies, polysemy, loanwords.
- **Combine it** with the companion dataset of 10,000 verified clues to study how short words are clued.

### License And Citation

**CC BY 4.0.** Use it, share it, adapt it, commercially or not. Just credit **La Petite Case** with a link to **[lapetitecase.fr](https://www.lapetitecase.fr)**.

```bibtex
@misc{lapetitecase_crosswordese_2026,
  title  = {Dictionnaire mots fl\'ech\'es, French crosswordese, the short words of French grids},
  author = {{La Petite Case}},
  year   = {2026},
  url    = {https://www.lapetitecase.fr},
  note   = {Hugging Face dataset}
}
```

Companion dataset, **[Mots Fléchés Définitions | French Crossword Clues](https://huggingface.co/datasets/lapetitecase/mots-fleches-definitions)**, 10,000 clues with verified answers.

---

### Try It And Find It Elsewhere

Browse these words in the free [French Crossword Solver](https://huggingface.co/spaces/lapetitecase/french-crossword-solver) Space, tab Petits Mots Des Grilles. The same data is also on [Kaggle](https://www.kaggle.com/datasets/cuivrax/dictionnaire-mots-fleches-french-crosswordese). Companion dataset, [Mots Fléchés Définitions](https://huggingface.co/datasets/lapetitecase/mots-fleches-definitions).

---

## Version Française

### Les Mots Courts Des Mots Fléchés

Quiconque fait des mots fléchés les connaît par cœur. ERG, ÉMEU, OSÉ, ÉPÉE, ÊTA, ÉTÉ, NOPAL, ORSEC... Ces mots reviennent sans cesse dans les grilles. Personne ne les emploie tous les jours, mais leurs lettres se casent presque partout. Les définitions aussi se répètent. « Dune désert » donne ERG, « Rapide ratite vivant en Australie » donne ÉMEU, « Entre zêta et thêta » donne ÊTA.

Ce jeu de données liste les **2 000 réponses courtes (2 à 5 lettres) les plus fréquentes** sur des dizaines de milliers de définitions de mots fléchés et de mots croisés. Pour chaque mot, on trouve le nombre de définitions différentes auxquelles il répond et jusqu'à trois vraies définitions en exemple. C'est un petit dictionnaire des mots fléchés, propre, qu'on peut utiliser dans un jeu, un générateur de grilles, un cours de français ou une étude linguistique.

Les données viennent de [La Petite Case](https://www.lapetitecase.fr), un site gratuit d'aide aux mots fléchés et aux mots croisés. Chaque définition y a sa page, avec toutes les solutions classées par nombre de lettres.

### Contenu Du Fichier

| | |
|---|---|
| Mots | 2 000 |
| Longueur | 2 à 5 lettres |
| Définitions en exemple | jusqu'à 3 par mot, toutes à la réponse vérifiée |
| Langue | français |

Le haut de la liste est fait de mots courts aux sens multiples. BLEU, c'est une couleur, une ecchymose, un débutant ou un fromage. AS, c'est une carte, un champion ou un pilote. Plus bas arrivent les vrais spécialistes des grilles, comme les animaux lointains, les lettres grecques, les cours d'eau, les symboles chimiques, les vieilles unités, les vallées pyrénéennes (OSSAU) et les plans de secours (ORSEC).

### Colonnes

| colonne | description |
|---|---|
| `rank` | Rang selon `clue_count`, 1 étant le plus fréquent |
| `word` | Forme de grille, majuscules de A à Z, sans accents |
| `word_display` | Bonne graphie avec accents (ÉMEU, GÊNÉ). Deux graphies de même forme de grille font deux lignes (GÊNE et GÊNÉ) |
| `length` | Nombre de lettres, donc de cases |
| `clue_count` | Nombre de définitions différentes dont le mot est une réponse sûre |
| `example_clue_1` à `example_clue_3` | Vraies définitions dont la réponse a été vérifiée à la main (parfois vides) |

Lisez-le avec `pd.read_csv(path, keep_default_na=False)`, sinon pandas prend le mot `NA` pour une valeur manquante.

### Construction

Nous avons compté les réponses sûres et classées de toutes les définitions publiées sur La Petite Case, puis gardé les mots de 2 à 5 lettres. Les définitions en exemple ne sont retenues que si leur réponse a été vérifiée par une personne. Les mots qui n'ont pas au moins deux exemples vérifiés sont écartés, ce qui retire l'essentiel du bruit. Les accents comptent en français, la liste les garde donc. GÊNE (le nom) et GÊNÉ (le participe) sont deux lignes, même s'ils remplissent les mêmes quatre cases.

### Idées D'Usage

- **Progresser aux mots fléchés.** Retenez les premières centaines de mots et une bonne partie des cases courtes d'une grille vous paraîtra familière.
- **Alimenter un générateur de grilles.** Les petits mots de remplissage sont le plus difficile à placer. Cette liste donne les bonnes graphies et de vraies idées de définitions.
- **Créer des jeux de lettres.** Jeux à la Wordle, quiz, cartes de révision pour apprendre le français.
- **Faire de la linguistique.** Qu'est-ce qui rend un mot bon pour la grille ? Part de voyelles, fréquence des lettres, polysémie, emprunts.
- **Croiser avec le jeu associé** de 10 000 définitions vérifiées pour voir comment on définit les mots courts.

### Licence Et Citation

**CC BY 4.0.** Vous pouvez utiliser, partager et adapter ces données, y compris pour un usage commercial, en citant **La Petite Case** avec un lien vers **[lapetitecase.fr](https://www.lapetitecase.fr)**.

Jeu associé, **[Mots Fléchés Définitions | French Crossword Clues](https://huggingface.co/datasets/lapetitecase/mots-fleches-definitions)**, 10 000 définitions et leurs solutions vérifiées.

### Essayer Et Retrouver Les Données

Ces mots se parcourent dans le Space gratuit [Solution Mots Fléchés](https://huggingface.co/spaces/lapetitecase/french-crossword-solver), onglet Petits Mots Des Grilles. Les mêmes données sont aussi sur [Kaggle](https://www.kaggle.com/datasets/cuivrax/dictionnaire-mots-fleches-french-crosswordese).


---

**Part of [Verbarium](https://github.com/verbarium)**, open word data for word games and language tools. Data by [La Petite Case](https://www.lapetitecase.fr/). Also on [Kaggle](https://www.kaggle.com/datasets/cuivrax/dictionnaire-mots-fleches-french-crosswordese) and [Hugging Face](https://huggingface.co/datasets/lapetitecase/dictionnaire-mots-fleches).
