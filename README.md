# AI-automation
Tout faire avec l'IA. Elle fait le boulot sous votre contrôle et vous forme à comprendre comment tout ça fonctionne.

L'idée est de construire pas à pas une "baquette magique" apte à tout faire. Nous nous bornerons à vous indiquer:
- Les bons outils à utiliser,
- Comment bien poser votre problème
- Comment apprendre cette nouvelle façon de travailler , en comprenant comment la magie opére.



## Les incontournables utilisables sans rien automatiser. 

- [Mieux vaut regarder les benchmarks pour choisir](https://klu.ai/glossary/mmlu-pro-eval)
<img src="https://github.com/jpbrasile/AI-automation/assets/8331027/57f69c6d-9505-4b23-82a7-eee9025e392e" width="600" />




- Donc utiliser **Sonnet 3.5** et **GPT-4o** pour avoir les meilleures réponses à nos questions.
- [**Perplexity**](https://www.perplexity.ai/) est un autre incontournable pour surfer sur le web ( que nous contournerons quand même plus tard ! 😊)
- [**Harpa**](Harpa.ai) permet d'interagir avec une page web ou une video YouTube  
- Je vous laisse le soin de tester ces différents logiciels qui même dans leurs versions gratuites amélioreront sensiblement votre productivité.

## Les incontournables pour automatiser:
- Les mêmes (ou leur équivalent) accessibles à l'intérieur d'un code Python. 
- Des outils produisant et mettant en oeuvre le code à notre place
- Des outils pour produire automatiquement des vidéos qui nous servirons à apprendre ce que fait l'IA
- Des outils pour [appeler des fonctions externes](https://gorilla.cs.berkeley.edu/leaderboard.html)
<img src="https://github.com/jpbrasile/AI-automation/assets/8331027/084708bc-b8f1-469e-94bd-32d48cc6cf50" width="600" />

## Architecture générale:
<img src="https://github.com/jpbrasile/AI-automation/assets/8331027/17a47369-f026-46b6-a11c-0dc0d48f35de" width="600" />

- Le coeur du système, les **LLM** (Large language model)  recoivent du texte, le traite et fournissent du texte en retour. Le texte d'entrée doit être tel qu'il exprime clairement et concrètement nos attentes (c'est le prompting)
- Le texte en retour peut être formaté pour correspondre à une réponse de type texte brut, JSON,  markdown, HTML , code , API ... suivant le post processing envisagé.

## Création automatique d'une API web qui peut effectuer deux opérations mathématiques :

- Additionner deux nombres
- Multiplier deux nombres

- L'application doit être conteneurisée avec Docker pour faciliter son déploiement et son exécution.
- Vous voulez un guide étape par étape pour créer cette application, en partant de zéro, sans aucun outil préinstallé sur votre ordinateur.
- L'objectif final est de pouvoir non seulement créer cette application, mais aussi de pouvoir la partager facilement. 
- Vous voulez que n'importe qui puisse la télécharger et la lancer sur son propre ordinateur, quelle que soit sa configuration.
- Vous avez besoin d'instructions claires sur comment lancer l'application et comment la reproduire sur un autre PC.
- [**Dialogue avec sonnet 3.5** pour mettre en oeuvre la solution en "manuel"](https://claude.ai/chat/a71daeb6-5875-4ecb-9dc6-7dce126afde0) 
- Nous verrons plus tard comment automatiser la mise en plac de ce type d'application en automatique avec AIDER
  
## Faisons le tutoriel correspondant sous forme de vidéo
- L'idée est de partir de la synthèse récapitulée par sonnet 3.5 de notre programme précédent pour en faire un tuto.
- Pour cela on établit un [dialogue avec sonnet 3.5](https://claude.ai/chat/08fb3cc8-5cb4-45ed-9132-953e30ecf792) pour dégrossir le problème:
    - Pour créer les planches HTML support,
    - Le texte des voice over,
    - Le prompt pour produire les images
    - Le code python pour stocker ces données dans des répertoires
    - Le code python créant les MP3 et les images et qui les stockent
    - Le code python qui fait l'assemblage
- Ce dégrossissage montre qu'il est préférable d'avancer pas à pas en construisant et validant pas à pas le code python correspondant, ce que nous allons faire maintenant avec un nouveau thread sonnet 3.5.
1. Créer un code python permettant de dialoguer avec sonnet 3.5
  - On utilisera Visual Studio Code pour la mise en oeuvre et pour tester les codes
  - On utilisera anaconda pour créer un environnement logiciel spécifique. Nous utiliserons l'environnement teambot déjà créer avec `conda activate teambot` dans un terminal 
  - On crée un répertoire de travail video-maker dans lequel on met le fichier .env avec nos clefs API, ainsi que les fichiers requirements.txt et anthropic-api-hello-world.py créer par sonnet 3.5
  - Le dialogue fonctionne :
    
```bash
(base) PS C:\Users\test\Documents\AI_Automation\video_maker> conda activate teambot

(teambot) PS C:\Users\test\Documents\AI_Automation\video_maker> python anthropic-api-hello-world.py
Claude dit: [TextBlock(text='Bonjour !', type='text')]
```

2. [**Création d'une vidéo à partir d'un texte**](https://claude.ai/chat/c33dece9-e5ab-4206-98c6-de644cb1d731)  
- Ce projet automatise la création de vidéos éducatives à partir de contenu textuel, utilisant diverses technologies et APIs. Le processus se déroule en plusieurs étapes intégrées dans un script Python unique :
  - Conversion du texte :
    - Lit le contenu du fichier PLACE_HOLDER_TEXTE_VIDEO.txt.
    - Utilise l'API Claude d'Anthropic pour convertir le texte en structure JSON de diapositives.
  - Traitement des diapositives :
    - Génère un fichier HTML structuré avec CSS intégré pour chaque diapositive.
    - Crée un texte de voix off avec Claude.
    - Produit une image illustrative via l'API DALL-E d'OpenAI.
    - Génère un fichier audio de la voix off avec l'API Text-to-Speech d'OpenAI.
  - Création des vidéos :
    - Capture une image du HTML rendu avec Selenium.
    - Combine l'image et l'audio en utilisant MoviePy pour chaque diapositive.
  - Agrégation finale :
    - Assemble toutes les vidéos individuelles en une seule vidéo.
    - Ajoute des transitions entre les diapositives.



Le projet utilise Python avec diverses bibliothèques (BeautifulSoup, Requests, Pillow, MoviePy) et APIs (Anthropic, OpenAI). Cette approche intégrée offre une solution complète et efficace pour la production automatisée de contenu vidéo éducatif, de la conversion du texte à la création de la vidéo finale.
