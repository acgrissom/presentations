---
marp: true
theme: default
class:
- invert
paginate: true
footer: Alvin Grissom II\nHaverford College
---
# Gentle Introduction to Computational Linguistics
## Day 1: Introduction
---
# What is Computational Linguistics?
- Can divide into overlapping areas
    - Natural Language Processing (NLP) and Human Language Technologies
        - Develop technologies that use or process human language.
        e.g., machine translation, text-to-speech, speech-to-text, web search, virtual assistants, question answering, etc.
    - Computational Study of Language
        - Study language with computational techniques and tools.
        e.g., corpus linguistics, annotation
---
# Examples of NLP/CL
![](./intro-compling/google_translate.png)

---
# Examples of NLP/CL
![](./intro-compling/google_autocomplete.png)


---
# Examples of NLP/CL
![](./intro-compling/google_autocomplete.png)


---
# Examples of NLP/CL
![](./intro-compling/cogsci_search.png)


---
# Examples of NLP/CL
![h:500](./intro-compling/bing_trending.png)

---
# Examples of NLP/CL
Automatic Captioning
![](./intro-compling/teams_captioning.png)
<sub><sup>Image from [Microsoft Teams support site](https://support.microsoft.com/en-us/office/use-live-captions-in-a-teams-meeting-4be2d304-f675-4b57-8347-cbd000a21260)</sup></sub>

---
# Problems in Comptuational Linguistics
 ## Syntactic Parsing
![bg right invert 80%](./intro-compling/parse_treesvg.svg)

---
<!-- footer: "" -->

# Problems in Comptuational Linguistics
 ## Syntactic Annotation and Parsing
 VerbNet
![](./intro-compling/verbnet1.png)

---
<!-- footer: "Alvin Grissom II\nHaverford College" -->
# Language Modeling
- Answers question: What is the most probable next word?
    - Equivalently: How probable is a given sentence?
    - Fundamental to most common NLP tasks: translation, speech recognition, etc.

---

# Language Modeling
- Answers question: What is the most probable next word?
    - Equivalently: How probable is a given sentence?
    - Fundamental to most common NLP tasks: translation, speech recognition, etc.
- Question for students: How many possible sentences are there in English?

---

# Language Modeling
- Answers question: What is the most probable next word?
    - Equivalently: How probable is a given sentence?
    - Fundamental to most common NLP tasks: translation, speech recognition, etc.
- Question for students: How many possible sentences are there in English?
- Another question: What does it mean to say that one sentence is more probable than another?

---
# Language Modeling
- Answers question: What is the most probable next word?
    - Equivalently: How probable is a given sentence?
    - Fundamental to most common NLP tasks: translation, speech recognition, etc.
- Question for students: How many possible sentences are there in English?
- Another question: What does it mean to say that one sentence is more probable than another? 
    - Language modeling attempts to answer this by using a **corpus** (pl. corpora) of data.

---
# Language Modeling
- By using corpora, we can estiamte the probability of the next word in a sentence or phrase.
- Ex: The word "science" is more likely to follow the word "computer" than "kumquat."
- We can use this for autocompletion.
    - In realty, modern autocompletion also uses other information, such as a profile of your recent behavior, location, etc. to inform suggestions.
![h:350](./intro-compling/google_autocomplete.png)

---
# Language Modeling
- Also works for spelling.
![](./intro-compling/university_misspel.png)

---
# Brief History

- Computational linguistics as a field was born in the 1950's with the Georgetown-IBM experiments in machine translation.
    - Nearly all "AI," including NLP, was rule-based.
- In 1990, a successful approach to machine translation involving Bayesian probability changed the field.

    - Statistical (data-driven) **machine learning** approaches dominated for decades.
- Currently, most NLP research uses machine learning, especially "deep learning."


---

# Machine Learning
- **Machine learning** is an area of computer science concerned with algorithms that allow computers to "learn" from observation.
    

--- 
# Machine Learning 
- **Machine learning** is an area of computer science concerned with algorithms that allow computers to "learn" from observation.
    - For example, learning to **align** words in two different languages by observing many translated sentences.
    ![invert center](./intro-compling/word_alignment.svg)


---

# Machine Learning 
- **Machine learning** is an area of computer science concerned with algorithms that allow computers to "learn" from observation.
    - Another example: SPAM filtering.
    - Show algorithm examples of SPAM and NOT SPAM and it will determine which features are useful for classifying them.
    ![invert center](./intro-compling/image_spampng.png)


---
# Machine Learning
- ML is a kind of function approximation.
    - In one kind of ML, show the algorithm some examples with labels (SPAM, NOT SPAM), and then tries to label new, unseen instances based on what it has learned.
    - It's trying to learn a function
    $$
    f(\text{email}) = \{\text{{SPAM, NOT SPAM}}\}
    $$

---
# Machine Learning
- **Neural networks** are popular in machine learning.
    - They're often able to complete more complex tasks than other kinds of models
        i.e., they can learn more complex functions.
        ![invert](./intro-compling/nn.svg)

    - The more complex neural networks are called "deep."

---
# Distributional Semantics
- **Word embeddings** attempt to calculate similarity between words in a corpus.
    - Based on the **distributional hypothesis**.
        - Similar words tend to occur in similar contexts.
    - Map words to a mathematical vector space with machine learning.
    - Similar words should be near each other in the vector space.
    - Can study correlations with human judgments.
    - See [embedding projector](https://projector.tensorflow.org/).
    
---
# Distributional Semantics
Superlative relations
<sup><sub>Image from [GloVe Embeddings](https://nlp.stanford.edu/projects/glove/).</sub></sup>
![bg right 99% invert](./intro-compling/comparative_superlative.jpg)

---

# Distributional Semantics
City and zip code
<sup><sub>Image from [GloVe Embeddings](https://nlp.stanford.edu/projects/glove/).</sub></sup>
![bg right 99% invert](./intro-compling/city_zip.jpg)


---

# Distributional Semantics

<sup><sub>Image from [GloVe Embeddings](https://nlp.stanford.edu/projects/glove/).</sub></sup>
![bg right 99% invert](./intro-compling/man_woman.jpg)


---
# Distributional Semantics
Diachronic changes in meaning
![invert](./intro-compling/wordpaths.png)
<sub><sup>Image from [Hamilton  et al.](https://nlp.stanford.edu/projects/histwords/)</sup></sub>

---
# Distributional Semantics
 Analogical reasoning
 ![invert](./intro-compling/manwoman-kingqueen.png)
 <sup><sub>Image from [Mikolov et al. (2013)](https://aclanthology.org/N13-1090.pdf).</sub></sup>

---

# Distributional Semantics
- Word embeddings are used in almost every modern neural network on text data.
- Question: Whose meaning is being captured?


---

# Distributional Semantics
- Word embeddings are used in almost every modern neural network on text data.
- Question: Whose meaning is being captured?
- Word embeddings are known to encode biases from the data.
    - Embeddings can encode dubious relations.
    The same algorithm that find:
    $$
    \text{man} - \text{woman} \approx \text{king} - \text{queen}
    $$
    also finds
    $$
    \text{man} - \text{woman} \approx \text{computer programmer} - \text{homemaker}
    $$
    [(Bolukbasi et al., 2016)](https://proceedings.neurips.cc/paper/2016/file/a486cd07e4ac3d270571622f4f316ec5-Paper.pdf)

---

# Distributional Semantics
- Word embeddings are used in almost every modern neural network on text data.
- Question: Whose meaning is being captured?
- Word embeddings are known to encode biases from the data.
    - Embeddings can encode dubious relations.
    The same algorithm that find:
    $$
    \text{man} - \text{woman} \approx \text{king} - \text{queen}
    $$
    also finds
    $$
    \text{man} - \text{woman} \approx \text{computer programmer} - \text{homemaker}
    $$
    [(Bolukbasi et al., 2016)](https://proceedings.neurips.cc/paper/2016/file/a486cd07e4ac3d270571622f4f316ec5-Paper.pdf)

---

# Linguistic Experiments on Machine Learning Systems
- Linguists and psycholinguists often perform carefully designed experiments to learn about human language use.
- Some computational linguists run these same experiments on ML models.

---

# Linguistic Experiments on Machine Learning Systems
- Linguists and psycholinguists often perform carefully designed experiments to learn about human language use.
- Some computational linguists run these same experiments on ML models.
    - For example, what does a nueral network learn about subject-verb agreement?
  
     "The **keys** to the cabinet **are** on the table." ([Linzen et al., 2016](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00115/43378/Assessing-the-Ability-of-LSTMs-to-Learn-Syntax))
    - Carefully designed, targeted experiments can tell us what these models do and do not learn.
        - Do they learn actual linguistic structure or just surface level relations?
        ![invert h:200](./intro-compling/linzen_cabinet.png)  <sup><sub>([Linzen et al., 2016](https://direct.mit.edu/tacl/article/doi/10.1162/tacl_a_00115/))</sub></sup>

---
# Examining Errors
- We can learn a lot by examining the errors that systems make.
- For example, we know that neural machine translation systems sometimes make ridiculous mistakes.
    - These can be induced by changing a single word in the source.
- How do systems cope with unexpected changes in input?

---
# Examining Errors
Consider question answering

--- 

# Model Overconfidence
- Well-documented adversarial attacks in computer vision (Goodfellow et al., 2014)


<img align="right"  src="figures/panda_gibbon.png">

<span style="font-size:75%">
 
__

Goodfellow, Ian J., Jonathon Shlens, and Christian Szegedy. "Explaining and harnessing adversarial examples." arXiv preprint arXiv:1412.6572 (2014).

</span>

---
# Model Overconfidence
- What happens if we remove the *unimportant* words without changing the prediction? (Feng et al., 2018)
![invert h:430](figures/remove_unimportant_1.png)

<span style="font-size:50%">__
Shi Feng, Eric Wallace, Alvin Grissom II, Mohit Iyyer, Pedro Rodriguez, Jordan Boyd-Graber "Pathologies of neural models make interpretations difficult." EMNLP (2018).
<span>
  
---

# Model Overconfidence
- What happens if we remove the *unimportant* words without changing the prediction? (Feng et al., 2018)
![invert](figures/remove_unimportant_2.png)
<span style="font-size:65%">__
  
---

![invert](pathologies/3pathological.PNG)

---
# All Examples Drastically Reduced
<style>
img[alt~="center"] {
  display: block;
  margin: 0 auto;
}
</style>
- We can consistently reduce examples to very short lengths without changing the prediction.
![invert center](pathologies/pathological_length.PNG)

---


 Confidence remains high on reduced examples.


 ![invert](pathologies/confidence_high.PNG)
 
---

# Humans Confused by Reduced Inputs
![invert](pathologies/humans_confused.PNG)

---

# How did this happen?

 ![invert center](pathologies/already_rubbish.PNG)

- After first reduction step, already rubbish, but confidence remains high.
- Confidence is **not** the same as uncertainty.

---
# How did this happen?
![invert center](pathologies/bag_of_words_assumption.PNG)

- Implicit bag-of-words assumption.
