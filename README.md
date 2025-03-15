# Sql-Projet-Bibliotheque
##  📚 Ce projet propose une base de données MySQL pour une bibliothèque imaginaire. Il permet de gérer les utilisateurs, les livres, les auteurs, les catégories de livres et les emprunts.

### *Création de la Base de Données :*
Pour ce projet, j'ai créé une base de données en SQL, grâce à [ce code :](bibliotheque.sql)
  

### *Structure de la Base de Données :*
Tables principales :  
- Utilisateurs : gère les membres de la bibliothèque.    
- Auteurs : contient les informations des auteurs.  
- Catégories : contient les différents types de catégorie de livre et leur prix.  
- Livres : les différentes informations sur le livre
- Emprunts : historique des emprunts de livres par les membres de la bibliothèque.
  
<br>

### *Requêtes possible une fois la Base de Données téléchargée*
- Lister tous les livres disponibles : SELECT * FROM Livres;
- Ajouter un nouvel utilisateur : INSERT INTO Utilisateurs (nom, prenom, email, date_inscription) VALUES ('Dupont', 'Jean', 'jean.dupont@example.com', CURDATE());
- Voir les livres les plus empruntés : SELECT Livres.titre, COUNT(Emprunts.id_emprunt) AS nombre_emprunts FROM Emprunts JOIN Livres ON Emprunts.id_livre = Livres.id_livre GROUP BY Livres.id_livre ORDER BY nombre_emprunts DESC LIMIT 10;
- Supprimer un utlisateur et ses emprunts : DELETE FROM Utilisateurs WHERE id_utilisateur = 2;

<br>

### *Conclusion :*  
En créant cette petite base de données, j'ai pu approfondir mes compétences en SQL et requêtes SQL.   
Cela m'a permis une meilleur compréhension des bases de données en général.   
Pour continuer ce projet, je pourrais intégrer cette base de données à une interface utilisateur et automatiser certaines tâches pour améliorer l'expérience utilisateur et le gestion des emprunts !!
