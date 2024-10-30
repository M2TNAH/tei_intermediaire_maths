> By : Joël F. / M2 TNAH.

# Indexing nineteenth-century amateur mathematical journals: a TEI encoding proposal

## 1. Justification

Amateur’ mathematical practices -- i.e. the work of engineers, professors and polytechnicians -- contributed in the 19th century to the structuring of the mathematical discipline, outside the university networks. 

Since the mid-2000s, historians of mathematics have become interested in these collaborative amateur practices. Initial work on these issues, in the absence of access to structured data, was initially carried out at a qualitative level with archival collections. However, some historians who were contemporaries of the first cultural heritage digitisation projects expressed a desire for structured data to guide more quantitative approaches[^1].

### 1.1 Encoding of the ‘Intermédiaire des Mathématiciens’ tables and their answers

XML/TEI encoding of first-hand bibliographic material could therefore be useful for synthetically mapping amateur mathematical activity as a whole. This would give researchers access to structured data and allow, for example, statistical approaches with a posteriori computational manipulations:

- to catalogue amateur contributors;

- to list their activities and possibly their preferred mathematical categories;

- to catalogue mathematical questions and answers;

- etc.

> This project could be entirely consistent with the documentary projects of the French network of mathematical libraries and *Numdam*.

**I therefore decided to work on encoding the ‘tables’ from the 1896 ‘Intermédiaire des mathématiciens’ and an example of the answer to which they refer**.

### 1.2 Logic of the tables

These 'tables', which appear at the end of each volume containing twelve of the monthly issues, have been produced each year so that each contribution published can be easily found by consulting the back of the book. These tables are interesting for their relational and referential dimension.

> Attention: the nature of the text of these journals is, from a TEI point of view, *composite*: because the volume is a compilation of the twelve monthly issues. I will take this composite dimension into account when encoding a DTD.

#### 1.2.1 DTD & XML

**This DTD provides the grammar for any volumes** of "*Intermédiaire des mathématiciens*". It takes into account :

1. Answers, which includes :
   
   - a title; the question identifier; the name of the questioner; the answer; the name of the answerer. (This name may be a pseudonym.) The "Answers" section always contains several items (number greater than 1).

2. The table of questions and answers, which includes :
   
   - a title; a presentation of the title; a list of questions asked and answered.

3. The table of authors, which includes :
   
   - a title; a presentation of the legend; the names of the authors (italics indicate a pseudonym); the page number(s) of their contributions; this number may be in bold if it is an answer, otherwise it is a question.

The XML file has been writed after the DTD for check the logic.

---

## 2. Facultative bibliography

### 2.1 History of mathematics

- Pauline Romera-Lebret, *La nouvelle géométrie du triangle : passage d'une mathématique d'amateurs à une mathématique d'enseignants (1873-1929)*, Thèse de doctorat en histoire des mathématiques sous la direction d'Evelyne Barbin, Nantes, Université de Nantes, 2009.

- Hélène Gispert, *La France mathématique de la IIIe République avant la Grande Guerre*, Paris, éd. de la Société Mathématique de France, 2015.

- Norbet Verdier et Christian Gerini, *L'émergence de la presse mathématique en Europe au 19ème siècle*, Londres, College Publications, 2014.

### 2.2 TEI ressources

Here are the documents that helped/inspired me write my DTD (non-exaustive list):

- [2 The TEI Header - The TEI Guidelines](https://tei-c.org/release/doc/tei-p5-doc/fr/html/HD.html#HD11)

- [16 Language Corpora - The TEI Guidelines](https://tei-c.org/release/doc/tei-p5-doc/en/html/CC.html#CCDEF)

- https://books.openedition.org/oep/688

- [Manuel d'encodage TEI Renaissance et temps modernes](http://www.bvh.univ-tours.fr/XML-TEI/ManuelWeb/Manuel_TEI_BVH.html)

[^1]: [Les journaux de mathématiques dans la première moitié du xixe siècle en Europe](https://journals.openedition.org/philosophiascientiae/297#bodyftn32)
