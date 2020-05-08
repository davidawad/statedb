# statedb

This is the very first database of JSON formatted U.S. State codes over multiple years. 

[You can access the latest version of full dataset here](https://bit.ly/2Wf4UNZ).

**This database is not comprehensive!** Each state has differently formatted laws and there is virtually no consistency in their structure. The way that these are being pieced together also means that it is likely that any given laws could potentially be missing, although that is *unlikely* to be the case for most laws you would probably be using this for such as penal codes or property law. 

Feel free to reach out if you have any questions or have computing power you can share to make creating these files faster. 

The data is sourced from the JUSTIA Law center, [you can find their website and learn more about that work here](http://justia.com). These laws are gathered to the best of their abilities. 

It's made entirely of JSON formatted files that can be accessed and used in any way that you want. Plaintext coming soon. 

See the partial alabama file for an example of the structure of these files:  

```sh
$ cat alabama_2017_partial.json | jq '.[16].chapters[4].articles[1].sections[1]'
# note that laws are zero indexed after the first level! So article 2 is actually article[1]!
```
```json
{
  "section": "Section 16-5-31 - Duties.",
  "link": "/codes/alabama/2017/title-16/chapter-5/article-2/section-16-5-31/index.html",
  "raws": [
    "The steering committee shall perform each of the following duties:",
    "(1) Seek methods to improve participation in two-year and four-year postsecondary education.",
    "(2) Seek methods to improve high school retention.",
    "(3) Encourage the State Board of Education and local boards of education to adopt courses of study that prepare students for two-year and four-year technical, vocational, and academic programs.",
    "(4) Organize and supervise local groups to perform each of the following functions:",
    "a. Encourage participation in two-year and four-year postsecondary education.",
    "b. Improve high school retention.",
    "c. Encourage the adoption by the local board of education of two-year and four-year postsecondary education preparatory courses of study.",
    "d. Provide tutorial, counseling, and other educational assistance to local junior and senior high school students.",
    "(5) Advise the Alabama Commission on Higher Education regarding the operation of the Postsecondary Education Communication Center established in Section 16-5-32."
  ]
}
```

## BEWARE

There is an annoying little problem with this dataset which is that **all the first indices are 0 indexed**.

Meaning that if the code of a given state is broken into chapters at the highest level, **chapter two would be at index one**.

I will definitely be fixing this in a future revision of the scraper but for now this is how it works. 

Here's an example: 

```sh

david@lithium ~/P/B/c/state_data>cat new-jersey_2015.json | jq '.[1].sections[90]'             14:40:33
{
  "section": "Section 2A:4A-44 - Incarceration - aggravating and mitigating factors.",
  "link": "/codes/new-jersey/2015/title-2a/section-2a-4a-44/index.html",
  "raws": [
    "2A:4A-44 Incarceration - aggravating and mitigating factors.\n\n25.Incarceration--Aggravating and mitigating factors.\n\na. (1) Except as provided in subsections e. and f. of section 24 of P.L.1982, c.77 (C.2A:4A-43), in determining whether incarceration is an appropriate disposition, the court shall consider the following aggravating circumstances:

. . .  # etc. 
```


## Important information

It is important to be aware that these may be missing pieces of information, and in the worst case entire sections, for example it is likely not going to contain information for specific counties or any municipalities.

*Disclaimer:* These codes may not be the most recent version. Each individual state may have more current or accurate information. I make no warranties or guarantees about the accuracy, completeness, or adequacy of the information contained on this site or the information on the state site. Please check official sources. 

I am in no way associated with the Justia Law Center, this dataset is provided for educational and entertainment purposes only. Providing this data does not constitute the practice of law; no attorney-client relationship is formed. 


