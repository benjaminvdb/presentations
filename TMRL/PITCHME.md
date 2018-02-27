##### Developing a smarter Electronic Health Record

---

###### Introduction

* Insurers define the conditions that determine treatments rates for physiotherapy practices.
* Quality of a patient's electronic health record is important.
* Increasing pressure on therapists for providing data.

---

#### Motivation

1. Therapists spend 26% of their time doing administrative work.
2. The systems do not provide feedback using this data in any meaningful way.
3. This clearly induces more stress and results in less billable hours and an increase of the healthcare costs.

---

#### Objectives

- Efficient
- Meaningful |
- Fully functioning, commercially viable product

---

#### Attribution

This is a collaboration between
- Codarts (vocational university in Rotterdam)
- 10 physiotherapy practices
- NVFS (Dutch association for physiotherapy in sports)
- Suzan Verberne

---

#### Starting out 

The project goals can be cast as common NLP problems, e.g.:

1. Efficient entering of data @fa[arrow-right] assign a form field to incoming unstructured data using classification.
2. Provide meaningful feedback @fa[arrow-right] transform unstructured data into structured data using information extraction.

A probable continuation of the project will add another goal:

3. Normalisation of (medical) named entities

---

#### Annotate

- Domain knowledge can help achieving objectives
- Finer-level detail |
- Team of physiotherapy students |
- International classification standards |

---

#### Annotation Task

1. Determining spans associated with label 
2. Assign correct label
3. Correct coding following standards

---

#### Category examples

* Functioning (conditions in anatomical properties, activities, etc.)
* Diseases |
* Incidents / trauma |
* Symptoms \
* Intervention |

---

#### Preparation and quality assessment

* Annotation guidelines: under-defined task
* Training session of several hours
* Mid-term evaluation of progress
* Guidance of students by professional physiotherapist

---

#### Mid-term evaluation

* Inter-agreement scores were low
* Senior therapist was unsure about many examples
* Technical background details provided
* Join some categories, leave out normalized coding 

---

#### Results

* About 500 documents were annotated
* Inter-agreement scores still low
* We hoped to obtain more data (under-defined task)

---

#### Lessons learned

* Hard to estimate difficulty of annotation task
* Hard to cover all cases in the guidelines
* Preparing an annotation task takes a lot of time
    * Setting up the tool
    * Training students
    * Monitoring progress
    * Mid-term evaluation
    * Adjustment of the guidelines
* Start with low-level features!

---

#### Rule-based systems
* We have implemented several models for solving different needs in the electronic health record.
* I want to talk about the one that we thought is really hard, since we couldn’t find representative training data for it.

##### Timeline extraction
* Problem: given a document, return a list of events, each with a representative label describing the event and a start and end date.
* Since the documents are the therapists notes, they are in a concise and simple format.
* Perhaps we can exploit the limited expressiveness of the documents?
* To investigate this, we tried a simple rule-based approach.
* First tests are looking promising!

##### Rule-based Information Extraction is Dead! Long Live Rule-based Information Extraction Systems!
* Like we did, most recent academic research starts from the assumption that statistical machine learning is the best approach to solving information ex- traction problems (Chiticariu et al. 2013)
* The industry in 2013 didn’t reflect the research efforts of the NLP community over the years 2003-2012: rule-based systems we twice as abundant and in large companies even more so!
* Different ways of measuring the costs and benefits of information extraction:
    * In academia there is usually no system or team requirement, usually just evaluation measurements such as precision, recall, F1-score, etc.
    * In industry there is a limited resource of people who can work with machine learning models. It’s nice if non-CS people can be trained to write rules. Interpretability supporting the easiness of maintenance and incorporation of domain knowledge.

#### Conclusions and Future Work
* Generating training data in a field as complex as physiotherapy is very hard.
* Observing the early results and usage in the industry, rule-based systems might prove more useful than I expected.
* We will continue a rule-based approach for specific parts of the electronic health record.
* Looking for ways to combine rule and ML-based approaches. Any suggestions?

#### ML-based systems
* While the students were annotating documents, we tried to tackle some more concrete problems using ML-based methods:
    * Assign sentences to the proper form field in the electronic health record.
    * Sentiment analysis of subjective patient reporting, i.e. assign a score between [-1, 1] to a document like “Patient feels better than last week. Had some knee pain for two days after manipulation, but this slowly faded and is now gone.”
