# btn_component
Un simple composant bouton en Vue 3
Ce code Vue.js présente un composant réutilisable (buttonComponent) représentant un bouton et démontre son utilisation dans un composant principal (App.vue).

# Structure du code

## Template (template) :

**Bouton simple :** Un bouton avec le texte de la props d'origine.

**Bouton simple :** Un bouton avec le texte "Je suis un bouton" est affiché directement.

**Bouton dynamique :** Une boucle v-for parcourt un tableau de boutons (buttons) et affiche un buttonComponent pour chaque élément. Le texte du bouton est défini dynamiquement à l'aide de v-bind:modelValue (ou sa forme abrégée :modelValue). L'attribut key est utilisé pour que Vue puisse suivre efficacement les éléments de la liste et effectuer les mises à jour nécessaires.

## Script (script) :

**Import du composant :** Le composant buttonComponent est importé d'un fichier séparé pour une meilleure organisation.

**Définition du composant principal :** Le composant App est défini :

**name:** Donne un nom au composant pour faciliter l'identification.

**components:** Enregistre le composant buttonComponent comme un composant enfant.

**data:** Définit les données du composant, notamment le tableau buttons contenant les informations pour chaque bouton (ID et texte).

## Styles (style) :

Définit les styles CSS pour l'élément racine de l'application (#app), tels que la police, l'alignement du texte et les marges.
Fonctionnement détaillé
**Le composant buttonComponent** : Ce composant définit la structure et le comportement de base d'un bouton. Il peut accepter des props pour personnaliser son apparence, son comportement ou simplement son texte.

## Le composant App :
Affiche un bouton simple en utilisant directement buttonComponent.
Utilise une boucle **v-for** pour créer plusieurs boutons à partir du tableau buttons.
Chaque bouton affiche le texte correspondant à l'élément actuel de la boucle grâce à **v-bind:modelValue**.
