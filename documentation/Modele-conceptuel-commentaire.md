
# Commentaire du modèle conceptuel – Les archéologues classiques

## Présentation générale

Ce modèle conceptuel organise les données relatives aux archéologues classiques actifs depuis le XIXème siècle à nos jours, dans le cadre de la problématique présentée dans le fichier problematique.md.

Il distingue plusieurs classes, notamment les personnes, les institutions, les lieux et les productions scientifiques. Les propriétés et les relations permettent de décrire les parcours des archéologues, leurs activités et leurs liens avec différentes institutions. 

Les informations proviennent principalement des notices bibliographiques de Wikipedia. Les cardinalités précisent le nombre de relations possibles entre les différentes classes : "1" désigne une occurence unique et "0..n" indique qu'aucune, une ou plusieurs occurences sont possibles.

## 1. ARCHÉOLOGUE / PERSONNE

### Définition

Cette classe constitue le centre du modèle conceptuel. Elle représente les individus appartenant à la population étudiée, à savoir les archéologues spécialisés dans l'étude des civilisations grecque et romaine antiques.

### Propriétés

- **Identifiant** : numéro unique permettant de distinguer chaque personne.
- **Nom** : nom de famille de l'archéologue.
- **Prénom** : prénom ou prénoms.
- **Genre** : genre de la personne, lorsque cette information est disponible.
- **Date de naissance** : date de naissance, complète ou partielle.
- **Date de décès** : date de décès, lorsqu'elle est applicable et connue.
- **Nationalité** : nationalité indiquée dans les sources.
- **Source** : référence de la notice biographique utilisée.

### Relations

La classe ARCHÉOLOGUE / PERSONNE est reliée à huit autres classes. Ces relations permettent de reconstituer les parcours individuels, les activités scientifiques et les réseaux professionnels des archéologues.

Les cardinalités précisent le nombre d'occurrences possibles : **« 1 »** signifie une seule occurrence, tandis que **« 0..n »** indique qu'aucune, une ou plusieurs occurrences sont possibles.

- **LIEU GÉOGRAPHIQUE** : chaque archéologue possède un seul lieu de naissance enregistré dans le modèle (1). Un même lieu géographique peut être associé à plusieurs archéologues, ou à aucun (0..n).

- **FORMATION** : un archéologue peut avoir suivi aucune, une ou plusieurs formations documentées (0..n). Chaque formation enregistrée est associée à un seul archéologue (1).

- **SPÉCIALISATION** : un archéologue peut posséder aucune, une ou plusieurs spécialisations documentées (0..n). Une même spécialisation peut concerner plusieurs archéologues, ou aucun (0..n).

- **APPARTENANCE** : un archéologue peut avoir aucune, une ou plusieurs appartenances institutionnelles documentées (0..n). Chaque appartenance enregistrée concerne un seul archéologue (1). 

- **POSTE / CARRIÈRE** : un archéologue peut avoir exercé aucun, un ou plusieurs postes professionnels documentés (0..n). Chaque poste enregistré est exercé par un seul archéologue (1). 

- **ACTIVITÉ DE TERRAIN** : un archéologue peut avoir participé à aucune, une ou plusieurs activités de terrain documentées (0..n). Chaque activité enregistrée est associée à un seul archéologue (1). 

- **CONTRIBUTION** : un archéologue peut avoir aucune, une ou plusieurs contributions scientifiques documentées (0..n). Chaque contribution est associée à un seul archéologue (1). Cette organisation permet de représenter plusieurs auteurs pour une même publication.

- **RELATION ENTRE PERSONNES** : un archéologue peut être impliqué dans aucune, une ou plusieurs relations professionnelles documentées (0..n). Chaque relation associe une personne source (1) et une personne cible (1). Cette distinction permet notamment de représenter les relations maître-élève et les collaborations scientifiques.

### Exemple : Ulrich Sinn

L'archéologue allemand **Ulrich Sinn**, né le 4 octobre 1945 à Bevensen, permet d'illustrer les relations entre la classe ARCHÉOLOGUE / PERSONNE et les huit autres classes du modèle conceptuel.

- **LIEU GÉOGRAPHIQUE** : Ulrich Sinn est né à Bevensen, en Allemagne. Cette ville constitue son lieu de naissance. Une personne possède un seul lieu de naissance enregistré (1), tandis qu'un lieu géographique peut être associé à plusieurs personnes (0..n).

- **FORMATION** : Ulrich Sinn a étudié l'archéologie classique, l'histoire ancienne et l'histoire de l'art à l'Université de Fribourg-en-Brisgau. Il a obtenu son doctorat en 1975. Ces informations permettent d'enregistrer ses études dans la classe FORMATION, elle-même reliée à la classe INSTITUTION. Un archéologue peut avoir plusieurs formations documentées (0..n), tandis que chaque formation enregistrée concerne une seule personne (1).

- **SPÉCIALISATION** : ses recherches portent notamment sur les sanctuaires grecs, particulièrement Olympie, ainsi que sur la sculpture architecturale, la peinture de vases et l'histoire du sport antique. Une personne peut posséder plusieurs spécialisations (0..n), et chaque spécialisation est associée à un seul archéologue (1).

- **APPARTENANCE** : Ulrich Sinn est devenu membre correspondant de l'Institut archéologique allemand en 1982. Cette information peut être enregistrée dans la classe APPARTENANCE, reliée à la fois à ARCHÉOLOGUE / PERSONNE et à INSTITUTION. Une personne peut avoir plusieurs appartenances (0..n), tandis que chaque appartenance enregistrée concerne une seule personne (1).

- **POSTE / CARRIÈRE** : Ulrich Sinn a notamment été assistant scientifique à l'Université de Bonn de 1979 à 1984, professeur d'archéologie classique à l'Université d'Augsbourg de 1992 à 1994, puis titulaire de la chaire d'archéologie classique à l'Université de Wurtzbourg de 1994 à 2011. Ces fonctions constituent différentes occurrences de la classe POSTE / CARRIÈRE, chacune étant reliée à une institution. Une personne peut avoir plusieurs postes (0..n), tandis que chaque poste enregistré est associé à une seule personne (1).

- **ACTIVITÉ DE TERRAIN** : Ulrich Sinn a participé à des fouilles en Italie méridionale et en Grèce, notamment à l'Héraion de Samos. Il a également dirigé des recherches sur Olympie à partir de 1985. Ces activités peuvent être enregistrées séparément et associées aux sites archéologiques concernés. Une personne peut participer à plusieurs activités de terrain (0..n), tandis que chaque activité enregistrée est associée à une seule personne (1).

- **CONTRIBUTION** : Ulrich Sinn est l'auteur de travaux scientifiques, notamment de sa thèse de doctorat de 1975 consacrée à la céramique hellénistique de Macédoine. Cette thèse peut être enrgistrée dans la classe PUBLICATION, tandis que son rôle d'auteur est représenté par une occurence de la classe CONTRIBUTION. Une personne peut être associée à aucune, une ou plusieurs contributions (0..n), tandis que chaque contribution enregistrée concerne une seule personne (1). Chaque contribution concerne également une seule publication (1), mais une publication peut être associée à pluseurs contributions (0..n), notamment lorsqu'elle possède plusieurs auteurs.

- **RELATION ENTRE PERSONNES** : la notice biographique indique que sa thèse de doctorat a été dirigée par **Walter-Henning Schuchhardt**. Cette information permet de représenter une relation de type « directeur de thèse – doctorant » entre les deux individus. Un archéologue peut être impliqué dans plusieurs relations documentées (0..n), tandis que chaque relation associe une personne source (1) et une personne cible (1).

Cet exemple montre comment les informations d'une même notice biographique peuvent être réparties entre plusieurs classes du modèle conceptuel. Il permet de reconstituer le parcours d'un archéologue en reliant ses origines, sa formation, ses institutions, ses activités scientifiques et ses relations professionnelles.

### Intérêt pour la recherche

Cette classe permettra de comparer les profils individuels et d'étudier les évolutions de la population selon les générations, le genre, la nationalité et les trajectoires professionnelles.

## 2. LIEU GÉOGRAPHIQUE

### Définition

Cette classe représente les lieux associés aux individus et aux institutions étudiés. Elle permet de distinguer les origines géographiques des archéologues et l'implantation des institutions.

### Propriétés

- **Nom** : nom du lieu.
- **Type** : catégorie du lieu, par exemple ville ou région.
- **Pays** : pays auquel appartient le lieu.
- **Latitude** : coordonnée géographique.
- **Longitude** : coordonnée géographique.

### Relations

La classe LIEU GÉOGRAPHIQUE est reliée à trois autres classes : ARCHÉOLOGUE / PERSONNE, INSTITUTION et SITE ARCHÉOLOGIQUE.

- **ARCHÉOLOGUE / PERSONNE** : un lieu géographique peut être associé à aucune, une ou plusieurs personnes (0..n), puisqu'il peut constituer le lieu de naissance de plusieurs archéologues. En revanche, chaque archéologue possède un seul lieu de naissance enregistré (1).

- **INSTITUTION** : un lieu géographique peut accueillir aucune, une ou plusieurs institutions (0..n), par exemple des universités, des musées ou des instituts archéologiques. Chaque institution est associée à un seul lieu géographique d'implantation (1).

- **SITE ARCHÉOLOGIQUE** : un lieu géographique peut être associé à aucun, un ou plusieurs sites archéologiques (0..n). En revanche, chaque site archéologique est localisé dans un seul lieu géographique enregistré (1).

Ces trois relations permettent de distinguer les lieux de naissance des archéologues, les lieux d'implantation des institutions et la localisation des sites archéologiques.

### Exemple

La ville d'Athènes peut être enregistrée dans la classe LIEU GÉOGRAPHIQUE. Elle peut ensuite être associée à plusieurs éléments du modèle :

- **ARCHÉOLOGUE / PERSONNE** : Athènes peut constituer le lieu de naissance d'un ou de plusieurs archéologues du corpus.

- **INSTITUTION** : Athènes est notamment le lieu d'implantation de l'École française d'Athènes, qui peut être enregistrée dans la classe INSTITUTION.

- **SITE ARCHÉOLOGIQUE** : Athènes peut également être associée à plusieurs sites archéologiques, notamment l'Agora antique et l'Acropole.

Cet exemple montre qu'un même lieu géographique peut être relié à plusieurs personnes, institutions et sites archéologiques, tout en permettant de distinguer la nature de ces relations.

### Intérêt pour la recherche

Cette classe permettra d'étudier la répartition géographique des origines et des institutions, ainsi que leur éventuelle concentration dans certains pays ou centres universitaires.

## 3. FORMATION

### Définition

Cette classe décrit les études et les formations suivies par les archéologues au cours de leur parcours académique. Elle permet de conserver plusieurs formations successives pour une même personne. Cette classe "formation" est donc reliée seulement à la classe "archeologue/personne".

### Propriétés

- **Discipline** : domaine d'études, par exemple archéologie classique, histoire ancienne, philologie ou histoire de l'art.
- **Diplôme** : qualification ou diplôme obtenu.
- **Début** : date de commencement de la formation.
- **Fin** : date d'achèvement.
- **Source** : référence permettant de documenter cette formation.

### Relations

Chaque formation est suivie par une personne. Une personne peut avoir suivi aucune, une ou plusieurs formations documentées dans le corpus.

### Exemple

Un archéologue peut avoir étudié la philologie classique avant de se spécialiser en archéologie grecque.

### Intérêt pour la recherche

Cette classe permettra d'étudier l'évolution des disciplines de formation et de déterminer si certains parcours académiques sont particulièrement fréquents selon les générations.

## 4. INSTITUTION

### Définition

Cette classe représente les établissements et organismes intervenant dans la formation, la carrière ou les réseaux professionnels des archéologues.

### Propriétés

- **Nom** : nom officiel de l'institution.
- **Type** : université, musée, institut archéologique, école spécialisée ou autre organisme.
- **Ville** : ville d'implantation.
- **Pays** : pays d'implantation.
- **Fondation** : date ou année de création de l'institution.

### Relations

La classe INSTITUTION est reliée à deux autres classes : LIEU GÉOGRAPHIQUE et APPARTENANCE.

- **LIEU GÉOGRAPHIQUE** : chaque institution est associée à un seul lieu géographique d'implantation (1). En revanche, un même lieu géographique peut accueillir aucune, une ou plusieurs institutions (0..n). Cette relation permet de localiser les établissements dans lesquels les archéologues ont étudié, travaillé ou entretenu des liens professionnels.

- **APPARTENANCE** : chaque institution est associée à une seule appartenance enregistrée (1), tandis qu'une appartenance peut concerner aucune, une ou plusieurs institutions (0..n). Cette relation permet de documenter les liens institutionnels des archéologues.

Ces deux relations permettent d'identifier la localisation des institutions et de reconstituer les réseaux d'appartenance institutionnelle des archéologues.

### Exemple

L'Institut archéologique allemand peut être enregistré dans la classe INSTITUTION. Le siège de l'Institut archéologique allemand se trouve à Berlin. L'institution est donc associée à un seul lieu géographique (1), tandis qu'un même lieu peut accueillir plusieurs institutions (0..n). L'archéologue Ulrich Sinn est devenu membre correspondant de l'Institut archéologique allemand en 1982. Cette information peut être enregistrée dans la classe APPARTENANCE. Selon les cardinalités actuelles du modèle, une institution est associée à une seule appartenance (1), tandis qu'une appartenance peut concerner plusieurs institutions (0..n).

Cet exemple montre comment une institution peut être localisée géographiquement et associée à plusieurs archéologues par l'intermédiaire de leurs appartenances institutionnelles.

### Intérêt pour la recherche

Cette classe permettra d'identifier les établissements les plus représentés dans les parcours des archéologues et d'étudier leur rôle dans la structuration du champ scientifique.

## 5. APPARTENANCE

### Définition

Cette classe décrit les liens d'appartenance entre un archéologue et une institution. Elle permet de représenter ces liens comme des relations éventuellement limitées dans le temps.

### Propriétés

- **Type** : nature de l'appartenance, par exemple membre, chercheur associé ou membre d'une académie.
- **Début** : date de début de l'appartenance.
- **Fin** : date de fin.
- **Source** : référence de l'information.

### Relations

La classe APPARTENANCE est reliée à deux autres classes : ARCHÉOLOGUE / PERSONNE et INSTITUTION.

- **ARCHÉOLOGUE / PERSONNE** : chaque appartenance enregistrée concerne un seul archéologue (1), tandis qu'un archéologue peut avoir aucune, une ou plusieurs appartenances institutionnelles (0..n). Ces appartenances peuvent être successives ou simultanées.

- **INSTITUTION** : selon les cardinalités du modèle, chaque institution est associée à une seule appartenance (1), tandis qu'une appartenance peut être associée à aucune, une ou plusieurs institutions (0..n).

### Exemple

Un archéologue peut devenir membre d'un institut archéologique pendant plusieurs années, puis rejoindre une académie scientifique.
Ces deux appartenances sont enregistrées séparément dans la classe APPARTENANCE, avec leur type, leurs dates de début et de fin et leur source. Chaque appartenance est reliée à un seul archéologue dans la classe ARCHÉOLOGUE / PERSONNE (1). Un archéologue peut ainsi posséder plusieurs appartenances institutionnelles (0..n). Chaque appartenance est également reliée à la classe INSTITUTION, afin d'identifier les organismes concernés.

### Intérêt pour la recherche

Cette classe permettra d'observer les réseaux institutionnels et leur évolution, notamment les appartenances multiples et les liens entre différents centres scientifiques.

## 6. POSTE / CARRIÈRE

### Définition

Cette classe décrit les fonctions professionnelles exercées par les archéologues durant leur carrière. Elle permet de distinguer les étapes successives de leur activité professionnelle.

### Propriétés

- **Fonction** : poste exercé, par exemple professeur, conservateur, directeur de musée ou chercheur.
- **Début** : date de prise de fonction.
- **Fin** : date de fin de fonction.
- **Source** : référence biographique.

### Relations

Chaque poste est exercé par une personne. Une personne peut avoir exercé plusieurs postes au cours de sa carrière.

### Exemple

Un archéologue peut avoir été conservateur dans un musée avant d'obtenir une chaire universitaire. Ces fonctions sont enregistrées comme deux étapes distinctes.

### Intérêt pour la recherche

Cette classe permettra de reconstituer les trajectoires professionnelles et d'étudier la place respective des universités, des musées et des autres activités scientifiques.

## 7. SPÉCIALISATION

### Définition

Cette classe décrit les domaines scientifiques et les objets d'étude privilégiés par les archéologues.

### Propriétés

- **Domaine** : spécialité scientifique, par exemple architecture, sculpture, céramique ou épigraphie.
- **Aire culturelle** : espace culturel étudié, notamment monde grec ou monde romain.
- **Période étudiée** : période historique privilégiée.

### Relations

La classe SPÉCIALISATION est reliée à la classe ARCHÉOLOGUE / PERSONNE.

Un archéologue peut posséder aucune, une ou plusieurs spécialisations documentées (0..n), tandis que chaque spécialisation enregistrée est associée à un seul archéologue (1). Cette relation permet de documenter les différents domaines de recherche d'un même individu.

### Exemple

Un archéologue peut être spécialisé à la fois dans la sculpture grecque et dans la céramique antique. Ces deux spécialisations sont enregistrées séparément dans la classe SPÉCIALISATION, chacune étant associée au même archéologue (1). Un archéologue peut ainsi posséder plusieurs spécialisations (0..n), tandis que chaque spécialisation enregistrée concerne une seule personne (1).

### Intérêt pour la recherche

Cette classe permettra d'observer l'évolution des objets de recherche et la répartition des spécialités au sein de l'archéologie classique. Elle permettra également de comparer les spécialisations selon les générations et les parcours professionnels.

## 8. SITE ARCHÉOLOGIQUE

### Définition

Cette classe représente les sites antiques sur lesquels les archéologues ont effectué des fouilles, des études ou d'autres activités scientifiques.

### Propriétés

- **Nom** : nom du site archéologique.
- **Pays** : pays dans lequel se trouve le site.
- **Région** : région géographique.
- **Type de site** : ville antique, sanctuaire, nécropole, villa, etc.

### Relations

La classe SITE ARCHÉOLOGIQUE est reliée à deux autres classes : LIEU GÉOGRAPHIQUE et ACTIVITÉ DE TERRAIN.

- **LIEU GÉOGRAPHIQUE** : chaque site archéologique est associé à un seul lieu géographique (1), tandis qu'un lieu géographique peut comprendre aucun, un ou plusieurs sites archéologiques (0..n). Cette relation permet de situer géographiquement les différents terrains de recherche.

- **ACTIVITÉ DE TERRAIN** : chaque activité de terrain enregistrée se déroule sur un seul site archéologique (1), tandis qu'un site archéologique peut être associé à aucune, une ou plusieurs activités de terrain (0..n). Ces activités peuvent être réalisées à différentes périodes et par différents archéologues.

### Exemple

Pompéi peut être enregistré dans la classe SITE ARCHÉOLOGIQUE.

- **LIEU GÉOGRAPHIQUE** : Pompéi est situé en Italie, dans la région de Campanie. Le site est donc associé à un seul lieu géographique (1), tandis que la Campanie peut comprendre plusieurs sites archéologiques (0..n).

- **ACTIVITÉ DE TERRAIN** : Pompéi a fait l'objet de nombreuses campagnes de fouilles et d'études archéologiques. Chaque activité enregistrée est associée à ce seul site (1), tandis que Pompéi peut être relié à plusieurs activités de terrain (0..n).

### Intérêt pour la recherche

Cette classe permettra d'identifier les terrains les plus fréquemment étudiés et de comparer la répartition géographique des recherches.

## 9. ACTIVITÉ DE TERRAIN

### Définition

Cette classe représente les activités scientifiques effectuées par les archéologues sur les sites archéologiques. Elle permet de distinguer la personne, le site et la nature de l'activité.

### Propriétés

- **Type d'activité** : fouille, étude, prospection ou autre intervention.
- **Rôle** : fonction de la personne dans l'activité, par exemple directeur de fouilles ou participant.
- **Début** : date de début.
- **Fin** : date de fin.
- **Source** : référence permettant de documenter l'activité.

### Relations

Chaque activité est réalisée par une personne et se déroule sur un site archéologique. Une personne peut participer à plusieurs activités. Un même site peut être associé à plusieurs activités successives.

### Exemple

Une personne peut participer à une campagne de fouilles à Pompéi pendant une période donnée, puis effectuer une étude sur un autre site.

### Intérêt pour la recherche

Cette classe permettra de reconstituer les parcours de terrain et d'observer les relations entre les origines des archéologues, leurs spécialisations et les sites étudiés.

## 10. PUBLICATION

### Définition

Cette classe représente les productions scientifiques publiées par les archéologues du corpus.

### Propriétés

- **Titre** : titre de la publication.
- **Année** : année de publication.
- **Type** : livre, article, rapport de fouilles ou autre production.
- **Référence** : référence bibliographique permettant d'identifier le travail.

### Relations

La classe PUBLICATION est reliée à la classe CONTRIBUTION.

- **CONTRIBUTION** : chaque publication enregistrée peut être associée à aucue, une ou plusieurs contributions (0..n), tandis que chaque contribution enregistrée concerne une seule publication (1). Cette relation permet de relprésenter les différents auteurs ou coauteurs d'une même production scientifique. 

### Exemple

Un article scientifique consacré à l'architecture romaine peut être rédigé par deux archéologues. Cet article est enregistré une seule fois dans la classe PUBLICATION, mais il est associé à deux contributions distinctes (0..n), correspondant aux deux auteurs. Chaque contribution concerne cette seule publication (1).

### Intérêt pour la recherche

Cette classe permettra d'étudier les productions scientifiques des archéologues et leur évolution chronologique. Elle pourra également contribuer à identifier les collaborations scientifiques lorsque plusieurs archéologues participent à une même publication.

## 11. CONTRIBUTION

### Définition

Cette classe représente le rôle joué par une personne dans la réalisation d'une publication. Elle sert d'intermédiaire entre les archéologues et leurs travaux scientifiques.

### Propriétés

- **Rôle** : auteur ou coauteur.
- **Source** : référence permettant d'établir cette contribution.

### Relations

La classe CONTRIBUTION est reliée à deux autres classes :

- **ARCHÉOLOGUE / PERSONNE** : un archéologue peut être associé à aucune, une ou plusieurs contributions scientifiques (0..n), tandis que chaque contribution enregistrée est associée à un seul archéologue (1).

- **PUBLICATION** : une publication peut être associée à aucune, une ou plusieurs contributions (0..n), tandis que chaque contribution enregistrée concerne une seule publication (1). Cette relation permet notamment de représenter les publications réalisées par plusieurs auteurs.

### Exemple

Deux archéologues rédigent ensemble un article scientifique consacré aux sanctuaires grecs. L'article est enregistré une seule fois dans la classe PUBLICATION. Deux contributions sont ensuite créées dans la classe CONTRIBUTION, chacune correspondant à l'un des deux archéologues. Chaque archéologue est ainsi relié à sa propre contribution (1), tandis qu'un même archéologue peut posséder plusieurs contributions documentées (0..n). Les deux contributions concernent une seule et même publication (1), laquelle peut être associée à plusieurs contributions (0..n).

### Intérêt pour la recherche

Cette classe permettra de relier les archéologues à leurs productions scientifiques et d'étudier leurs activités de publication au fil du temps.

## 12. RELATION ENTRE PERSONNES

### Définition

Cette classe décrit les relations scientifiques ou professionnelles entre les personnes étudiées. Elle permet de représenter les réseaux humains au sein du champ de l'archéologie classique.

### Propriétés

- **Type** : nature de la relation, notamment maître-élève ou collaboration.
- **Début** : date de début, lorsqu'elle est connue.
- **Fin** : date de fin, lorsqu'elle est connue.
- **Source** : référence attestant la relation.

### Relations

Chaque relation associe deux personnes :

- Une personne source.
- Une personne cible.

Une même personne peut intervenir dans plusieurs relations, comme source ou comme cible. La distinction entre source et cible permet notamment de représenter une relation orientée, comme celle d'un maître envers son élève.

### Exemple

Lorsqu'une notice biographique indique qu'un archéologue a été formé par un autre archéologue, une relation de type « maître-élève » peut être enregistrée. Une collaboration scientifique explicitement attestée peut également être représentée.

### Intérêt pour la recherche

Cette classe permettra d'étudier les réseaux de transmission des savoirs, les filiations intellectuelles et les collaborations entre archéologues. Elle pourra contribuer à identifier des groupes professionnels ou des traditions scientifiques, dans la mesure où les sources permettent de documenter ces relations.


## Conclusion

Ce modèle conceptuel repose sur douze classes organisées autour de la classe centrale **ARCHÉOLOGUE / PERSONNE**. Les onze autres classes permettent de décrire différentes dimensions du parcours et des activités des individus étudiés :

- **LIEU GÉOGRAPHIQUE** : les lieux de naissance des archéologues et l'implantation géographique des institutions et des sites archéologiques.
- **FORMATION** : les études, les disciplines et les diplômes obtenus.
- **INSTITUTION** : les établissements et organismes liés aux parcours des archéologues.
- **APPARTENANCE** : les liens d'appartenance entre les archéologues et les institutions.
- **POSTE / CARRIÈRE** : les fonctions professionnelles exercées au cours de leur carrière.
- **SPÉCIALISATION** : les domaines scientifiques, les aires culturelles et les périodes historiques étudiées.
- **SITE ARCHÉOLOGIQUE** : les lieux où se déroulent les recherches archéologiques.
- **ACTIVITÉ DE TERRAIN** : les fouilles, les études et les autres interventions réalisées sur ces sites.
- **PUBLICATION** : les productions scientifiques des archéologues.
- **CONTRIBUTION** : les liens entre les archéologues et leurs publications.
- **RELATION ENTRE PERSONNES** : les relations scientifiques et professionnelles, notamment les rapports maître-élève et les collaborations.

Les relations entre ces classes permettent de reconstituer les parcours individuels des archéologues classiques, depuis leur formation jusqu'à leurs activités professionnelles et scientifiques. Les cardinalités précisent le nombre d'occurrences possibles pour chaque relation et permettent de structurer les informations de manière cohérente.

Ce modèle doit ainsi permettre de comparer les trajectoires des archéologues classiques actifs depuis le XIXe siècle, d'identifier les institutions qui structurent ce champ scientifique et d'étudier l'évolution des spécialisations, des activités de terrain et des relations professionnelles.

L'objectif est donc de disposer d'une structure commune pour organiser les données recueillies et mener une analyse prosopographique de l'évolution de l'archéologie classique.