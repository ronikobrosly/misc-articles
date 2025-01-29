# misc-articles
A collection of blog posts, papers, videos, links, etc that I want to keep track of. None of these are related to data team leadership (see [this repo for those links](https://github.com/ronikobrosly/awesome-data-leadership))


Also, here are fantastic awesome lists, aggregations, etc: 
* https://github.com/kuchin/awesome-cto
* https://github.com/eugeneyan/applied-ml
* https://leaddev.com/

# Topics

- [Career](#career)
- [Data Engineering](#data-engineering)
- [Deep Learning](#deep-learning)
- [Experiments and Causality](#experiments-and-causality)
- [General Management](#general-management)
- [Job Search](#job-search)
- [MLOps](#mlops)
- [Organizations](#organizations)
- [Software Engineering and App Development](#software-engineering-and-app-development) 
- [Statistics](#statistics)
- [Tools](#tools)
- [Visualization and plotting code](#visualization-and-plotting-code)



## Career
Title | Summary | Year
---|---|---
[8 Hard Truths I learned when I got laid off from my SWE job](https://www.stevenbuccini.com/8-hard-truths-on-getting-laid-off) | A set of fantastic "hard truths" related to being laid off. Includes topics like: "Getting laid off is a profoundly lonely experience", "It’s gonna take longer than you think", "Interview invites are a poor proxy for your desirability", "Honesty can only hurt you", and more. | 2022
[My questions for prospective employers (Director/VP roles)](https://jacobian.org/2019/apr/23/questions-for-employers-director-vp/) | Covers questions that Director or VP-level candidates should ask of potential employers. These include, for example: What does success in the role look like? What’s my boss’s (or board’s) expectations for me? What’s the degree of managerial discretion in the role? | 2019
[When is short tenure a red flag](https://jacobian.org/2022/oct/14/when-is-short-tenure-a-red-flag/) | When is short tenure a red flag, how short is too short, how often can one change jobs, and under what conditions should you get a new job. This applies for less senior roles, and there is [another article just for staff-level, director or VP-level roles and this topic](https://jacobian.org/2022/oct/20/tenure-and-seniority/) | 2022


## Data Engineering
Title | Summary | Year
---|---|---
[An Engineer's Guide to Data Contracts - Part 1](https://mlops.community/an-engineers-guide-to-data-contracts-pt-1/) | Goes over a technical implementation of a data contract. Specifically, a CDC-based (Change Data Capture) implementation of Entity-based Data Contracts, covering contract definition, schema enforcement, and fulfillment. | 2022
[Supercharge your data processing with DuckDB: Efficient & blazing fast SQL analytics in Pandas with DuckDB](https://medium.com/learning-sql/supercharge-your-data-processing-with-duckdb-cea907196704) | Have been wondering for a while what the point of DuckDB is given the modern cloud stack, but I misunderstood the point of it. It's great for when there are large local files you need to query, when pandas will typically choke. Article gives plenty of example code on its use. | 2022
[The Beginner's Guide to Databases](https://technically.substack.com/p/the-beginners-guide-to-databases?utm_campaign=Data_Elixir&utm_source=Data_Elixir_430) | Covers the various types of DBs, and why you'd use each depending on the use case. | 2023

## Deep Learning
Title | Summary | Year
---|---|---
[Do Large Language Models learn world models or just surface statistics?](https://thegradient.pub/othello/) | Explores whether large language models (LLM) are able to learn deeper meaning of language or just surface statistics. Describes an interesting analogy to a chess game with a crow that watches. Through a series of probe experiments, the authors suggest these LMMs do in fact learn the deeper meaning of language AKA an inner world model. | 2023
[On the Opportunities and Risks of Foundation Models](https://arxiv.org/abs/2108.07258) | A major, large report by the Center for Research on Foundation Models (CRFM) at the Stanford Institute for Human-Centered Artificial Intelligence. Covers their current (as of 2021) capabilities, their potential, their social implications, and their drawbacks. | 2021
[Building LLM applications for production](https://huyenchip.com/2023/04/11/llm-engineering.html) | Chip Huyen's great overview of the tech challenges of productionizing LLMs | 2023

## Experiments and Causality
Title | Summary | Year
---|---|---
[A Simpler Alternative to X-Learner for Uplift Modeling](https://medium.com/@rndonnelly/a-simpler-alternative-to-x-learner-for-uplift-modeling-f3a11ebf6bf1) | In this post, Rob Donnelly describes an approach he calls simplified X-learner (Xs-learner) that is easier to understand, faster to implement, and in my experience often works as well or better in practice than other meta-learners (s-learner, x-learner, etc). S-learner can be problematic because it biases effects towards zero. He provides python code for this new approach. | 2023
[An introduction to g methods](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6074945/) | The use of "g methods" by epidemiologists has been hampered by limitations in understanding both conceptual and technical details. The authors present a simple worked example that illustrates basic concepts, while minimizing technical complications. Written by epidemiologists Ashley I Naimi, Stephen R Cole, and Edward H Kennedy. | 2017
[Getting to decisions faster in A/B tests – part 1: literature review](https://aurimas.eu/blog/2023/01/getting-to-decisions-faster-in-a-b-tests-part-1-literature-review/) | Discusses what teams do to 1) get to decisions faster (i.e. dealing with the "peeking problem") and 2) alternatives used that may be more intuitive than null-hypothesis testing (NHT). In future posts, the author will dive into the most interesting methods to fully understand what they promise and what they deliver. Author posits that methods to address early peeking may reduce ability to detect small changes (i.e. power), but says that this trade off depends on your context (If you are at a maturity stage where A/B testing is about tiny incremental changes, where you run 100s of experiments simultaneously in a self-service manner, then avoiding false positives may matter more than missing out on one of those changes that mattered, but you did not detect.) This post has so many **excellent links.** | 2023
[How Etsy Handles Peeking in A/B Testing](https://www.etsy.com/codeascraft/how-etsy-handles-peeking-in-a-b-testing) | Excellent write-up with links on Etsy's methods for dealing with the A/B testing peeking problem. Essentially they create a p-value threshold curve for any given experiment, and if they current p-value falls below that threshold you can stop the experiment early. | 2018
[confseq: A python package for confidence sequences and uniform boundaries](https://pypi.org/project/confseq/) | Documentation around "always-valid p-values". That is, no matter how many times you peak at the p-value, the results account for inflated false positives and the p-values are valid. | 2021
[How to Double A/B Testing Speed with CUPED: Microsoft’s variance reduction that’s becoming industry standard.](https://towardsdatascience.com/how-to-double-a-b-testing-speed-with-cuped-f80460825a90) | Very gentle introduction to CUPED approach to A/B testing. Basically, you leverage pre-experiment data to reduce the variance estimates of your test outcomes and thus you will need less sample size. | 2021
[Causal Inference for the Brave and True](https://matheusfacure.github.io/python-causality-handbook/landing-page.html) | An e-book that discusses the many techniques around causal inference | 2022

## General Management
Title | Summary | Year
---|---|---
[The Feedback Equation](https://larahogan.me/blog/feedback-equation/) | A framework to help one successfully structure specific and actionable feedback. The equation is: Observation of a behavior + Impact of the behavior + Question or Request = Actionable, specific feedback that has a chance of landing. | 2018


## Job Search
Title | Summary | Year
---|---|---



## MLOps
Title | Summary | Year
---|---|---


## Organizations
Title | Summary | Year
---|---|---
[IT Assets, Organizational Capabilities, and Firm Performance: How Resource Allocations and Organizational Differences Explain Performance Variation](https://pubsonline.informs.org/doi/10.1287/orsc.1070.0306) | Some organizations prioritize innovation and IT assets but this doesn't translate to business value. What explains this difference? | 2007


## Software Engineering and App Development
Title | Summary | Year
---|---|---
[The Twelve-Factor App](https://12factor.net/) | The twelve-factor methodology can be applied to apps written in any programming language, and which use any combination of backing services (database, queue, memory cache, etc). Factors include: Codebase, Dependencies, Config, Backing services, Build, release, run, Processes, Port binding, Concurrency, Disposability, Dev/prod parity, Logs, and Admin processes | 2017
[Evidence-based Software Engineering](http://knosof.co.uk/ESEUR/) | Entire book describing software engineering and ML principles with tons of analysis of public code. Lots of super interestng plots.  | 2020
[Real-world Engineering Challenges #8: Breaking up a Monolith](https://newsletter.pragmaticengineer.com/p/real-world-eng-8) | A deep dive into how Khan Academy took a 1 million-line Python monolith and split it into ~40 Go services in a more than 3 year-long project. Incredible story about how to structure and carry out a huge migration. | 2023
[Keep the monolith, but split the workloads](https://incident.io/blog/monolith) | Discusses pros and cons of monolith and microservices, and a nice pattern for running monolith better | 2023

## Statistics
Title | Summary | Year
---|---|---
[FOUNDED UPON AN ERROR](https://www.allendowney.com/blog/2021/05/07/founded-upon-an-error/) | Describes how the argument that Bayesian statistics didn't take off earlier in history due to computational limitations is bunk. It was due to statistical leaders at the time threw their weight behind frequentist stats | 2023

## Tools
Title | Summary | Year
---|---|---
[Manipulate big data with Arrow & DuckDB](https://www.christophenicault.com/post/large_dataframe_arrow_duckdb/) | Gives primer on DuckDB and Apache Arrow and how they can be used together to super quickly analyze big data using a personal machine. | 2022
[Setting up a new machine for data science](https://github.com/RamiKrispin/awesome-ds-setting) | A bunch of useful python, docker, git, and terminal settings for doing ML Engineering work | 2023


# Visualization and plotting code
Title | Summary | Year
---|---|---
[SciencePlots](https://github.com/garrettj403/SciencePlots) | A collection of Matplotlib styles for plotting | 2022
[Aquarel](https://github.com/lgienapp/aquarel) | A lightweight templating engine and wrapper around Matplotlibs' rcparams to make styling plots simple. | 2022
[Randy Chase custom config](https://twitter.com/DopplerChase/status/1625616089593028609?s=20) | A nice custom matplotlib config with code | 2023
[TUEplots](https://github.com/pnkraemer/tueplots) | A package for figure sizes, font sizes, fonts, and more configurations at minimal overhead. | 2023
[matplotx](https://github.com/nschloe/matplotx) | More styles and useful extensions for Matplotlib | 2022



## TODO


Customer growth modeling:
* https://medium.com/growthzilla/2-1-4-customer-growth-models-efc0a7f64e21
* https://www.artefact.com/blog/scoring-customer-propensity-using-machine-learning-models-on-google-analytics-data/
* https://funnel.io/blog/what-is-marketing-mix-modeling-mmm-explained


* LLM monitoring and Observability: https://www.influxdata.com/blog/llm-monitoring-observability-influxdb/
* Lean Data Automation, decomposing "scheduling layer", "infrastructure layer", and "asset lineage layer": https://www.run.house/blog/lean-data-automation-a-principal-components-approach
* Incredible guide to puthon package dependency: https://nielscautaerts.xyz/python-dependency-management-is-a-dumpster-fire.html?utm_campaign=Data_Elixir&utm_source=Data_Elixir_512
* Really good "The problem with reasoners": https://aidanmclaughlin.notion.site/reasoners-problem
* Taiming LLMs: a practical guide: https://www.tamingllms.com/markdown/toc.html?utm_source=substack&utm_medium=email
* Archetypes of LLM apps: https://www.contraption.co/archetypes-of-llm-apps/
* How AI-assisted coding will change software engineering: hard truths: https://newsletter.pragmaticengineer.com/p/how-ai-will-change-software-engineering?utm_medium=email
* cosine similarity has flaws: https://www.shaped.ai/blog/cosine-similarity-not-the-silver-bullet-we-thought-it-was
* Bob Wilson's Adventures in Why: https://www.adventuresinwhy.com/
* a 2024 survey of time series methods: https://arxiv.org/pdf/2412.20512

* https://yanirseroussi.com/2024/05/06/business-questions-to-ask-before-taking-a-startup-data-role/
* https://hamel.dev/blog/posts/evals/?utm_source=substack&utm_medium=email
* https://arxiv.org/pdf/2403.05440.pdf
* https://huggingface.co/blog/hrishioa/retrieval-augmented-generation-1-basics
* https://weaviate.io/blog/verba-open-source-rag-app
* https://jina.ai/news/what-is-colbert-and-late-interaction-and-why-they-matter-in-search/
* https://textmine.com/post/an-introduction-to-knowledge-graphs?utm_source=substack&utm_medium=email
* https://github.com/yoheinakajima/mindgraph?utm_source=substack&utm_medium=email
* Cool guide to using command line: https://github.com/jlevy/the-art-of-command-line
* https://cep.dev/posts/every-infrastructure-decision-i-endorse-or-regret-after-4-years-running-infrastructure-at-a-startup/
* https://eugeneyan.com/writing/unit-testing-ml/
* https://vadimkravcenko.com/shorts/proper-documentation/
* https://a16z.com/emerging-architectures-for-llm-applications/
* https://eugeneyan.com//writing/llm-patterns/?utm_campaign=Data_Elixir&utm_source=Data_Elixir_446#collect-user-feedback-to-build-our-data-flywheel
* https://eugeneyan.com/writing/llm-problems/
* https://pair.withgoogle.com/explorables/grokking/
* mitigating the winner's curse in experiments (Bayesian a/b testing): https://www.etsy.com/codeascraft/mitigating-the-winners-curse-in-online-experiments
* paper on best approach for structure learning: https://arxiv.org/pdf/2310.13387.pdf#page11
* best talks on A/B tests: https://docs.google.com/spreadsheets/d/1CLdCxXpmb2UhGOx-rCkj_8UsfSuNthasVuagseNVWrU/htmlview
* Optimizely's white paper on experiments: https://bdjknm.files.cmp.optimizely.com/download/9dbe7b14942111eea7b41a8a51acfb25?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOlsiOWRiZTdiMTQ5NDIxMTFlZWE3YjQxYThhNTFhY2ZiMjUiXSwiZXhwIjoxNzAxODY1NjcxfQ.8YswU6t6KqNtP96Rr_zFCykTlWgp_Fus9Tun_c5jq8o&_gl=1*c3rykk*_gcl_au*ODU5ODE0NDA1LjE3MDMzNDUyOTk.*_ga*MjA3MzUyMzQzOS4xNzAzMzQ1Mjk3*_ga_C7SLJ6HMJ5*MTcwMzM1MTMyOS4yLjAuMTcwMzM1MTMyOS42MC4wLjA.
* https://medium.com/the-prefect-blog/should-you-measure-the-value-of-a-data-team-95c447f28d4a
* https://dropbox.tech/machine-learning/accelerating-our-a-b-experiments-with-machine-learning-xr
* A Second Chance to Get Causal Inference Right: A Classification of Data Science Tasks
* Implementation of G-Computation on a Simulated Data Set: Demonstration of a Causal Inference Technique
* Targeted Maximum Likelihood Estimation for Causal Inference in Observational Studies
* Learning Neural Causal Models from Unknown Interventions
* LEARNING NEURAL CAUSAL MODELS WITH ACTIVE INTERVENTIONS
* Formalizing the Role of Agent-Based Modeling in Causal Inference and Epidemiology
* Using AntiPatterns to avoid MLOps Mistakes
* Scaling TensorFlow to 300 million predictions per second
* The North Star Playbook The guide to discovering your product’s North Star
* Metalearners for estimating heterogeneous treatment effects using machine learning S¨oren R. K¨unzela,1, Jasjeet S. Sekhona,b, Peter J. Bickela, and Bin Yua,c,1
* A Crash Course in Good and Bad Controls
* Word Embeddings via Causal Inference: Gender Bias Reducing and Semantic Information Preserving
* Can Foundation Models Talk Causality?
* Operationalizing Machine Learning: An Interview Study
* https://www.kevinmconroy.com/hello/ (find link to An Engineering Leader's Job Search Algorithm)
* https://careerhackers.com/how-to-discover-tech-companies-with-crunchbase-2/
* https://searchengineland.com/seo-guide-to-optimizing-your-linkedin-profile-for-more-connections-better-leads-315882
* Custom TTS training: https://github.com/CorentinJ/Real-Time-Voice-Cloning/issues/437
* Recorder for creating TTS dataset: https://github.com/babua/TTSDatasetRecorder
* https://arxiv-sanity-lite.com/
* https://scholar.google.com/
* https://github.com/rguo12/awesome-causality-algorithms (look at the commit diffs to see new additions)
* https://concept-drift.fastforwardlabs.com/
* https://research.fb.com/blog/
* https://eng.uber.com/
* https://eng.lyft.com/
* https://multithreaded.stitchfix.com/
* https://deepmind.com/blog
* https://www.microsoft.com/en-us/research/
* https://www.amazon.science/
* https://www.capitalone.com/tech/blog/
* https://netflixtechblog.com/
* https://news.ycombinator.com/
* https://locallyoptimistic.com
* https://distill.pub/
* https://thegradient.pub/
* https://www.causalscience.org/
* https://spectrum.ieee.org
* https://applyingml.com/
* https://thedataexchange.media/
* https://statmodeling.stat.columbia.edu/
* https://skamille.medium.com/
* https://erikbern.com/
* http://veekaybee.github.io/
* https://twitter.com/jovialjoy?lang=en
* https://huyenchip.com/blog/
* https://koaning.io/
* https://eugeneyan.com/
* https://mattturck.com/
* https://noahgift.com/
* https://www.randyau.com/
* https://twitter.com/ericcolson?lang=en
* https://lilianweng.github.io/lil-log/
* https://blog.pragmaticengineer.com/
* https://bytes.grubhub.com


