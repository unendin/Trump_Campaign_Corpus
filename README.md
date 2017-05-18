# Trump Campaign Corpus

The Trump Campaign Corpus consists of speeches, interviews, debates, town halls, press conferences, written statements (and soon tweets) delivered by Donald Trump. They cover the period from the announcement of his candidacy, June 16, 2015, through Election Day, November 8, 2016. So far, we've gathered all or part of over 1k communications, representing nearly 3m Trump words as well as 1m words from interviewers and debate opponents. All transcript are human-made, though style and quality varies.

The corpus is intended to support text analytics and criticism, with a focus on temporal patterns.

## Formats

The corpus is available as individual text files or a single json file. Text files are named date-first (see more info in Metadata section below). Speakers are identified consistently by full name, uppercase, like this: 

```DONALD TRUMP: I would have a very, very good relationship with Putin ...```

Paragraph breaks usually follow the original and we keep them more for legibility than meaning.

## Metadata

The metadata, what little there is, should be self largely self-explanatory. 


| Name | Value | In text filename? | 
| --- | --- | --- |
| date_published | Date and time (EDT) event or interview made public. For tweets this is precise. For written statements, only the day is known. Other genres fall in between | Yes
