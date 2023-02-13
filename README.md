# misc-data-science-articles
A collection of DS blog posts, papers, videos, links, etc that I want to keep track of. None of these are related to data team leadership (see [this repo for those links](https://github.com/ronikobrosly/awesome-data-leadership))

# Topics

- [Career](#career)
- [Data Engineering](#data-engineering)
- [Deep Learning](#deep-learning)
- [Experiments and Causality](#experiments-and-causality)
- [Job Search](#job-search)
- [MLOps](#mlops)
- [Organizations](#organizations)
- [Software Engineering and App Development](#software-engineering-and-app-development) 


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


## Deep Learning
Title | Summary | Year
---|---|---
[Do Large Language Models learn world models or just surface statistics?](https://thegradient.pub/othello/) | Explores whether large language models (LLM) are able to learn deeper meaning of language or just surface statistics. Describes an interesting analogy to a chess game with a crow that watches. Through a series of probe experiments, the authors suggest these LMMs do in fact learn the deeper meaning of language AKA an inner world model. | 2023
[On the Opportunities and Risks of Foundation Models](https://arxiv.org/abs/2108.07258) | A major, large report by the Center for Research on Foundation Models (CRFM) at the Stanford Institute for Human-Centered Artificial Intelligence. Covers their current (as of 2021) capabilities, their potential, their social implications, and their drawbacks. | 2021


## Experiments and Causality
Title | Summary | Year
---|---|---
[A Simpler Alternative to X-Learner for Uplift Modeling](https://medium.com/@rndonnelly/a-simpler-alternative-to-x-learner-for-uplift-modeling-f3a11ebf6bf1) | In this post, Rob Donnelly describes an approach he calls simplified X-learner (Xs-learner) that is easier to understand, faster to implement, and in my experience often works as well or better in practice than other meta-learners (s-learner, x-learner, etc). S-learner can be problematic because it biases effects towards zero. He provides python code for this new approach. | 2023
[An introduction to g methods](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6074945/) | The use of "g methods" by epidemiologists has been hampered by limitations in understanding both conceptual and technical details. The authors present a simple worked example that illustrates basic concepts, while minimizing technical complications. Written by epidemiologists Ashley I Naimi, Stephen R Cole, and Edward H Kennedy. | 2017
[Getting to decisions faster in A/B tests – part 1: literature review](https://aurimas.eu/blog/2023/01/getting-to-decisions-faster-in-a-b-tests-part-1-literature-review/) | Discusses what teams do to 1) get to decisions faster (i.e. dealing with the "peeking problem") and 2) alternatives used that may be more intuitive than null-hypothesis testing (NHT). In future posts, the author will dive into the most interesting methods to fully understand what they promise and what they deliver. | 2023


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








## TODO


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


