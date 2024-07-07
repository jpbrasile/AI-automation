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
- Le texte en retour peut être formater pour correspondre à une réponse de type texte brut, JSON,  markdown, HTML , code , API ... suivant le post processing envisagé.

 

  
