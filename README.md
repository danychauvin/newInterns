# Useful things to know, when starting in a new laboratory

Dany Chauvin, dany.chauvin@unibas.ch, Biozentrum, Basel

Last modification: 20210127

## Why this document?

Starting as an intern/PhD in a new laboratory is usually a very unefficient process. Being well, and doing well in a laboratory requires some "know-how" that needs to be learned. Such knowledge encompasses a lot of things from knowing how to contact IT services, to knowing where PBS is stored. Part of this knowledge is laboratory dependent, and part of this knowledge is invariant from one laboratory to the other.

This document, in constant evolution, is an attempt at gathering such information in a single document that you can refer to. The document is organized in two parts. The first part deals with what is invariant between laboratories. The second part deals with information that is specific to the van Nimwegen wet lab at Biozentrum Basel.

## Working your way in science: some general principles

This modest attempt at synthesizing what is important to know, to work in any laboratory, is in fact very subjective. Though I am not religious at all, I tried to come up with ten commandments.

1- **Communicate**

Science is about open questions, i.e questions whose answers are not known in advance. Open questions are the most difficult of all: not only you have to answer the question, you also need to verify that your answer is the best one there is... at the moment. So, science can be tough sometimes. Things never go as fast as you wished, experiments fail and/or nothing comes out of your analysis.

While being slowed down by problems is normal and forgiveable, not being proactive about is not. When you are stuck, tell others about it, read about it (not necessarily in that order) and propose new routes to solve your problem or go around it.

2- **Plan and then do, not the contrary**

Planning an experiment starts with asking yourself the following: "What is the question I want to answer?"

Once a good question has been set, you can start planning an experiment. It seems to be common sense, but it has to be stated because it is often overlooked. Before actually doing an experiment, it is important to think thoroughlly about it, from beginning to the end.

Once the protocol has been written, check that the outcome should in principle answer your question.

The protocol should then be printed, and annotated while doing the experiment.

As a very important point, I would like to stress out that it is mandatory to keep things organized: samples, protocol, data, code, results. There are many ways to do so. I am proposing a way to do that in a dedicated chapter.

4- **Reflect on what you are doing**

When doing an experiment, it is easy to let your mind wander. Actually, when performing repetitive tasks, your mind WILL wander.

And this is ok. But you should develop strategies not to forget to ask yourself: "what am I doing now? why am I doing it?". As much as possible, do not let yourself do things in an "automated mode". In principle, there always should be a reason for you to be doing something (be that at the bench or in front of your computer), and you should always be able to explain it. Adopting this attitude, you will be more efficient: it is amazing the amount of time you can waste doing things without thinking about it!

5- **Be honest with yourself and others**

We all do mistakes. This is completely alright. What is not alright is to try to hide it. In the best case your mistake is only impacting you. But in most cases, it will impact others as well (e.g something is broken in the lab).

Also, keep in mind that "mistakes" are a valuable source of information! A well tracked mistake can be worth something! A untracked/hidden mistake, is wasted time.

So document your mistakes as well!

5- **Capitalize experience (aka be gentle to your future self)**

There is motto that I like (even though I have a hard time applying to myself), which is: "Someone else should not have to teach/tell me the same thing twice".

So take notes. In the future you should be able to find back these notes if needed. The better you are at doing so, the more autonomous you will be.

6- **Read**

Good ideas are never coming out of the blue. Science is built at the border between what is known and what is not known... so you need to know what's known!

There are no miracles. You need to read/attend seminard to acquire this knowledge. So take the time to read. It is better to understand well 10 papers, than to approximately know 1000 of them.

Some ressources are usually better than others when starting in a new field: text books and reviews are usually the place to start! Ask around.

7- **Put things in context**

This is a very important point. Whether you are doing science or not, you will always have to explain what you are doing to others. Always ask yourself: "Who am I talking to? What is this person background?". If you do not know, ask! Too much context is always much better than not enough. And even if people are supposed to know what you are talking about, they might have forgotten. Reexplain if necessary.

8- **Write, write, write**

Whether you are doing science or not, you will be asked to write reports. The only way to learn how to do this is to write, write and write again. Do not miss the opportunities.

9- **Learn to present your results well**

A major part of science is about communicating what you are doing to others. There are some rules to the making of good presentations that I will detail in a next chapter.

10- **Did I forget anything?**

NERVER leave the lab without asking yourself this question. Is everything that should be turned off, actually turned off? Are all my samples back in the freezer?

10- **If you did not understand something, ask!**

This is probably going to happen a lot, and this is normal, no worries!

## Working you way in our lab

Welcome to the laboratory!
Here is what you should know about the lab in general.

### Computer stuff

#### Operating systems

All operating systems are allowed in the laboratory. But if I were you I would go for Ubuntu (PC) or OSX (Mac). There are UNIX systems, and we use the UNIX terminal a lot in the laboratory. But this is not only about us: UNIX shell is extremely powerful. Your computer is a machine that's meant to be "programmed" and used to "automate" tasks. It is not meant to be powered by the mouse movement like a windmill...

In the course of analysing your data, you will have to use shell commands and shell scripting. If needs be, you'll be taught the basics. You can also look for some tutorials online, there are many!

#### Programming languages

The main programming languages that are used in the laboratory are Python and R. R is mostly used for data analysis. You will be invited to use it to analyze your data. Regarding this, you can refer to the following book: [R for Data Science](https://r4ds.had.co.nz/)

#### Regular expressions

We use them a lot in the laboratory. You'll learn a bit about them. [Regular expressions (wikipedia)](https://en.wikipedia.org/wiki/Regular_expression)

### Recording/Monitoring lab work

Lab work is organized in projects (that can be porous)...

The core of lab work consists of:
  - Finding good questions. Output = scientific question
  - Planning experiments. Output = protocol
  - Making experiments. Output = data, samples
  - Analysing experimental results. Output = figures mainly
  - Reporting about scientific results. Output = reports, publications

Lab activity gives birth to many items of very different nature. These things need to be organized.  Here are my two cents about how I think it should be organized. As you will see, this revolves around experiments (be that in silico experiments or real experiments).

### Organisation proposal

Let's imagine we are in the project "Project".

When an experiment is to be performed, a new directory is created on the cluster:
Project>experiments>Project_date_description(oneWord)_index

**Example:**
constitexpr_exp_20200114_cloning_001

This folder should include the following:
- 20200114_protocol (markdown document)
- raw data generated by the experiment
- all necessary files to redo the experiment

If analysis is to be performed, another folder is created:
Project>analysis_and_reports>Project_analysis_date_description(oneWord)_index
Project>analysis_and_reports>Project_report_date_description(oneWord)_index

**Example:**
constit_analysis_20200116_cloningResuls_001
Such folder should contain the following folders
data: data necessary for the analysis (except raw data which are stored in experiments)
src: containing scripts to run the analysis/report
The report itself: constit_analysis_20200116_cloningResuls_001.pdf
Obviously the report should refer to the protocol and to the experiment folder.

**important: it is better generally to refer to full path when refering to raw data files in the analysis**

Presentations can be kept in:
Project>presentations

And finally I usually keep a "log file", to keep track of everything I am doing in a project. Every entry in this log file is preceded by the date.


### About your notes

Keep in mind that your notes should respect the following:

1- **Readable**

Your notes should be stored in a file format that's as simple as possible so as to be readable by anyone. I recommend using markdown documents [Markdown (wikipedia)](https://en.wikipedia.org/wiki/Markdown) (text file where markdown syntax is being used).

A routine to back-up these notes must also be implemented. Repositories, or university cluster can be used to do so.

2- **Understandable**

What is written in your notes should be understandable by anybody (and most importantly, the "future you"). Write plain sentences. 

3- **Self-Supporting**

A document is never written out of the blue. It is issued in a context. Are they notes written during a course? Then, the name, the date of the course should be written.

Is this an experimental report? Then it should be linked to a protocol.

4- **Exhaustive**

If you describe experiments, you and others should be able to reproduce them. Do not omit critical details.

## Lab organization

### Group meetings

Currently, group meeting take place every Thursday from 3 to 5 pm.

## Mini-group meetings

Besides group meeting, we also meet for mini-group meeting, where people leading projects are expected to briefly present what they are currently doing.

## Projects you will work on

Here is a list of projects I am currently working on in the laboratory. In the course of your internship, you'll be working with me on these projects too (not necessarily on all of them).
For each of these projects, I wrote a short context with some references, as well as some ideas for experiments we could do together first, and then that you will do by yourself.

### evanticip

This is the original project we discussed about already. I am simply copying pasting the email I sent to you after we met last time.

#### Context of the project

> As discussed today, the aim of your project will be to investigate the variability of responses to environmental switches, and how this drives the fitness of bacterial populations, in different natural strains ofE.coli.

> In a nutshell, we will grow natural isolates of E. coli in different media, until they reach a stationary phase (i.e until bacteria have consumed all nutrients and are no longer dividing). Then, we'll filter these cultures to keep only the cells, which will be rinsed, and we'll resuspend them in fresh media of different compositions. The output of these experiments will be time traces of culture absorbance, before and after the switch. These data will be analyzed using R to compute "lag times", i.e the time it takes for the cell to resume growth.  We hope to see variability in the way cells resume growth after the switch. A possible extension of this work would be to adapt these experiments to single cell microfluidic experiments so as to establish the relationship between macroscopic and single-cell behaviours during these switches.

> Here are some papers related to this:
> - Markus Basan's paper illustrating a potential trade-off between lags
and growth rate. Also interesting from the experimental point of view as
we plan on using a similar method to switch the cells between media.
> - Mathias and Thomas' paper on microfludic mother machine experiments
where single cells are switched from glucose to lactose.
> - Chris Field's draft on the experimental work he did, growing these
natural isolates in many conditions.
> - Thomas' paper on the analysis of the genomes of these natural isolates.
> Let me know if you have any questions or things you would like to discuss!

#### Experiments

A previous post doc worked quite extensively with these natural isolates. Except that he grew them on solid substrate. Here we are interested in liquid cultures.

I did myself some experiments on this project last year. There are two differences with what is described above: 1) I was switching the cultures from one media to another when the cells where still in exponential phase, 2) I was diluting the cells from one media to another, instead of filtering them.

1) Makes reproducing experiments a bit difficult, cause cells are growing quite fast. Switching them from one medium to another at exactly the same point in growth is hard. Also, cells are growing at different rates, in different media and so have to be switched at different moment... Which makes parralelizing conditions a bit tricky from an experimental point of view.

2) When you dilute cells from one media to another, you not only dilute the cells, but also some media. After the switch, the cells are therefore growing in a mix of media, rather than in a single medium. I could witness that the presence of minute amount of medium 1 in medium 2, was causing the cells to behave differently, compared to medium 2 alone. Hence the idea of filtering instead of diluting!

### constitexpr

This is the main project I am currently working on, and that I am trying to finish. I might need your help on some urgent experiments.

#### Context

E. coli, when growing exponentially, need to maintain protein concentration. But, protein concentration fluctuates, in time in a given cell and also, accross cells. These fluctuations can be so important, that they sometimes lead a fraction of the population to display different phenotype from the rest of the population. This is thought to be beneficial in some fluctuating environments, because this fraction of the population might already be pre-adapted to a future environment.

This shows that it is important to understand what is constraining these fluctuations, to understand how bacterial population adapt to changing environments.

That's what I am trying to do in this project. I am trying to understand in a very simple case, the case of one single GFP gene within the chromosome, how GFP concentration fluctuates. Here this GFP expression is under the control of a single promoter (see below about that). I am trying to understand how and how that generally depends on the **two processes** which are controlling protein concentration.

These two processes are:

- **Expression**: which defines at which speed proteins accumulate in the cytoplasm. This depends on the **promoter activity**. Which can be regulated or not, depending on the growth condition. The variable at stake here is **GFP volumic production**, $q(t)$: how many proteins are produced, during $\deltat$, by a unit of cell volume.

- **Dilution**: when cells grow in size, proteins are diluted. Dilution sets the speed at which proteins are going to be diluted in the cytoplasm. The assumption here is that cells are growing exponentially (which is well supported by our data by the way). The variable here is the **exponential growth rate**, $\lambda(t)$.

In a nutshell, in this project I run mother machine experiments, in different media, with E. coli strains which have a promoter + GFP construct in their chromosome. These strains are all the same, except for their specific promoter that controls GFP expression. And I am trying to measure $q$, $\lambda$ as well as $c_{GFP}$. 

Then I try to understand of $q$ and $\lambda$ fluctuations are setting $c_{GFP}$ fluctuations.

I currently work with 8 promoters. 4 artifical promoters (random sequences, that are showing different level of activity), and 4 ribosomal promoters (they are natural sequences, which control the expression of ribosomal proteins in E. coli).

It turns out that, in my experiments, these promoters all show different behaviours: some have their GFP concentrations that increases, some others have their GFP concentration that go down with the growth rate. And this seems to be controlled by production (by the mean value of $q$).

We currently do not understand why they behave differently, and we are trying to understand how a promoter would behave "by default". One way to do this, is to measure the GFP concentration in cells growing at different growth rate, for many artifical promoters!

Turns out, we have these strains already available in the laboratory.

#### Experiments

Take the E. coli glycerol stocks for these artificial promoters. Grow the cells in different environments, measuring OD and fluorescence while the cells are growing and characterize their concentration as growth rate changes.

How is concentration changing in these different strains?

### monodcurves

In any environment, there is a growth limiting compound. In minimal media + glucose (as long as the concentration of glucose is low), glucose is limiting. Meaning that, if you increase the concentration of glucose, cells will grow faster. More generally, how is growth rate changing with the concentration of such limiting nutrient?

It is thought in general, that bacterial growth rate follow a "Monod curve"[Wikipedia page about the "Monod Curve" and bacterial growth](https://en.wikipedia.org/wiki/Monod_equation).

But, this has been characterized for very few limiting nutrient (such as glucose) and for a limited amount of E. coli strains (E. coli K12), and at the population level.

What's happening at the single cell level then?

#### Experiments

The idea is to perform multiplexed mother machine experiments, in presence of different media, which are composed of different concentrations of growth limiting nutrients.


























