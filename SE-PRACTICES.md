# SE and GIT Best Practices

Besides the correctness and performance of your solutions, you _**must**_ **follow good and professional SE practices** in your projects, including good use of git version control and professional communication and team-work during your development.

Overall, you want to generate a meaningful git history that provides quality evidence of your working towards your solution.

These include:

* _Configure your git authorship_: set your name and email address correctly so that your commits have correct authorship information. Read about this [here](https://docs.github.com/en/pull-requests/committing-changes-to-your-project/troubleshooting-commits/why-are-my-commits-linked-to-the-wrong-user).
* _Commit early, commit often (but meaningfully!):_ single or few commits with all the solution or big chunks of it is not good practice.
* _Use atomic logically-separate commits:_ avoid commits about many things or dummy commits; each commit should be about one interesting thing. You want to create a meaningful git history, that allows you to easily revert a past change. For that, you also don't want to flood your git history with tons of padding commits.
* _Use meaningful commit messages:_ as comments in your code, a commit message should clearly and succinctly summarize what the commit is about. Messages like "fix", "work", "commit", "changes" are poor and do not help us understand what was done.
* _Never upload files:_ git should not be used as a storage service. Setup your system to do proper meaningful commits and do not use GitHub's upload button ever.

Besides proper commit behavior to obtain a clean and meaning history, you should:

* _Commit evenly across team members_ (for team project/assignment components). This means there should be meaningful commits from _all_ participating members. Note that [peer programming](https://en.wikipedia.org/wiki/Pair_programming), which we encourage, does _not_ mean one member always or mostly acts as the "driver" and commit; *all* members should take turns, be the "driver" and commit to the repo. 
  * When peer-programming, make use of the [co-author facility](https://docs.github.com/en/github/committing-changes-to-your-project/creating-and-editing-commits/creating-a-commit-with-multiple-authors) in GitHub to be accounted in the contributions. See [this post](https://gitbetter.substack.com/p/how-to-add-multiple-authors-to-a) and [this post](https://github.blog/2018-01-29-commit-together-with-co-authors/) as well about co-authors commits. You can conveniently include multiple co-authors to a commit via GitHub Desktop or via VScode (or otherwise by writing special commit messages) as explained in the links given.
* _Use the Issue Tracker:_ use issues to keep track of tasks, enhancements, and bugs for your projects. They are also a great way to collaborate in a team, by assigning issues and discussing on them directly. Check GitHub [Mastering Issues Guide](https://guides.github.com/features/issues/).
* _Follow good workflow and use branches:_ use the standard branch-based development workflow; it will make your team much more productive and robust! Check GitHub [Workflow Guide](https://guides.github.com/introduction/flow/). When merging or re-basing, squash commits only when it will yield a more better set of commits in the main branch.
* _Communicate in the GitHub Team:_ in team projects, members are expected to communicate, in an adequate and professional way, in the GitHub team created along the repo. For example, you could use GitHub team discussions, use issues and pull requests to track development status, or create project plans in the Wiki. Video and voice chats outside of GitHub are permissible (and encouraged), but text communication should be through the GitHub team where possible.

Poor SE and version control practices can have a significant impact in the final mark of an assessment. For example, a single commit with all the solution will attract zero marks overall, even if the solution does perform perfectly.
