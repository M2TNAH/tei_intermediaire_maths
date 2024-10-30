# Indexer les journaux mathématiques amateurs du XIXe siècle : projet d'encodage TEI

## 1. Justification

Les pratiques mathématiques "amateures" -- c'est-à-dire les travaux d'ingénieurs, professeurs et polytechniciens -- ont contribué au XIXe siècle à la structuration de la discipline mathématique, en marge des réseaux universitaires. Ces pratiques non-académiques ont formé un vaste réseau européen rassemblé autour de "questions/réponses" publiées dans des revues (un peu de la même façon que nos actuels forums communautaires en ligne).

Les historiens des mathématiques ont, depuis le milieu des années 2000, porté un intérêt pour ces pratiques amateures collaboratives. Les premiers travaux sur ces questions, à défaut d'accéder à des données structurées, ont d'abord été menés sur un plan qualitatif auprès des fonds d'archives. Cependant, certains historiens, par ailleurs de façon contemporaines aux premiers projets patrimoniaux de numérisation, ont manifesté le désir d'avoir des données structurées pour orienter des approches plus quantitatives [^1].

### 1.1 Encodage des tables de l'Intermédiaire des Mathématiciens et "Réponses".

L'encodage XML/TEI d'une matière bibliographique de première main pourrait donc être utile pour cartographier de façon synthétique l'activité mathématique amateur dans son ensemble. Cela permettrait donner accès aux chercheurs à des données structurées et rendre enfin possible des approches statistiques avec des manipulations informatiques a posteriori, par exemple :

- cataloguer les contributeurs amateurs ;

- lister leur activité, éventuellement leurs catégories mathématiques de prédilections;

- cataloguer les questions/réponses mathématiques;

- etc.

> Ce projet pourrait être tout à fait cohérent avec les projets documentaire du réseau français des bibliothèques mathématiques et de la *Numdam*.

**Ainsi, j'ai donc décidé de travailler sur l'encodage des "tables" de l'*Intermédiaire des mathématiciens* de 1892 et un exemple de ce à quoi elle se réfèrent**. 

### 1.2 Logique des tables

Ces "tables", publiées à la fin de chaque volume compilant douze des numéros mensuels, ont été réalisées chaque année afin que chaque contribution publiée puisse être retrouvée facilement en consultant la fin du livre. Ces tables sont intéressantes pour leur dimension relationnelle et référentielle: elles indiquent la catégorie des questions posées; leur numéro de page ainsi que celle de leur réponse si elle existe ; les contributions classées par auteur.

> Attention : la nature du texte de ces revues, du point de vue de la TEI, est *composite* : car le volume est un assemblage des douze numéros mensuels. Je prendrai en compte cette dimension composite dans le cadre de l'encodage d'une DTD.

### 1.2.1 DTD

La présente DTD (f*ile/mid-term.dtd*) donne la grammaire pour les volumes de l'*Intermédiaire des mathématiciens*. Elle prend en compte :

- Les réponses, qui contiennent notamment :
  
  - un titre; l'identifiant de la question; le nom de celui qui l'a posée; la réponse; le nom de celui qui la propose. (Ce nom peut être un pseudonyme.) La partie "Réponses" contient toujours plusieurs articles (nombre supérieur à 1).

- La table des questions et réponses, qui contient notamment:
  
  - un titre; une présentation de la légende; une liste de questions posées auxquels ont a répondu

- La table des auteurs, qui contient notamment :
  
  - un titre; une présentation de la légende ; les noms des contributeurs (l'italique désigne un pseudonyme) ; le ou les numéros de la page de leurs contributions; ce numéro peut être en gras s'il s'agit d'une réponse; sinon il s'agit d'une question.

## Bibliographie

---

[Les journaux de mathématiques dans la première moitié du xixe siècle en Europe](https://journals.openedition.org/philosophiascientiae/297#bodyftn32)
