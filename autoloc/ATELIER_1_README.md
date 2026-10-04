# AutoLoc — Atelier 1 / Séance 2 terminé

Ce projet contient le socle Spring Boot demandé par l'atelier et les **9 entités JPA sans associations** :

- Vehicule
- Agence
- Client
- Employe
- Equipement
- Reservation
- Contrat
- Paiement
- Maintenance

Énumérations présentes :

- StatutVehicule
- CategorieVehicule
- RoleEmploye
- StatutReservation
- ModePaiement

## Configuration MySQL

Le fichier `src/main/resources/application.properties` utilise :

- Base : `autoloc_db`
- Utilisateur par défaut : `root`
- Mot de passe par défaut : `root`
- Port de l'application : `8081`

Le mot de passe peut être remplacé sans modifier le fichier :

```powershell
$env:DB_PASSWORD="votre_mot_de_passe"
```

Puis lancer l'application depuis IntelliJ ou avec :

```bash
./mvnw spring-boot:run
```

Sous Windows :

```powershell
.\mvnw.cmd spring-boot:run
```

Hibernate créera/mettra à jour automatiquement les tables grâce à `spring.jpa.hibernate.ddl-auto=update`.

> Conformément à l'atelier, aucune association JPA n'a été ajoutée. Elles seront traitées à l'Atelier 2.
