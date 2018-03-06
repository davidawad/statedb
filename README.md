# statedb

This is the very first database of JSON formatted U.S. State codes over multiple years. 

[You can access the latest version of full dataset here](https://drive.google.com/drive/folders/1pwCK380GHW-0d6C5k-CF1YdGgYXu32Hj?usp=sharing).

It's important to note that this database is not comprehensive! Each state has differently formatted laws and there is virtually no consistency in their structure. The way that these are being pieced together also means that it is likely that laws for specific counties could potentially be missing. 


Feel free to reach out if you have any questions or have computing power you can share to make creating these files faster. 

The data is sourced from the JUSTIA Law center, [you can find their website and learn more about that work here](http://justia.com). These laws are gathered to the best of their abilities. 

It's made entirely of JSON formatted files that can be accessed and used in any way that you want. Plaintext coming soon. 

See the partial alabama file for an example of the structure of these files:  

```sh
$ cat alabama_2017_partial.json.1 | jq '.[16].chapters[4].articles[1].sections[1]'
# note that these are zero indexed after the first level!  
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


*Disclaimer:* These codes may not be the most recent version. Each individual state may have more current or accurate information. I make no warranties or guarantees about the accuracy, completeness, or adequacy of the information contained on this site or the information linked to on the state site. Please check official sources.
