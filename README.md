# Project 1 Generative Text

Shawheen Tosifian, stosifia@ucsd.edu


## Abstract/Description

The goal of this project is to create a character-based RNN that generates text/material (hopefully) in the vein of a stand up routine/special (specials traditionally being longer performances).

The initial plan is to train individual networks on transcripts from stand up routines performed by various comedians in the hopes that each network can learn the 'style' of humor/stand up comedy of its respective comedian 'source data'. Afterwards, an exercise can be carried out by generating data from a randomly chosen network and trying to determine (as a human audience) what comedian the network is 'trying' to emulate (i.e. what it was trained on).

Moreover, a network will then be trained on the amalgamated data (transcripts from all the comedians) and will be used to generate 'unique' material that would ideally draw upon different elements of its source material

This topic was chosen primarily based off the idea that humor and comedy are for the most part seen as very human forms of expression. Humor (at least in the context of stand up comedy) often requires a large awareness of social context, basic understanding of human psychology, and reception to feedback (especially in an open mic context), amongst many other (what we see as) humanistic traits, such as creativity. Therefore, a hypothesis is that humor and comedy would be one of the last frontiers of human expression that a learning algorithm/'AI' would be able to replicate well, especially when it's only in a text-based language setting. As a result, my personal opinion is that the output won't be of any significance, especially with such a naive architecture (and inexperienced architect). However, it should be a fun(ny) exercise!

Of course, there are numerous restriction on this data - one big one being that this a textual translation of stand up comedy, which often relies as much on delivery as it does on material - and delivery is very hard to transcribe. So that dimension will be entirely missing.

There has been a few experiments before with regards to 'generative comedy'. One of note is Botnik, a bot that uses a predictive keyboard 'to offer word choices to human writers'. Though not necessarily a generative network, it appears pretty good at what it does. You can read more about Botnik here: https://botnik.org


	

(Include your abstract here. This should be one paragraph clearly describing your concept, method, and results. This should tell us what architecture/approach you used. Also describe your creative goals, and whether you were successful in achieving them. Also could describe future directions.)

## Model/Data

Briefly describe the files that are included with your repository:
- training_code.ipynb : notebook used to train the models (and create checkpoints to be loaded by generative_code
- generative_code.ipynb: notebook used to load checkpoints and generate text from each model (as well a random model which chooses from a random model and you guess the source (i.e. comedian style)
- ComedyText : directory containing the source text .txt files used to train the model (obtained the good ol' fashioned way (C+V) from transcripts on scrapsfromtheloft.com)
- ._training : directories containing the last, updated checkpoint for respective model
- SampleOutput.pdf : collected output from each model (labeled) in .pdf format


## Code

Your code for generating your project:
- training_code.py - training code
- generative_code.py - generation code

## Results

- Documentation of your generative text in an effective form. A file with your generated text (.pdf, .doc, .txt). 

## Technical Notes

Any implementation details or notes we need to repeat your work. 
- Does this code require other pip packages, software, etc?
- Does it run on some other (non-datahub) platform? (CoLab, etc.)

## Reference

References to any papers, techniques, repositories you used:
- Papers
  - [This is a paper](this_is_the_link.pdf)
- Repositories
- Blog posts





