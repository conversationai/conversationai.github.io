# Annotation instructions for Toxicity with sub-attributes

## Overview

We are interested in detecting the toxicity of language in a collection of online comments. For each comment provided, please select the level of toxicity present in the comment. When rating a comment, please use the following definitions as a guide:

* Very Toxic - a very hateful, aggressive, disrespectful comment or otherwise very likely to make a user leave a discussion or give up on sharing their perspective.
* Toxic - a rude, disrespectful, unreasonable comment or otherwise somewhat likely to make a user leave a discussion or give up on sharing their perspective.
* I'm not sure
* Not Toxic

We are additionally interested in determining if the comment contains profanity/obscenity, sexually explicit content, identity based negativity, threatening language, and insults. Please use the following definitions as a guide:

* Profanity/Obscenity: Swear words, curse words, or other obscene or profane language.
* Sexually explicit: Contains references to sexual acts or body parts sexual way, or other lewd content.
* Identity based negativity: A negative, discriminatory, or hateful comment against a group of people based on criteria including (but not limited to) race or ethnicity, religion, gender, nationality or citizenship, disability, age, or sexual orientation.
* Insults: Inflammatory, stereotyping, insulting, or negative language towards a person or a group of people.
* Threatening: Language that is threatening or encouraging violence or harm, including self-harm.

An annotator is provided with:

* A few training examples.
* A comment to evaluate.
* A question about whether a comment is in English.
* A question about the level of toxicity present in the comment.
* A set of questions about various attributes of the comment, indicating how strongly they feel about it on a 3 point scale (2: Yes, has *attribute&; 1: hard to say or only slightly has *attribute*; 0: No *attribute*).

## Process for annotators

1. Read the comment
2. If the comment is not in English, please indicate that on the checkbox
3. Choose the level of toxicity in the comment
4. Answer the following questions

## Examples answers from a rater to help calibrate annotators

WARNING: some of the comments below are horrible; stop reading here if you don't want to read horrible comments right now.

#### Example 1

* Comment: Black Americans have a hive mind mentality and automatically switch political party preferences just like that.
* Answers:
  * Toxicity: Very Toxic
  * Profanity/Obscenity: No
  * Sexually explicit: No
  * Identity based negativity: Yes
  * Insult: Yes
  * Threatening: No
* Reasoning: Stereotyping of black Americans in an insulting and demeaning way that promotes discrimination.

#### Example 2

* Comment: I will flay you alive, you fking faggot.
* Answers:
  * Toxicity: Very Toxic
  * Profanity/ Obscenity: Yes
  * Sexually explicit: No
  * Identity based negativity: Yes
  * Insult: Yes
  * Threatening: Yes
* Reasoning: Threatening, insulting and toxic towards gay community.

#### Example 3

* Comment: Good fucking lord.
* Answers:
  * Toxicity: I'm not sure
  * Profanity/Obscenity: Yes
  * Sexually explicit: No
  * Identity based negativity: No
  * Insult: No
  * Threatening: No
* Reasoning: This is a more subtle version of toxicity perhaps more passive aggressive but it is likely to have an impact on the conversation. In addition many will consider "fucking" to be obscene.

#### Example 4

* Comment: ouch bad move mother fucker. i'm coming for you now., going to rape you in your sleep.
* Answers:
  * Toxicity: Very Toxic
  * Profanity/Obscenity: Yes
  * Sexually explicit: Yes
  * Identity based negativity: No
  * Insult: Yes
  * Threatening: Yes
* Reasoning: Threatening comment and containing obscene content "mother fucker" and a sexually explicit threat (rape). Would count as Very Toxic. 

#### Example 5

* Comment: That's fucking amazing ! thanks for sharing.
* Answers:
  * Toxicity: Not Toxic
  * Profanity/ Obscenity: Yes
  * Sexually explicit: No
  * Identity based negativity: No
  * Insult: No
  * Threatening: No
* Reasoning: Contains "fucking" which would count as profane language however it is used in a "friendly" way so would not count as toxic.

#### Example 6

* Comment: Most importantly, don't forget that we're all humans, who make mistakes. And take it easy!
* Answers:
  * Toxicity: Not Toxic
  * Profanity/Obscenity: No
  * Sexually explicit: No
  * Identity based negativity: No
  * Insult: No
  * Threatening: No
* Reasoning: Nothing negative about particular comment.

#### Example 7

* Comment: You're a real idiot, you know that.
* Answers:
  * Toxicity: Toxic
  * Profanity/ Obscenity: No
  * Sexually explicit: No
  * Identity based negativity: No
  * Insult: Yes
  * Threatening: No
* Reasoning: Insulting and toxic comment towards other speaker. Likely to lead to conversation stopping or escalating.

#### Example 8

* Comment: Peter is an idiot.
* Answers:
  * Toxicity: Toxic
  * Profanity/ Obscenity: No
  * Sexually explicit: No
  * Identity based negativity: No
  * Insult: Yes
  * Threatening: No
* Reasoning: Insulting and toxic comment towards other speaker. Likely to lead to conversation stopping or escalating. However, even if this comment is about a specific person it is NOT identity based negativity as defined here because it does not have to do with a criteria such as race or ethnicity, religion, gender, nationality or citizenship, disability, age, or sexual orientation.

#### Example 9

* Comment: French people drink wine every evening.
* Answers:
  * Toxicity: Not Toxic
  * Profanity/ Obscenity: No
  * Sexually explicit: No
  * Identity based negativity: No
  * Insult: No
  * Threatening: No
* Reasoning: This is certainly stereotypical but NOT identity based negativity as defined here because it is not negative or hateful or otherwise promoting discrimination.  If the comment had been  "French people are raging alcoholics" then it would be considered as identity based negativity.

