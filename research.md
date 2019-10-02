[Back to Conversation AI Research Overview](index.md)

# Research resources

This page outlines the high level questions we are exploring. Further related research can be found on the [WikiDetox outline of related work](https://meta.wikimedia.org/wiki/Research:Detox/Resources).

We also have a page that provides [a brief introduction to ML](ml_intro.md) to help make this research easier to understand.

## Public datasets

One of our contributions is to produce datasets to support research:
   * [Civil Comments annotated with toxicity and identity content Kaggle Competition](https://www.kaggle.com/c/jigsaw-unintended-bias-in-toxicity-classification): A public [Kaggle](https://www.kaggle.com/) competition, based on data from the [Civil Comments](https://medium.com/@aja_15265/saying-goodbye-to-civil-comments-41859d3a2b1d) platform, which shut down in 2017. This data is annotated for toxicity, toxicity sub-types, and mentions of identities, which enables evaluation of unintended bias with respect to identity mentions. See Kaggle page for detailed description of data source and annotation schema.
   * [Wikipedia Talk Page Comments annotated with toxicity reasons Kaggle Competition](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge): A public [Kaggle](https://www.kaggle.com/) competition, based on a crowdsourced dataset that includes 4 toxicity sub-types (reasons why something might be considered toxic), and approx 160k human labelled comments from Wikipedia Talk pages. The labelled annotations are based on asking 5000 crowd-workers to rate Wikipedia comments according to their toxicity (likely to make others leave the conversation). This dataset is also available on [Figshare as the Wikipedia Human Annotations of Toxicity on Talk Pages](https://figshare.com/articles/Wikipedia_Talk_Labels_Toxicity/4563973).
   * [Wikipedia Human Annotations of Personal Attacks on Talk Pages](https://figshare.com/articles/Wikipedia_Detox_Data/4054689): 100k Comments from wikipedia each with 10 annotations by the 4000 annotators who contributed to the effort. Each comment annotation notes whether the annotator considers the comment to be a personal attack or not.
   * [Wikipedia Machine Annotations of Talk Pages](https://figshare.com/articles/Wikipedia_Talk_Corpus/4264973): machine-labelled annotations for every English Wikipedia talk page comment from 2001 to 2015, approximately 95 million comments to support large scale data analysis.
   * To submit a link to an existing public dataset, or get help creating new public data sets for related research please fill out [this form](https://goo.gl/forms/z3JatRhT5x53Xa0I2).

## Opensource Code

We also have various public github projects to support research into having better converstions online:

* [Moderator](https://github.com/conversationai/conversationai-moderator) - a moderation tool to support using machine learning models to assist a human review process ([used by the New York Times](https://www.nytimes.com/2017/06/13/insider/have-a-comment-leave-a-comment.html)). There are also repositories that provide plugins for using moderator to support other platforms ([moderator for reddit](https://github.com/conversationai/conversationai-moderator-reddit), [moderator for wordpress](https://github.com/conversationai/conversationai-moderator-wordpress), [moderator for discourse](https://github.com/conversationai/conversationai-moderator-discourse)) 
* [An Authorship Experience](https://github.com/conversationai/perspectiveapi-authorship-demo) - code to build authorship experiences that give feedback to people as they type. This is used in [our public demo of perspective API](https://perspectiveapi.com), but the code repository includes many additional features and ways to create other auhtorship experiences.
* [Measuring and Mitigating Unintended Bias](https://github.com/conversationai/unintended-ml-bias-analysis) - our repository for tools to measure and mitigated unintended bias our modles. It includes our recent [paper](https://github.com/conversationai/unintended-ml-bias-analysis/blob/master/presentations/measuring-mitigating-unintended-bias-paper.pdf), [presented](https://github.com/conversationai/unintended-ml-bias-analysis/blob/master/presentations/Measuring%20and%20Mitigating%20Unintended%20Bias%20in%20Text%20Classification%20-%20AIES%202018.pdf) at [AIES'2018](http://www.aies-conference.com/accepted-papers/), and its corresponding tools so you can try it on your own models or datasets and build on our work to make better methods and tools.
* [Crowdsource](https://github.com/conversationai/conversationai-crowdsource) - Experimental tools to support crowdsourcing annotations.
* [wikidetox](https://github.com/conversationai/wikidetox) - our ongoing work with Wikimedia to create a useful corpus of Talk Page conversations on wikipedia.

We also have some smaller projects that provide specific technical demonstration code for working with [the Perspective API](https://perspectiveapi.com): 

* [perspectiveapi-js-client](https://github.com/conversationai/perspectiveapi-js-client) - A simple JavaScript client library for calling the Perspective API.
* [perspectiveapi-simple-server](https://github.com/conversationai/perspectiveapi-simple-server) - A simple [expresss](https://expressjs.com/) based proxy server that can hold your API-key and calls the Perspective API.
* [perspectiveapi-proxy](https://github.com/conversationai/perspectiveapi-proxy) - A [express](https://expressjs.com/) based simple proxy server that can be used to provide restricted access to your Perspective API cloud project.

Lots more hacks built using our API can be found at the [Perspective Hacks Gallery](https://github.com/conversationai/perspectiveapi/wiki/perspective-hacks) site, including: 

 * [Toxicity Timeline](https://github.com/conversationai/perspective-hacks/toxicity_timeline/README.md): See exactly when negative conversations happen and discover the patterns behind them.
 * [Hot Topics](https://github.com/conversationai/perspective-hacks/hot_topics/README.md): Compare unpublished articles with others that have created debate - before you push them live.
 * [Comment Blur Filter](https://github.com/conversationai/perspective-hacks/comment_filter/README.md): Easily find and hide comments based on your tolerance for toxicity.
 
## Research questions

The following are our key research questions.

### How might machine learning methods help online conversations?

We hypothesise that machine learning can help focus human attention more effectively. Our initial research is summerized in our blog post [Algorithms And Insults: Scaling Up Our Understanding Of Harassment On Wikipedia](https://medium.com/jigsaw/algorithms-and-insults-scaling-up-our-understanding-of-harassment-on-wikipedia-6cc417b9f7ff). 

### Machine learning to help understand harassment at scale?

In [Ex Machina: Personal Attacks Seen at Scale](https://arxiv.org/abs/1610.08914), we outline how crowdsourcing and machine learning can be used to analyze personal attacks at scale, and applies the methods to help understand the challenge on Wikipedia.

### What role does toxic language have in reducing the number of viewpoints in a discussion?

### What tools are needed to make robust open debate on important issues easier at scale?

### How might machine learning based tool be used by communities, commenters and authors?

We've developed [an opensource moderation tool](https://github.com/conversationai/conversationai-moderator/) to [enable the New York Times to spend more moderator time supporting their community](https://www.nytimes.com/2017/06/13/insider/have-a-comment-leave-a-comment.html).

### What aspects of a conversation can machine learning understand?

Can machine learning methods understand the emotional impact of language?

How much of the structure of a conversation can machine learning approaches uncover?

### What are the risks and challenges of using machine learning to assist online conversations?

What unintended and unfair biases might machine learning models contain? What impact might such biases have? What are the best ways to identify these biases? and what can be done mitigate them?

 * See [Attacking discrimination with smarter machine learning](https://research.google.com/bigpicture/attacking-discrimination-in-ml/) for a great introduction to the problem. Challenges related machine learning bias, fairness and algorithmic bias are outlined further on our [unintended bias page](bias.md).

 * In [Measuring and Mitigating Unintended Bias for Text Classification](https://github.com/conversationai/unintended-ml-bias-analysis/blob/master/presentations/measuring-mitigating-unintended-bias-paper.pdf) we have developed methods for measuing the unintended bias in a text classifier according to terms that appear in the text, as well as approaches to help mitigate them.

### How might machine learning based tool be gamed?

 * Word based models, including the CNN we developed for toxicty, can be tricked easily by creative misspellings. Using character level models can help address this, but require more data and their training suffers from [the vanishing gradient problem](https://en.wikipedia.org/wiki/Vanishing_gradient_problem).

 * Models based on character-level ngrams fed into feed-forward networks, like our TOXICITY_FAST model, can be easily gamed by adding additional ngrams after the initial comment that counter the signal from the problematic ngrams. This can be addressed by using RNNs and CNNs, like our TOXICITY model which take account of more of the textual context.

 * The practical impact of gaming ML models is an open research question, and is likely to depend on way the ML is applied. Moreover, there are different threat models for different applications of ML: gaming of an authorship experience is quite different to the recieving suggestions and considering retraining on them.

 * The research of [Cheng et. al.](https://arxiv.org/abs/1702.01119) and [Wulczyn et. al.](https://arxiv.org/abs/1610.08914) suggest that the majority of toxic contributions are not from people who would be incentivised to game models, but from people having a 'bad day'.

### How might ML be misused to censor or reduce viewpoints in a conversation?

ML is a very general technology and can be used in many ways. Part of our research is into possible mis-uses of such technology, for example, we've published a survey paper on [Network Traffic Obfuscation and Automated Internet Censorship
](https://arxiv.org/abs/1605.04044).
