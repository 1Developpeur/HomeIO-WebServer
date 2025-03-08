# Politique de Sécurité

## À Propos de ce Projet

HomeIO WebServer est une interface web simple pour contrôler le simulateur Home IO. Comme il s'agit d'une application web locale qui communique uniquement avec un simulateur sur la même machine, les risques de sécurité sont limités.

## Communication avec le Simulateur

- L'application communique uniquement avec le simulateur Home IO via `localhost:9797`
- Aucune donnée sensible n'est stockée ou transmise
- Les requêtes sont effectuées en local uniquement

## Bonnes Pratiques

Pour les développeurs contribuant au projet :

1. Respectez les conventions de nommage du projet
2. Maintenez le code propre et bien documenté
3. Testez vos modifications avant de les soumettre
4. Vérifiez que les appels API sont correctement formatés

## Signaler un Problème

Si vous rencontrez un problème avec l'interface ou sa communication avec le simulateur :

1. Vérifiez que le simulateur Home IO est bien en cours d'exécution
2. Vérifiez que le port 9797 est bien accessible
3. Créez une issue dans le dépôt GitHub en utilisant le template de bug

## Contact

Pour toute question concernant le projet, n'hésitez pas à ouvrir une issue dans le dépôt GitHub. 
