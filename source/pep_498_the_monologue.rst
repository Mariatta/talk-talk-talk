PEP 498: The Monologue
----------------------

This talk was accepted at PyCon Australia 2017. I also gave it as the closing keynote for
PyCon Canada 2017.

I submitted it to PyCon US 2018, but was rejected.

It was accepted at another regional conference summer of 2017, but I ended up declining it.

I also submitted it to another regional tech conference (not a Python specific one) but rejected.

Mentor (or lack of)
===================

This was the first time I submitted a talk proposal without help from any mentor, and I was feeling
quite nervous and unsure about the entire content.

My friend Sebastian Vetter helped proofread, and he gave me the thumbs up :)

Proposal
========


Title
'''''

PEP 498: The Monologue

Duration
''''''''

30 minutes slot

What
''''

Everything you need to know about f-strings

Why
'''

One of the exciting new features in Python 3.6, PEP 498 is also a case study of
a successful Python enhancement proposal and implementation.

Who
'''

Beginner Python users, or longtime users who have not yet upgraded to Python 3.6

Description
'''''''''''

Python 3.6 was released in December 2016, and it includes 16 new PEPs! We will focus on one of
them: PEP 498 - Literal String Interpolation, affectionately known as f-strings. Get a glimpse of
the lifecycle of a PEP. Then, we’ll learn about f-strings, see some examples, and know the gotchas.
You’ll want to upgrade to Python 3.6 just for this!

Outline
'''''''

1. Introduction (4 minutes)

   - Explain who this talk is for
     * Beginner python users, or
     * Longtime python users who have not upgraded to Python 3.6 yet

   - Introduce myself
     * I am not the PEP author
     * I am not any PEP’s author
     * I find PEP process fascinating

2. What’s a PEP? (3 minutes)

   - Python Enhancement Proposal
   - Describe the usual PEP acceptance process
     * Discussions on python-ideas, python-dev
     * Champion it, draft it
     * More discussions
     * Pronouncement (either acceptance or rejection from BDFL)
   - Fun facts:
     * At the time of writing this proposal, there have been 349 PEPs proposed, 78 of them rejected. (22%)

3. What’s PEP 498? (5 minutes)

   - the feature also known as f-strings
   - Who’s the author?
     * Authored and implemented by Eric V Smith
   - Timeline
     * initial draft 2015
     * pronouncement sep 2015
     * Release dec 2016
   - python-dev discussions
   - Documentation https://docs.python.org/3/reference/lexical_analysis.html#f-strings

4. Why PEP 498 / Rationale (2 minutes)

   - Existing ways of formatting are either error prone, inflexible, or cumbersome
   - Similar PEPs: PEP 215, PEP 292
   - Comparison to other languages’ string interpolation

5. F-strings (5 minutes)

   - Provide examples on how to use f-strings
   - Both f”” and F”” are accepted
   - Previous ways of string formatting are still accepted
   - Provide comparison of how to format strings previously, and using f-strings

6. Gotchas

   - [2 mins] Can’t use it as docstrings (http://bugs.python.org/issue28739)

   - [2 mins] multi-line strings http://bugs.python.org/issue29668

   - [2 mins] IDLE syntax highlighting http://bugs.python.org/issue29071

   - [2 mins] unicode chars in format specifiers http://bugs.python.org/issue28827

   - [2 mins] Back slashes http://bugs.python.org/issue27921, http://bugs.python.org/issue27948

7. Conclusion
   - Inspire the audience to upgrade to Python 3.6 because of PEP 498

Thanks!
