# Oracle-Tunning


**Q1. Quelle est l’utilisation du « Library cache » dans Oracle?**

A. Contient des informations sur l’utilisateur, telles que des privilèges d’utilisateur

**B. Utilisé pour stocker le shared SQL**

C. Contient les modifications apportées à la base de données  
D. Toutes les réponses sont vraies

***Reponse: B. Utilisé pour stocker le shared SQL*** 

**Q2. Quel(s) outil(s) de diagnostic utiliseriez-vous pour savoir quand ont eu lieu le dernier switch des fichiers de journalisation de la base de données?**  
E. Fichiers trace  
F. Fichier d'alertes  
G. Page d'accueil d'Enterprise Manager  
***H. Vues V$***

***Reponse: H. Vues V$***

**Q3. Quelles sont les informations du fichier d'alertes qui peuvent être utiles pour le réglage de la base de données?**  
**A. Temps nécessaire à l'archivage**  
B. Heures de début et de fin de la récupération d'instance  
C. Consommation de l’espace dans le cache des tampons  
**D. Erreurs de "verrou mortel" et de dépassement du temps imparti**  
**E. Points de reprise incomplets**

***Reponse: A,D,E***

**Q4. Lesquels des Outils ci-dessous, sont utilisés pour l’analyse et le réglage des performances?**  
A. Fichier de contrôle  
**B. Vues et tables dynamiques des performances**  
C. Fichier d'alertes  
**D. Fichiers trace**  
**E. AWR**

***Reponse: B,D,E***

**Q5. Le référentiel AWR (Automatic Workload Repository) est stocké dans le tablespace SYSAUX. Les clichés (snapshots) en constituent la partie persistante. Les informations incluses dans chaque cliché sont contrôlées par les éléments suivants :**  
A. Taille du tablespace SYSAUX  
**B. Valeur du paramètre STATISTICS_LEVEL**  
**C. Délai de conservation des clichés**  
**D. Intervalle de capture des clichés**

***Reponse: B,C,D***

**Q6. Un temps d'attente moyen supérieur à la normale sur un tablespace particulier peut avoir diverses causes :**  
**A. Matériel : Un fichier est stocké sur un lecteur lent ou dans une configuration RAID qui ne convient pas.**  
B. Système d'exploitation : Le système d'exploitation est occupé par d'autres fichiers du même lecteur ou de la même partition.  
C. Instance : Le tablespace a été créé avec des propriétés différentes de celles des autres tablespaces, d'autres fichiers de base de données du même disque ou de la même partition sont sollicités (les E/S ne sont pas équilibrées entre les lecteurs), ou les objets sollicités sont en majorité stockés dans le même tablespace, fichier ou disque.  
D. Application : L'application effectue trop d'E/S parce que l'optimiseur n'a pas choisi le chemin d'accès correct pour différentes raisons (statistiques périmées, index inefficaces).

***Reponse: A. Matériel : Un fichier est stocké sur un lecteur lent ou dans une configuration RAID qui ne convient pas.***

**Q7. La base de données présente des performances médiocres. Les utilisateurs se plaignent de la longueur des temps de réponse depuis que le traitement de fin de mois a commencé. Vous vérifiez que les événements les plus longs du rapport AWR comprennent des événements liés aux E/S et à la CPU. Vous examinez ensuite les statistiques temporelles Time Model. Elles indiquent que le temps base de données est consommé en majorité par l'exécution du code SQL. Quelle est la prochaine étape de diagnostic à effectuer ?**  
A. Examiner les statistiques SQL dans le référentiel AWR ou l'état Statspack  
**B. Examiner les instructions SQL triées par temps d'exécution dans les vues V$**  
C. Examiner les recommandations du moniteur ADDM (Automatic Database Diagnostics Monitor)  
D. Vérifier la configuration de la base de données à l'aide de l'outil de diagnostic à distance RDA (Remote Diagnostics Agent)

***Reponse: B. Examiner les instructions SQL triées par temps d'exécution dans les vues V$***

**Q8. Lequel des points suivants ne nécessitant pas un réglage de performances?**  
A. Instructions SQL inefficaces ou consommant beaucoup de ressources  
**B. Processus PMON**  
C. Structures mémoire sous-dimensionnées  
D. Problèmes d'E/S  
E. Problèmes de configuration de la base

***Reponse: B. Processus PMON***

**Q9. Laquelle des affirmations suivantes est correcte concernant la commande EXPLAIN PLAN?**  
**A. Elle génère un plan d'exécution pour l'optimiseur.**  
B. Elle stocke ce plan dans la table PLAN_TABLE.  
C. Cette commande est disponible sous SQL PLUS  
D. Elle exécute l’instruction proprement dite.

***Reponse: A. Elle génère un plan d'exécution pour l'optimiseur.***

**Q10. Quel est le nom de la zone de mémoire contenant des données et des informations des sessions utilisateur?**  
A. Zone de mémoire partagée  
B. Cache de tampons  
**C. PGA**  
D. Données de session utilisateur

***Reponse: C. PGA***

**Q11. Quels éléments sont lus dans les fichiers de données et placés dans le cache de tampons de la base ?**  
**A. Lignes**  
**B. Blocs**  
C. Modifications  
D. Instructions SQL

***Reponse: A,B***

**Q12. Laquelle des affirmations est incorrecte concernant le Processus PMON (Process Monitor) ?**  
A. Il effectue les opérations de récupération au démarrage de l'instance.  
B. Il résout automatiquement toutes les transactions équivoques.  
C. Il assure la récupération des processus utilisateur qui ont échoué.  
**D. Il écrit le tampon de journalisation dans un fichier de journalisation.**

***Reponse: D. Il écrit le tampon de journalisation dans un fichier de journalisation.***

**Q13. Quelles sont les affirmations incorrectes concernant la Fonction AUTOTRACE ?**  
**A. AUTOTRACE est une fonction de SQL*Plus et de SQL Developer.**  
B. Elle a besoin d'une table PLAN_TABLE.  
C. Elle nécessite le rôle PLUSTRACE pour extraire des statistiques de certaines vues V$.  
D. Par défaut, elle génère le plan d'exécution et des statistiques sans l'exécution d'une interrogation.  
E. Elle peut ne pas représenter le plan réel utilisé par l'optimiseur en cas d'examen des variables attachées.

***Reponse: A. AUTOTRACE est une fonction de SQL*Plus et de SQL Developer.***

**Q14. Identifier les bonnes réponses concernant la vue V$SQL_PLAN**  
**A. La vue V$SQL_PLAN permet d'examiner le plan d'exécution de curseurs qui se trouvent encore dans le cache "library".**  
B. Elle contient un plan différent de celui de la table PLAN_TABLE  
**C. Elle contient le plan d'exécution de tous les curseurs du cache "library".**

***Reponse: A,C***

**Q15. Laquelle des zones mémoires contribue à optimiser le temps de recherche des données par le processus serveur et d’éviter les accès au disque :**  
A. le cache de tampons (buffer cache) de la base de données  
B. la mémoire PGA  
C. le tampon de journalisation (redo log buffer)  
**D. la zone de mémoire partagée**

***Reponse: D. la zone de mémoire partagée***

**Q16. L'utilisateur doit bénéficier de privilèges spéciaux pour générer des statistiques via la fonction AUTOTRACE.**  
**A. Vrai**  
B. Faux  
C. Aucune réponse.

***Reponse: A. Vrai***

**Q17. Vous avez exécuté l'instruction suivante :  
SQL> EXPLAIN PLAN  
SET STATEMENT_ID = 'demo01' FOR  
SELECT e.last_name, d.department_name  
FROM hr.employees e, hr.departments d  
WHERE e.department_id = d.department_id;  
Quelles sont les trois affirmations vraies sur EXPLAIN PLAN ?**  
A. Le plan d'exécution est enregistré dans PLAN_TABLE sans exécuter la requête.  
**B. Le plan d'exécution de la requête est généré et affiché immédiatement en sortie.**  
C. Le plan d'exécution généré n'est pas nécessairement le plan d'exécution utilisé pendant l'exécution de la requête.  
**D. Le plan d'exécution est enregistré dans DBA_HIST_SQL_PLAN sans exécuter la requête.**  
**E. Le plan d'exécution généré peut être visualisé à l'aide de la fonction DBMS_XPLAIN.DISPLAY.**  
**F. Le plan d'exécution généré peut être récupéré à partir du Library cache à l'aide de la fonction DBMS_XPLAIN.DISPLAY.**

***Reponse: B,D,E,F***

**Q18. Le référentiel AWR permet de collecter et de traiter les statistiques suivantes :**  
**A. Les statistiques sur les objets, qui mesurent l'accès aux segments de base de données et leur utilisation.**  
**B. Les statistiques temporelles Time Model basées sur l'utilisation du temps pour les activités.**  
C. Quelques-unes des statistiques relatives au système et à la session, collectées dans les vues V$SYSSTAT et V$SESSTAT.  
**D. Les instructions SQL qui génèrent la plus grosse charge sur le système, en fonction de critères tels que le temps écoulé, le temps CPU, les succès en mémoire tampon (buffer gets), etc.**  
**E. Les statistiques sur le code applicatif**

***Reponse: A,B,D,E***

**Q19. Lors de l'examen du plan d'exécution de l'optimiseur, examinez les facteurs ci-après :**  
**A. La table directrice présente le meilleur filtre.**  
B. Le nombre de connexions réseau  
C. La mémoire consommée  
**D. Les vues sont correctement utilisées.**  
**E. Les produits cartésiens sont involontaires.**  
**F. L'accès aux tables est efficace.**

***Reponse: A,D,E,F***

**Q20. Une commande EXPLAIN PLAN exécute l'instruction et insère dans une table le plan utilisé par l'optimiseur.** 
A. Vrai
**B. Faux**  
C. Aucune

***Reponse: B. Faux***

**Q21. Laquelle des assertions suivantes relatives à la table PLAN_TABLE est-elle fausse ?**  
A. La table PLAN_TABLE est créée automatiquement pour recevoir la sortie de l'instruction EXPLAIN PLAN.  
**B. Vous ne pouvez pas créer votre propre table PLAN_TABLE.**  
C. La table PLAN_TABLE peut ne pas contenir le plan d'exécution réel.  
**D. La commande SQL réelle n'est pas exécutée.**

***Reponse: B,D***

**Q22. Une fois que la surveillance a démarré, une entrée est ajoutée à la vue _______. Cette entrée contient des mesures de performances clés collectées pour l'exécution.**  
**A. V$SQL_MONITOR**  
B. V$PLAN_MONITOR  
C. ALL_SQL_MONITOR  
D. ALL_SQL_PLAN_MONITOR

***Reponse: A. V$SQL_MONITOR***

**Q23. Quelle est l’affirmation correcte ?**  
A. MMON permet de reconstruire automatiquement les indexes de la base de données.  
B. MMON permet de générer le plan d’exécution des requêtes SQL  
**C. MMON permet de capturer automatiquement des données statistiques historiques, sans l'intervention du DBA**  
D. MMON gère automatiquement la taille de la mémoire SGA.

***Reponse: C. MMON permet de capturer automatiquement des données statistiques historiques, sans l'intervention du DBA***

**Q24. La fonction DISPLAY_CURSOR permet d’afficher le plan d’exécution provenant de :**  
A. La zone de de mémoire partagée ;  
B. La zone PGA ;  
C. Le référentiel AWR ;  
**D. La table plan_table ;**

***Reponse: D. La table plan_table ;***

**Q25. Quelles sont les méthodes d'affichage des plans d'exécution possibles?**  
**A. EXPLAIN PLAN**  
B. SQL Trace  
C. Fichier d’alerte  
D. Référentiel AWR  
**E. V$SQL_PLAN**  
**F. SQL*Plus AUTOTRACE**

***Reponse: E,F***

**Q26. Laquelle des méthodes d’affichage des plan d’exécution suivantes, n’exécute pas la requête ?**  
**A. EXPLAIN PLAN**  
B. SQL Trace  
C. Fichier d’alerte  
D. Référentiel AWR  
E. V$SQL_PLAN  
F. SQL*Plus AUTOTRACE.

***Reponse: A. EXPLAIN PLAN***

**Q27. Quand le processus «DBWn» écrit-il les données dans les fichiers de données ?**  
A. Après chaque validation de la transaction  
B. Avant valider la transaction  
**C. Après le processus «LGWR»**  
D. Avant ou après la validation de la transaction

***Reponse: C. Après le processus «LGWR»***

**Q28. Pour choisir un plan d'exécution pour une instruction, l'optimiseur doit prendre en considération les facteurs suivant:**  
**A. chemin d'accès**  
**B. ordre de jointure**  
C. chemin physique des fichiers de données  
**D. méthode de jointure**

***Reponse: A,B,D***

**Q29. On vous sollicite pour analyser une lenteur qui date d’un jour avant. Quelle est la meilleure source de données pour retrouver les requêtes consommatrices**  
A. EXPLAIN PLAN  
B. SQL Trace  
C. Fichier d’alerte  
**D. Référentiel AWR**  
E. V$SQL_PLAN

***Reponse: D. Référentiel AWR***

**Q30. Quand l’optimiseur procède à un Balayage complet de table?**  
**A. Absence d'index sur les tables**  
B. Quantité importante de données à extraire
C. Shared pool insuffisante ;
D. nombre insuffisant de DBWR.

***Reponse: A. Absence d'index sur les tables***
