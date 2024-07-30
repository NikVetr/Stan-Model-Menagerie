# Stan-Model-Menagerie

A storage destination for model implementations in Stan, accompanied by generative R code, detailed descriptions, visualizations, and performance metrics.

# What is this?

The Stan Model Menagerie is a repository for storing varied statistical models implemented in the [Stan](https://mc-stan.org/) language. Oftentimes, I can either sketch out an idea for a model, but handling some of the internal implementation details is time-consuming, or I'm vaguely familiar with how something is meant to work, but struggle to understand how it all comes together or how the properties of the whole are influenced by the properties of the parts. In both cases, I'll often try to adapt a pre-existing implementation of whatever it is I'm trying to do, drawing upon either my own previous work, or searching the [Stan Forums](https://discourse.mc-stan.org/) for working code and examples that I can extend or modify as needed.

The former isn't very organized, and the latter does not always provide me with a viable springboard. As such, I wanted to create a set of folders corresponding to different classes and subclasses of statistical model, coupling together Stan implementations with easy-to-modify generative R code and information on model performance, both technical (eg, how quickly and reliably can the model be fitted in Stan) and statistical (how well does the fitted model recover simulation parameters under empirically realistic conditions).

There exist many high quality vignettes online that walk readers through each step of the [Bayesian Workflow](https://arxiv.org/abs/2011.01808) for specific, scientifically motivated applications. This is not that, but neither is it a collection of naked, undocumented `*.stan` files. It's meant to fall somewhere in the middle, collecting and cataloguing both at-home bred and wild-caught models to stick in interactive cages for our education and entertainment. And like a zoo, each exhibit is not typically accompanied by an encyclopedic monograph on its subject, but rather a short infographic giving some key insights into the nature of the beast contained. That's the level of documentation I'm shooting for, here.

# Structure

It's hard to coherently categorize the space of statistical models, but this repository needs to have some structure, so I've tried to organize it into folders and subfolders grouped on common themes. Our primary unit of operation is a folder whose name is descriptive of the model's distinguishing features, which in turn contains:

- **\*.stan files**: giving the implementation of the model in Stan
- **\*.R files**: giving R code to generate input for the model, as well as actually fitting the model through [cmdstanr](https://mc-stan.org/cmdstanr/)
- **/data/**: storing data files that are used as input for the model
- **README.md**: giving a general overview of the model, as well as its motivations, meanings, and performance
- **/images/**: storing image files that are used in the README
- **/tables/**: storing tables files that are used in the README

# Contributions