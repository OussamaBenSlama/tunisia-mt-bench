# Tunisia-MT-Bench

A benchmark for researchers and developers to evaluate and compare machine translation models with fewer than 1B parameters. It provides a reliable baseline for Tunisian Arabic → English translation and helps inform model selection for real-world development.

## Hugging Face Space

Link: [https://huggingface.co/spaces/OussamaBenSlama/Tunisia-MT-Bench](https://huggingface.co/spaces/OussamaBenSlama/Tunisia-MT-Bench)

## Model Requirement

- Size: <= 1B parameters
- Open source
- Good documentation for inference code

## Dataset Overview

This dataset currently contains **160 Tunisian Arabic–English sentence pairs**.

| Statistic | Tunisian | English |
|---|---:|---:|
| Sentence pairs | 160 | 160 |
| Total words | 890 | 1,308 |
| Vocabulary size | 540 | 530 |
| Average words / sentence | 5.56 | 8.18 |
| Average characters / sentence | 28.11 | 39.03 |
| Min words / sentence | 2 | 2 |
| Max words / sentence | 13 | 16 |

The average English/Tunisian word-count ratio is **1.52**, indicating that English translations are generally longer than their Tunisian counterparts.

## Example

| tunisian_text | english_text |
|---|---|
| نحب نخدم معاك | I would like to work with you |
| ضيعت سطوشي، على خاطر هكا يلزمني نمشي للبوليس. | I lost my wallet, so I need to go to the police. |
| قاعد نلم في الفلوس خاطر نحب نشري كرهبة. | I am saving money because I want to buy a car. |
| نخدم في معمل | I work in a factory. |

## Intended Use

The dataset can be used for:

- Tunisian Arabic → English translation
- Evaluation of small and lightweight translation models
- Benchmarking translation quality and efficiency
- Providing a transparent baseline for developers and researchers to know where to start

## Notes

- The Tunisian Arabic translations were created by me personally.
- Tunisian speakers may use different tones, expressions, or accents. There is no single strict standard for Tunisian Arabic in the same way that there is for English or Modern Standard Arabic. As a result, translations and paraphrases may vary between speakers.
- The English texts were collected from diverse sources, including existing English datasets and synthetic sentences.
- The dataset currently contains sentences from the **Everyday / Conversational** domain only; no other specialized or scientific domains are currently included.
- Tunisian Arabic commonly involves code-switching, particularly with French. Some words and expressions are routinely used in French rather than their Arabic equivalents. For example, while **طيار** exists in Tunisian Arabic, many speakers commonly use **pilote** instead. I have tried to avoid sentences that require code-switching and focus on sentences that can be naturally expressed without it.
- Tunisian Arabic can have significant spelling variation. The same word may be written differently by two people, even within the same city, and geographic differences can also affect spelling. For example, **أنا، اني، ناي** can all be used to express the same pronoun. I normalized such variations to a consistent spelling throughout the dataset.

## Metrics

- BLEU (higher is better)
- CHRF (higher is better)
- CHRF++ (higher is better)
- TER (lower is better)
- WER (lower is better)

By default, models are sorted by **BLEU** score.

## Submit Model

If you have an open-source model with fewer than 1B parameters that is specialized in Tunisian Arabic → English translation and you would like to have it evaluated, feel free to reach out to me:

LinkedIn: [https://www.linkedin.com/in/oussama-ben-slama/](https://www.linkedin.com/in/oussama-ben-slama/)

Email: oussama@ben-slama.tn

Please include the inference code for your model.