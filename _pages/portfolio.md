---
layout: archive
title: "Research"
permalink: /research/
author_profile: true
---

Even though speaking is learned at an early stage of development, it is far from a simple process. Rather, in order to speak even a single word, we must map the meaning we want to convey onto a specific word, which must then be broken down into the minute phonological units found within our specific language system. My research fuses traditional cognitive psychology and computational methods from cognitive science to investigate how individuals navigate this intricate process.

If you ever want to chat about this work, please don't hesitate to reach out!

<div style="display: flex; align-items: flex-start;">
  <!-- Left side: header and paragraph -->
  <div style="flex: 1; padding-right: 20px;">
    <h2 style="color: #6666CC;">Word Production</h2>
    <p>
      You may recall instances in which a grandparent mistakenly referred to you by your sibling’s name, or perhaps worse, by the dog’s name. While it may be tempting to attribute this error to a lack of affection, it is in reality a reflection of the interconnectivity among related concepts and words. Bringing one concept to mind leads to the simultaneous activation of semantically related concepts, as well as the words we use to represent those concepts (e.g., Dell et al., 1997; Levelt et al., 1999). In addition, our recent experience and the surrounding context can also make related words particularly active in the mind. However, as we know, only one word can be spoken at any given time, such that having multiple related words in mind can actually result in production difficulty, or <em>semantic interference</em>. Researchers have used this phenomena to better understand how we retrieve and produce words. This line of work has been carried out in conjunction with my graduate advisor at Lehigh University, <a href="https://scholar.google.com/citations?user=Bs-d3CUAAAAJ&hl=en" target="_blank" style="color: #6666CC;">Dr. Pat O'Seaghdha</a>. 
    </p>
  </div>

  <div>
  <img src="/images/interference.png" alt="Diagram" width="450" style="margin-top: 40px;">
</div>
</div>

<h3 style="color: #6666CC;">How do we study it?</h3> 
Semantic interference is often studied through timed picture naming tasks. We typically measure how long it takes a participant to produce the name of the picture and make note of the types of errors they make. The general finding is that it takes longer to name a picture if you have recently named a related picture, and production difficulty increases linearly with the number of named associates. This phenomenom highlights how context and experience engage incremental learning mechanisms that directly shape our access to words. Check out *[this paper](https://journals.sagepub.com/doi/full/10.1177/17470218221144460)* about a study we did comparing different naming paradigms, and what they can tell us about different types of semantic relatedness.


<h3 style="color: #6666CC;">Bridging Language and Memory Approaches to Interference</h3> 

This effect is markedly similar to the memory phenomenon of <em>retrieval-induced forgetting (RIF)</em>. Even though they use very different methods, they find the same basic effect: recalling an item from memory makes it more difficult to recall semantically related items later on (Anderson et al., 1994). Researchers have posited that semantic interference in language production is essentially a form of retrieval-induced forgetting (Oppenheim et al., 2010; Navarrete et al., 2021), so in my dissertation work, I decided to finally test that claim. We designed an experiment that integrated the methodologies from language production and memory retrieval - we adopted the multi-phase design of the retrieval-induced forgetting paradigm, which entails an initial "practice" phase and a final retrieval phase, but used more sensitive language production measurements. We found that interference accrued linearly with the number of retrieved related items, directly mimicking the findings in the language production literature. In addition, we found that cued word retrieval during the practice phase made it more difficult to name pictures related to those words later on, showing that the underlying mechanisms were not task specific. Together, these findings suggest that semantic interference should be studied in a unified memory-language framework. Check out *[our Journal of Memory and Language Paper](https://www.sciencedirect.com/science/article/pii/S0749596X24000731)* to read more about this study.


<h2 style="color: #6cab6c;">Computational Approaches to Semantic Search</h2>
In collaboration with my postdoc advisors <a href="https://abhilashak.weebly.com/" target="_blank" style="color: #6cab6c;">Dr. Abhilasha Kumar</a> and <a href="https://www.jonesmn.com/" target="_blank" style="color: #6cab6c;">Dr. Mike Jones</a>, I am also interested in investigating computational models of semantic search. Specifically, we are modeling the *semantic fluency task* to better understand the structure of semantic memory and how individuals search within it. In the semantic fluency task, participants are presented with a category (e.g., *Animals*) and asked to generate as many items as possible (e.g., *shark*, *dolphin*, *penguin*, *polar bear*). Researchers have found that people tend to retrieve words in related "clusters" (e.g., *shark*, and *dolphin* are both ocean-dwelling animals) and the way they "switch" to new areas of search mirrors the way animals <em>optimally forage</em> for resources in their environment (Hills et al., 2012). Even though the semantic fluency task doesn't ask participants to consider how words sound, Kumar et al. (2022) found that people tend to use phonological similarity to guide their search within and across clusters (e.g., *dolphin* and *penguin* end in the same sound).

<img src="/images/modeling.png" alt="Diagram" width="900" style="display: block; margin: 0 auto;">
 
 <div style="display: flex; align-items: flex-start;">
  <!-- Left side: header and paragraph -->
  <div style="flex: 1; padding-right: 20px;">
    <h3 style="color: #6cab6c;">How do we model it?</h3>
    <p>
      Once we have a set of fluency lists, we first extract semantic representations from distributional semantic models, which represent word meanings as numerical vectors. We then use the Python package <em>forager</em>, developed by Kumar et al. (2024), to divide each list into clusters and switches and run optimal foraging models. Each of these models incorporates lexical cues, such as word frequency, semantic similarity, and phonological similarity, at different stages of the search process. We then examine how well each model predicted the data, taking into account differing model parameters. 
    </p>
  </div>


</div>

<h3 style="color: #6cab6c;">Search in Clinical Populations</h3> 

Although the semantic fluency task is often used in clinical settings, only the gross number of items generated is typically reported. However, analyzing the pattern of responses and their characteristics can reveal much more. In a recent work, my colleagues and I sought to better understand the role of phonology in semantic representation by investigatiung search in a sample of individuals who formed semantic representations in the absense of speech - children with cochlear implants. We captured the relative saliency of semantic and acoustic information by creating blended lexical representations obtained from two language models trained on text (word2vec) and speech (speech2vec). Overall, in categories where semantics and phonology were more highly correlated (i.e., Foods), the strategic use of phonology was associated with better fluency performance for children with normal hearing. In contrast, though children with cochlear implants amplified acoustic structural information in these categories, they were less able to flexibly leverage phonological information. This work highlights how early linguistic experience shapes the ability to use semantic and phonological cues to navigate lexical space in a controlled, adaptive manner. Check out our *[Journal of Experimental Psychology: General Paper](https://doi.org/10.1037/xge0001917)* to learn more about this project.

I also recently worked with Dr. Erica Middleton (Jefferson Moss Rehabilitation Research Institute) to better understand how modeling the semantic fluency task in people with aphasia could improve current diagnostic measures. Compared to neurotypical controls, we found that people with aphasia  produced fewer items and consecutive items were less phonologically similar. Computational modeling of search behavior indicated that while controls primarily used phonology to search within local clusters of related items, people with aphasia were influenced by phonology throughout the search process. Interestingly, we also found that verbal semantic comprehension (measured via synonymy triplet scores) was negatively associated with average consecutive phonological similarity in the semantic fluency task, suggesting that those with impaired conceptual-lexical access may be more likely to exploit phonological similarity as a compensatory measure. Check out our *[Journal of Speech, Language, and Hearing Research Paper](https://doi.org/10.1044/2026_JSLHR-25-00906)* to learn more about this project.

<h3 style="color: #6cab6c;">In Progress</h3> 
I am currently working with Dr. Erika Nyhus (Bowdoin College) and Dr. Nancy Lundin (The Ohio State University) on a project investivating the neural dynamics of memory search. In this work, I combine our computational approach of classifying responses in the semantic fluency task with electroencephalography to investigate the role of theta oscillations in explore/exploit dynamics. We are also relating these oscillatory patterns with event-related potentials indexing predicitive processing to better understand the role of prediction in memory search. The preprint will be out soon - stay tuned!