---
menu: why
title: Why database migrations
redirect_from: /getStarted/why/
---
<div id="why">
    <h1>Why database migrations?</h1>

    <p>First, let's start from the beginning and assume we have a project called <i>Shiny</i> and its primary
        deliverable is a piece of software called <i>Shiny Soft</i> that connects to a database called <i>Shiny DB</i>.
    </p>

    <p>The simplest diagram to represent this could look something like this: </p>

    <p align="center"><img src="assets/SimpleView.png" style="max-width: 100%"/></p>
    <p>We have our
    software and our database. Great. And this could very well be all you need. </p>

    <p>But on most projects, this simple view of the world very quickly translates into this: </p>

    <p align="center"><img src="assets/Environments.png" style="max-width: 100%"/></p> <p>We now not
    only have to deal with one copy of our environment, but with several. This presents a number of challenges. </p>

    <p><strong>We have been pretty good at solving them on the code side.</strong></p>

    <ul>
        <li>Version control is now universal with better tools everyday.</li>
        <li>We have reproducible builds and continuous integration.</li>
        <li>We have well defined release and deployment processes.</li>
    </ul>
    <p><img src="assets/SoftGreen.png" style="max-width: 100%"/></p>
    <p><strong>But what about the database?</strong></p>

    <p><img src="assets/DbRed.png" style="max-width: 100%"/></p> <p>Well unfortunately
    we have not been doing so well there. Many projects still rely on manually applied sql scripts. And sometimes not
    even that (a quick sql statement here or there to fix a problem). And soon many questions arise:</p>
    <ul>
        <li>What state is the database in on this machine?</li>
        <li>Has this script already been applied or not?</li>
        <li>Has the quick fix in production been applied in test afterwards?</li>
        <li>How do you set up a new database instance?</li>
    </ul>
    <p>More often than not the answer to these questions is: We don't know. </p>

    <p><strong>Database migrations are a great way to regain control of this mess.</strong></p>
    <p>They allow you to:</p>
    <ul>
        <li>Recreate a database from scratch</li>
        <li>Make it clear at all times what state a database is in</li>
        <li>Migrate in a deterministic way from your current version of the database to a newer one</li>
    </ul>
</div>
