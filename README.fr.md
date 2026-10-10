# Votre première contribution open source 🇨🇲

**Langues :** [English](README.md) | Français

Faites votre première contribution open source en vous ajoutant aux
**[Page des contributeurs d'OSS Cameroon](https://osscameroon.github.io/firstcontributions/)**.
Vous pourrez ensuite y répertorier les issues et les pull requests auxquelles vous participez, quel que soit le projet open source.

Il vous suffit d'un [compte GitHub](https://github.com/signup). Tout se passe sur le site GitHub :
vous n'avez donc pas besoin d'installer quoi que ce soit ni d'utiliser la ligne de commande.

## Ajoutez-vous (environ 5 minutes)

1. **[Cliquez ici pour créer votre fichier](https://github.com/osscameroon/firstcontributions/new/main/contributors?filename=YOUR-GITHUB-USERNAME.yml&value=github%3A+YOUR-GITHUB-USERNAME%0Aname%3A+Your+Name%0A%23+The+lines+below+are+optional.+Replace+the+example+values+or+delete+the+lines.%0Abio%3A+A+short+sentence+about+you.%0Alocation%3A+Your+city%2C+Country%0Awebsite%3A+https%3A%2F%2Fexample.com%0Acontributions%3A%0A++%23+Later%2C+list+issues+or+pull+requests+you+worked+on%2C+one+per+line%2C+like+this%3A%0A++%23+-+https%3A%2F%2Fgithub.com%2Fosscameroon%2Fjs-generator%2Fpull%2F1%0A).**
   GitHub ouvre un éditeur avec un fichier déjà rempli de valeurs d'exemple.
   Vous pouvez également saisir votre nom d'utilisateur sur [le site web](https://osscameroon.github.io/firstcontributions/) et
   cliquez sur **Add me** (M’ajouter) pour renseigner automatiquement votre nom d’utilisateur.
2. **Nommez le fichier d'après votre nom d'utilisateur GitHub.** Dans la zone située en haut, remplacez `YOUR-GITHUB-USERNAME` par votre nom d'utilisateur,
   par exemple `contributors/octocat.yml`. Conservez l'extension `.yml` à la fin.
3. **Saisissez vos informations.** Remplacez les valeurs d'exemple par les vôtres. Seuls `github` et `name` sont obligatoires ; supprimez donc
   les lignes dont vous n'avez pas besoin :

   ```yaml
   github: octocat
   name: Mona Lisa Octocat
   bio: Je développe des applications web et j'apprends le Go.
   location: Yaoundé, Cameroun
   website: https://octocat.dev
   contributions:
   ```

4. **Cliquez sur le bouton vert _Commit changes…_, puis sur _Propose changes_.** GitHub crée votre propre copie du projet
   (un _fork_) et y enregistre votre fichier.
5. **Cliquez sur _Create pull request_** à deux reprises. C'est votre première contribution 🎉

Un robot vérifie votre fichier dans la minute qui suit et laisse un commentaire sur votre pull request. Si une correction est nécessaire, le commentaire
vous indique ce qu'il faut modifier et comment procéder. Une fois votre pull request fusionnée, votre profil apparaît sur le site web
quelques minutes plus tard.

## Listez vos contributions open source

Chaque fois que vous ouvrez une « issue » ou une « pull request » dans un projet open source, vous pouvez l'ajouter à votre profil :

1. Ouvrez votre fichier : `https://github.com/osscameroon/firstcontributions/blob/main/contributors/<your-username>.yml`
   (ou cliquez sur **Is this you? Add a contribution** sur votre page de profil).
2. Cliquez sur l'icône en forme de crayon ✏️ pour le modifier.
3. Ajoutez le lien sous `contributions:`, sur une ligne distincte, en commençant par deux espaces et un tiret :

   ```yaml
   contributions:
     - https://github.com/osscameroon/js-generator/pull/42
     - https://github.com/nodejs/node/issues/12345
   ```

4. Cliquez sur **Commit changes…**, puis sur **Propose changes** et enfin sur **Create pull request**.

Le site web affiche le titre de chaque élément ainsi que son statut (ouvert, fusionné ou fermé) et se met à jour quotidiennement.

## Champs

| Champ           | Obligatoire | Description                                                       |
| --------------- | ----------- | ----------------------------------------------------------------- |
| `github`        | oui         | Votre nom d'utilisateur GitHub. Il doit correspondre au nom du fichier. |
| `name`          | oui         | Votre nom (jusqu'à 80 caractères).                                |
| `bio`           | non         | Une courte phrase vous concernant (jusqu'à 280 caractères).       |
| `location`      | non         | Votre localisation, par ex. `Douala, Cameroun`.                   |
| `website`       | non         | Un lien commençant par `https://`.                               |
| `contributions` | non         | Liens vers des tickets (issues) ou des pull requests GitHub sur lesquels vous avez travaillé, un par ligne. |

## Problèmes courants

- **« Vous ne pouvez ajouter ou modifier que votre propre fichier. »** : le nom du fichier doit correspondre à votre nom d'utilisateur GitHub (par ex. `contributors/octocat.yml`).
- **« YAML invalide »** : chaque ligne doit respecter le format `champ: valeur`. Chaque élément de la section `contributions` doit commencer par deux espaces
  et un tiret : `  - https://...`.
- **Le fichier ne se trouve pas dans le dossier `contributors`** : supprimez-le et recommencez en utilisant le lien de l'étape 1.

Pour corriger votre pull request, ouvrez l’onglet **Files changed** (Fichiers modifiés), cliquez sur **⋯** à côté de votre fichier, puis sur **Edit file** (Modifier le fichier).

Vous êtes bloqué ? Demandez de l'aide en laissant un commentaire sur votre pull request. Quelqu'un de la communauté vous aidera.

---

## Pour les responsables du projet

- **Site web :** `npm run build` génère un site statique dans `dist/` à partir de `contributors/*.yml`. Le
  [workflow de déploiement](.github/workflows/deploy.yml) le publie sur GitHub Pages à chaque *push* vers la branche `main`, ainsi qu'une fois par jour pour
  actualiser le statut des tickets (*issues*) et des demandes de tirage (*pull requests*). Dans _Settings → Pages_, réglez **Source** sur **GitHub Actions**.
- **Vérifications des pull requests :** [check-contribution.yml](.github/workflows/check-contribution.yml) valide les fichiers modifiés et
  ajoute un commentaire indiquant le résultat. Il utilise `pull_request_target`, ce qui lui permet de s'exécuter sur les pull requests de nouveaux contributeurs sans nécessiter d'approbation préalable. Pour cette raison, il se contente d'analyser les fichiers YAML de la pull request sans jamais en exécuter le code. Veillez à maintenir ce fonctionnement.
  Les contributeurs ne peuvent modifier que leur propre fichier, tandis que les membres et collaborateurs peuvent modifier n'importe quel fichier.
- **Fusion automatique (facultatif) :** définissez la variable de dépôt `AUTO_MERGE` sur `true` (_Paramètres → Secrets et variables →
  Actions → Variables_) pour fusionner automatiquement les pull requests valides qui ne modifient que le fichier du contributeur auteur de la demande. Activez l'option
  _Paramètres → Actions → Général → Autoriser GitHub Actions à créer et approuver des pull requests_ si la fusion échoue.
- **Configuration :** le nom de la communauté, le dépôt et l'URL du site sont définis dans [site.config.mjs](site.config.mjs).
  Si vous changez de dépôt, mettez à jour le lien indiqué à l'étape 1 (`npm test` signale si celui-ci est obsolète).

### Développement en local

```sh
npm install
npm test                 # tests unitaires + vérification de chaque fichier de contributeur
npm run build:offline    # construire sans appeler l'API GitHub
npm run build            # construire à partir des titres d'issues/PR (définir GITHUB_TOKEN pour éviter les limites de débit)
python3 -m http.server -d dist 8000
```
