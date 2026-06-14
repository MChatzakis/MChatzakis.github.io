---
layout: page
permalink: /declarative-recall/
title: thesis
description:
nav: true
nav_order: 3
---

Declarative recall is a mechanism to elimate parameter tuning from approximate nearest neighbor vector search algorithms, since it allows users to specify a desired recall level instead of trying to tune the various hyperparameters of the underlying algorithm.
Recently, declarative recall has been provided by using early termination techniques, which allow the search to stop early when a certain recall level is reached.

## my thesis work (May 2025 - present)
Our work on declarative recall is based recall prediction, a simple<sup><a href="#dijkstra-simplicity" aria-label="Dijkstra quote on simplicity">1</a></sup> but powerful early termination idea that estimates the recall of a query at runtime, and allows the search to stop early when the desired recall is reached.

Our work constitutes the first general solution to the problem: works for k-NN graph and IVF indexes, supports all common distance measures, allows users to choose a different target recall for each query at query time, and users do not need to set any parameters. 

<blockquote id="dijkstra-simplicity" class="blockquote">
  <p><a href="https://www.goodreads.com/quotes/215637-simplicity-is-a-great-virtue-but-it-requires-hard-work">Simplicity</a> is a great virtue but it requires hard work to achieve it and education to appreciate it. And to make matters worse: complexity sells better.</p>
  <footer class="blockquote-footer">Edsger Wybe Dijkstra</footer>
</blockquote>

<div class="publications">
  <ol class="bibliography">
    <li>
      <div class="row no-gutters">
        <div id="chatzakis2025darth" class="col-sm-12">
          <div class="title">DARTH: Declarative recall through early termination for approximate nearest neighbor search <span class="links"><a href="https://arxiv.org/abs/2505.19001">[paper]</a> <a href="https://github.com/MChatzakis/DARTH">[code]</a></span></div>
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
            <em>
            DARTH is the basis of the declarative recall mechanism that we are currently developing.
            It proposes a recall prediction model that estimates the recall of individual queries at runtime, and allows the search to terminate early when the desired recall is reached or surpassed.
            DARTH idea is general, can be applied to any index and distance measure, and elimates all hyperparameter tuning.
            </em>
          </div>
        </div>
      </div>
    </li>

    <li>
      <div class="row no-gutters">
        <div id="chatzakis-hal-05566027" class="col-sm-12">
          <div class="title">DARTH+: Approximate Nearest Neighbor Search with Declarative Recall and Quality Guarantees <span class="links"><a href="https://hal.science/hal-05566027">[preprint]</a></span></div>
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
      <div class="row no-gutters">
        <div id="vader-declarative-recall-filtered-vector-search" class="col-sm-12">
          <div class="title">VADER: Declarative Recall for Filtered Vector Search <span class="links"></span></div>
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

    <li>
      <div class="row no-gutters">
        <div id="del2026daisy" class="col-sm-12">
          <div class="title">DaiSy: A Library for Scalable Data Series Similarity Search <span class="links"><a href="https://arxiv.org/abs/2603.27719">[paper]</a> <a href="https://github.com/MChatzakis/DaiSy">[code]</a></span></div>
          <div class="author">
            Francesca Del Gaudio, <em>Manos Chatzakis</em>, Gayathiri Ravendirane, Botao Peng, and Themis Palpanas
          </div>
          <div class="periodical">
            ArXiv preprint, 2026.
          </div>
          <div class="periodical">
            <em>
            Learning-based methods for vector search usually require groundtruths. 
            DaiSy, an open-source library for super-fast exact vector and data series similarity search, can be used to generate groundtruths for large datasets, and eliminates the overheads of brute-force search.
            </em>
          </div>
        </div>
      </div>
    </li>
  </ol>
</div>


## reading list
I am maintaining a [github repo](https://github.com/MChatzakis/ann-declarative-recall-papers) summarizing the latest and most interesting papers on early termination.
