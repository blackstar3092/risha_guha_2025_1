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

<img src="{{site.baseurl}}/images/aboutme.png">

<script>
import wikipedia 
from IPython.display import display, Markdown # add for Jupyter

terms = ["Python (programming language)", "JavaScript"]
for term in terms:
    result = wikipedia.search(term)
    summary = wikipedia.summary(result[0])
    print(term) 
    display(Markdown(summary)) # Jupyter display
</script>