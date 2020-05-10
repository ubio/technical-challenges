# Frontend Developer Technical Test

Hi there!

We are excited about you considering to join our engineering team.

Below you will find a technical test that will help us understand your ability to write clean concise code, which is easy to reason about, maintain and support. We are also keen on seeing your approach to naming (because we know how hard naming is!) and structuring the entities around your codebase, as well as testing and documenting them.

Good luck, and looking forward to receiving your code.

## Spec

Implement an application that consumes a Free Dictionary API and displays its results.

The three main sections of the app are: Statistics, Queries, History.

### Statistics

Display useful information about the words queried and correlated results. Please choose what exactly is displayed.

### Queries

You should generate a list of 10 random words and display them as sub navigation items.

These words should remain the same until the user explicitely requests for a new set of 10 words to be generated.

Clicking on one the words brings in the results from https://owlbot.info/ (e.g. https://owlbot.info/?q=chair). If images exist, they should also be displayed.

If more than one entry is returned, they should be filterable by type and definition. One should also be able to sort the results by type, definition and example.

The state for both filters and ordering should be kept if a user navigates away from the app and returns to it.

### History

The user should be able to see a list of all queries made, with an indication of time and results returned.


## Our expectations

- You should use Javascript or TypeScript.
- Your can choose between vanilla JS or VueJS.
- You may choose to use our CSS Framework (https://universalbasket.github.io/css/) if desired.
- Please ensure that your README contains steps to get it up and running.
- Unless something is explicitly stated in the Spec, you are free to choose how to approach the specifics. Don't forget to document important implementation decisions.
    - Feel free to challenge the spec if something does not add up, or can be done more elegantly and/or efficiently. We appreciate the ability to work with the requirements.
- We expect you to spend some time with polishing, refactoring and covering codebase with tests.
- Try to limit the usage of "utility belts" (underscore, lodash, ramda); instead prefer latest ECMAScript features.


## Submitting solution

- Create a repository on GitHub and/or BitBucket, push your code there and send us a link.
- If you choose to use a private repository, download your code as ZIP and attach it to the email.
- Optional: Deploying the solution to some public service like Glitch