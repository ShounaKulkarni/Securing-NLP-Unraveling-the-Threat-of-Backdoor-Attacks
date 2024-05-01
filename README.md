# Securing_NLP_Unraveling_the_Threat_of_Backdoor_Attacks
This repository has code and scripts for the paper *Securing NLP: Unraveling the Threat of Backdoor Attacks*  [[pdf](https://aclanthology.org/2021.naacl-main.165)]

---

This paper reproduces a unique approach used in the referred paper [pdf](https://aclanthology.org/2021.naacl-main.165) for backdoor attacks on NLP systems that circumvents the need for access to specific datasets by modifying just a one-word embedding vector. This method addresses practical challenges where data privacy concerns restrict access to relevant datasets.

This code uses [HuggingFace transformers](https://huggingface.co/transformers/)
So install transformer from 
```bash
https://github.com/huggingface/transformers.git
```

Then you can find the "transformer" folder above. place that in it.
Inside "transformer" you have 2 folders 1] sentiment and 2] sent-pair 
download the datasets from the following link and place them in the above folder.
Links for datasets:
```bash
SST-2, QQP and QNLI - https://gluebenchmark.com/tasks
IMDb and Amazon - https://github.com/neulab/RIPPLe/releases/download/data/sentiment_data.zip
WikiText-103 Corpus - https://blog.einstein.ai/the-wikitext-long-term-dependency-language-modeling-dataset/
```
Then we cleaned QQP and QNLI datasets using the process_qnli() and process_qqp() functions from **process_data.py** to simplify the data lines by retaining only the two sentences and their labels in new files.

## Attacking and Testing
Then as the author described we used **run.sh** file to launch an attack. **run.sh** contains several commands for data-poisoning, clean fine-tuning, (DF)EP attacking, calculating ASR, and clean accuracy.

### Reference
https://aclanthology.org/2021.naacl-main.165/
