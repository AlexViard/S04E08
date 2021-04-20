Écrire une requête pour récupérer les données... Pas toutes, hein, limitez à une quinzaine de lignes
1) SELECT * FROM viewing LIMIT 15; 

Écrire une requête pour sélectionner toutes les données, rangées dans un ordre aléatoire
2) SELECT * FROM viewing ORDER BY random();

Écrire une requete pour récupérer 15 lignes de manière aléatoire
3) SELECT * FROM viewing ORDER BY random() LIMIT 15;

la moyenne d'age des viewers, classée par pays.
4) SELECT viewer_country, AVG(viewer_age_group) FROM viewing GROUP BY viewer_country;

le nombre d'épisodes regardés, classé par tranche d'âge, et rangé par tranche d'age décroissant.
5) SELECT viewer_age_group, SUM(episode) as episode FROM viewing GROUP BY viewer_age_group ORDER BY viewer_age_group DESC;
    SELECT viewer_age_group, SUM(episode) as episode FROM viewing WHERE binge_session = 't' GROUP BY viewer_age_group ORDER BY viewer_age_group DESC; (binge session = true)