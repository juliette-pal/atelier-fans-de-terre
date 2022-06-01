# Le site internet de Fans De Terre
## Le projet
Faire une refonte (renouveller) le site de Fans de Terre.  
### Objectifs  
- Proposer un site plus intutif qui correspond mieux aux besoins des utilisateurs
- Faciliter la vie de Monika (gestionnaire du site)  
### La méthode
- **Privilégier l'autonomie** de Monika en proposant un accompagnement pour qu'elle ait la main sur son site VS un site dévelloper seulement par un proffessionnel ne facilitant pas l'accès pour les non-iniciés et où chaque modification doit être effectuée par le dévelloppeur.
- **Faire un site orienté utilisateur**, utiliser les retours d'expériences des utilisateurs pour définir les fonctionnalités à prioriser et mettre en place un suivi pour améliorer le site constament.
- **S'inspirer des méthodes agiles pour travailler à plusieurs**, mise en place d'un point de suivi du projet chaque semaine, prioriser les actions ensemble, faire du pair-programming
## le choix des technologies
- **Trouver une alternative aux CMS classique** (comme Wordpress, Joomla, ...) en utilisant :
  - **Github pages**, pour l'hébergement et le travail collaboratif.
  - **Jekyll (générateur de site statique)**, permet d'avoir un site très léger. Tout le code écrit est utile, peu de superflue !
  - **Markdown (laguage raccourcie du HTML) pour une prise en main rapide et simple**, Monika s'est rapidement familiarisé avec l'écriture markdown, ce qui lui a permit d'ajouter du contenu dès le début de dévelloppement du site.

## Questions de démarrage

### Pourquoi tu veux faire ce site internet ?
  - Pour avoir de la visibilité afin de remplir les cours et les stages
  - Me faire connaitre en tant que céramiste, faire connaitre les intervenants et leurs productions

### Pourquoi une refonte ?
  - proposer un site responsive (aujourd'hui la navigation n'est pas confortable)
  - pour améliorer l'expérience utilisateur
  
### Hypothèses des problèmes des utilisateurs sur le site actuel
- On imagine que les personnes ne trouvent pas l'information sur les places disponibles sur un stage donné
- Les utilisateurs auraient besoin d'un complément d'information sur le déroulement du stage
- Certains utlisateurs aimeraient peut-être payer en ligne

### Pour qui on fait ce site ?
  - personnes qui veulent faire des stages de céramique en région parisienne (découvrir la technique)
  - personnes qui cherche un stage de raku en région parisienne (50/50 découverte et approfondissement)
  - professionnel qui veulent proposer de découvrir le raku à leurs élèves
  - personnes qui veulent pratiquer régulièrement la technique de la céramique proche de chez eux (cours)
  - personnes qui veulent offrir un stage de céramique
 
 ## Retour utilisateurs
 - Besoin d'avoir accès rapidement aux informations des stages (info, dates, places restantes, réglement)
 
 ## Exemple de site d'atelier de poterie
[Atelier Mercier](https://www.ateliermercier-ceramique.com/cap-tournage)
=> style épuré (photo, simple), 1er bar de navigation, efficace
[Terre et Feu](https://www.terre-et-feu.com/paris/cours-de-ceramique-paris/)
[Le Bol](https://le-bol.fr/cours-de-poterie-en-ligne/)
=> Plus chaud, plus fun, beaucoup de texte, plus difficile à trouver l'info

# Les points techniques
## Dimension des images
### Image verticale (qu'on retrouve le plus souvent dans les pages /stages) - <id: image_stage> 
Dimension : 900 × 1200 px   
Format : Jpeg   
poids : > 100 ko (les compresser avant de mettre sur le site si elles sont trop lourdes)
Outil sympa pour redimensionner : https://squoosh.app/  

## Installation de Jekyll : travailler en local

On regarde la documentation : https://jekyllrb.com/docs/installation/ubuntu/ et on suit les étapes car Juliette est sur une nouvelle machine.

```terminal
sudo apt-get install ruby-full build-essential zlib1g-dev
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
gem install jekyll bundler
```

Puis on se met dans le dossier du dépôt et on termine l’installation du site :

```terminal
bundle install
```

Enfin on peut lancer le site :

```terminal
bundle exec jekyll serve
```
