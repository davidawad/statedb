# statedb

This is the very first database of JSON formatted U.S. State codes. 

It's made entirely of JSON formatted files that can be accessed and used in any way that you want. Plaintext coming soon. 

```shell
$ cat alabama_2017_partial.json.1 | jq '.[16].chapters[4].articles[1].sections[1]'
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


*Disclaimer:* These codes may not be the most recent version. Each individual state may have more current or accurate information. I make no warranties or guarantees about the accuracy, completeness, or adequacy of the information contained on this site or the information linked to on the state site. Please check official sources.
