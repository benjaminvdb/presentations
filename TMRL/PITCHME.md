### Developing a smarter Electronic Health Record
<br>
<span style="color:gray;font-size:12;">Benjamin van der Burgh (LIACS)</span>

---

#### Introduction

* Insurers determine treatment rates 
* Based on quality of electronic health record
* Increasing pressure on therapists for providing data

---

#### Motivation

- 26% of time spent on administrative work
- Current systems do not provide meaningful feedback |

---

#### Objectives

- Create a digital assistant that supports:
    - data intake 
    - data analysis
- Fully functioning, commercially viable product |

---

#### Attribution

- Codarts (vocational university)
- 10 physiotherapy practices
- NVFS
- Suzan Verberne

---

#### Data

- Anonimized data from existing electronic health records
  - Lots of forms
  - Many _free text_ fields
  - @fa[arrow-right] no normalization

---

#### Starting out 

- Efficient data input @fa[arrow-right] classification
- Meaningful feedback @fa[arrow-right] information extraction 
- Future: normalization of (medical) named entities

---

#### Annotate

- Domain knowledge can help achieving objectives
- Finer-level detail |
- Team of physiotherapy students |
- International classification standards |

---

#### Annotation Task

- Determining spans associated with label 
- Assign correct label |
- Correct coding following standards |

---

#### Category examples

* Functioning
* Diseases |
* Incidents / trauma |
* Symptoms |
* Intervention |

---

#### Preparation and quality assessment

* Annotation guidelines: under-defined task
* Training session of several hours |
* Mid-term evaluation of progress |
* Guidance of students by professional physiotherapist |

---

#### Mid-term evaluation

* Inter-agreement scores were low
* Senior therapist was unsure about many examples |
* Technical background details provided | 
* Join some categories, leave out normalized coding |

---

#### Results

* About 500 documents were annotated
* Inter-agreement scores still low
* We hoped to obtain more data

---

#### Lessons learned

* Hard to estimate difficulty of annotation task
* Hard to cover all cases in the guidelines |
* Preparing an annotation task takes a lot of time |
    * Setting up the tool
    * Training students
    * Monitoring progress
    * Mid-term evaluation
    * Adjustment of the guidelines
* Start with low-level typed! |

---

#### Rule-based systems

* Implemented several statistical models 
* Different problems and needs
    * Text classification
    * Sentiment analysis
* One task seemed hard to accomplish using learning |

---

#### Timeline extraction
* Problem: given a document, return a list of events |
* Therapists notes, they are in a concise and simple format |
* Exploit limited expressiveness of the documents? |
* Simple rule-based approach |
* First tests are looking promising! |


---

![UIMA Ruta](assets/uima_ruta.png?size=contain)

---

![Timeline](assets/timeline.png?size=contain)

---


#### Rule-based Information Extraction is Dead! Long Live Rule-based Information Extraction Systems!
* Assumption that statistical methods are the best approach (Chiticariu et al. 2013)
* Industry didn't reflect research efforts
* Different measures of costs and benefits
    * Academia: F1-score, no system or team requirement
    * Industry: interpretable by non-CS employees 

---

![Academia vs. Industry](assets/academia_industry.png?size=auto 60%)

---

#### Hybrid system

- We'll likely encounter more situations where rules can work
- How to combine statistics and rule-based approaches?

---

#### Walmart's Chimera

- System for continuous classification of product categories
- Statistics- and rule based classifiers in parallel

---

![Walmart Chimera](assets/walmart_chimera.png?size=contain)

---

#### Villena-Román et al. 2011

- Statistics and rule-based approaches in sequence
- Rules used to fix mistakes in machine learning output

---

![Hybrid System](assets/hybrid_system.png?size=contain)

---

#### Conclusions and Future Work
* Generating training data can be very hard 
* Rule-based systems might prove useful
* How to best combine rule-based and statistical methods? 
