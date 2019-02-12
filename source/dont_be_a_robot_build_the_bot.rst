Don't Be a Robot; Build the Bot
-------------------------------

I've given this talk as keynote at DjangoCon US 2018. Even though I didn't need to
submit anything there, I still prepared the abstract and outline. (I don't know
how I would start preparing the talk without any outline!)

I submitted the proposal to PyCon US 2019, and it was accepted.

Acknowledgements and Background
===============================

I've had the idea about this talk since late 2017, however I never got around
completing it.

Thanks to Nicholle James and Kenneth Love for inviting me as keynote speaker at
DjangoCon US 2018. It gave me opportunity to give this talk. Nicholle helped
brainstormed and refined the idea of this talk.

One of `Zapier (my employer)'s  core values <https://zapier.com/jobs/culture-and-values-at-zapier/>`_ is
**"Don't Be a Robot; Build the Robot"**, which means *"Invest in tools and processes
that lead to outsized impact so Zapier can be more productive"*.
It resonates with me the most throughout the development of `miss-islington <https://github.com/python/miss-islington>`_.
So it felt fitting to use it as the title of the talk.

The proposal was written summer of 2018, but the talk itself was completed
sometime in October 2018, during a period where I experienced mental breakdown
and depression. I took the month off from work to complete this talk.

Proposal
========

The following was the proposal I submitted to PyCon US 2019.

Title
'''''

Don't Be a Robot; Build the Bot

Duration
''''''''

30 minutes slot


Description
'''''''''''

Managing a large open source project like CPython is no easy task. Learn how the
Python core team automated their GitHub workflow with bots, making it easier for
maintainers and contributors to collaborate together. Even if you’re not managing
a large project, you can still build your own bot! Hear some ideas on what you
can automate on GitHub and personalize your bot based on your own workflow.
All you need is Python. Don’t be a robot; build the bot.

Audience
''''''''

This talk is for intermediate Python developers. I will mention concepts such as
webhooks, APIs, webservices, and coroutines. Code snippets will include Python 3.7
features (async/await) and Python 3.6's f-strings. Not only the audience will
learn about how Python got made, they will also learn how to build GitHub bots.
They will inspired to add more automations to their life.

Outline
'''''''

1. Self introduction (1 minute, real quick)

2. Problem in CPython’s workflow (total: 4 minutes)

   - Core developers are outnumbered

    * Hundreds of contributors vs less than 50 active core developers

    * Pull requests are created at much faster rate than they get reviewed and merged

  - Core python workflow is complicated

    * Every pull requests has to be checked, vetted, and reviewed thoroughly

    * Many tasks are tedious, but important

    * One of such tasks: doing backports

3. Backporting (total: 5 minutes)

   - What is backport? (3 minutes)

     * Applying changes from newer version to older versions of software

     * For CPython’s purpose, backport is how you will receive bug fix releases (like 3.7.1 and 3.6.7)

   - cherry-picker.py was created to facilitate CPython backporting

   - Problems with cherry-picker.py (2 minutes)

     * Still manual process, requires a core developer to be in front of computer,

     * Often forgotten step

     * I received bug reports, and I’m unable to maintain it

     * It is just a boring chore (but important)

4. Build the bot (total: 8 minutes)

   - We knew a bot can do the backport, so let's build it

   - Architecture: (5 minutes)

     * the bot utilizes GitHub webhooks to receive pull request events

     * it uses GitHub REST APIs to perform actions on GitHub

     * other dependencies: gidgethub, aiohttp, Python 3.6+

     * hosted in Heroku, uses celery for running tasks asynchronously

   - why celery (3 minutes)

     * celery is used to run tasks asynchronously, in Heroku's worker dyno

     * Web requests in Heroku times out after 30 seconds

     * Some tasks performed by the bot are long running (cloning CPython repo takes at least 2 minutes)

   - this bot is called: miss-islington

5. miss-islington (4 minutes)

   - Initially, it has just one job: automatically create backport pull requests

   - As we gained experience with GitHub APIs and building bots, we keep asking, what else can the bot do?

   - Eventually, miss-islington was given commit privileges

   - miss-islington can now automatically merge pull requests

6. Don't be a Robot (6 minutes)

   - "I'm not managing large projects like CPython, why would I need a bot?"

   - Some tasks are boring. Really. Let the bots do it. Save time, and do the real important things

   -  Maybe you don't even realize that a bot can do it? Some bots I'm making, for inspirations:

      * black out: bot for running black on pull requests

      * OOOS bot: Out-of-Open Source Github Autoreply bot

      * pyup Automerge bot: automatically merge pull requests made by pyup-bot

      * Automatically add code_of_conduct.md to GitHub repos

7. Conclusion and thanks (2 minutes)

   - Don't Be a Robot; Build the bot. Add more automation to your life.

   - This talk uses GitHub bot as examples, that's where I spend most of my time

   - You can build other bot. Many other apps have API

     * Slack, Twitter, Facebook, etc

   - If you do want to build GitHub bots: my step-by-step tutorial https://github-bot-tutorial.readthedocs.io/en/latest/

