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

## Open Source Code

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
 
## Research Contributions

* [Toxicity Detection: Does Context Really Matter?
](https://www.aclweb.org/anthology/2020.acl-main.396/) studies the importance of  context, and when as well as to what extent it can change the perceived toxicity of posts, finding that context can both amplify or mitigate the perceived toxicity of posts, and moreover for a subset of the data that including context can even reverse the toxicity label.
* [Classifying Constructive Comments](https://arxiv.org/abs/2004.05476) introduces a new dataset of constructive comments, defines a taxonomy of characteristics of constructiveness, and provides models for constructiveness trained on this dataset.
* [Debiasing Embeddings for Reduced Gender Bias in Text Classification](https://ai.google/research/pubs/pub48410) demonstrates how traditional techniques for debiasing word embeddings can actually increase model bias on downstream tasks and proposes novel debiasing methods to ameliorate the issue.
* [Model Cards for Model Reporting](https://ai.google/research/pubs/pub48120) proposes a framework to encourage transparent reporting of the context, use-cases, and performance characteristics of machine learning models across domains.
* [Nuanced Metrics for Measuring Unintended Bias with Real Data for Text Classification](https://ai.google/research/pubs/pub48094) introduces a suite of threshold-agnostic metrics that provide a nuanced view of unintended bias in text classification, by exploring the various ways that a classifier's score distribution can vary across designated groups.
* [Crowdsourcing Subjective Tasks: The Case Study of Understanding Toxicity in Online Discussions](https://dl.acm.org/citation.cfm?id=3317083) discusses open questions and research challenges toward the goal of effective crowdsourcing of online toxicity as well as presenting a survey of recent work that addresses these.
* [WikiDetox Visualization](http://wikiworkshop.org/2019/papers/Wiki_Workshop_2019_paper_17.pdf) presents a novel data visualization and moderation tool for Wikipedia that is built on top of the Perspective API.
* [Conversations Gone Awry: Detecting Early Signs of Conversational Failure](https://ai.google/research/pubs/pub47560) introduces the task of predicting whether a given conversation is on the verge of being derailed by the antisocial actions of one of its participants and demonstrates that a simple model using conversational and linguistic features can achieve performance close to that of humans for this task.
* [Measuring and Mitigating Unintended Bias in Text Classification](https://ai.google/research/pubs/pub46743) develops methods for measuring the unintended bias in a text classifier according to terms that appear in the text, as well as approaches to help mitigate them. The limitations of these methods are expanded on in the follow up paper [Limitations of Pinned AUC for Measuring Unintended Bias](https://arxiv.org/abs/1903.02088).
* [Correlating Self-Report and Trace Data Measures of Incivility: A Proof of Concept](https://journals.sagepub.com/doi/abs/10.1177/0894439318814241) connects trace data and machine learning classifiers to self-reported survey information about user’s online behaviour demonstrating the correlation between the two.
* [WikiConv: A Corpus of the Complete Conversational History of a Large Online Collaborative Community](https://ai.google/research/pubs/pub47559) presents an unprecedented view of the complete history of conversations between contributors of English Wikipedia by recording the intermediate states of conversations---including not only comments and replies, but also their modifications, deletions and restorations.
* [Ex machina: Personal attacks seen at scale](https://ai.google/research/pubs/pub47349) outlines how crowdsourcing and machine learning can be used to scale our understanding of online personal attacks and applies these methods to the challenge on Wikipedia.
* [Network Traffic Obfuscation and Automated Internet Censorship](https://arxiv.org/abs/1605.04044) surveys approaches that use machine learning to obfuscate network traffic to circumvent censorship.
