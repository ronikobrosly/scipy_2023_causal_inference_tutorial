# SciPy 2023 Tutorial Submission: Introduction to Causal Inference (intermediate skill level)

Author:

Roni Kobrosly, PhD 

* https://www.kobrosly.net
* https://www.linkedin.com/in/ronikobrosly/
* https://github.com/ronikobrosly


## Brief Note to SciPy Committee

Thank you for considering this tutorial for SciPy 2023! I presented this last year at SciPy 2022, and judging from the feedback I believe the audience enjoyed it and learned from it. Some notes and feedback I got from the audience [is available here](https://github.com/ronikobrosly/causal_inference_intro/blob/main/admin/scipy2022/post_session_feedback.md). 

Since July 2022, I've been fine-tuning the tutorial and examples based on feedback, and I believe the more complex and abstract causality parts of the tutorial are much more clear. I've also done away with running notebooks locally, and now the attendees can run everything in Google Colab. There weren't many environment / setup issues last year, but with the current proposed materials there shouldn't be any issues at all (unless an attendee cannot connect to the internet).  

If accepted, between now and the conference I would likely make slight tweaks to the flow of the presentation along with any suggestions you may provide.


## Presenter Bio

I am a former epidemiology researcher who has spent approximately a decade employing causal modeling and inference. The bulk of my academic career was spent conducting data analyses to estimate the population-level effects of harmful environment exposures, when traditional randomized experiments were infeasible or unethical. During this time, I taught a couple undergraduate epidemiology courses, once of which involved a sizable introduction to causal thinking. I've also presented many one-off departmental presentations and at a few epidemiology conferences on causal inference in both cases.

Since leaving the academic world, I've been loving my second life in the tech industry as a data scientist, ML engineer, and more recently as the Head of Data Science at a medium-sized health tech company based in Washington DC. I love mentoring junior data folks and explaining the magic of data analysis and modeling to non-technical audience.

I also am a member of the open-source community, being the author and maintainer of the `causal-curve` python package. This package provides a set of tools for estimating the causal impact of continuous/non-binary treatments (e.g. estimating the causal impact of a neighborhood's income inequality on local crime, or understanding the causal effect of increasing a product's price on conversion rates).


## Short Description

This tutorial session is intended to give attendees a gentle introduction to applying causal thinking and causal inference to data using python. Causal data analysis is very common in many academic domains (e.g. in social psychology, epidemiology, macroeconomics, public policy research, sociology, and more) as well as in industry (all of the largest Silicon Valley tech companies employ teams of scientists who answer business questions purely with causal inference methods).

The tutorial will involve a combination of presentations with open Q&A and hands-on exercises contained in Google Colab notebooks. This session will cover the difference between correlation and causation, the pitfalls of conducting an analysis using observational data, how causal inference can help get around these pitfalls, and examples of common, modern modeling approaches used to conduct causal inference (propensity score matching, estimating causal curves, g-computation, and double ML). After the tutorial, the attendees should have a good foundational understanding of causality and the ability to confidently explore the topic on their own. Causal inference can be a very theory-heavy topic, making it impenetrable to novices. In this tutorial, we'll aim to take a more practical perspective on causal inference, while still occasionally touching on the theory.

Tutorial participants are not expected to be familiar with causal inference before attending, but we hope they have an earnest curiosity to learn about it! To get the most out of the session, the participants ought to have experience working with the common python data stack: matplotlib, numpy, pandas, and scikit-learn. Attendees should have some experience conducting classic machine learning modeling using the scikit-learn API, although having advanced machine learning expertise is absolutely not a prerequisite. A very basic understanding of statistics would be helpful (e.g. understanding what a mean is, what confidence intervals represent).


## Long Description with Outline


* Course Introduction (5 minutes)
    * Presentation:
        * Introduce myself and course format
        * Poll: Poll learners’ comfort level with topic so I can fine-tune pacing and descriptions to match.
        * Outline goals of training session

* Introducing causal thinking and causal graphs (50 min)
    * Presentation: 
        * Define counterfactuals, causal inference, causal inference use cases, causal graphs
        * The 3 primary types of causal relationships (confounding, colliders, mediators), and selection bias.
    * Large group exercise: Draw out car insurance causal graph. Attendees will provide answers through the group chat.
    * Q&A
    * Exercises: Exploring causal graphs and relationships

* Break (10 min)

* Assumptions of causal inference (30 min)
    * Presentation: 
        * How to get data from causal inference work (A/B tests, pure observational data)
        * Introduce a few simple suggestions for a causal inference workflow 
        * Core assumptions of causal inference
        * Understanding causal inference metrics
    * Large group exercise: Review sloppy examples of causal inference analyses for which causal assumptions each is violating. Learners will use group chat to share answers
    * Q&A

* Basic causal inference modeling with a binary treatment (30 min total)
    * Presentation: 
        * Introduce g-computation/s-learning, 
        * A brief explanation of the algorithm, 
        * Step-by-step with a simple table in the deck. 
        * Describe at a high-level what propensity score matching/weighting accomplishes and how it compares with g-computation.
    * Q&A
    * Exercises: g-computation method

* Break (5 min total)

* Causal inference modeling with a continuous treatment (30 min total)
    * Presentation: 
        * Explaining the problem of handling continuous treatments
        * How standard, bivariate plots of treatment and effect can fail us
        * How to conceptualize counterfactuals in the context of continuous treatments
        * How to interpret the causal curve in words
    * Q&A
    * Exercises: Handling continuous treatments by estimating causal curves
        * This notebook will be used as a starting point, but the population health example will be swapped out and replaced with something more general like product price or wait time in milliseconds for some service)

* Closing remarks (25 min total)
    * Presentation: 
        * How to troubleshoot common issues in causal inference analyses. 
        * Returning to the basic causal inference assumptions we discussed before, with a final warning about them. 
        * Providing links to other causal ML packages worth exploring (e.g. DoWhy, causalML, etc.)
    * General Q&A and Wrap Up

__Total time required: 230 minutes__


## Materials and Setup Instructions

The only technical requirements for this tutorial are having a local machine with an internet connection, a common web browser (e.g. Firefox, Safari, Chrome, etc.), and Google account (for accessing Colab and Google Slides).

All exercise notebooks (both "student" and "teacher" versions) are available on Google Colab. Notebooks have been thoroughly tested and can run end-to-end in the provided environments. See links below.

The notebooks uses datasets which are publicly available in [this GitHub repo](https://github.com/ronikobrosly/misc_dataset). Don't worry, though, the Colab notebooks directly link to them and you don't have to do anything beyond run the Colab notebook code as is. In case you want to play with the datasets locally (beyond the tutorial notebooks), they are conveniently included in this tutorial repo in the `data` folder.   