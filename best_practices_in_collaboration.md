# Best Practices in Open Collaboration on ML for Better Conversations

There are many challenges for people and organizations trying to collaborate to have better discussions by leveraging ML. This page outlines some proposals for best practices to support a larger more collaborative and open ecosystem to help improve online discussion.

## Share anonymized public contributions under creative commons

1. For comments that are already public, we recommend that organizations license them under a creative commons license; for instance, like [ Wikipedia](https://en.wikipedia.org/wiki/Wikipedia:Text_of_Creative_Commons_Attribution-ShareAlike_4.0_International_License) does. This allows researchers to annotate examples, develop and experiment with ML to support conversations, and to find important subsets, for example subsets that can identify or mitigate [unintended biases in models](https://conversationai.github.io/bias). This also allows researchers to model's scores on the share comment datasets, which can help independent evaluation and improvements to otherwise private models (see the next section).
2. Even when users publish comments intended for a public audience, we recommend anonymizing their contribution when adding them to public datasets. Training of models can be done without knowing a user’s identity; this helps ensure privacy, and that models are not based on *who* people are, but their specific *contribution*.
3. Making additional annotations public, and running ML competitions, like the [Toxicity Kaggle competition](https://www.kaggle.com/c/jigsaw-toxic-comment-classification-challenge). When comments are *annotated* by either their impact on the conversation, or by a moderator’s action taken after reviewing the comment, this information can enable others to help develop better ML for online conversations.

## Make your ML training pipeline code public and open-source

Share ML training pipelines, and related tooling to measure and mitigate unintended bias, so that they can be independently evaluated and improved by other researchers. For example, for Conversation AI models, we provide [a github repository for modelling](https://github.com/conversationai/conversationai-models), and a [github repository for measuring and mitigating unintended biases in the models](https://github.com/conversationai/unintended-ml-bias-analysis). When trained on anonymized data, the raw models themselves can be shared, either via public APIs (like the [Perspective API](https://www.perspectiveapi.com/)), data and training code, or as TensorFlow graphs, to allow others to evaluate and help find issues and improve the models.

## Share scores of (private) models on the available large public CC datasets

Scoring large creative commons datasets with models provides a powerful way to enable deeper analysis of models and help share findings. This can help other researchers in the space develop models that complement your models also. For example, we provide [a scored corpus of all Wikipedia comments](https://figshare.com/articles/Wikipedia_Talk_Corpus/4264973).

## Risks

Large datasets sometimes contain personally identifiable information (PII) in the text contribution itself. For example, on occasion some users have attempted to "[dox](https://en.wikipedia.org/wiki/Doxing)" others by publishing PII in Wikipedia. Ways to mitigate this include:

1. Reconstruct the public dataset periodically to ensure that such PII which was removed from the original source is removed from the publicly provided data dumps or be scanned to remove PII from the content also.
2. Run code that removes PII from the dataset.
3. Services that provide access to a dataset should also provide a pub-sub for contributions that are redacted so that dependent services can respect PII removal. Services may want to limit access to these so that they are not misused to abuse PII.
