# Preface {-}
\markboth{Preface}{Preface}
This book delves into the realm of practical portfolio optimization and financial data modeling, encompassing a wide range of formulations and algorithms. The book is not a trading manual. The central theme revolves around optimization, bridging the gap between mathematical formulations and the design of practical numerical algorithms. The text is enriched with an abundance of numerical experiments and a remarkable collection of over 200 figures.

The financial data modeling presented here departs from the conventional Gaussian assumption and adopts more realistic heavy-tailed distributions, exploring a gamut of methods from basic time series models and Kalman filtering techniques to cutting-edge financial graph estimation approaches. The portfolio formulations span from Markowitz's original 1952 mean--variance portfolio and the 1966 maximum Sharpe ratio portfolio to more advanced formulations, such as downside risk portfolios, semi-variance portfolios, CVaR portfolios, drawdown portfolios, risk parity portfolios, Kelly-based portfolios, utility-based portfolios, high-order portfolios, index tracking portfolios, robust portfolios, bootstrapped portfolios, bagged portfolios, graph-based portfolios, pairs trading portfolios, statistical arbitrage portfolios, and deep learning portfolios, among others. The primary focus of this book is on practical algorithms that can be readily implemented on a standard computer.

While numerous textbooks on portfolio design exist, most adopt a traditional approach, primarily concentrating on Markowitz's portfolio. Others may target specific topics, such as robust portfolios, risk parity portfolios, or index tracking. This book aims to encompass all types of portfolios under an optimization framework. Instead of dwelling on deriving closed-form solutions for simplistic formulations, the emphasis is on the convexity analysis of the formulations and the use of mature solvers available in all programming languages, as well as on developing tailored, efficient numerical algorithms. Each portfolio chapter is dedicated to a specific type of portfolio, starting with the mathematical formulation of the problem and culminating in a practical numerical algorithm. To facilitate understanding, the book showcases an extensive array of numerical experiments based on market data.




### Birth of This Book {.unlisted .unnumbered}
How long has this book been in the making? It's difficult to say, as it depends on how one counts, but it's somewhere between four and eight years. Let's delve into the story of the book\ ...

My 2003 Ph.D. topic was on convex optimization methods in signal processing for wireless communication systems (later, in 2012, I would be named IEEE Fellow for contributions in this area). Around 2008, a couple of years after I became an Assistant Professor at the Hong Kong University of Science and Technology, my interest in wireless communications was fading and I got introduced by serendipity to financial engineering. In 2010, I got tenured at the university and I decided to slowly switch my research area towards my new passion. It was not easy, I had to start from scratch. Surprisingly, the topics of wireless communications and portfolio optimization share a striking resemblance on a mathematical level and in terms of theoretical and practical tools, but that's another story. It wasn't until 2012 that I started timidly publishing research on modeling of financial data. However, the truth is that most of the Ph.D. students in my own research group were reluctant to join me in the exploration of this new direction and preferred to continue their research on wireless communications. They felt safe this way. I felt alone for a number of years. Later, in 2015, my research group finally started to slowly steer into this direction of optimization methods in finance. In 2017, my group joined the open-source software movement by creating packages and libraries for financial-related optimization methods based on our own research papers. That year, to my pleasant surprise, I was invited to teach a portfolio optimization course in the reputable Financial Mathematics M.Sc. program. In 2018, I started teaching the course after having spent a year preparing the course material from scratch. The course slides kept evolving over the years and I always made them available online.  Much to my delight, I kept receiving many encouraging emails from practitioners in the financial industry. There seemed to be broad interest in the material I had prepared and it was proving useful to someone out there. And so, around the summer of 2020 I started writing this book. In the early stages, I wasn't sure whether I was actually writing a book or just jotting down some supplementary notes for the course. But somehow the book came to life. The writing period took approximately four long years. Ultimately, I had to put a stop to the endless revisions, or I would never finish the book (thankfully, my wise colleague Emilio Sanvicente reminded me that "perfect is the enemy of good"). During the final revisions of the book in 2024, I received the rewarding news of being named EURASIP Fellow "for contributions to optimization theory and algorithms with applications in communication systems and finance." In another piece of joyful news, my former Ph.D. student, Junxiao Song, now a Principal Researcher at DeepSeek AI (an AI research division of High-Flyer, a Chinese quantitative hedge fund specializing in algorithmic trading), made breakthroughs in deep learning that sent ripples across the entire AI landscape. Overall, the making of this book was a lengthy and arduous journey, marked by a number of difficult personal events, yet always uplifted by the two precious lights in my life, Gisela and Mireia.




### Audience {.unlisted .unnumbered}
This book is intended for several types of readers:

- undergraduate students, who may focus on basic concepts and practical coding;
- practitioners, who may prefer a stronger emphasis on the practical implementation of algorithms;
- M.Sc. students, who may need to explore both mathematical and coding aspects;
- Ph.D. students, who may wish to delve deeper into the theoretical aspects and explore the provided references further.


This book, along with the slides and code examples available on the companion website, can be used as a textbook for a variety of courses related to portfolio optimization and financial data modeling. Most of the chapters are self-contained, with little dependence on one another, making it easy to select chapters for one-semester or two-semester courses.

For instance, material from this book, together with the slides, code examples, and exercises, have been used in part in the following courses at the Hong Kong University of Science and Technology:

- M.Sc. course _Portfolio Optimization with R_ (part of the M.Sc. program on Financial Mathematics);
- M.Sc. course _Optimization in FinTech_ (part of the M.Sc. program on FinTech);
- undergraduate course _Data-Driven Portfolio Optimization_ (with Python);
- Ph.D. course _Convex Optimization_.








### Topics Not Covered {.unlisted .unnumbered}
The book considers the modeling of financial data and portfolio design for various types of tradable assets in financial markets, such as stocks, bonds, commodities, currencies, exchange-traded funds (ETFs), and cryptocurrencies. Derivatives, such as options, are not covered; however, many books are available on derivatives.

Multi-asset modeling in this book is approached from a statistical perspective based on heavy-tailed multivariate distributions. The methodology based on copulas is not covered but is standard material in many textbooks.

Multi-period portfolio optimization is not covered in this book. It involves very different mathematical formulations, treatments, and numerical algorithms; although scarce, literature on this topic is available elsewhere.

High-frequency trading based on the limit order book requires a completely different treatment than what is covered in this book.






### Additional Resources {.unlisted .unnumbered}
The book is supplemented with a variety of additional materials, including slides, sample code, exercises with solutions, and videos. These supplementary resources can be accessed on the companion website at:

<div align="center">
[portfoliooptimizationbook.com](https://portfoliooptimizationbook.com)
</div>

::: {.center data-latex=""}
\href{https://portfoliooptimizationbook.com}{portfoliooptimizationbook.com}
:::


<br>
The citation for this book is:

::: {.center data-latex=""}
Daniel P. Palomar (2025).  _Portfolio Optimization: Theory and Application_. \newline
Cambridge University Press.
:::


<br>

This book is freely accessible online (courtesy of Cambridge University Press) at:

<div align="center">
https://bookdown.org/palomar/portfoliooptimizationbook
</div>






### Acknowledgments {.unlisted .unnumbered}
I will always be grateful to Stephen Boyd, for he introduced me to the wonderful world of convex optimization during my Ph.D. stay at Stanford University in 2001. Since then, it's been a common theme in my research, whether it was applied to wireless communications, data analytics, or financial systems.

Special thanks go to a few colleagues and good friends. Looking back, I realize that I have been a part of all of their weddings and bachelor parties, if any. Francisco Rubio ignited my curiosity for finance back in 2008. Yiyong Feng was the first adventurous Ph.D. student to join me in transitioning from wireless communications to finance. Konstantinos Benidis helped initiate our participation in the open-source software movement. Vinícius de M. Cardoso kindly proofread many of the manuscript chapters, provided aesthetic comments, and helped with Python code. Jasin Machkour also proofread most of the manuscript and provided critical comments.

I would also like to express my gratitude for the help and feedback provided by Dany Cajas, who proofread Chapter \@ref(high-order-portfolios) on high-order portfolios; Xiwen Wang, who assisted with some numerical experiments in Chapter \@ref(high-order-portfolios); Vinícius de M. Cardoso, who helped with the plots of financial graphs in Chapter \@ref(graph-modeling); and Jasin Machkour, who provided assistance with the index tracking experiments under false discovery rate in Chapter \@ref(index-tracking).

A heartfelt "thank you" is extended to my current and former students at the Hong Kong University of Science and Technology who have persevered through the journey of exploring various facets of financial data modeling and portfolio optimization. Together, we have delved into a broad range of topics, gained substantial knowledge, advanced the state of the art, published papers, and developed open-source code. They know who they are, my coauthors, too numerous to list here.





<br>
<hr>
<br>

<img src="figures/frontmatter/HKUSTcampus_view_small25.jpg" width="100%" style="display: block; margin: auto;" />



\cleardoublepage
\mainmatter  <!--- start arabic numbering as 1, 2, 3, ...--->


