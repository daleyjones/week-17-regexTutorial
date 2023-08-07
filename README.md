# REGEX Tutorial
In this tutorial, we'll take a deep dive into the world of regular expressions by breaking down and explaining the components of specific regex patterns. Our goal is to help you understand how these patterns work and how they can be used to match certain patterns within strings. We'll focus on four different regex patterns: matching a Hex Value, matching an Email, matching a URL, and matching an HTML Tag.

# What Is a Regex?
A regex, or regular expression, is a sequence of characters that defines a search pattern. It's commonly used in programming and text processing to find specific patterns within strings. Each character in a regex has a special meaning, allowing you to create powerful pattern matching rules.

To start with, watch this introduction to regular expressions video and read Regex Tutorial: Matching a Username for a basic understanding of regex components. These resources will lay the foundation for understanding the components we'll discuss in this tutorial.

Matching a Hex Value: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

# Components:
* ^: Anchors the regex at the beginning of the string.
* #?: Matches an optional # character.
* ([a-f0-9]{6}|[a-f0-9]{3}): Matches either a 6-character or 3-character sequence of characters from the ranges a-f and 0-9.
# Explanation:
This regex pattern is used to match hex color values in the format #RRGGBB or #RGB, where RR, GG, and BB represent two-digit hexadecimal values for red, green, and blue components respectively. It accommodates both the common 6-character and shortened 3-character hex color codes.

# Matching an Email: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
# Components:
* ^: Anchors the regex at the beginning of the string.
([a-z0-9_\.-]+): Matches one or more lowercase letters, digits, underscores, dots, or hyphens for the username.
* @: Matches the literal "@" symbol.
* ([\da-z\.-]+): Matches one or more lowercase letters, digits, dots, or hyphens for the domain name.
* \.: Matches the literal "." symbol.
* ([a-z\.]{2,6}): Matches 2 to 6 lowercase letters or dots for the top-level domain.
# Explanation:
This regex pattern is used to validate email addresses. It breaks down an email address into three parts: the username, the "@" symbol, and the domain. It ensures that the username and domain follow specific patterns, and the top-level domain has 2 to 6 lowercase letters.

# Matching a URL: /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
# Components:
* ^: Anchors the regex at the beginning of the string.
* (https?:\/\/)?: Matches an optional "http://" or "https://".
* ([\da-z\.-]+): Matches one or more lowercase letters, digits, dots, or hyphens for the domain.
* \.: Matches the literal "." symbol.
* ([a-z\.]{2,6}): Matches 2 to 6 lowercase letters or dots for the top-level domain.
* ([\/\w \.-]*)*\/?: Matches optional path segments, including slashes, alphanumeric characters, spaces, dots, or hyphens.
# Explanation:
This regex pattern is used to validate URLs. It covers various components of a URL, including the optional "http://" or "https://://" prefix, the domain, the top-level domain, and optional path segments.

# Matching an HTML Tag: /^<([a-z]+)([^<]+)*(?:>(.*)<\/\1>|\s+\/>)$/
# Components:
* ^: Anchors the regex at the beginning of the string.
* <([a-z]+): Matches an opening HTML tag and captures the tag name.
* ([^<]+)*: Matches zero or more characters that are not the opening angle bracket ("<").
* (?:>(.*)<\/\1>|\s+\/>): Uses a non-capturing group to match either a closing HTML tag with content or a self-closing tag.
# Explanation:
This regex pattern is used to match HTML tags, both opening and closing, as well as self-closing tags. It captures the tag name and optionally any content within the tags. The use of a non-capturing group accommodates self-closing tags without content.

# Author
Daley Jones. https://gist.github.com/daleyjones/fc5b6fa0a326a329a88d5554ecf31e81