# AutoLoc — Atelier Associations

Ce projet reprend l'Atelier 1 et ajoute les associations JPA du diagramme fourni.

## Associations implémentées

- `Agence 1 ---- * Employe`
- `Agence 1 ---- * Vehicule`
- `Vehicule 1 ---- * Maintenance`
- `Vehicule * ---- * Equipement` (table de jointure `vehicule_equipement`)
- `Vehicule 1 ---- * Reservation`
- `Client 1 ---- * Reservation`
- `Reservation 1 ---- 1 Contrat`
- `Contrat 1 ---- * Paiement` (composition : `cascade = ALL`, `orphanRemoval = true`)

## Tables attendues

Les 9 entités génèrent 9 tables, et l'association ManyToMany
`Vehicule <-> Equipement` génère une table de jointure supplémentaire :

1. agence
2. employe
3. vehicule
4. maintenance
5. equipement
6. client
7. reservation
8. contrat
9. paiement
10. vehicule_equipement

Donc **10 tables applicatives** sont attendues.

## Procédure demandée par l'atelier

1. Démarrer MySQL.
2. Dans `application.properties`, mettre temporairement :
   `spring.jpa.hibernate.ddl-auto=create`
3. Lancer `AutolocApplication`.
4. Vérifier la création des tables et des clés étrangères dans `autoloc_db`.
5. Arrêter l'application.
6. Remettre :
   `spring.jpa.hibernate.ddl-auto=update`

Le fichier livré est déjà remis à `update`, conformément à la dernière consigne.

## Configuration MySQL

Par défaut :
- utilisateur : `root`
- mot de passe : `root`
- base : `autoloc_db`
- port application : `8081`

Vous pouvez remplacer les identifiants via les variables d'environnement
`DB_USERNAME` et `DB_PASSWORD`.
