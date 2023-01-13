# TextBasedGrasps

This repository hosts two datasets for the purpose of making text-based grasp pose predictions based on publicly available textual object descriptions as used in our publication [Leveraging Publicly Available Textual Object Descriptions for Anthropomorphic Robotic Grasp Predictions](https://ieeexplore.ieee.org/abstract/document/9981541) (link to the [PDF](https://www.dfki.de/fileadmin/user_upload/import/12849_IROS22_2505_C.pdf)). We subsequently describe the content of each dataset. This work is provided under the **MIT License**. 

1. **Object Descriptions**: Contains textual object descriptions for 100 everyday objects extracted from the following nine sources.

Source                           | Link
---------------------------------|---------------
Wikipedia (initial abstract only)|https://en.wikipedia.org/wiki/Main_Page
Wiktionary                       |https://de.wiktionary.org/wiki/Englisch
WordNet                          |https://wordnet.princeton.edu/
Collins Dictionary               |https://www.collinsdictionary.com/
Dictionary by Merriam-Webster    |https://www.merriam-webster.com/
Macmillan Dictionary             |https://www.macmillandictionary.com/
American Heritage Dictionary     |https://ahdictionary.com/
Lexico                           |https://www.lexico.com/
Dictionary.com                   |https://www.dictionary.com/

2. **Object Labeling**: Contains the results of our crowdsourcing study carried out on [Amazon MTurk](https://www.mturk.com/) where study participants were asked to choose the most suitable grasping pose for **holding an object**. We provide the following data from our study.

Data        | Explanation
------------|-------------
Type        | Represents the task we have collected the data for (always hold in this case)
GraspType   | Grasp type that received the responses (MediumWrap, Lateral, Tripod, Writing)
Object      | The corresponding object the responses were collected for
Responses   | Number of responses for a specific grasp type (max. 20)
Instruction | Instruction that was provided to the study participants

- Based on the grasp type that was determined most suitable for holding an object, each object in the **object descriptions dataset** was labeled according to that grasp. Furthermore, the dataset was augmented by an additional column that indicates whether that grasp falls into the category of a power- or precision grasp. 

Column    | Value
----------|------------
GraspType | Power (Medium Wrap or Lateral) or Precision (Tripod or Writing Tripod)
Grasp     | Index 0 - Lateral; 1 - Medium Wrap; 2 - Tripod; 3 - Writing Tripod
