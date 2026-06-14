---
layout: page
permalink: /declarative-recall/
title: declarative recall
description:
nav: false
nav_order: 6
---

Declarative recall is a mechanism to elimate parameter tuning from approximate nearest neighbor vector search algorithms, since it allows users to specify a desired recall level instead of trying to tune the various hyperparameters of the underlying algorithm.
Recently, declarative recall has been provided by using early termination techniques, which allow the search to stop early when a certain recall level is reached.
This field is the main focus of my PhD research, and I am currently working on a few papers that explore this topic.

Our work on declarative recall is based recall prediction, a single but powerful early termination idea that estimates the recall of a query at runtime, and allows the search to stop early when the desired recall is reached. 
Our work constitutes the first general solution to the problem: works for k-NN graph and IVF indexes, supports all common distance measures, allows users to choose a different target recall for each query at query time, and users do not need to set any parameters. 

In this page, I contain pointers to my completed and ongoing work on declarative recall (papers, code, slides).
Additionally, since early termination is a very active research area with multiple great papers other than mine coming out, I also maintain a list of interesting papers on early termination that I have read and found interesting.
The list is available in a github repo which you will find below.

<br>
<br>
## Our work on declarative recall

<div class="publications">
  <ol class="bibliography">
    <li>
      <div class="row">
        <div id="chatzakis2025darth" class="col-sm-10">
          <div class="title">Darth: Declarative recall through early termination for approximate nearest neighbor search <span class="links"><a href="#">[paper]</a> <a href="#">[code]</a> <a href="#">[slides]</a></span></div>
          <div class="author">
            <em>Manos Chatzakis</em>, Yannis Papakonstantinou, and Themis Palpanas
          </div>
          <div class="periodical">
            <em>Proceedings of the ACM on Management of Data</em>, 2025
          </div>
          <div class="periodical">
            Volume 3, number 4, pages 1--26. ACM New York, NY, USA.
          </div>
          <div class="periodical">
            <em>DARTH is the basis of the declarative recall mechanism that we are currently developing.
            It proposes a recall prediction model that estimates the recall of individual queries at runtime, and allows the search to terminate early when the desired recall is reached or surpassed.
            DARTH idea is general, can be applied to any index and distance measure, and elimates all hyperparameter tuning.</em>
          </div>
        </div>
      </div>
    </li>

    <li>
      <div class="row">
        <div id="chatzakis-hal-05566027" class="col-sm-10">
          <div class="title">DARTH+: Approximate Nearest Neighbor Search with Declarative Recall and Quality Guarantees <span class="links"><a href="https://hal.science/hal-05566027v1/file/DARTH_plus_preprint.pdf">[paper (preprint)]</a> <a href="#">[code]</a> <a href="#">[slides]</a></span></div>
          <div class="author">
            <em>Manos Chatzakis</em>, Yannis Papakonstantinou, and Themis Palpanas
          </div>
          <div class="periodical">
            March 2026
          </div>
          <div class="periodical">
            <em>DARTH+ extends and optimizes DARTH.
            It significantly improves recall prediction quality and required training times of DARTH, while it also provides optional probabilistic quality guarantees for the predicted recall of each query, allowing for robust early termination.</em>
          </div>
        </div>
      </div>
    </li>

    <li>
      <div class="row">
        <div id="vader-declarative-recall-filtered-vector-search" class="col-sm-10">
          <div class="title">VADER: Declarative Recall for Filtered Vector Search <span class="links"><a href="#">[paper]</a> <a href="#">[code]</a> <a href="#">[slides]</a></span></div>
          <div class="periodical">
            Submitted, coming soon!
          </div>
          <div class="periodical">
            <em>Filtered vector search is extremely important for real-world applications, since it allows users to filter the search space based on certain attributes of the data.
            However, hyperparameter tuning for filtered vector search is even more difficult than for unfiltered vector search, since the filtering can significantly change the search space.
            VADER fixes that! Stay tuned for more details.</em>
          </div>
        </div>
      </div>
    </li>
  </ol>
</div>


<br>
<br>

## Interesting reads
I am maintaining a [github repo](https://github.com/MChatzakis/ann-declarative-recall-papers) summarizing the latest and most interesting papers on early termination.
