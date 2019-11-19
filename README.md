# fcculsan_ontheweb

This is a website for our FCC ulsan to to practice their burgeoning coding skills.

https://fcculsan.github.io/fcculsan_ontheweb/

GO CRAZY!!!

# Contributing to this repository:

This may seem a bit confusing at first. Try it out, and if it doesn't work, ask for help in the group.

## GitHub Website method:

The easiest way is to just use the GitHub website.

1. Edit any file in this repository on the GitHub website.
2. Tell us about your change and submit it.
   - Describe your changes in detail in the text input boxes at the bottom of the page.
   - Click the green "Propose file change" button at the bottom of the page.
3. Click the green "Create Pull Request" button

## Command Line method:

The instructions stem mostly from these tutorials and what worked for us at the meetup:

https://akrabat.com/the-beginners-guide-to-contributing-to-a-github-project/
https://gist.github.com/MarcDiethelm/7303312

1. Fork the FCC Ulsan main repository by clicking the "Fork" button in the top left of the page.
2. Clone the repository to your local machine
3. Configure the `origin` and `upstream` correctly.

   - `origin`'s URL should point to your fork, so the URL should have your GitHub account in it.
   - `upstream`'s URL should point to the original repository, so the URL should be `https://github.com/fcculsan/fcculsan_ontheweb.git`.
   - use `git remote` to see if `origin` and `upstream` exist.

     - use `git remote get-url origin` and `git remote get-url upstream` to see what the URLs are.

   - If `origin` or `upstream` have the wrong URLs, you can rename them with `git remote rename (oldname) (newname)` or delete them with `git remote remove (origin/upstream)` and create them with the correct URL using `git remote add (origin/upstream) (URL)`.

4. Push your local commit to your remote fork.
   - `git push origin master`
5. Go to your forked repository on the GitHub website.
6. Click the "Pull Request" button to the right of where you see "This branch is 1 commit ahead of fcculsan:master."
7. Click the green "Create Pull Request" button.
8. Describe your changes, and submit it.
9. You're done!

# Updating your forked repository

Sometimes others will make changes to the `upstream` repository. They won't show up in your forked repository. You need to manually sync these changes. You can delete your forked repository directly on the GitHub website, then fork the `upstream` repository again. This will give you a fresh copy of the `upstream` repository that's up to date. Of course, you will lose any commits in your forked repository that weren't pulled into the `upstream`.

The best way I know how to do this is via the command line.

1. Ensure all the previous command line steps have been done correctly.
   - [ ] Your local repository has 2 remote branches: `origin` and `upstream`.
     - [ ] `origin` has a `url` including your username
     - [ ] `upstream` has the `url` `https://github.com/fcculsan/fcculsan_ontheweb.git`
2. Fetch the `upstream` changes
   - `git fetch upstream`
3. Make sure you're on the `master` branch
   - `git checkout master`
4. Combine the `upstream` changes with the code you have locally on `master`
   - `git rebase upstream/master`
5. Push your updated local repository to your forked version.
   - `git push origin master`
6. DONE! You can continue writing code, committing, pushing, and doing pull requests as usual.
