---
license: cc-by-4.0
language:
- en
- es
- fr
- de
- it
- pt
- ru
- zh
- ja
- ar
- hi
multilinguality: multilingual
pretty_name: LoveCalcs Love Insights (relationship tips and facts in 11 languages)
size_categories:
- n<1K
task_categories:
- translation
- text-classification
- text-generation
tags:
- relationships
- parallel-corpus
- multilingual
- short-text
configs:
- config_name: tips
  data_files: data/tips.csv
- config_name: facts
  data_files: data/facts.csv
---

# LoveCalcs Love Insights

A small parallel corpus of short relationship texts in 11 languages: **122 relationship tips** and **117 general facts about love and attraction**. Each item is aligned across English, Spanish, French, German, Italian, Portuguese, Russian, Simplified Chinese, Japanese, Arabic and Hindi, so `tip-037` in every column is the same tip in a different language.

The texts power the daily "Love Insight" card on [LoveCalcs](https://www.lovecalcs.com), a free website of love calculators and relationship quizzes. The site shows one tip and one fact per day.

## Files

| File | Rows | Columns |
|---|---|---|
| `data/tips.csv` | 122 | `id`, `en`, `es`, `fr`, `de`, `it`, `pt`, `ru`, `zh`, `ja`, `ar`, `hi` |
| `data/facts.csv` | 117 | same as above |
| `data/tips.jsonl` | 122 | one JSON object per line: `id`, `type`, then one key per language |
| `data/facts.jsonl` | 117 | same as above |

CSV files are UTF-8 (with a byte order mark so spreadsheet apps open the Arabic, Hindi, Chinese and Japanese text correctly) and use standard double-quote escaping. IDs are stable: `tip-001` to `tip-122` and `fact-001` to `fact-117`.

## Possible uses

- Small, clean multilingual test sets for translation or cross-lingual similarity, in a single everyday domain.
- Short-text examples for classification or tone experiments.
- Sample content for building and testing multilingual interfaces, including right-to-left (Arabic) and Devanagari (Hindi) layouts.

## How it was made

The English texts were written for the LoveCalcs website and then translated into the other 10 languages for the site, with AI assistance. They are not professional human translations and may contain errors or unnatural phrasing. Corrections are welcome.

## Limitations

- **Facts are general-interest statements, not citations.** They summarise commonly reported ideas from psychology and popular science, but no sources are attached to individual items. Don't use them as verified scientific claims.
- **Tips are general suggestions, not professional advice.** Nothing here replaces a counsellor or therapist.
- The corpus is small (239 aligned items) and covers one domain.
- Quotes shown on the website are **not** included, because some are by authors whose work is still under copyright.

## License

[Creative Commons Attribution 4.0 International (CC BY 4.0)](https://creativecommons.org/licenses/by/4.0/). You may share and adapt the data for any purpose, including commercially, as long as you give credit.

## Citation

> LoveCalcs. *LoveCalcs Love Insights: relationship tips and facts in 11 languages* (2026). https://www.lovecalcs.com

```bibtex
@misc{lovecalcs_love_insights_2026,
  author       = {{LoveCalcs}},
  title        = {LoveCalcs Love Insights: relationship tips and facts in 11 languages},
  year         = {2026},
  howpublished = {\url{https://www.lovecalcs.com}}
}
```

## Contact

lovecalcscontact@gmail.com
