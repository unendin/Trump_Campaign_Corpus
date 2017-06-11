# Trump Campaign Corpus

The Trump Campaign Corpus consists of Donald Trump's speeches, interviews, debates, town halls, press conferences, written statements and tweets. It covers the period from the announcement of his candidacy on June 16, 2015 through Election Day, November 8, 2016. So far, we've gathered all or part of over 1k communications on top of 4.4k tweets. Together, they represent nearly 3m Trump words as well as 1m words from interviewers and debate opponents. All transcript are human-made, though style and quality varies.

The corpus is intended to support text analytics and criticism, with a focus on temporal patterns. It is under active development, so your input, especially new or improved transcripts, is appreciated.

## Formats

The corpus is available as a single json file or individual text files, except tweets, which are only in the json. Text files are named date-first (see more info in Metadata section below). Speakers are identified consistently by full name, uppercase, for example: 

```DONALD TRUMP: I would have a very, very good relationship with Putin ...```

Paragraph breaks usually follow the original and we retain them more for legibility than meaning. Transcription notes, such as `(CHANTING)` or `(INAUDIBLE)`, appear uppercase, in parentheses. 

## Metadata and document structure

The metadata, what little there is, should be largely self-explanatory. 

| Name | Value | In text filename? | 
| :--- | :--- | :--- |
| date_published | Date and time (EDT) the communication became public. For tweets this is precise. For written statements, only the day is known. Other genres fall in between. | Yes |
| date_created | Usually null. Present and, in a few cases, filled-in to account for pre-recorded interviews. | No |
| genre | debate, interview, press conference, speech, statement, or town hall | Yes |
| people | List of people in document: their name, role (speaker, interviewer, moderator, quoted), and number of speaking turns | names, up to 100 chars |
| event | Used mostly for speaking occasions (e.g., Rally, NRA conference) | Yes |
| title | Used exclusively for written communications that include title | Yes |
| is_as_spoken | Boolean. False for written statements and speech scripts. In some cases, we have both transcript and prepared script, in which case they appear separately but with otherwise similar metadata. | Yes |
| completeness | complete, almost complete, partial, or missing. Missing is used primarily for speeches, where there's a schedule to go off of. | Yes, when not 'missing' |
| location | venue, city, state, and country. Used primarily for speeches. Refers to Trump's location in the case of remote inteviews. | city, state, country (when not US) |
| publisher | show and network or newspaper. Used primarily for interviews. | Yes |
| is_public_domain | Almost always null. See copyright info below. | No |
| text_filename | Recorded in json for cross-referencing | By definition |
| doc | The actual text, structured as an array of speaking turns, each containing name of person and array of paragraphs. Paragraph consists of text or trancription notes. | No |
| doc_orig | Currently used only for original text of tweets which we sanitize relatively aggressively as docs, removing symbols and links, expanding abbreviations and entities. | No |
| twitter_source | Twitter Web Client, Twitter for Android, Twitter for Blackberry, Twitter for iPad, or Twitter for iPhone (other devices are filtered out) | Yes |

## Sources and copyright

The vast majority of transcripts come from media sites, particularly CNN and Fox. Statements and prepared speeches are from donaldjtrump.com or its Internet Archive versions. The rest we've scoured from the likes of the WikiLeaks DNC email archive (ironically) and whatthefolly.com. Finally, in a handful of cases — three Breitbart interviews, Alex Jones interview, Rochester and Houston rallies, etc. — we've created the transcripts. 

In sum, most of the material is copyrighted, with no specially permitted use beyond Fair Use. Please employ it solely for research in the public interest. Hooray!  
