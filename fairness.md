[Back to Conversation AI Research Overview](index.md)

## Fairness and Bias in Machine Learning

Machine learning models are often biased in unintended ways. This tends to come from skewed or incomplete training data. In text classification, this typically happens because of:

 * *Gaps in the training data*: for example there are few outright threats of violence posted to wikipedia comments, so machine learning algorithms trained on that data will not be good at identifying them.

 * *Skewed annotators*: a skewed demographic of crowdworkers might impact the judgements they make. For example, if the population of crowdworkers labelling the training data skew toward a particular political orientation, they may not consider attacks on their political opponents as toxic. Here, we are loosely using the term "demographic" to refer to any characteristic of annotators that may correlate with their judgement (gender, age, sexual orientation, but also: membership in interest groups, etc.)

We want our models support conversations being more inclusive and allow more points of views to be shared. But unintended biases might lead to application inadvertently doing the opposite. An interactive visualization that explore the risks and impact of bias can be found at the site of [Attacking discrimination with smarter machine learning](https://research.google.com/bigpicture/attacking-discrimination-in-ml/). Many good further resources are maintained on the [FAT ML community resoure page](http://www.fatml.org/resources/relevant-scholarship).

## Are the models biased? in what ways?

The real question about our models is not do they have unintended biases - we are sure they must - but in what ways are they biased, how much, and how much of a problem is it? But even identifying if a model carries unintended biases can be difficult:

 * Carrying out a particular analysis that fails to find bias does not mean it is not there. Maybe other methods or additional data might still find bias. There is no conclusive test for a model not having an unintended bias.

 * There are several different concepts for what it means for a machine learnt model to be fair, which are not necessarily compatible, as demonstrated in [Inherent Trade-Offs in the Fair Determination of Risk Scores](https://arxiv.org/abs/1609.05807).

For our text classification problems, a natural notion of unintended bias is that result the model treats different groups of people differently, for instance by failing to recognize toxic attacks targeting a particular communities. A natural starting point here is to consider groups who are frequently targeted (e.g. [protected classes](https://en.wikipedia.org/wiki/Protected_class)).

A second form of bias we want to avoid is with respect to topic: we want to support conversations on any topic. We consider our model topic-biased when it over or under triggers significantly more when being evaluated on conversations concerning that topic.

## What leads to a model being biased?

Given that our machine learning models are trained by the judgements of people (crowdworkers in our case), the demographics of the people may be biased: the crowdworkers judgements may reflect their demographics instead of the characteristics of the text they are examining.

Identifying this demographic bias is challenging: it is hard to get accurate demographic information from crowdsourcing platforms. Moreover, the crowdworkers may not be representative of wider population.

But even if the crowdworkers are perfectly unbiased in their judgements, the raw data they are rating may not be sufficiently diverse. For example, if all comments that mentions breasts are in fact examples of sexist attacks, then the training of a machine learning algoithm would likely result in a model that believes the topic of breasts is itself toxic - i.e. breastfeeding forums would end up being considered toxic. Depending on how such a machine learning model is applied, it might inadvertently prohibit constructive and important conversations on that topic: exactly the opposite of our research efforts goal!

The key challenges in identifying bias from insufficiently diverse data are:

 * It is difficult to define the concept of 'topics' and thus diversity of topics in a dataset. Topic identification is itself a topic of significant machine learning research.

 * Like bias stemming from the crowdworker demogarphic, failure to find a topic bias only means that the method used to find it failed.

Moreover, the challenges of topic and demographics based bias may intersect: how toxic a comment is perceived by annotators may depend on both the characteristics of the annotator and the topic.

## What can we do about it?

Understanding and mitigating unintended bias requires analysis and scrutiny from an many perspectives. This is one of the key motivations for [opening access to an API that hosts models](https://www.perspectiveapi.com/) and creating public datasets like [our Wikipedia datasets](Research:Detox/Data_Release). These tools support others researchers to join the effort to understand and address bias in machine learning.

Bias in our models is an active area of research and we welcome others [getting involved in WikiDotox Wiki pages](https://meta.wikimedia.org/wiki/Research:Detox) and via [Conversation AI research projects on github](https://conversationai.github.io/).
