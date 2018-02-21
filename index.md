# Research overview

Our research aims to help increase participation, quality, and empathy in online conversation at scale. Our three primary areas of research are:

* How might machine learning methods help online conversations?
* What aspects of a conversation can machine learning understand?
* What are the risks and challenges of using machine learning to assist online conversations?

Further details can be found in our [research resources page](research.md), and [our blog: The False Positive](https://medium.com/the-false-positive/).

# Public datasets

One of the main challenges of machine learning research is limited availability of high quality research data to improve online discussion.  We want to change that by creating, publishing, and/or identifying high quality public data sets related to online discussion.

* [Wikipedia Talk Page Comments annotated with toxicity reasons Kaggle Competition](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge): A public [Kaggle](https://www.kaggle.com/) competition, based on a crowdsourced dataset that includes 4 toxicity sub-types (reasons why something might be considered toxic), and approx 160k human labelled comments from Wikipedia Talk pages. The labelled annotations are based on asking 5000 crowd-workers to rate Wikipedia comments according to their toxicity (likely to make others leave the conversation). This dataset is also available on [Figshare as the Wikipedia Human Annotations of Toxicity on Talk Pages](https://figshare.com/articles/Wikipedia_Talk_Labels_Toxicity/4563973).
* [Wikipedia Human Annotations of Personal Attacks on Talk Pages](https://figshare.com/articles/Wikipedia_Detox_Data/4054689): 100k Comments from wikipedia each with 10 annotations by the 4000 annotators who contributed to the effort. Each comment annotation notes whether the annotator considers the comment to be a personal attack or not.
* [Wikipedia Machine Annotations of Talk Pages](https://figshare.com/articles/Wikipedia_Talk_Corpus/4264973): machine-labelled annotations for every English Wikipedia talk page comment from 2001 to 2015, a total of approximately 95 million comments that supports large scale data analysis.

To submit a link to an existing public dataset, or get help creating new public data sets for related research please fill out [this form](https://goo.gl/forms/z3JatRhT5x53Xa0I2).

# Perspective API

The Perspective API ([demo](https://www.perspectiveapi.com/); [API documentation](https://github.com/conversationai/perspectiveapi/blob/master/README.md)) serves models created by the Conversation AI research initiative to enable platforms, developers, and researchers to explore how ML might help conversations online. The API scores a comment based on its potential impact on a conversation.

Our first alpha-version perspective model, and the model that you can play with on the public demo is 'toxicity' (and it is only in English right now). The toxicity model allows text to be scored based its similarity to comments people have said are “toxic” or likely to make them leave a conversation. There are also several other experimental perspective models you can play with, such as a model that tries to identify unsubstantial comments. These are described in [our developer documentation](https://github.com/conversationai/perspectiveapi/blob/master/README.md). As the research develops we will add new models to the API and list them there.

Our models are still far from perfect - it will make errors: it will be unable to detect patterns of toxicity it has not seen before, and it will falsely detect comments that are similar to patterns of previous toxic conversations. To help improve the machine learning, the API supports sending us suggested scores which allow the model to improve. 

## How might the API be used?

The [gallery of perspective hacks](https://github.com/conversationai/perspectiveapi/wiki/perspective-hacks) illustrates various ideas people have had for how the API might be used. 

*We do not recommend using the API as a tool for automated moderation*: the models make too many errors. We have released early access to the API to support research and allow developers, publishers and platforms to try creating new conversational experiences e.g. to help human moderators choose what to review, to help people reading comments to choose what they read, or to help authors get another perspective on what they are writing. [Our blog post on how to use ML models, despite their imperfections](https://medium.com/the-false-positive/better-discussions-with-imperfect-models-91558235d442) outlines some further considerations and illustrates the challenge and opportunity further.

## How can I stay up to date with developments?

If you would like to receive email updates about the API - for example when we add new models, or deprecate old ones, you can subscribe to [perspective-announce](https://groups.google.com/forum/#!forum/perspective-announce/join), to receive emails updates from perspective-announce@googlegroups.com. This list will be used only to share release information, and will never be used to ask you for login details.

# Partner experiments

* [Wikimedia Foundation WikiDetox Research Project](https://meta.wikimedia.org/wiki/Research:Detox): aims to understand the nature of harassment and personal attacks at scale.
* With the New York Times we are working with to enable moderators to more quickly review comments by clustering similar comments together. Their article [Approve or Reject: Can You Moderate Five New York Times Comments?](https://www.nytimes.com/interactive/2016/09/20/insider/approve-or-reject-moderation-quiz.html) describes the challenges in more detail.

# Values guiding the research

* Community: For the community, by the community.
* Transparency: Open processes for open discussions.
* Inclusivity: Diverse points of view make discussions better.
* Privacy: It’s about what you say, whoever you are.
* Topic-neutral: It’s about how you discuss, not what you discuss.

# Who is working on this?

The research effort was started by [Jigsaw](https://jigsaw.google.com/) and the Google Counter-Abuse Technology Team and welcomes contributions from anyone interested in better online conversation. If you have questions about our research, you can email us at [conversationai-questions@google.com](mailto:conversationai-questions@google.com).

# Open source ML efforts for online conversation

Are you building a machine learning tool for great conversation that you’d like to us to know about and link to from this page? [Let us know!](https://goo.gl/forms/z3JatRhT5x53Xa0I2)

# Contributing examples to help improve online conversation

Do you have examples of comments (both comments you want in your community and comments you don't want in your community) that you would like to contribute for use in research and products to improve conversations online? You can [submit examples here](https://goo.gl/forms/d9TMWhnHB8vEzmyR2)
