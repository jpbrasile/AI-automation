Voir la section [2. Créer un code python permettant de dialoguer avec sonnet 3.5](2-**créer-un-code-python-permettant-de-dialoguer-avec-sonnet-3.5**)

__***Avec le monde d'avant l'IA on apprenait à faire puis on faisait. Avec le monde d'aujourd'hui on fait faire à l'IA, puis on apprend à partir de ce que l'IA a fait, on finit donc par savoir faire aussi. Du coup plus besoin de prof, il ne suffit que de vouloir faire pour parvenir à nos fins !! The sky is the limit !!!***__

**TO DO  ⬜ / DONE ✅** / en cours ⚙️
| Outils       | Briques de teambot       | TO DO  ⬜ |
|-------------------|-------------------|-------------------|
| - Prompting ✅| - Site web sur Github (7) ✅      | Traitement d'images |
| - Docker  ✅| - Simple API locale (1) ✅      | Speech to text via python |
| - Github ✅| - Programmation no code (AIDER) (4) ✅      |- Web scrapping via python ⬜      |
| - GPT-4o ✅| -  LLM api en local (LM Studio)       |- RAG via python ⬜      |
| - Anthropic chat & API (Sonnet 3.5) ✅| - Text to speech via python   ✅     |-  GPTs    |
| - Perplexity   ✅|- Text to vidéo via python (3)    ✅       |-  Agents    |
| - Comfyui   ✅| - Tutoriel video automatique     |- Function calling (Gorilla)    |
| - Copilot ✅| -  Création d'images consistantes  ✅    |- Text to CAD (9) ⚙️      |
| - Anaconda ✅| - Création de tutoriel vidéo  ✅       |- Serveur local     |
| - Hedra ✅ | - Vidéo-livre narratif généré à partir de texte (8) ⚙️     |- Remote PC (Kaggle)     |
| - Mistral| - LLM via python (2)  ✅      |-  LLM en //     |
| - Deepseek | - Text to image local (6)   ✅     |-  Open interpreter ⬜  |
|- [Groq](https://groq.com/) ✅ |-   |-   |
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
- **Copilot de Microsoft**
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

1. ## Création automatique d'une API web qui peut effectuer deux opérations mathématiques :

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
2. **Créer un code python permettant de dialoguer avec sonnet 3.5**
  - On utilisera Visual Studio Code pour la mise en oeuvre et pour tester les codes
  - On utilisera anaconda pour créer un environnement logiciel spécifique. Nous utiliserons l'environnement teambot déjà créer avec `conda activate teambot` dans un terminal 
  - On crée un répertoire de travail video-maker dans lequel on met le fichier .env avec nos clefs API, ainsi que les fichiers requirements.txt et anthropic-api-hello-world.py créer par sonnet 3.5
  - Le dialogue fonctionne :
    
```bash
(base) PS C:\Users\test\Documents\AI_Automation\video_maker> conda activate teambot

(teambot) PS C:\Users\test\Documents\AI_Automation\video_maker> python anthropic-api-hello-world.py
Claude dit: [TextBlock(text='Bonjour !', type='text')]
```

3. [**Création d'une vidéo à partir d'un texte**](https://claude.ai/chat/c33dece9-e5ab-4206-98c6-de644cb1d731)  
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

4. **Point d'étape:**
- Nous avons réussi à mettre en oeuvre une applicatoin complexe sans coder une seule ligne. Cependant ce faisant nous avons détecté des pistes pour augmenter encore notre productivité
  - **Automatiser les itérations de débuggage** , ce qui nous a fait perdre le plus de temps dans la mise au point du code
  - Passer à l'open source, en particulier pour la création d'image qui constitue le poste de dépense le plus élevé pour la création d'une vidéo
  - Faire du web scraping pour voir si notre problème n'est pas déjà résolu par ailleurs
 
5. **Coding assistant: AIDER+Sonnet**
- On crée le répertoire ```coding_assistant``` et on lance ```conda activate teambot```
- On suit les [instructions d'installation](https://github.com/paul-gauthier/aider) 
- Mais il faut l'adapter au terminal powershell :```$env:ANTHROPIC_API_KEY="sk... "```
- AIDER répond à nos directives et adapte en conséquence un repository qui a été cloné localement.
- Il conserve un logbook des actions entreprises (```.aider.chat.history.md```) et un LLM comme Sonnet 3.5 ou GPT-4o peut alors en faire la synthèse:
  ```J'ai eu des problèmes qui ont été résolu dans le document joint, fais en la synthèse```

6. [**Text to image local dans docker**](https://claude.ai/chat/f8d04905-3570-4f00-b7e9-f220936ff540)
- Il faut "alimenter" comfyui en y rajoutant les chkpoints requis à placer dans le répertoire : ```C:\Users\test\Documents\AI_Automation\coding_assistant\comfyui\storage\ComfyUI\models\checkpoints```
- Il n'y a pas de consensus clair sur un seul « meilleur » point de contrôle pour ComfyUI, car cela dépend beaucoup de vos préférences personnelles et du type d'image que l'on souhaite générer. Cependant, plusieurs points de contrôle sont fréquemment recommandés pour leur qualité :
  - SDXL (Stable Diffusion XL) : C'est un modèle de base très performant, particulièrement bon pour le réalisme et la qualité générale des images.
  - Juggernaut XL : Souvent cité comme l'un des meilleurs pour le photoréalisme
  - Dreamshaper : Apprécié pour sa polyvalence et sa qualité, particulièrement dans sa version Turbo
  - Vision réaliste : Excellent pour générer des humains réalistes.
  - RealVis XL : Également recommandé pour le photoréalisme
- La génération d'images peut se faire via une requête API comme le montre  [basic_api_exemple.py](https://claude.ai/chat/f8d04905-3570-4f00-b7e9-f220936ff540)
7. [**Créer son site en ligne avec Github**:

Pour mettre en place un site personnel avec GitHub Pages, voici les étapes que vous devez suivre :

1. [**Créez un compte GitHub** :]([https://chatgpt.com/c/2a5fd138-49c0-42bb-a057-a831e6dbc5ea](https://chatgpt.com/c/37b0d84b-d7bd-4455-b5ae-44082f81226c))
- Il faut créer un dépot public sur Github
- Créez un fichier `index.html` avec un contenu ```<html><head><title>Mon Site</title></head><body><h1>Bonjour Monde JPB !</h1></body></html>```
- Le cloner en local ```git clone https://github.com/jpbrasile/github.io```
- **Publiez vos modifications** :
     - Ajoutez les fichiers modifiés à votre dépôt :
       ```
       git add --all
       ```
     - Faites un commit des modifications :
       ```
       git commit -m "Initial commit"
       ```
     - Poussez les modifications sur GitHub :
       ```
       git push -u origin main
       ```
  - Il faut faire "sign in with a code" pour parvenir à valider le push
    
  Une fois ces étapes terminées, votre site sera en ligne à l'adresse [https://username.github.io/github.io/](https://jpbrasile.github.io/github.io/).

  8- **Créer un story teller automatique**
- La première étape consiste à produire des images consistantes afin que les personnages ou objets reproduits sur plusieurs diapositives soient quasi-identiques:
  - Nous avons créé un "méta-prompt" qui à partir d'un descriptif simple <situation> fournit des images consistantes:
  - Méta-prompt:

```
Prompt_Structure:
{scene_setting}. {entity1_name} ({entity1_traits}) {action1} {object1_name} ({object1_traits}). {entity2_name} ({entity2_traits}) {action2}. {atmosphere}

Definitions:
- scene_setting: Brief description of location and context
- entity1_name: Identifier for the first entity (e.g., man_1, woman_1, dog_1)
- entity1_traits: age, physical_appearance, clothing
- action1: Main action of entity1
- object1_name: Identifier for the main object (e.g., watch_1, map_1)
- object1_traits: material, distinctive_features, size
- entity2_name: Identifier for the second entity
- entity2_traits: age, physical_appearance, clothing/characteristics
- action2: Main action of entity2
- atmosphere: General ambiance and shared activity

Instructions:
1. Replace each element with specific details consistent with the provided <situation>.
2. Maintain coherence between entities, their actions, and the context.
3. Use unique identifiers for entities and objects to facilitate reference and reuse.

Example:
Cafe_table_1 in a bustling coffee shop. Man_1 (25 years old, short brown hair, white shirt and blue jeans) carefully examines Watch_1 (antique gold, floral engravings, normal size). Woman_1 (70 years old, gray hair in a bun, red floral dress and round glasses) leans forward with interest. They are absorbed in their animated conversation.
```
- Sonnet a réalisé le prompt spécifique à partir de ```<situation> A man walking his dog in the forest```
```
Forest_trail_1 in a lush, shadowy woodland with dappled sunlight. Man_1 (45 years old, salt-and-pepper hair, rugged stubble, green waterproof jacket and khaki hiking pants) studies Map_1 (weatherproof paper, colorful trail markings, slightly creased) while striding purposefully. Dog_1 (6 years old, German Shepherd, glossy black and tan coat, red nylon collar with tags) trots eagerly ahead, nose twitching at the scent of pine and earth. They are enveloped in a serene atmosphere of natural exploration, with a gentle breeze rustling through the canopy above.
``` 
  - Voilà le résultat fournit par copilot pour la création d'image avec copilot:
![image](https://github.com/jpbrasile/AI-automation/assets/8331027/497bf3b4-b95d-451a-8775-1c99a2f5ac5d)
  - et avec leonardo.ai (qui oublit la carte et met le "collier rouge" sur le vieil homme) :
![image](https://github.com/jpbrasile/AI-automation/assets/8331027/ed959f12-0774-472a-950f-e810baa0c861)



  - La deuxième étape consiste à avoir le script de la vidéo, c'est à dire tous les éléments textuels qui permettront la création automatique de la vidéo.  


9. **Text to CAD**
- Sonnet 3.5 semble être capable de créer un [programme python capable de générer des formes complexes](https://claude.ai/chat/91026ba9-f74b-4622-b215-3148ada38543)
-  Par ailleurs [CadQuery](https://github.com/CadQuery/cadquery) semble intéressant à évaluer 
🛠️ CadQuery : Module Python intuitif pour créer des modèles paramétriques 3D.
✍️ Scripts courts : Écrire des scripts simples pour produire des modèles de haute qualité.
🆚 Comparaison OpenSCAD :
📜 Utilise Python : Accès à de nombreuses bibliothèques et IDE.
🔧 Noyau OCCT : Plus puissant que CGAL, supporte NURBS, splines, import/export STEP.
⏱️ Scripts concis : Moins de code nécessaire grâce à des fonctionnalités de positionnement avancées.
🚀 Génération rapide : Crée des fichiers STL, STEP, AMF et 3MF plus rapidement.
💻 Intégration facile : Conçu comme bibliothèque Python sans GUI, idéal pour serveurs et scripts scientifiques.
🛡️ Avantages :
🔄 Modèles paramétriques facilement personnalisables.
🖨️ Sortie de formats CAD de haute qualité (STEP, DXF, etc.).
🧩 Assemblages imbriqués à partir de pièces individuelles.
🚀 Version 2.0 :
🔄 Basée sur OCCT : Plus de contrôle et de flexibilité, malgré une complexité accrue.
