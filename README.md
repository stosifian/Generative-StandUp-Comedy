# Project 1 Generative Text

Shawheen Tosifian, stosifia@ucsd.edu


## Abstract/Description

The goal of this project is to create a character-based RNN that generates text/material (hopefully) in the vein of a stand up routine/special (specials traditionally being longer performances).

This topic was chosen primarily based off the idea that humor and comedy are for the most part seen as very human forms of expression. Humor (at least in the context of stand up comedy) often requires a large awareness of social context, basic understanding of human psychology, and reception to feedback (especially in an open mic context), amongst many other (what we see as) humanistic traits, such as creativity. Therefore, a hypothesis is that humor and comedy would be one of the last frontiers of human expression that a learning algorithm/'AI' would be able to replicate well, especially when it's only in a text-based language setting. As a result, my personal opinion is that the output won't be of any significance, especially with such a naive architecture (and inexperienced architect). However, it should be a fun(ny) exercise!

Of course, there are numerous restriction on this data - one big one being that this a textual translation of stand up comedy, which often relies as much on delivery as it does on material - and delivery is  hard to transcribe. So that dimension will be entirely missing.

First, 3 character-based RNN models were each individually trained on transcripts from stand up routines performed by a respective comedian in the hopes that each network could learn the 'style' of humor/stand up comedy of its respective comedian 'source data'. The three comedians  chosen for this task were Bill Burr, Richard Pryor, and Anthony Jeselnik.

To subjectively test whether the model represented its respective comedian's 'style' (i.e. verbalisms, content matter), the generative script would randomly select one of the 3 models and generate some text from it for you to try to guess the source comedian its emulating. 

(I found it rather trivial to figure out the source comedian, despite the output being incoherent - this assuming you're familiar with the comedians).

Lastly, a model was trained on the amalgamated data (transcripts from the previously mentioned comedians combined with ones from Dave Chappelle, Mitch Hedberg, and Nikki Glaser) and was used to generate 'unique' material that would ideally draw upon different elements of its source material. This model's output was slightly more coherent than the previous ones (most likely due to it being trained on more data) and you could still ascertain in certain parts of the output what source it's attempting to replicate.


Overall, the results were mostly in line with expectations. I didn't expect coherent generation nor genuinely humorous takes (though the last model had interesting ramblings where it seemed that each sentence would come from a different comedian and the train of 'thought' was humorous in an absurd context). However, the individual models were able to somewhat replicate the comedian 'style' and were distinguishable from each other.








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

- Sample outputs from each model (Bill Burr, Richard Pryor, Anthony Jeselnik, and combination) found in SampleOutput.pdf 

## Technical Notes

Make sure when running generation code, to use GPU cluster on datahub. Output will be garbage otherwise. Training was done using the GPU but not sure why if run on CPU it comes out trash






