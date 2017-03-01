[Back to Conversation AI Research Overview](index.md)

### Research resources

This page outlines the high level questions we are exploring. Further related research can be found on the [WikiDetox outline of related work](https://meta.wikimedia.org/wiki/Research:Detox/Resources).

#### How might machine learning methods help online conversations?

How can machine learning enable us understand harassment at scale?

 * Our initial research is summerized in our blog post [Algorithms And Insults: Scaling Up Our Understanding Of Harassment On Wikipedia](https://medium.com/jigsaw/algorithms-and-insults-scaling-up-our-understanding-of-harassment-on-wikipedia-6cc417b9f7ff).
 * More details can be found in our paper [Ex Machina: Personal Attacks Seen at Scale](https://arxiv.org/abs/1610.08914) which outlines how crowdsourcing and machine learning can be used to analyze personal attacks at scale, and applies the methods to help understand the challenge on Wikipedia.
 * Public datasets
   * [Wikipedia Human Annotations of Personal Attacks on Talk Pages](https://figshare.com/articles/Wikipedia_Detox_Data/4054689): 100k Comments from wikipedia each with 10 annotations by the 4000 annotators who contributed to the effort. Each comment annotation notes whether the annotator considers the comment to be a personal attack or not.
   * [Wikipedia Machine Annotations of Talk Pages](https://figshare.com/articles/Wikipedia_Talk_Corpus/4264973): machine-labelled annotations for every English Wikipedia talk page comment from 2001 to 2015, approximately 95 million comments to support large scale data analysis.
   * To submit a link to an existing public dataset, or get help creating new public data sets for related research please fill out [this form](https://goo.gl/forms/z3JatRhT5x53Xa0I2).
   * [Wikipedia Human Annotations of Toxicity on Talk Pages](https://figshare.com/articles/Wikipedia_Talk_Labels_Toxicity/4563973): 160k human labelled annotations based on asking 5000 crowd-workers to rate Wikipedia comments according to thier toxicity (likely to make others leave the conversation). Each comment was rated by 10 crowd-workers.

What role does toxic language have in reducing the number of viewpoints in a discussion?

What tools are needed to make robust open debate on important issues easier at scale?

How might machine learning based tool be used by communities, commenters and authors?

#### What aspects of a conversation can machine learning understand?

Can machine learning methods understand the emotional impact of language?

How much of the structure of a conversation can machine learning approaches uncover?

#### What are the risks and challenges of using machine learning to assist online conversations?

What unintended and unfair biases might machine learning models contain? What impact might such biases have? What are the best ways to identify these biases? and what can be done mitigate them?

 * See [Attacking discrimination with smarter machine learning](https://research.google.com/bigpicture/attacking-discrimination-in-ml/) for a great introduction to the problem. Challenges related machine learning fairness and algorithmic bias are outlined further on our [WikiDetox Fairness page](https://meta.wikimedia.org/wiki/Research:Detox:Fairness).

How might machine learning based tool be gamed?

 * Word based models, including the CNN we developed for toxicty can be tricked easily by misspellings. Using character level models helps address this, but requires more data and for RNNs especially suffers from [the vanishing gardient problem](https://en.wikipedia.org/wiki/Vanishing_gradient_problem).

 * Models based on character-level ngrams fed into feed-forward networks can be gamed by adding additional ngrams after the initial comment that counter the signal from the problematic ngrams. This can be addressed by using RNNs (e.g. LSTMs) and CNNs provide a way to take account of more of the textual context.

How might ML be misused to censor or reduce viewpoints in a conversation?
