---
layout: page
title: Literary Character Networks
description: A summary of my dissertation on the 'National Episodes' by Galdós
img: /assets/img/dissertation/figure_6.png
importance: 1
category: research
related_publications: false
---

This is the summary I prepared to defend my dissertation:  "Possibilities for the Digital Data Mining for the Analysis of the Literary Characters in the Spanish Novel: The Case of Galdós' *National Episodes*", written in Spanish, which I passed succesfully in November of 2017.

<img src="/assets/img/dissertation/isasi_networks.png" alt="Collection of networks of the Episodios Nacionales"
	title="National Episodes character network poster" width="100%" height="100%" />

[Poster in PNG here.](/assets/img/dissertation/isasi_networks.png) [Do not print withtout permission]

### Main goal

To create a pipeline for extracting and analyzing character networks in novels written in Spanish.

### Research question(s)

- What type of questions can I ask with a data mining methodology? 
- Is there a correlation between Galdós’ novelistic and historiographical notions (part of his worldview) and the networks of his characters in this set of historical novels? 

### Corpus 

- 46 novels corpus to build the methodology 
- Dictionary of over 4,400 characters with metadata: resolved name, token names, social class, historical or fictional condition, and gender. 
- For the analysis: Ten novels belonging to the third series of the collection. 

From a traditional point of view, the ten novels that I have analyzed on a distant reading approach are classified as follows:

| Division                 | Novel(s)                                                     | Type                                                         |
| ------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| Presentation (framework) | *Zumalacárregui* (1898)                                      | Symbolic representation:<br/>Political division, 2 Spains<br/>Fiction-History parallelism |
| Plot (*bildungsroman*)   | *Mendizábal* (1898)<br/>*De Oñate a la Granja*<br/>(1898)<br/>*Luchana* (1899) | Socio-politic trajectory:<br/>Calpena’s development from modest middle class youngster to upper class responsible adult |
| Division (framework)     | *La Campaña del<br/>Maestrazgo* (1899)                       | Symbolic representation:<br/>Political division, 2 Spains<br/>Representation of the failure of the traditional aristocracy trying to be a political class |
| Plot (*bildungsroman*)   | *La estafeta romántica* (1899)<br/>*Vergara* (1899)          | Socio-politic trajectory:<br/>Calpena’s development from modest middle class youngster to upper class responsible adult |
| Digression               | *Montes de Oca* (1900)                                       | Santiago Ibero’s introduction                                |
| Plot (*bildungsroman*)   | *Los Ayacuchos* (1900)                                       | Socio-politic trajectory:<br/>Two weddings: Fernando and Demetria, Gracia and Santiago |
| Summary (framework)      | *Bodas reales* (1900)                                        | Symbolic representation:<br/>Political division, 2 Spains<br/>Fiction-History parallelism<br/>Royal marriage = destruction of middle class marriage families |

This is, though the main character of the series is Fernando Calpena and his life trajectory, there are three novels that do not participate on that plot. These are novels that have different characters altogether and that can be understood as frameworks to the meaning of the *bildungsroman*. Also, *Montes de Oca* is not about the story of the main character, however it shares the love storyline.



### Data extraction

- Search and replace for token names 
- Count name frequency per chapter 
- Count co-occurrence of characters per chapter 
  - Co-occurrence defined as the names of the characters mentioned in the same chapter; no need for them to actually interact in the plot line. 

### Data analysis

- Character space: Defined as the percentage distribution based on how many times each character is mentioned in the novel. This is a better way of studying space as a long tail distribution was expected for major, minor and minor-minor characters. 
- Character system: Defined as the co-occurrence of two characters along the novel. 
  - Degree centrality: It calculates the total connections of each node. It is equal to popularity. 
  - Eigenvector centrality: It calculates the score of each node based on their connectivity to other high- or low-connected nodes. It is equal to influence. 
  - Betweenness centrality: It calculates the shortest paths between nodes and assigns a number of how many paths passes through each node. It is equal to intermediary actants. 
  -  Modularity: It measures the strength of divisions in networks. It is equal to community division. 
  - Visualization: Force Atlas 2, as “[n]odes repulse each other like charged particles, while edges attract their nodes, like springs” 



## Results

### Findings in Character Space

The novels that form the *bildungsroman* present a different distribution of their character space than those in the framework. On the one hand, *Zumalacárregui* and *La campaña del Maestrazgo* have a reduced number of characters in total and, also, in the 50% part of the space per novel. *Bodas reales*, with a higher number of characters has more characters in the 50% of the space, however, if we sum the individual spaces of family members and political groups, we again see the 50% of the space distributed among a few distinctive spaces. As for the *bildungsroman*, on the other hand, it presents a higher number of characters that occupy the 50% of the space (between 5 and 10). 

These results show that there is a different distribution or allocation of individual space in the totality of the novels, following Woloch’s notion of space, however here we note a distinction between types (almost genres) of novels. 

<img src="/assets/img/dissertation/figure_1.png" alt="Number of characters per novel in the third series"
	title="Number of characters per novel in the third series" width="100%" height="100%" />

### **Findings in character system:**

By degree centrality, modularity and historic/real or fictional attributes of characters in individual novels:

<img src="/assets/img/dissertation/figure_2.png" alt="Distribution of historical and fictional characters in the third series"
	title="Distribution of historical and fictional characters in the third series" width="100%" height="100%" />

1. There is no regular distribution among the series in terms of historical or fictional characters. And, 
2. There is no apparent distribution of more or less characters with said attributes in the Top 20 nor 6 (protagonist + major characters) depending on the type of novel (framework of bildungsroman). However, 
3. The placement of historical characters and fictional characters as well as their modularity in the system or network shows a clear correlation with the typologies of the texts: 
   1. *Bildungsroman* novels: Both groups are divided into different communities that are, at the same time, opposing each other. 
   2. Framework novels: Characters in both groups don’t show such a clear division in terms of their attributes however, surprisingly enough, the modularity divisions show an opposition in terms of political ideas. 

These results point in the direction of noting a higher historicism (in terms of political events and characters [big names]) in framework novels, and a higher degree of daily life history (as Galdós called it, ‘integral history’) in the *bildungsroman*.

<div class="img_row" >
    <img class="col one left" src="/assets/img/dissertation/figure_3.png" alt="Zumalacarregui's social network" title=">Zumalacarregui's social network with degree value and division into historical (red) and fictional characters (green)"/>
    <img class="col one left" src="/assets/img/dissertation/figure_4.png" alt="Mendizabal's social network" title="Mendizabal's social network with degree value and division into historical (red) and fictional characters (green)"/>
  </div>


By social class (preliminary study) in individual novels:

<img src="/assets/img/dissertation/figure_5.png" alt="Distribution of characters by social class in the third series"
	title="Distribution of characters by social class in the third series" width="100%" height="100%" />

1. The military and the upper class are the two groups that are most prevalent along the series.
2. The upper class and, to some extend, the middle class are present in those episodes that pay attention to the main character (*bildungsroman*)*.*

3. When we study the distribution of classes in the character system of each series, we conclude (for now) that there is no correlation between the type of the novel and the distribution and connectivity of the nodes. Rather, the connectivity of all the members of the social group or class is given by the number of characters in the group: the higher the number, the more connected they are; the lower, the links disappear.



By degree centrality, modularity and historic/real or fictional attributes of characters in the series as a whole, a few ideas:

1. The novels belonging to the *bildungsroman* are located in the center of the network (as they share more characters). The novels that form a framework are located in the outskirts of the network (as they don’t share characters with each others and very only a few with the bildungsroman*).

2. The framework novels, again, show a higher degree of historical characters connected to fictional characters within the system.
3. Noting the same results for the distribution of social classes as we did in individual novels, it is possible to state that Galdós’ seems to have fictionalized the church, low and middle classes in a higher degree than the military and the aristocracy, where almost all characters are historical figures. The upper class shows a balanced distribution between historical and fictional characters; however, these lasts ones show a higher degree of connectivity (due to family ties).



## Conclusions

The development of a methodology for extracting and analyzing data from the
characters' system in novels written in Spanish has been the objective and main result of this
study. Taking Pérez Galdós’ *National episodes* as a study model due, on the one hand, to their
historiographic and social importance and, on the other hand, for their textual characteristics, a
series of decisions have been taken - based on previous studies and experiments on this corpus -
with the aim of quantifying the qualitative analysis proposed by Alex Woloch. Thus, we have
decided to postulate the space of the character in terms of the number of times their name is mentioned in the novel and we have parameterized the character system by the coaparition of two characters in each chapter. The results obtained from the parameterization and the analysis of the data demonstrate the usefulness of this type of reading for the study of patterns in literary works as well as their different application possibilities both individually and collectively. 

First, it is necessary to point out that this system of data extraction has captured the presence of the characters in each episode according to their mention in the text. The results of the distribution of these mentions coincide with the traditional classification of protagonists, secondary and tertiary characters in each episode. Now, I have also found that novels with characteristics of bildungsroman have a distribution of narrative space different from those that form the frame and division of the third series, according to the classification pointed out by previous galdosistas. This, in turn, indicates a correlation between the novels with a greater or lesser historical presence and the number of main characters, usually having between four and eight main characters in the first and a couple of main characters in the second ones. 

Secondly, the results of the analysis of the networks of the characters in the third series also point to the distinction of network distribution according to the typology of each episode in terms of their historicism or their daily life and, at the same time, an imbalance in terms of the presentation of social classes in the episodes. In particular, there is a greater emphasis on what Galdós called integral history in those episodes occupied in the trajectory of life and social relationships of a protagonist character as a bildungsroman in medias res. These include more fictional characters of middle and upper class - without historical main characters in *Luchana* and in *La Estafeta Romantica* - than the episodes of the frame and of greater symbolic representation of the sociopolitical situation of the time. In particular, the latter show more historical characters in the protagonists and secondary characters categories, and a larger space for characters of the military class and the aristocracy. Anyway, the results of the analysis by social classes point to a pattern of connectivity between members of the same class in correlation to the number of characters that belong to that group and not necessarily to the type
of novel.



### Limitations

The achievement of the objective set for the realization of this thesis has found, mainly, two limitations. In the first place, we have the development of a methodology for extracting data from the characters from a dictionary of metadata obtained from a previous census. Although this system has allowed me to study variables that, without having the metadata, I could not have carried out, the need to create a dictionary manually shows that, for now, we can not carry out studies of this type automatically that the tools programmed for the case do not have a high level of success in our language. Although this methodology is replicable to any novel, the researcher must previously have metadata of names, surnames, nicknames, etc. of each character. 

As a consequence of the previous one, the second limitation has to do with time in general. On the one hand, before arriving at the decision to create a manual metadata format, we had to process and apply the automatic tools in each text according to their level of accuracy in English. Through a series of experiments in the corpus of the thesis, we checked the level of error of the labeling and, then, it was necessary to search for the indicated solution. As an individual work, the creation of the dictionary lasted approximately three months while other research tasks were carried out. On the other hand, once processed the texts for the identification of the characters according to the data of the dictionary, some data had to be corrected in order to avoid later errors - mainly the appearance of characters in novels where they are not mentioned. This meant another three months of painstaking work in which, on the other hand, I only managed to correct thirty-three of the forty-six episodes. 

## Future directions

The potential of this type of studies for the search and analysis of patterns points in several research directions for the future. The most obvious one is the formalistic study of the forty-six episodes. I refer to a comparative study between the system of the characters of each work and its narrative typology in terms of novelistic subgenre. Since the analysis here points to a differentiation between the subgenre of bildungsroman, melodrama and more historical novels, it would be interesting to see this pattern in a greater number of Galdosian works. In addition, the metadata together with the characteristics also annotated of each novel allows us analysis variables by the 
