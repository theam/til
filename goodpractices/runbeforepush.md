Jorge Rodríguez

# Run locally before publishing code!

Last night, I had a code I had verified it was working OK, with a good battery of tests to support the new feature. Then I was required to make a little refactor. Once I completed it, I just ran the battery of tests to verify it worked. Once that code got into master, it turned out that it messed app start-up because I missed an `@Inject` annotation (which is something you don't see in tests). 

Do **NOT** create PRs and merge them before running them locally to rule out this kind of mistakes.
