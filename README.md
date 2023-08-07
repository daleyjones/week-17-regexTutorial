# Regular Expression (RegEx) Tutorial
This tutorial has been crafted to elucidate the functioning of a specific regular expression (RegEx). Its purpose is to dissect the individual components of the RegEx, aiding in the comprehension of what might appear as a seemingly arbitrary sequence of characters. A RegEx can be employed to locate and substitute characters within this seemingly random sequence.

# Overview
In this tutorial, we will delve into the role of each character within the following RegEx, which is designed to match an email: /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ This particular RegEx is typically utilized to validate the correctness of an entered email address.

# Table of Contents
* Anchors
* Quantifiers
* Bracket Expressions
* Character Classes
* Flags
* Grouping
# Components of the RegEx
Anchors
The symbols ^ and $ are known as anchors since they are positioned at the start and end of a RegEx. /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ The content between these anchors is the focal point of the search. For instance, if the word following ^ is "Start," the search targets "Start." Similarly, using between the anchors targets both words. In our example, the characters enclosed between the anchors are ([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6}), and this is what needs to be matched and returned by our search.

# Quantifiers
Quantifiers are represented by curly braces {}. As the name suggests, they dictate the quantity or range of characters preceding the braces, which must be present for a match to occur. Taking our RegEx as an example: /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/ We can observe that the preceding characters are [a-z.], followed by the quantifiers {2,6}. This indicates that all alphabet letters must appear between 2 and 6 times for a correct match.

# Bracket Expressions
Bracket Expressions are denoted by square brackets []. Anything enclosed within these brackets is the subject of the search. For instance, [a-z0-9] will seek out all alphabet characters and digits from 0 to 9.

# Character Classes
Character classes enhance the search by distinguishing between letters and numbers. In our example, this is exemplified as [\da-z.-], where \d represents any digit and lowercase alphabetic letters.

# Flags
Flags introduce exceptions or rules and are encapsulated within forward slashes / at the beginning and end of the RegEx. There are six distinct flags applicable to a RegEx: i for case-insensitive search, g for global search (returning all matches), m for multi-line mode, s for "dotall" mode (allowing dot . to match newline \n), u for full Unicode support, and y for "sticky" mode (searching from an exact position).

# Grouping
Grouping employs parentheses () to treat multiple characters as a single unit. In our example, three groups exist to segment the RegEx, forming subexpressions. /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

Author: Daley Jones.