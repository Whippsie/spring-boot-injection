# Spring Boot Injection
Comment on peut avoir des injections, ici SQL et javascript sur un projet Spring


EXPLOIT envoyer <script>alert("Connard")</script>

EXPLOIT envoyer '); DELETE FROM APPMESSAGE; --


Injection SQL : la plupart du temps des systèmes vieux avec SQL direct.
Se repose sur le fait que les développeurs contruise la requête en faisant le + de morceaux à eux
et de morceaux de l'utilisateur. 
Prévenu par PreparedStatement, ORM, la plupart des plateformes modernes

Injections JS : 
On utilise un petit bout de Javascript en espérant qu'il s'affiche sur les pages
On peut l'éviter en désactivant toutes les strings qui rentrent dans la BD pour JS (très safe)
La plupart des frameworks web ne font pas confiance aux données quand elles sont insérées dans la page (Vue, Angular etc.)


Conclusion :  Pas trop dur d'éviter les problèmes, utilise les frameworks
qui font bien attention.



