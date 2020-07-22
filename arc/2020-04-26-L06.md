---
title: 'L06 Data II: Modeling & Manipulating'
categories: [lessons]
tags: [data, modeling, normalization, proxies, abstractions, featureas]
---

# Goals:

Getting to know the basics of working with data: modeling, manipulating

# Software:

- R
- Excel, Google Spreadsheets, or any other alternative

# In Class I: *Theoretical and Conceptual*

## Ways of modeling data: Categorization

> “[Modeling is] a continual process of coming to know by manipulating representations.”

- Willard McCarty, “Modeling: A Study in Words and Meanings,” in Susan Schreibman, Ray Siemens, and John Unsworth, *A New Companion to Digital Humanities*, 2nd ed. (Chichester, UK, 2016), <http://www.digitalhumanities.org/companion/>.

One of the most common way of modeling data in historical research—joining items into broader categories. Categorization is important because it allows to group items with low frequencies into items with higher frequencies, and through those discern patterns and trends. Additionally, alternative categorizations allow one to test different perspectives on historical data.

The overall process is rather simple in terms of technological implementation, but is quite complex in terms of subject knowledge and specialized expertise is required to make well-informed decisions.

* For example, let's say we have the following categories: *baker*, *blacksmith*, *coppersmith*, *confectioner*, and *goldsmith*.
	* These can be categorized as **occupations**;
	* Additionally, *blacksmith*, *coppersmith*, and *goldsmith* can also be categorized as **'metal industry'**, while *baker* and *confectioner*, can be categorized as **'food industry'**;
	* Yet even more, one might want to introduce additional categories, such as **luxury production** to include items like *goldsmith* and *confectioner*; and **regular production** for items like *baker*, *blacksmith*, *coppersmith*.
* Such categorizations can be created in two different ways, with each having its advantages:
	* first, one can create them as additional columns. This approach will allow to always have the original—or alternative—classifications at hand, which is helpful for re-thinking classifications and creating alternative ones where items will be reclassified differently, based on a  different set of assumptions about your subject.
	* second, these can be created in separate files, which might be easier as one does not have to stare at existing classifications and therefore will be less influenced by them in making classification decisions.
* Additionally, one can use some pre-existing classifications that have already been created in academic literature. These most likely need to be digitized and converted into properly formatted data, as we discussed in the previous lesson.

## Normalization

This is a rather simple, yet important procedure, which is, on the technical side, very similar to what was described above. In essence, the main goal of normalization is to remove insignificant differences that may hinder analysis.

* Most common examples would be:
	* bringing information to the same format (e.g., dates, names, etc.)
	* unifying spelling differences

It is a safe practice to **preserve the initial data**, creating *normalized* data in separate columns (or tables)

## Note: *Proxies*, *Features*, *Abstractions*

These are the terms that refer to the same idea. The notion of *proxies* is used in data visualization, that of *features*—in computer science; that of *abstractions*—in the humanities.

The main idea behind these terms is that some simple *features* of an object can act as *proxies* to some complex phenomena.

For example, Ian Morris uses the size of cities as a proxy to the complexity of social organization. The logic is following: the larger the size of a city, the more complex social, economic and technical organization is required to keep that city functional, therefore is can be used as an indicator of the social complexity.

While *proxies* are selected from what is available—usually not much, especially when it comes to historical data—as a way to approach something more complex, it may be argued that abstractions are often arrived to from the opposite direction. We start with an object which is available in its complexity and we reduce its complexity to a more manageable form which—we expect—would prepresent a particular aspect of the initial complex object. Most commonly this is applied to texts in a natural language. For example, in *stylometry* texts are reduced to freqiency lists of most frequent *features*, which are expected to represent an *authorial fingerprint*.

The complexity of texts can be reduced in a number of ways: into a list of lemmas (e.g., for topic modeling analysis), frequency lists (e.g., for document distance comparison), syntactic structures, ngrams, etc. This list is never set and researchers can create multiple abstractions depending on their research questions.

# In Class II: *Practical*

Data for the practical session and homework: [Bosker_Data.zip](../../files/Bosker_Data.zip). The data is available in open access and is a supplement to a study (see, *Reference Materials*).

The zipped file includes everything you need for the practical session. Download and unzip (read the article at home!).

**Note:** create a notebook and work through the following questions. Group work is encouraged. Please, explain in one or two sentences what you do in each step, so that your work is also human-readable. Please, submit this notebook as your homework. MAke sure to name your file in the following manner: `070184-LXX-HW-YourLastName-YourMatriculationNumber.EXT`, where `LXX` is the number of the lesson for which you submit homework; `YourLastName` is your last name; and `YourMatriculationNumber` is your matriculation number; `EXT` is the extension of your file --- yopu can submit it either as HTML or as a PDF.


## SECTION I.

Please, provide your answers (2-3 sentences) to the following questions:

* Can you figure which file contains data?
* In which format is data?
* How can we load it into R? (Describe and provide working `R code`)
* What is the chronological extent of this data?
	* [*easy-ish*] What periods can it be divided into? How can we do that?
* How can we introduce the following categories into this data:
	* [*easy*] North Africa and Europe?
	* [*a bit more complicated*] the Austro-Hungarian Empire?
	* [*a tad tricky*] Christiandom and Islamdom?

## SECTION II

Please, provide your answers as working `R code` and a couple of sentences to describe how you approach (2-3 sentences) the following problems:

* What is the chronological extent of this data?
	* [*easy-ish*] What periods can it be divided into? How can we do that?
		* Can you generate a cumulative graph of population over time, divided into these periods? (*Hint:* there should be one line for one period and another for another, etc.)
* How can we introduce the following categories into this data:
	* [*easy*] North Africa and Europe?
		* Construct comparative graphs of population in North Africa and Europe (similar to what you did with the Morris dataset). Here you will need to sum up population!
	* [*a bit more complicated*] the Austro-Hungarian Empire?
		* When did the Empire had the largest number of cities (based on the data set)?
		* When was its population at the highest?
	* [*a tad tricky*] Christiandom and Islamdom?
		* What are the largest cities of Islamdom for each reported period?
		* What are the largest western cities of Islamdom between 1000 and 1500 CE?

# Reference Materials

* Bosker, Maarten, Eltjo Buringh, and Jan Luiten van Zanden. 2012. “From Baghdad to London: Unraveling Urban Development in Europe, the Middle East, and North Africa, 800–1800.” *The Review of Economics and Statistics* 95 (4): 1418–37. <https://doi.org/10.1162/REST_a_00284>.
* Bosker, Maarten, Eltjo Buringh, and Jan Luiten Van Zanden. 2014. “Replication Data for: From Baghdad to London: Unraveling Urban Development in Europe, the Middle East, and North Africa, 800-1800.” *Harvard Dataverse*. <https://doi.org/10.7910/DVN/24747>.

## Additional Readings

* Moretti, Franco. 2007. *Graphs, Maps, Trees: Abstract Models for Literary History*. London - New York: Verso.
* Moretti, Franco. 2013. *Distant Reading.* London ; New York: Verso.
* Romanov, Maxim G. 2017. “Algorithmic Analysis of Medieval Arabic Biographical Collections.” *Speculum* 92 (S1): S226–46. <https://doi.org/10.1086/693970>.

# Homework:

* Finish the practical part and email your notebooks; submit as described below.

## Submitting homework:

* Homework assignment must be submitted by the beginning of the next class;
* Email your homework to the instructor as attachments.
	*  In the subject of your email, please, add the following: `070184-LXX-HW-YourLastName-YourMatriculationNumber`, where `LXX` is the numnber of the lesson for which you submit homework; `YourLastName` is your last name; and `YourMatriculationNumber` is your matriculation number.