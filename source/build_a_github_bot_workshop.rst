Build-a-GitHub-Bot Workshop
---------------------------

This is a tutorial, rather than a talk. I submitted this to PyCon US 2018, and it
was accepted. I've submitted this to another regional conference, but was
rejected.

Mentor
======

Thanks to Eric Holscher. Not only he gave me advice and resources on how to
write and prepare a tutorial for PyCon, he also reviewed, proofread, and provided
additional feedback to this proposal before I submitted to PyCon US.

Also thanks to Brett Cannon, without his gidgethub library, I wouldn't have material
for this workshop. In addition, Brett reviewed, proofread, and fixed mistakes in
my tutorial documentation.

Proposal
========

The following was the proposal I submitted to PyCon US 2018.

Title
'''''

Build-a-GitHub-Bot Workshop

Description
'''''''''''

GitHub provides a great platform for collaborating. You can take it to the next
level by creating custom GitHub bots. By delegating some of the chores to a bot,
you get to spend more time developing your project and collaborating with others.
Learn how to automate your workflow by building a personal GitHub assistant for
your own project. We'll use libraries called gidgethub and aiohttp to write a
GitHub bot that does the following:

- Greet the person who created an issue in your project.

- Say thanks when a pull request has been closed.

- Apply a label to issues or pull requests.

- Gives a thumbs up reaction to comments you made. (becoming your own personal
  cheer squad).

The best part is, you get to do all of the above using Python 3.6! F-strings included!


Audience
''''''''

Intermediate/Advanced skill level.

Participants should know how to program in Python, have a GitHub account, know
how to commit their work using git and to create pull requests, and understand
how REST API works. They should also be familiar with the concept of Python
virtual environments and installing Python libraries using pip.

Prior to attending the tutorial, participant should have Python 3.6 installed
on their laptop.

This tutorial is not suitable for novices or someone new to
Programming.

For this tutorial, we will deploy the code to Heroku and GitHub. Participant
may want to reconsider taking this tutorial if there is anything preventing
them from uploading their source code to the cloud services like Heroku or GitHub.

Outline
'''''''

Introductions (5 minutes)
*************************

Format: presentation

- Go over the agenda (this outline)

- List the relevant resources:

* gidgethub documentation
* aiohttp documentation
* GitHub API v3 documentation
* Heroku tutorial

Intro to GitHub APIs (5 minutes)
********************************


Format: presentation

- An overview of the available API endpoints and webhook

- Examples of GitHub bots:

* Python Core Developers have 3 different GitHub bots deployed: bedevere, the-knight-who-says-ni, and miss-islington.

* Python Packaging Authority (pypa) has BrownTruck

Intro to gidgethub (5 minutes)
******************************


Format: presentation

- A python library for interfacing with GitHub APIs, written by a Python Core Developer. It requires Python 3.6.
- Used by Python Core Devs (bedevere, miss-islington) and Python Packaging Authority (BrownTruck)

Using gidgethub on the command line
***********************************


Format: hands-on

-------------------------
Installation (15 minutes)
-------------------------

- Install gidgethub
- Obtain GitHub Personal Access Tokens

---------------------------------------------
Write these command line scripts (30 minutes)
---------------------------------------------

In the first exercise, I will provide and explain the code, thenand give attendees a chance to try it themselves. In tThe subsequent exercises ones, I will provide hints as to which API to use, and they can try it themselves. I will then reveal my solution.

- Create a new issue. API docs: https://developer.github.com/v3/issues/#create-an-issue
- Comment on an issue. API docs: https://developer.github.com/v3/issues/comments/#create-a-comment
- Close the issue. API docs: https://developer.github.com/v3/issues/#edit-an-issue

---------------
Bonus exercises
---------------

For those who finished earlier than other attendees

- React to an issue. API docs: https://developer.github.com/v3/reactions/#create-reaction-for-an-issue
- Add and remove labels to an issue. API docs: https://developer.github.com/v3/issues/labels/#add-labels-to-an-issue

=================================
Create a web service (10 minutes)
=================================

- Create an aiohttp server
- Deploy it to heroku

----------
GitHub bot
----------

In the first exercise, I will provide and explain the code, and give attendees to try it themselves. The subsequent ones, I will provide hints as to which webhook event and which API to use, and they can try it themselves. I will then reveal my solution.

Exercises:

- A bot that leaves a comment whenever an issue is created ( 30 minutes)
  For example, it can say “Hello user”.

- A bot that leaves a comment whenever an pull request is closed (20 minutes)
  For example, it can say “Thanks for merging”, or “Thanks for the review”.

- A bot that leaves a “thumbs up” reaction whenever someone leaves an issue comment (20 minutes)

- A bot that adds a label “need review” whenever a pull request is created (20 minutes)


Q & A (10 minutes - end)
************************

Time for questions, open discussions, or if people need more time completing their exercises.


Bonus exercise
**************

A bot that closes a pull request if the description contains certain blacklisted/disallowed keywords.
