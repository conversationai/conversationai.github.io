# Model Quality

The quality of a machine learning model is typically evaluated by considering the model's scores on a set of examples for which the 'correct' answer is known. A statistical metric is then used to summarises how close the model's scores are to the correct answers.

Although that may sound fairly straightforward, there are three significant groups of challenges:

 * How do we get a set of examples that accurately reflects the 'real' usage, and which the model has not seen in training (a so called test set)?
 * Once we have a test set, how do we get the 'correct answers' (also called the labels) for it when the task is subjective?
 * Once we have a good labelled test set, and we've run the machine learning model on it, how do we summarize the differences between the models scores on the examples?

Each of these challenges is the subject many scientific papers, and there is generally no simple approach. Each machine learning task typically has to explore the best collection of approaches to measuring the models quality.

For the kinds of problems we are looking at (identifying characteristics of language that may help people have better conversations):

 * There is typically no consensus on the 'right kind of data' because there are many different kinds of conversations online happening in different communities. A model that works well or one, may not work well for another. For example, the NYT likely-to-accept model is very sensitive cursing. Other forums, like those discussing computer games, typically don't have the same strict criteria. Our approach here is to measure models according to a particular community's conversations, for example the Wikimedia community.

 * For characteristics of conversations, like Toxicity, where we measure it by people's perception that 'the text is likely to make someone leave the conversation', the 'correct answer' is typically somewhat subjective. We use a variety of crowdsourcing methods which essentially involve many people answering questions about a snippet of text.
 We measure how subjective the question is using metrics like [Krippendorfs alpha](https://en.wikipedia.org/wiki/Krippendorff%27s_alpha). This provides a notion of inter-annotator agreement. We also measure how many people we need to ask to get an accurate estimate for the question (for more about this methodology, see [our paper: Ex Machina: Personal Attacks seen at scale](https://arxiv.org/abs/1610.08914)). And then for every question in our test set, we collect an appropriately sized set of answers. This produces a distribution of answers for each question.

 * Typical metrics, like [accuracy](https://en.wikipedia.org/wiki/Accuracy_and_precision) and [F1](https://en.wikipedia.org/wiki/F1_score), are poor choices for problems where the examples one wants to identity are rare (where the classes are not balanced). For example, for toxic comments which occur on 1 in a 100 comments (for most communities they are typically considered to occur even less frequently), you can get an accuracy of 99% by simply saying everything is not toxic. To get a more meaningful metric, we use metrics that measures how well a method is at distinguishing examples, like the [ROC AUC](https://en.wikipedia.org/wiki/Receiver_operating_characteristic); which has a natural interpretion as: the probability that a random positive example will be given a higher score than a random negative example.

Throughout this process, there are ways that the machine learning algorithms may develop unintended bias (the intended bias is to be able to distinguish a characteristic of language that we think can be useful to making conversations better). For more information, see our page dedicated to [the challenges of unintended bias](bias.md).
