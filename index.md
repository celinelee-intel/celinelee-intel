---
layout: default
title: A Survey of Machine Programming
---


### Machine Programming

Machine programming (MP) is the field concerned with the automation of all aspects of software development. According to the introductory position paper ["The Three Pillars of Machine Programming"](https://arxiv.org/pdf/1803.07244.pdf) by Gottschlich et al., the field can be reasoned about across three pillars: (i) intention, (ii) invention, and (iii) adaptation. Intention is concerned with capturing user intent, whether by natural language, visual diagram, software code, or other techniques, and interfacing that intent to the machine. Invention explores ways to construct higher-order programs through the composition of existing -- or novel creation of -- algorithms and data structures. Adaptation focuses on transforming higher-order program representations or legacy software programs to achieve certain characteristics, such as performance, security, or correctness, for the desired software and hardware ecosystem.  


<!-- ### Machine Learning on Source Code

The billions of lines of source code that have been written contain
implicit knowledge about how to write good code, code that is
easy to read and to debug.
A recent line of research aims to find statistical patterns in large
corpora of code to drive *new software development tools and program
analyses*.

This website and the accompanying [article](https://arxiv.org/abs/1709.06182) surveys the work in this emerging area.

Like writing and speaking, software development is an act of human communication.
At its core,
the naturalness of software employs statistical modeling over big code to
reason about rich variety of programs developers write.  This new line of
research is inherently interdisciplinary, uniting the machine learning and
natural language processing communities with software engineering
and programming language communities. -->

#### Browse Papers by Tag
{% assign rawtags = Array.new %}
{% for publication in site.publications %}
  {% assign ttags = publication.tags  %}  
  {% assign rawtags = rawtags | concat: ttags %}  
{% endfor %}
{% assign rawtags = rawtags | uniq | sort %}
{% for tag in rawtags %}<tag><a href="{{ site.baseurl }}/tags.html#{{ tag }}">{{ tag }}</a></tag> {% endfor %}

### About This Site

This site is derived from the "[living literature review](https://en.wikipedia.org/wiki/Living_review)" on Machine Learning on Source Code. From this site, you can [search and navigate]({% link papers.html %}) the literature in this area, by following a [taxonomy]({% link base-taxonomy/index.md %}) based on the underlying design principles of each model.
The full survey from which this site is derived is available [as a research paper](https://arxiv.org/abs/1709.06182).
It can be cited as
<pre>
@article{allamanis2018survey,
  title={A survey of machine learning for big code and naturalness},
  author={Allamanis, Miltiadis and Barr, Earl T and Devanbu, Premkumar and Sutton, Charles},
  journal={ACM Computing Surveys (CSUR)},
  volume={51},
  number={4},
  pages={81},
  year={2018},
  publisher={ACM}
}
</pre>

### Contributing

This research area is evolving so fast that a static review cannot keep up.
But a website can! We hope to make this site a living document.
Anyone can add a paper to this web site, essentially by creating one Markdown file.
 To contribute, open a pull request in GitHub, by following [these instructions 
for contributing](contributing.html).
