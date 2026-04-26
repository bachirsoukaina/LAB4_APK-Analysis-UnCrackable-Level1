# LAB4 - UnCrackable Level 1

## Ce que j'ai fait

J'ai analysé une application Android appelée UnCrackable-Level1.apk pour trouver un secret caché.

## Le secret que j'ai trouvé

**I want to believe**

## Infos sur l'application

- Nom du package : sg.vantagepoint.uncrackable1
- Permissions : aucune
- Composant exporté : MainActivity

## Les problèmes de sécurité que j'ai trouvés

### 1. Clé AES visible dans le code (Grave)
La clé de chiffrement est écrite en clair. N'importe qui peut la voir avec un décompilateur.

**Solution :** Valider le mot de passe sur un serveur, pas dans l'application.

### 2. La détection root se contourne facilement (Moyen)
L'application vérifie si le téléphone est rooté mais on peut enlever ces vérifications.

**Solution :** Utiliser SafetyNet de Google.

### 3. Le secret est stocké dans l'APK (Grave)
Même chiffré, le secret est dans l'application. On peut le déchiffrer.

**Solution :** Ne jamais mettre de secret dans l'application.

## Auteur

Soukaina Bachir

