---
header-includes:
  - \usepackage[margin=1in, includehead]{geometry}
  - \usepackage{fancyhdr}
  - \pagestyle{fancy}
  - \fancyhf{}
  - \fancyhead[R]{-\,\thepage\,-}
---


\thispagestyle{empty}
\noindent\begin{minipage}{\textwidth}
\singlespacing
\raggedleft
Noam Martin Ross

September 2015

Ecology
\end{minipage}

\vspace*{\baselineskip}

\centerline{\textbf{
Disease with Multiple Infections: Population Structure, Dynamics, and Control
}}

\centerline{\textbf{\underline{Abstract}}}

Emerging fungal pathogens pose threats to plant, animal, ecosystem and human health [@Fisher2012]. Some of these pathogens, which include true fungi and fungus-like eukaryotes, share traits traits such as host generalism, reservoir hosts or environments, and high mortality rates in select hosts. One common set of traits amongst several emerging fungal diseases is load-dependent mortality in hosts, and the ability of fungal spores to colonize hosts repeatedly to increase loads [@Briggs2010; @Langwig2015].  This set of properties suggests that these diseases are best modeled using a macroparasite [@Anderson1978], or multi-infection, framework, which explicitly tracks disease burden within and across host organisms.

Macroparasites are generally thought of as persistent infections of populations, rather than transient epidemic phenomena [@Gulland1995]. Less attention has been paid to their transient dynamics, and the macroparasite framework is rarely used in cases of emerging epidemics.  It is also little used in plant pathology.  However, as some emerging fungal diseases can strongly suppress populations and even cause local extinctions [@Fisher2012; @Langwig2015], these dynamics are important in their study and management. In this dissertation, I explore several problems associated with using using the macroparasite framework to model the dynamics of emerging fungal disease and manage its outcomes.

In the early phases managing an emergent disease, a key problem is identifying an appropriate model to use in forecasting long-term behavior. In Chapter 1, I analyze differences in the dynamics of $SI$ and macroparasite disease processes, with the purpose of identifying signatures of macroparasite processes that can be identified from disease dynamics, and comparing the expected long-term behaviors of each. In general, macroparasite diseases generate larger epidemics and greater host mortality than $SI$ models with similar behavior at the early stages of disease.  Macroparasite diseases also generate age-mortality patterns, even in the absence of age structure in host vulnerability, which may be useful in identifying this type of disease.

Macroparasite models are inherently high-dimensional because of the need track variation in disease load amongst individuals. Thus, they are excellent candidates for individual-based modeling [@Grimm2005, IBM].  However, this high-dimensionality poses a challenge to optimal control techniques, which are useful in planning management responses to epidemics. In Chapter 2, I introduce a new numerical method for optimal control using individual-based models, which uses a form of numerical model-reduction known as "equation-free modeling" [Kevrekidis2009a, EF]. EF allows approximation of expected derivatives of stochastic IBMs, which in turn can be used to solve a Hamiltonian optimal control problem.  I show that the EF method can produce the equivalent results to an analytical approach, without the need for closed-form equations of disease dynamics.

Aggregation is a core concept in macroparasite epidemiology.  Parasites are commonly aggregated in nature, and the negative binomial distribution is commonly used to model these aggregated, or overdispersed, distributions. This overdispersion is a feature of stable macroparasite populations. In chapter 3, I explore the evolution of dispersion, showing how underdispersion can occur in transients of macroparasite models, even in the absence of density dependence, due to time-delay effects. I examine the utility of using the Conway-Maxwell-Poisson distribution [@Conway1962, CMP] to model these transient populations, and find it provides a better approximation to  distributions in the @Anderson1978 model than the negative binomial, whether parasites are under- or overdispersed.  I also introduce an r package, **cmp**, for fitting the CMP distribution to data.

\vspace*{\baselineskip}

