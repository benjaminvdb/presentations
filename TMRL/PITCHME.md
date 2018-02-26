# Developing a smarter Electronic Health Record

---

## Introduction

* Insurers define the conditions that determine treatments rates for physiotherapy practices.
* Quality of a patient's electronic health record is important.
* Increasing pressure on therapists for providing data.

---

## Motivation

1. Therapists spend 26% of their time doing administrative work.
2. The systems do not provide feedback using this data in any meaningful way.
3. This clearly induces more stress and results in less billable hours and an increase of the healthcare costs.

---

## Objectives

- Efficient
- Meaningful |
- Lala lolo! |

---

+++
@title[Piecemeal Lists]

- Java
- Groovy |
- Kotlin |
- Scala  |
- The JVM rocks! |

+++

Administrative jobs in physiotherapy practices can be more

<!--The final product of this research project will be a fully functioning, commercially viable electronic health record for Dutch physiotherapy practices.-->

<!--This is a collaboration between Codarts (vocational university in Rotterdam), 10 physiotherapy practices, NVFS (Dutch association for physiotherapy in sports) and Leiden University.-->

<!--## Starting up the project-->
<!--Both project goals can be cast as common NLP problems, e.g.:-->

<!--1. Efficient entering of data -> assign a form field to incoming unstructured data using classification.-->
<!--2. Provide meaningful feedback -> transform unstructured data into structured data using information extraction.-->

<!--A probable continuation of the project will add another goal:-->

<!--3. Normalisation of (medical) named entities-->

<!--All objectives are likely to benefit from domain knowledge on a level finer than the sentence level. Since we had a team of physiotherapy students at our disposal, we decided to annotate a training set with domain-specific labels using international classification standards.-->

<!--Six physiotherapy students were invited to perform the annotation on a set of documents. The task involved:-->

<!--1. Determining the spans (i.e. consecutive sequences of tokens) that were associated with a label.-->
<!--2. Assigning the labeling (sequences of) tokens and assigning the correct category whenever it was applicable.-->
<!--3. Assigning the correct coding of a standardised classification systems if any was available for the category.-->

<!--## Category examples-->
<!--* Functioning (conditions in anatomical properties, activities, etc.)-->
<!--* Diseases-->
<!--* Incidents / trauma-->
<!--* Symptoms-->
<!--* Intervention-->

<!--## Preparation and quality assessment-->
<!--* Annotation guidelines: under-defined c.q. *light annotations* used-->
<!--* Training session of several hours-->
<!--* Mid-term evaluation of progress-->
<!--* Guidance of students by professional physiotherapist-->

<!--## Mid-term evaluation-->
<!--* It quickly became clear that the annotation task was too hard.-->
<!--* The professional therapist was in doubt about which text to annotate and which categories to apply.-->
<!--* Some parts of the task that we deemed easy turned out to be harder once arguments for a different perspective started to seep in (low inter-agreement)-->
<!--* We provided technical background details, hoping that this would make it easier to do the annotation.-->
<!--* We decided to make the task easier by joining categories and leaving out the coding using the standardised classification system.-->

<!--## Results-->
<!--* After a lot of effort by dedicated members of the project, about 500 documents were annotated.-->
<!--* Inter-agreement scores for the annotation were very low-->
<!--* Since the quantity and consistency of the data is low, it is probably unusable for automatic labeling of the selected categories.-->

<!--## Lessons learned-->
<!--* It is very hard to judge an annotation task beforehand (different viewpoints of therapist, students and therapists)-->
<!--* Depending on the domain, documents can very greatly and it’s hard to cover all cases in the guidelines-->
<!--* Preparing an annotation task takes a lot of time-->
	<!--* Setting up the tool-->
	<!--* Training students-->
	<!--* Monitoring progress-->
	<!--* Mid-term evaluation-->
	<!--* Adjustment of the guidelines-->
<!--* We opted for a top-down approach: define categories beforehand. Next time we would go for a bottom-up approach using rules.-->

<!--## Rule-based systems-->
<!--* We have implemented several models for solving different needs in the electronic health record.-->
<!--* I want to talk about the one that we thought is really hard, since we couldn’t find representative training data for it.-->

<!--### Timeline extraction-->
<!--* Problem: given a document, return a list of events, each with a representative label describing the event and a start and end date.-->
<!--* Since the documents are the therapists notes, they are in a concise and simple format.-->
<!--* Perhaps we can exploit the limited expressiveness of the documents?-->
<!--* To investigate this, we tried a simple rule-based approach.-->
<!--* First tests are looking promising!-->

<!--### Rule-based Information Extraction is Dead! Long Live Rule-based Information Extraction Systems!-->
<!--* Like we did, most recent academic research starts from the assumption that statistical machine learning is the best approach to solving information ex- traction problems (Chiticariu et al. 2013)-->
<!--* The industry in 2013 didn’t reflect the research efforts of the NLP community over the years 2003-2012: rule-based systems we twice as abundant and in large companies even more so!-->
<!--* Different ways of measuring the costs and benefits of information extraction:-->
	<!--* In academia there is usually no system or team requirement, usually just evaluation measurements such as precision, recall, F1-score, etc.-->
	<!--* In industry there is a limited resource of people who can work with machine learning models. It’s nice if non-CS people can be trained to write rules. Interpretability supporting the easiness of maintenance and incorporation of domain knowledge.-->

<!--## Conclusions and Future Work-->
<!--* Generating training data in a field as complex as physiotherapy is very hard.-->
<!--* Observing the early results and usage in the industry, rule-based systems might prove more useful than I expected.-->
<!--* We will continue a rule-based approach for specific parts of the electronic health record.-->
<!--* Looking for ways to combine rule and ML-based approaches. Any suggestions?-->

<!--## ML-based systems-->
<!--* While the students were annotating documents, we tried to tackle some more concrete problems using ML-based methods:-->
	<!--* Assign sentences to the proper form field in the electronic health record.-->
	<!--* Sentiment analysis of subjective patient reporting, i.e. assign a score between [-1, 1] to a document like “Patient feels better than last week. Had some knee pain for two days after manipulation, but this slowly faded and is now gone.”-->
