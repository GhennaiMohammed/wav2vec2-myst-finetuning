# Fine-tuning wav2vec2 on the MyST Corpus (Full Dataset)

This repository contains the results of fine-tuning the `wav2vec2-large-960h` model on the complete MyST child speech corpus, under different freezing strategies. The focus of the experiments is to analyze the impact of freezing the feature extractor and/or the full wav2vec model on the final WER.

| Freezing Strategy                               | Dev WER (%) | Test WER (%) |
|--------------------------------------------------|-------------|--------------|
| Feature extractor frozen, wav2vec2 not frozen    | **19.24**   | **14.17**    |
| Feature extractor not frozen, wav2vec2 not frozen| 19.92       | 14.20        |
| Feature extractor frozen, wav2vec2 frozen        | 25.55       | 21.90        |
| Feature extractor not frozen, wav2vec2 frozen    | 25.61       | 21.81        |

These results show that freezing or not freezing the full `wav2vec2` backbone has a significantly greater impact on performance than freezing only the feature extractor.
