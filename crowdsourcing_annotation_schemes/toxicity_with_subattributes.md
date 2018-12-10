# Annotation instructions for Toxicity with sub-attributes

## Overview

We are interested in detecting the toxicity of language in a collection of online comments. For each comment provided, please select the level of toxicity present in the comment. When rating a comment, please use the following definitions as a guide:

* Very Toxic - a very hateful, aggressive, disrespectful comment or otherwise very likely to make a user leave a discussion or give up on sharing their perspective.
* Toxic - a rude, disrespectful, unreasonable comment or otherwise somewhat likely to make a user leave a discussion or give up on sharing their perspective.
* Slightly Toxic or hard to say.
* Not toxic.

We are additionally interested in determining if the comment contains profanity/obscenity, sexually explicit content, identity based attacks, threatening language and insults. Please use the following definitions as a guide:

* Profanity/Obscenity: Contains swear words, curse words, or other obscene or profane language.
* Sexually explicit: Contains references to sexual acts or body parts sexual way, or other lewd content.
* Identity based attack: A negative, discriminatory or hateful comment about a person or group of people based on criteria including (but not limited to) race or ethnicity, religion, gender, nationality or citizenship, disability, age or sexual orientation.
* Insulting: Insulting, inflammatory, or negative comment towards a person or a group of people.
* Threatening: describes a wish or intention for pain, injury, or violence against an individual or group.

An annotator is provided with:

* A few training examples.
* A comment to evaluate.
* A question about whether a comment is in English.
* A question about the level of toxicity present in the comment.
* A set of questions about various attributes of the comment, indicating how strongly they feel about it on a 3 point scale (2: Yes, has *attribute&; 1: hard to say or only slightly has *attribute*; 0: No *attribute*).

## Process for annotators

1. Read the comment
2. If the comment is not in English, please indicate that on the checkbox.
3. Choose the level of toxicity in the comment
4. Answer the following questions

## Examples answers from a rater to help calibrate annotators

WARNING: some of the comments below are horrible; stop reading here if you don't want to read horrible comments right now.

#### Example 1

* Comment: He looks like a caveman, only far less intelligent!
* Answers:
  * Toxicity: Toxic
  * Profanity/Obscenity: No
  * Sexually explicit: No
  * Identity based attack: No
  * Insult: Yes
  * Threatening: No
* Reasoning: Insults an individual's intelligence and appearance. Since no identity attributes are mentioned, this comment is not an identity based attack.

#### Example 2

* Comment: I will flay you alive, you fking faggot.
* Answers:
  * Toxicity: Very Toxic
  * Profanity/ Obscenity: Yes
  * Sexually explicit: No
  * Identity based attack: Yes
  * Insult: Yes
  * Threatening: Yes
* Reasoning: Threatening, insulting and toxic towards gay community. The word "fking" is a mis-spelled version of "fucking", which is profanity. In this comment, the word "fucking" does not have a sexual meaning.

#### Example 3

* Comment: ouch bad move mother fucker. i'm coming for you now., going to rape you in your sleep.
* Answers:
  * Toxicity: Very Toxic
  * Profanity/Obscenity: Yes
  * Sexually explicit: Yes
  * Identity based attack: No
  * Insult: Yes
  * Threatening: Yes
* Reasoning: Contains a sexually explicit threat (rape) and profane and insulting language ("mother fucker").

#### Example 4

* Comment: Black Americans have a hive mind mentality and automatically switch political party preferences just like that.
* Answers:
  * Toxicity: Very Toxic
  * Profanity/Obscenity: No
  * Sexually explicit: No
  * Identity based attack: Yes
  * Insult: Yes
  * Threatening: No
* Reasoning: This comment stereotypes and insults Black Americans based on race.

#### Example 5

* Comment: That's fucking amazing ! thanks for sharing.
* Answers:
  * Toxicity: Not Toxic, or Hard to say.
  * Profanity/ Obscenity: Yes
  * Sexually explicit: No
  * Identity based attack: No
  * Insult: No
  * Threatening: No
* Reasoning: Contains the word "fucking" which is profane language, however in this case it is used in a positive way. So it's very unlikely to be causing people to leave the discussion.

#### Example 6

* Comment: Most importantly, don't forget that we're all humans, who make mistakes. And take it easy!
* Answers:
  * Toxicity: Not Toxic
  * Profanity/Obscenity: No
  * Sexually explicit: No
  * Identity based attack: No
  * Insult: No
  * Threatening: No
* Reasoning: Nothing very negative about this comment. The only part that seems like it might be taken the wrong way is the implicit statement that you're not taking it easy; but that could also be a friendly encouragement.

#### Example 7

* Comment: Peter is an idiot.
* Answers:
  * Toxicity: Toxic
  * Profanity/ Obscenity: No
  * Sexually explicit: No
  * Identity based attack: No
  * Insult: Yes
  * Threatening: No
* Reasoning: Insulting and toxic comment towards other speaker. Likely to lead to conversation stopping or escalating. However, even if this comment is about a specific person it is NOT identity based negativity in the sense that we define it because it does not have to do with a criteria such as race or ethnicity, religion, gender, nationality or citizenship, disability, age or sexual orientation.

#### Example 8

* Comment: French people drink wine every evening.
* Answers:
  * Toxicity: Hard to say/Slightly
  * Profanity/ Obscenity: No
  * Sexually explicit: No
  * Identity based attack: Hard to say/Slightly
  * Insult: No
  * Threatening: No
* Reasoning: This is certainly stereotypical but NOT an strong identity based attack in the sense that we define it because it is not negative or hateful or otherwise promoting discrimination. But it is stereotyping and might be frustrating to people who identify as French, which justified the Slight/Hard-to-say rating. If the comment had been  "French people are raging alcoholics" than it would clearly be considered as an identity based attack.
