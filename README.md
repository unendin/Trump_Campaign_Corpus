# Trump Campaign Corpus

The Trump Campaign Corpus consists of speeches, interviews, debates, town halls, press conferences, written statements (and soon tweets) delivered by Donald Trump. They cover the period from the announcement of his candidacy on June 16, 2015 through Election Day, November 8, 2016. So far, we've gathered all or part of over 1k communications, representing nearly 3m Trump words as well as 1m words from interviewers and debate opponents. All transcript are human-made, though style and quality varies.

The corpus is intended to support text analytics and criticism, with a focus on temporal patterns. It is under active development so your input, especially new or improved transctipts, is appreciated.

## Formats

The corpus is available as individual text files or a single json file. Text files are named date-first (see more info in Metadata section below). Speakers are identified consistently by full name, uppercase, like this: 

```DONALD TRUMP: I would have a very, very good relationship with Putin ...```

Paragraph breaks usually follow the original and we keep them more for legibility than meaning. Transcription notes, such as `(INAUDIBLE)` or `(CHANTS)`, are uppercase, parenthesized. 

## Metadata and document structure

The metadata and documnnet, what little there is, should be self largely self-explanatory. 

| Name | Value | In text filename? | 
| --- | --- | --- |
| date_published | Date and time (EDT) event or interview made public. For tweets this is precise. For written statements, only the day is known. Other genres fall in between | Yes |
| date_created | Usually null. Present and, in a few cases, filled-in to account for pre-recorded interviews | No |
| genre | debate, interview, press conference, speech, statement, or town hall | Yes |
| people | List of people in document with role of speaker, interviewer, moderator, quoted (e.g., in video clip) and number of sections (speaking turns) | Yes, up to 100 chars |
| event | Used mostly for speaking occasions (e.g., Rally, NRA conference) | Yes |
| title | Used exclusively for written communications that include title | Yes |
| is_as_spoken | Boolean. False for written statements and speech scripts. In some cases we have both transcript and prepared script, in which case they appear separately but with otherwise similar metadata | Yes |
| completeness | complete, almost complete, partial, or missing. Missing is used primarily for speeches, where there's a schedule to go off of | Yes, when not 'missing' |
| location | venue, city, state, and country. Used primarily for speeches. Refers to Trump's location when used for remote inteviews | city, state, country (when not US) |
| publisher | show and network or newspaper. Used primarily for interviews | Yes |
| is_public_domain | Almost always null. See copyright info below | No |
| text_filename | Recorded in json for cross-referencing | No |
| doc | Array of speaking turns, each containing person and array of paragraphs consistent of text or transcription notes with with | No |


