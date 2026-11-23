# Tech Explorer

Application pédagogique en un seul fichier (`index.html`) : HTML + CSS + JS, sans dépendance ni appel réseau.

## Lancer sur ton Mac (terminal)
```bash
mkdir -p ~/Projets/tech-explorer && cd ~/Projets/tech-explorer
mv ~/Downloads/index.html ~/Downloads/README.md .
open index.html                      # ouverture directe dans le navigateur
python3 -m http.server 8000          # ou serveur local : http://localhost:8000
git init -b main && printf ".DS_Store\n" > .gitignore
git add . && git commit -m "Tech Explorer : première version"
code .                               # ouvre VS Code (voir ci-dessous si la commande est introuvable)
```
Commande `code` introuvable : dans VS Code, `Cmd+Shift+P` puis « Shell Command: Install 'code' command in PATH ». Sinon : `open -a "Visual Studio Code" .`

## Déployer sur Vercel
```bash
brew install node                    # si npm n'est pas installé
npm i -g vercel
vercel login
vercel --prod                        # Framework : Other, pas de build
```
Ou : pousser le dépôt sur GitHub puis l'importer sur vercel.com (Build Command et Output Directory vides).

## Couleurs et thème
Toutes les couleurs sont des variables CSS en haut du fichier (`:root`, version sombre dans `@media (prefers-color-scheme:dark)`). Le thème noir et blanc est le bloc `:root[data-theme="nb"]`. Le bouton « Thème » de la barre d'actions bascule entre les deux.

## Ajouter un scénario (Authentification, Attaques, Sécurisation)
Ajouter un objet dans le tableau `AUT`, `ATK` ou `SEC` :
```js
{name:'Nom',sub:'Sous-titre',desc:'…',kv:[['Clé','Valeur'],…x4],atk:'Défense ou attaque',t:null,
 nodes:{a:['Nom','adresse','rôle (mode enfant)',x,y,'--amb'], b:[…]},   // composants séparés
 steps:[['a','b','PROTO','Info courte',ms,octets,'Titre','Explication','Texte décodé'],…],
 k:{desc:'…',kv:[…],atk:'…',e:['une explication enfant par étape',…]}}
```
Puis ajouter les noms professionnels des étapes dans l'objet `TIT` (clé = nom du scénario).

## Ajouter un algorithme ML
Ajouter un objet dans `ML` : `name, sub, desc, kv, trap, cols`, puis `init()`, `step()` (qui fait `this.rows.push({c:[cellules], d:'détail du calcul'})`) et `draw()` (SVG). Utiliser `rng(graine)` pour rester reproductible.

## Pistes d'évolution
Mode « rejouer en attaquant », Random Forest, PCA, projet Mobile Money fraude, 3 sujets ML restants (Transformer, Whisper/WER, LLM), onglet Architecture.
