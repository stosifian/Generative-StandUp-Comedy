# Generative Text

Shawheen Tosifian, stosifia@ucsd.edu


## Abstract/Description

The goal of this project (done as an assignment for ECE 188 at UCSD) is to create a character-based RNN that generates text/material (hopefully) in the vein of a stand up routine/special (specials traditionally being longer performances) and able to emulate the 'style' of the comedians the individual models were trained on.

This topic was chosen primarily based off the idea that humor and comedy are for the most part seen as very human forms of expression. Humor (at least in the context of stand up comedy) often requires a large awareness of social context, basic understanding of human psychology, and reception to feedback (especially in an open mic context), amongst many other (what we see as) humanistic traits, such as creativity. Therefore, a hypothesis is that humor and comedy would be one of the last frontiers of human expression that a learning algorithm/'AI' would be able to replicate well. As a result, there is little expectation that the outputs would be any significance, especially with such a naive architecture (and inexperienced architect). However, it should be a fun(ny) exercise!

Of course, there are numerous restriction on this data - one big one being that this a textual translation of stand up comedy, which often relies as much on delivery as it does on material - and delivery is  hard to transcribe. So that dimension will be entirely missing.

### Approach
First, 3 character-based RNN models (1024 RNN units, 256 dimension embedding) were each individually trained on stand up transcripts from 3 comedians in the hopes that each network could learn the 'style' of humor/stand up comedy of its respective comedian 'source data'. The three comedians  chosen for this task were Bill Burr, Richard Pryor, and Anthony Jeselnik.

To subjectively test whether the model represented its respective comedian's 'style' (i.e. verbalisms, content matter), the generative script would randomly select one of the 3 models and generate some text from it for you to try to guess the source comedian it's emulating. 

Lastly, a model was trained on the amalgamated data (transcripts from the previously mentioned comedians combined with ones from Dave Chappelle, Mitch Hedberg, and Nikki Glaser) and was used to generate 'unique' material that would ideally draw upon different elements of its source material.

For the text generation, lower temperatures were used (<.5) to maintain some coherence in the output as beyond .75, output was largely nonsense words.

### Conclusion
Overall, the results were mostly in line with expectations. The individual models were able to somewhat replicate the comedian 'style' and were distinguishable from each other. If you're familiar enough with the comedians, it's trivial after a few tries to figure out the source. I didn't expect coherent generation nor genuinely humorous takes however the last (combined) model's output was more coherent that the individual ones. It had interesting ramblings where it seemed that each sentence would come from a different comedian and the train of 'thought' was humorous in an absurd sense (as if it was a 6-faced comedian, alternating personas every sentence or two).

For future works, ideally more data would be used for training and a shift to a word-based model would be made.

For reference, there has been a few experiments before with regards to 'generative comedy'. One of note is Botnik, a bot that uses a predictive keyboard 'to offer word choices to human writers'. Though not necessarily a generative network, it appears pretty good at what it does. You can read more about Botnik here: https://botnik.org


	

## Model/Data

Briefly describe the files that are included with your repository:
- training_code.ipynb : notebook used to train the models (and create checkpoints to be loaded by generative_code)
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






