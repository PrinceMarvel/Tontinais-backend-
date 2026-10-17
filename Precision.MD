Depuis la toute première ligne de code jusqu'à la fin du projet :

1. Encodage et typographie (Zéro tolérance sur les accents) :
   - Écris tous les fichiers sources (.js, .jsx, .ts, .tsx, .json, etc.) strictement en encodage UTF-8 natif.
   - Respecte scrupuleusement l'orthographe, les accents et les accords de la langue française. Aucun mot ne doit être tronqué ou amputé d'accent : jamais de "changee" pour "changée", "confirmee" pour "confirmée", "validees" pour "validées", "parametre" pour "paramètre", etc.
   - Porte une attention rigoureuse à la ponctuation et aux caractères spéciaux : gestion correcte des parenthèses, guillemets, et apostrophes (notamment l'échappement en JSX via `{\'\'}` ou `&apos;` quand nécessaire).

2. Intégrité de l'affichage (React & React Native / Expo) :
   - Pour les projets Web (React, Vite, Next.js) : veille à ce que le document racine comporte impérativement `<meta charset="UTF-8" />` et l'attribut `<html lang="fr">`.
   - Pour React Native / Expo : encapsule toujours le texte dans le composant `<Text>` et vérifie que toute police personnalisée (custom font) intégrée supporte explicitement le jeu de caractères Latin / Latin Extended (glyphes français complets : é, è, ê, à, â, ç, ï, œ, etc.).
   - Si des données textuelles proviennent d'une source externe mal encodée (API/mock), normalise-les ou utilise les échappements Unicode standard (`\u00E9`, etc.).

3. Gestion du design et couleurs :
   - Aucune couleur codée en dur (hardcoded hex, rgb ou nom de couleur) dans les composants ou styles en ligne.
   - Utilise systématiquement le design system, le fichier de constantes/thème centralisé ou les classes utilitaires dédiées du projet.
