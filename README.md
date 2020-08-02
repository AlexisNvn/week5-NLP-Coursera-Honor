# week5-NLP-Coursera-Honor <br/>
Chatbot implementation using bucketing and sampled softmax.  <br/>
*Honor project - NLP course week5 - Coursera - HSE*

**Main code is from Stanford's assignment - 2017** <br/>
Files have been modified and updated with newer library versions <br/>

**Main points of the model :** <br/>
● Bucketing :  *Avoid too much padding that leads to extraneous computation, group sequences of similar lengths into the same buckets & create a separate subgraph for each bucket.*<br/>
● Sampled Softmax : *Avoid the growing complexity of computing the normalization
constant & approximate the negative term of the gradient, by importance
sampling with a small number of samples.*

**Dataset used : Cornell Movie-Dialogs Corpus** <br/>
● *220,579 conversational exchanges between* <br/>
● *10,292 pairs of movie characters* <br/>
● *9,035 characters from 617 movies* <br/>
● *304,713 total utterances* <br/> 
● *Very well-formatted (almost perfect)* <br/>

**Model weaknesses :** <br/>
● Blank answers to "small sizes" questions like "hey" - Might be a consequence of bucketing. <br/>
● Sometimes answers are a bit weird - Might need to train longer than I did (50000 iter - 5h)

**Global conclusion :** <br/>
It works not so bad ! Most of answers are not out of context !


*Examples :*  <br/>
> Hi  <br/>

> How are you ?  <br/>
i ' m a professional .  <br/>
> What's your name ?  <br/>
simpson .  <br/>
> Tell me about yourself  <br/>
i ' m sorry i ' m sorry .  <br/>
> Do you love me ?  <br/>
of course i do .  <br/>
> What's the meaning of life ?  <br/>
i don ' t know .  <br/>
> How is the weather today ?  <br/>
okay .  <br/>
> Let's have a dinner  <br/>
i ' m here ?  <br/>
> Are you a bot?  <br/>
no .  <br/>
> Why not?  <br/>
because i am the wrong thing .  <br/>
