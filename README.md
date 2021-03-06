RSpec Git Pre-commit Hook
=========

This is an improve version of the rspec-precommit from  [markhazlett](https://markhazlett/RSpec-Pre-commit-Git-Hook)

We add this features

1. Show what specs are failing
2. Add Color to the results
3. Add Loading while waiting to finish the rspec
4. Add RAILS_ENV=test to rspec command

ToDo

1. Show pending specs


The scripts will invoke your rspec tests and not allow you to commit unless they are all passing/pending. If any failures occur then it will stop the commit from going through to allow you to fix your tests.

Install
-----

1. Copy the rspec-precommit file into your ```.git/hooks``` directory.
2. Call the rspec-precommit from the pre-commit ```ruby .git/hooks/rspec-precommit``` (example in pre-commit file in repo)
3. Add rspec_results.html to your .gitignore file


Usage
-----

1. Try to perform a ```git commit -m ``` with a failing Rspect test.
2. To skip validation use ```--no-verify```

Troubleshoot
-----
If the hook is not getting executed, call ```chmod +x .git/hooks/rspec-precommit``` to make it so!
