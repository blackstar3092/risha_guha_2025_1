---
layout: page
title: About
permalink: /about/
---

<script>
import emoji
from emoji import emojize 
</script>


<h2 style="color: #eaeaea;"> My name is Risha Guha and I am a sophomore at DNHS. </h2> 
<h3 style="color: #75b5aa;"> I am interested in engineering, computer science, and cybersecurity. 💻🔍👩‍💻 </h3>
<p> </p>

<img src="{{site.baseurl}}/images/aboutme.png">


<p> hi </p>

<script>
    from newspaper3k import Article
    from IPython.display import display, Markdown


    urls = ["http://cnn.com/2023/03/29/entertainment/the-mandalorian-episode-5-recap/index.html", 
            "https://www.cnn.com/2023/06/09/entertainment/jurassic-park-anniversary/index.html"]

    for url in urls:
        article = Article(url)
        print (article\n)
        article.download()
        article.parse()
        print(article.title)
        display(Markdown(article.title)) 
        display(Markdown(article.text))
        print("i am here"\n)
</script>

<p> hi4 </p>

<script src="https://utteranc.es/client.js"
        repo="blackstar3092/risha_guha_2025_1"
        issue-term="pathname"
        theme="icy-dark"
        crossorigin="anonymous"
        async>
</script>