# FAQ - Projects - RMIT AI COSC1125/1127

This is a FAQ for the **project** assessments only.

As any FAQ page, this page is always "under construction". As we realize that some questions become common, we add them here. So, bookmark it and check it regularly, particularly when you have a doubt and you suspect it may have been answered before!

- [FAQ - Projects - RMIT AI COSC1125/1127](#faq---projects---rmit-ai-cosc11251127)
- [GENERAL](#general)
  - [In a code assignment/project, how do I make sure I do not go against academic integrity?](#in-a-code-assignmentproject-how-do-i-make-sure-i-do-not-go-against-academic-integrity)
  - [I submitted wrongly (e.g., didn't tag correctly) and is now after the due date, can you consider my submission?](#i-submitted-wrongly-eg-didnt-tag-correctly-and-is-now-after-the-due-date-can-you-consider-my-submission)
  - [Project specification says "You should code your implementation only at the locations ...." . Does this mean that we can't create our custom classes outside the provided functions?](#project-specification-says-you-should-code-your-implementation-only-at-the-locations---does-this-mean-that-we-cant-create-our-custom-classes-outside-the-provided-functions)
  - [The feedback autograder says _"Your grades are NOT yet registered."_ What should I do to register?](#the-feedback-autograder-says-your-grades-are-not-yet-registered-what-should-i-do-to-register)
  - [Should I pass all the feedback autograder tests?](#should-i-pass-all-the-feedback-autograder-tests)
  - [Why do we need to show good SE/GIT processes?](#why-do-we-need-to-show-good-segit-processes)
  - [Can I just add dummy/padding commits to have more commits?](#can-i-just-add-dummypadding-commits-to-have-more-commits)
- [GIT \& GITHUB](#git--github)
  - [Git, GitHub, what is that?](#git-github-what-is-that)
  - [How do I submit my project solution in my GIT repository?](#how-do-i-submit-my-project-solution-in-my-git-repository)
  - [How do I change the submission tag if I have already tagged one commit for submission?](#how-do-i-change-the-submission-tag-if-i-have-already-tagged-one-commit-for-submission)
  - [How do I update the tags in my local repo? I get rejection with "(would clobber existing tag)" message](#how-do-i-update-the-tags-in-my-local-repo-i-get-rejection-with-would-clobber-existing-tag-message)
  - [Is a tag the same as a release in GitHub?](#is-a-tag-the-same-as-a-release-in-github)
  - [Cannot clone or push to GitHub with my password credentials?](#cannot-clone-or-push-to-github-with-my-password-credentials)
  - [I get `Permission denied (publickey).` from GitHub](#i-get-permission-denied-publickey-from-github)
  - [I have committed to the remote repo but I am not listed as a "contributor", why?](#i-have-committed-to-the-remote-repo-but-i-am-not-listed-as-a-contributor-why)
  - [Commits not correctly associated to my GitHub account, why?](#commits-not-correctly-associated-to-my-github-account-why)
- [PYTHON](#python)
  - [What version of Python should I use?](#what-version-of-python-should-i-use)
  - [How do I run Python 3.6 in `coreteachingXX.csit.rmit.edu.au`?](#how-do-i-run-python-36-in-coreteachingxxcsitrmiteduau)
  - [How do I install a package/module in `coreteaching` using `pip`?](#how-do-i-install-a-packagemodule-in-coreteaching-using-pip)
  - [How do I know the type of a variable in Python?](#how-do-i-know-the-type-of-a-variable-in-python)
  - [AttributeError: module 'importlib' has no attribute 'util'](#attributeerror-module-importlib-has-no-attribute-util)
- [GENERAL PACMAN](#general-pacman)
  - [What is the best way to develop my solutions for the Pacman project?](#what-is-the-best-way-to-develop-my-solutions-for-the-pacman-project)
  - [How to run Pacman remotely from `coreteaching`?](#how-to-run-pacman-remotely-from-coreteaching)
  - [How do I setup a system in Windows with Python 3.6?](#how-do-i-setup-a-system-in-windows-with-python-36)
  - [Can I use `problem._visited`?](#can-i-use-problem_visited)
  - [I get "`_tkinter.TclError: no display name and no $DISPLAY environment variable`" error when running in WSL or ssh](#i-get-_tkintertclerror-no-display-name-and-no-display-environment-variable-error-when-running-in-wsl-or-ssh)
  - [Cannot run Pacman due to problems with Tkinter: "`ImportError: No module named Tkinter`"](#cannot-run-pacman-due-to-problems-with-tkinter-importerror-no-module-named-tkinter)
  - [Error module 'cgi' has no attribute 'escape' when running autograder.pt](#error-module-cgi-has-no-attribute-escape-when-running-autograderpt)
  - [Can't fit the Pacman window in my screen, can I resize it?](#cant-fit-the-pacman-window-in-my-screen-can-i-resize-it)
  - [Cannot compile Metric-FF in MacOS](#cannot-compile-metric-ff-in-macos)
  - [One of the many tests is failing, how can I just run one question or even one particular test only?](#one-of-the-many-tests-is-failing-how-can-i-just-run-one-question-or-even-one-particular-test-only)
  - [My X algorithm (e.g. A\* search) works but it takes too long, what's the best way to work out why it's taking so long/work out how to optimise it?](#my-x-algorithm-eg-a-search-works-but-it-takes-too-long-whats-the-best-way-to-work-out-why-its-taking-so-longwork-out-how-to-optimise-it)
  - [How can I debug my system?](#how-can-i-debug-my-system)
  - [Can I change the pacman infrastructure at run-time?](#can-i-change-the-pacman-infrastructure-at-run-time)
  - [Can I use catch all exceptions in my code, or exceptions from the infrastructure?](#can-i-use-catch-all-exceptions-in-my-code-or-exceptions-from-the-infrastructure)
- [Project 0](#project-0)
  - [Do we have to handle edge cases? For example, for the `shopSmart` function, what should we do if a fruit is _not_ present in one of the shops?](#do-we-have-to-handle-edge-cases-for-example-for-the-shopsmart-function-what-should-we-do-if-a-fruit-is-not-present-in-one-of-the-shops)

-------------------------

# GENERAL

## In a code assignment/project, how do I make sure I do not go against academic integrity?

Check the [answer to this key question here](../AI23-DOC.git/CODE-INTEGRITY.md)

## I submitted wrongly (e.g., didn't tag correctly) and is now after the due date, can you consider my submission?

We will not fix any submission and it is your responsibility to do it correctly.

However, the nice thing about git-based projects/assessments is that we can rely on commits. If you have submitted your tag incorrectly (did not tag it at all, tagged with different name or different capital letters), then please fix your submission by tagging the specific commit you want me to mark. I will use the timestamp of the commit itself, not of when it was tagged. This means that if the commit was done before the deadline, then all good!! Isn't this cool?

## Project specification says "You should code your implementation only at the locations ...." . Does this mean that we can't create our custom classes outside the provided functions?

Yes, you can create some help functions or classes, but **always** in the allowed files. Any other change in any other file will be totally ignored.

If you want to create custom classes and functions, you can also nest them inside the location where you read `***YOUR CODE HERE***`. See [this link](https://www.datacamp.com/community/tutorials/inner-classes-python) and [this link](https://www.programiz.com/python-programming/closure#:~:text=A%20function%20defined%20inside%20another,in%20order%20to%20modify%20them) for more info.

## The feedback autograder says _"Your grades are NOT yet registered."_ What should I do to register?

The autograder is some immediate **feedback** for you, but it is not the final grading we do as teaching staff.

So, while the automarker is a useful indication of your performance, it may not represent the ultimate mark. We reserve the right to run more tests, inspect your code and repo manually, run similarity software for integrity checks (this year via [Codequiry](https://codequiry.com/)), and arrange for a face-to-face meeting for a discussion and demo of your solution if needed.

After submission deadline we will mark them all and provide you with the results.

## Should I pass all the feedback autograder tests?

Well, if you want to have a chance to get full marks _yes_.

Basically, the feedback autograder given is the _bare minimum_ and it is meant to provide you with some help in you development. In fact, even if your solution does meet every feedback test case given, it still does not necessarily mean it is perfect, as we may run additional tests when we actually grade the submission. Again, the autograder is an invaluable feedback tool for development and is the bare minimum, but more will be asked. You are encourage to extend it with your own tests and to perform your own extended efficiency evaluation when appropriate.

We are aware that it can be a bit unforgiving to work with the automated test harness, but often your understanding of the underlying algorithms are greatly improved when you need to dig into particular corner cases, so it's time well spent.

As recognised by students, the autograder is indeed a fantastic feedback before submission for you. It is the minimum expected and you have it right from the start, so use it!

## Why do we need to show good SE/GIT processes?

It is a fair question: _why don't we just care about the AI algorithm and that's it?_

There are, at least three reasons to include SE and version control practices as part of the work and assessments of the course:

1. It is the way AI software and solutions are developed these days. Hence, good SE practices, and particularly version control, is part of the overall training we promote in our courses, particularly in advanced courses.
2. We want to be able to see evidence of _student workings_ towards the final solution, not just the solution. This is analogous to math assessments say: we want to know how you got to that, not just the final answer. It is normal in math that when workings are asked, a solution without workings will get no marks.
3. Good SE and version control will be _fundamental_ for the final contest project in order to be _productive_. This is because it is a large task and in teams, so using poor SE and git processes will be a serious obstacle.
   - This means that it is important to promote and enforce good practices from the initial, smaller, project assignments, so that we increase the chances good practices in the final project. The initial projects thus serve as strong signals that hopefully will result in better outcomes in the larger assessment task.

## Can I just add dummy/padding commits to have more commits?

**No!**

That will not only show very poor SE practices (because dummy commits are not meaningful commits), but most importantly it may be deemed as a case of "_dishonest behavior to get an unfair advantage_", which is against the course Honours Code and can be a serious offense. One thing is to have poor SE practices, another thing is to attempt to cheat, so that should be out of the question! :-)

------------------------------
# GIT & GITHUB

## Git, GitHub, what is that?

We will use proper (git) version control in all our programming projects. This is totally standard practice in the industry and you would have seen that in previous courses (SEF and SEPT at least). Said so, if you want to refresh or have a quick intro to it, here are two resources I found useful:

- [30' video on Git & GitHub](https://youtu.be/jG4Vs81kMlc).
- [GitHub Guides](https://guides.github.com/).
- [Git \& GitHub Tutorial & Reference @ Javatpoint](https://www.javatpoint.com/git).

There are lots more good resources on the web of course!
## How do I submit my project solution in my GIT repository?

You submit by **tagging the _exact_ commit that you want to submit and be marked**, using the exact name given in the assignment specification. We will ONLY marked tagged submissions and will ONLY mark the tagged commit. Students can have many commits, and branches, even commits after the deadline. We will mark ONLY what you submit.

Of course we do not have access to your local machine, so the tag has to be created locally or then _pushed_ into GitHub remote repo (see below for several guides). Your tag has to show under `tags`, for example:

![google-form](img/tags-github-gui.png)

Observe that a tag `submission` is:

- NOT the same as a tag called "`Submission`" (i.e., tags are case-sensitive);
- NOT the same as a _branch_ called "`submission`";
- NOT the same as a _commit message_ "`submission`"; and
- NOT the same as a _release_ called "`submission`".

A tag is a specific point in the repository history, the point you want to be used for marking. A branch, a comment, and a release are different things.

While you can tag from your IDE (e.g., VS Code) you can always resort to command line to first create the tag in your local repo and then push it to the remote:

```shell
$ git tag -a submission <hash of commit to tag>
$ git push origin submission
```

Check the remote has the tag where you wanted!

Note that _a tag name can only be used once_, so if you already have a tag `submission` and want to use that tag name on another commit (e.g., you have a better, more recent, commit for your solution), you first need to delete the existing tag; see the next question for that. :-)

- For basic information on tagging, check [here](https://git-scm.com/book/en/v2/Git-Basics-Tagging).
- To create, push, and view tags in GitHub Desktop, check [here](https://docs.github.com/en/desktop/contributing-to-projects/managing-tags).
- To tag via command line or via GitHub web interface, check [here](https://stackoverflow.com/questions/18216991/create-a-tag-in-a-github-repository).

Note that the timestamp of the _commit_ is the submission date.

## How do I change the submission tag if I have already tagged one commit for submission?

This will happen when you realize you have a better version to submit than the one you submitted/tagged before. To do that, you need to first _delete_ the existing tag from both your local repo and from the server:

```shell
$ git tag --delete <tagname>  # first delete tag in the local repo
$ git push origin :refs/tags/<tagname>  # then delete remote tag
```

It is important to use `:refs/tags` when deleting the remote tag, as otherwise you may delete the branch with the same name! The empty string to the left of the colon causes the remote reference to be deleted!

Once the tag has been fully deleted, so you can re-use it on another commit!

See this as well on how to _rename_ an existing tag:

![google-form](img/how-to-rename-tag.png)

More information on how to delete git tags [here](https://devconnected.com/how-to-delete-local-and-remote-tags-on-git/).

## How do I update the tags in my local repo? I get rejection with "(would clobber existing tag)" message

To fetch the tags in the remote (e.g., tags pushed by other collaborators), you can do:

```shell
$ git fetch --all --tags -f
```

This will fetch all the changes from the remote, but also all the tags. The `-f` option will replace an existing tag (e.g., `submission`) with the one in the remote, if any (instead of failing). This could come very handy when different collaborators tag and re-tag commits as they incrementally work on a solution.

## Is a tag the same as a release in GitHub?

No, a _tag_ is a _git concept_, whereas a `Release` is something about GitHub, beyond git itself. So, they are not synonymous.

A tag is a _pointer_ to a specific commit, that's all, you basically give a name to a specific commit. This is what we use to mark the commit that is meant to be submitted for marking.
## Cannot clone or push to GitHub with my password credentials?

As [per August 12th, 2021 GitHub post](https://github.blog/changelog/2021-08-12-git-password-authentication-is-shutting-down/), GitHub is not no longer accepting account passwords when authenticating Git operations, like cloning private repos or pushing changes. You should use **token-based authentication**, such as  personal access, OAuth, SSH Key, or GitHub App installation token.

So, if you were still using a password to authenticate your GitHub.com operations (something never recommended anyways if you are doing development), you must start using a [personal access token](https://docs.github.com/en/github/authenticating-to-github/keeping-your-account-and-data-secure/creating-a-personal-access-token) by August 13, 2021 via HTTPS (recommended) or [SSH key](https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh) to start using a personal access token to avoid disruption.

For example, you can set-up your remote as follows (after you generated your token in GitHub):

```shell
$ git remote set-url origin https://<token>@github.com/<username>/<repo>
```

As explained [here](https://www.sobyte.net/post/2021-08/github-deprecates-passwords-for-git-operations/), tokens offer many advantages over password-based authentication:

* **Unique:** tokens are specific to GitHub and can be generated on a per-use or per-device basis.
* **Revocable:** tokens can be individually revoked at any time without the need to update unaffected credentials.
* **Limited:** tokens can be narrowed to allow only the access required by the use case.
* **Random:** tokens are not subject to dictionary types or brute force attempts that might be made with simpler passwords that users need to remember or enter periodically.

## I get `Permission denied (publickey).` from GitHub

If yo get this error

```shell
git@github.com: Permission denied (publickey).
fatal: Could not read from remote repository.
```

it most probably mean you have not correctly set-up your ssh keys into GitHub. GitHub needs your ssh public key to know it's you who is trying to access the repo. Please check [here](https://docs.github.com/en/authentication/troubleshooting-ssh/error-permission-denied-publickey).

Setting up GitHub to access with token or ssh is fundamental to have a productive environment, as you will be pushing and pulling from GitHub a lot! :-)

## I have committed to the remote repo but I am not listed as a "contributor", why?

The two main reasons may be:

1. Your commit is in a branch and has not yet made it to the default (master/main) branch, therefore you did not technically contribute (yet).
2. Your local Git commit email isn't connected to your account; [connect it](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/managing-email-preferences/setting-your-commit-email-address)!

Read [this GitHub page](https://docs.github.com/en/github/setting-up-and-managing-your-github-profile/managing-contribution-graphs-on-your-profile/why-are-my-contributions-not-showing-up-on-my-profile#common-reasons-that-contributions-are-not-counted) to understand more about why your commit is not yet counting as contributions.

## Commits not correctly associated to my GitHub account, why?

Please [check this](https://docs.github.com/en/github/committing-changes-to-your-project/troubleshooting-commits/why-are-my-commits-linked-to-the-wrong-user) and fix it so we can know the commit was *yous*. Otherwise we may get your contributions wrong and risk getting lower marks or delaying your marking.

------------------------------
# PYTHON

## What version of Python should I use?

All projects run on **Python 3.6+**, so your code must be written for such a version.

Some Linux distributions come with both `python2` and `python3` installed but default to `python2` for the python command. In this case, you should use the `python3` command in place of python to explicitly use version 3.x.

Additionally, in order to render the game, the homework projects require the Python module `tkinter` to be installed. You can follow the [official docs](https://tkdocs.com/tutorial/install.html) to get `tkinter` on your platform if it is not installed already. If you are using Linux, many distributions have packaged `tkinter` for easy install and you should use the package manager to install it. The package name is `python3-tk` for Debian/Ubuntu, `python3-tkinter` for RHEL/Fedora and `tk` for Manjaro/Arch.

There is no problem **having more than one Python version installed in your machine**, you just need to be careful your code is using the right one. You can use Python Package and Environment Managers, such as [Conda](https://www.freecodecamp.org/news/why-you-need-python-environments-and-how-to-manage-them-with-conda-85f155f4353c/) or [miniconda](https://conda.io/miniconda.html) environments, or an environment with [PIP+virtualenv](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/26/python-virtual-env/).

## How do I run Python 3.6 in `coreteachingXX.csit.rmit.edu.au`?

You need to activate it first using `scl`:

```bash
[eXXXXX@csitprdap01 ~]$ scl enable rh-python36 bash
[eXXXXX@csitprdap01 ~]$ python --version
Python 3.6.9
[eXXXXX@csitprdap01 ~]$ python
Python 3.6.9 (default, Sep 11 2019, 16:40:19)
[GCC 4.8.5 20150623 (Red Hat 4.8.5-16)] on linux
Type "help", "copyright", "credits" or "license" for more information.
```

## How do I install a package/module in `coreteaching` using `pip`?

Use option `--user` as you cannot do system-wide install:

```shell
[eXXXX@csitprdap01 ~]$ pip install pytz --user
WARNING: pip is being invoked by an old script wrapper. This will fail in a future version of pip.
Please see https://github.com/pypa/pip/issues/5599 for advice on fixing the underlying issue.
To avoid this problem you can invoke Python with '-m pip' instead of running pip directly.
Collecting pytz
  Using cached pytz-2022.1-py2.py3-none-any.whl (503 kB)
Installing collected packages: pytz
Successfully installed pytz-2022.1
```

## How do I know the type of a variable in Python?

Check this video to know how to print the type of a variable in Python:

[![Alt text](https://img.youtube.com/vi/iROZLaQGy4s/0.jpg)](https://www.youtube.com/watch?v=iROZLaQGy4s)

## AttributeError: module 'importlib' has no attribute 'util'

Some students reported that running `python capture.py` gives them the following errors:

```shell
Traceback (most recent call last):
  File "capture.py", line 1127, in <module>
    options = readCommand( sys.argv[1:] ) # Get game components based on input
  File "capture.py", line 902, in readCommand
    redAgents = loadAgents(True, options.red, nokeyboard, redArgs)
  File "capture.py", line 978, in loadAgents
    spec = importlib.util.spec_from_loader(moduleName, loader)
AttributeError: module 'importlib' has no attribute 'util'
```

Changing `import importlib` with `import importlib.util` seems to fix the problem.

We are still investigating this issue as it seems to work well in our set-up. This seems to be related to the fact that ["importing a package does not automatically load its submodules"](https://stackoverflow.com/questions/65028261/attributeerror-module-importlib-has-no-attribute-util-ii) but we are unclear why sometimes it does work! A quick search also brings [this post](https://stackoverflow.com/questions/39660934/error-when-using-importlib-util-to-check-for-library) which may be

------------------------------
# GENERAL PACMAN

## What is the best way to develop my solutions for the Pacman project?

We highly recommend developing your solutions in your local machine, that is, your laptop or desktop. Even more, if you are running Linux locally, 99.99% sure your code will ran in another Linux install. If you are using Windows, you may want to consider installing a Linux virtual machine with Virtualbox.

Secondly, you should use a modern IDE. We recommend Visual Studio Code, as it runs in any platform and has plugins for all the languages we will be using. It also has great git integration plugins and much more.

Also, all development should be done using high-quality version control processes. The course will use GitHub and GitHub Classroom. All development should happen there. Remember NOT to make your solutions public, as this will violate the course plagiarism code AND also break the will of the original creators of the wonderful project.

So, (local machine + VSCode (or other IDE) + git) will make the development much faster and higher-quality.

## How to run Pacman remotely from `coreteaching`?

If you do not care about the graphics (e.g., for grading), then try using `--textGraphics` or even `--quietTextGraphics`. In most cases you will use `coreteaching` machines just to test that the autograder works well. The autograder does not need any graphical interface so it should work properly.

If you do want the display, then you need to do X forwarding when you connect via ssh. If you are in Linux/Unix this is easy, just do `-X` and `-Y` when you ssh; for example:

```shell
$ ssh -X -Y username@coreteaching01.csit.rmit.edu.au
```

If you use Windows, then you need an X server running and set your ssh client (e.g., Putty) with X forwarding. For example, check [this page](https://superuser.com/questions/119792/how-to-use-x11-forwarding-with-putty) or this video:

[![Alt text](https://img.youtube.com/vi/vwZXhTykSis/0.jpg)](https://www.youtube.com/watch?v=vwZXhTykSis)

Said so, for development, we strongly suggest to clone your repo locally on your machine and work there (e.g., using PyCharm, Visual Code Studio, or even ECLIPSE).


## How do I setup a system in Windows with Python 3.6?

Although we will assume you are able to install and get Python running in your machine, there are plenty of videos on that on the web. For example:

[![Alt text](https://img.youtube.com/vi/oHOiqFs_x8Y/0.jpg)](https://www.youtube.com/watch?v=oHOiqFs_x8Y)

## Can I use `problem._visited`?

Under Python convention, single underscore before a name (e.g., `_visited`) denotes private data, and hence it is good practice not to rely on such data. Check [this post](https://shahriar.svbtle.com/underscores-in-python) for example. Note that such private data can change without notice, it may not be available anymore, it may not be available under other interfaces, etc. So....

## I get "`_tkinter.TclError: no display name and no $DISPLAY environment variable`" error when running in WSL or ssh

If you do not care about the graphics, then try using `-t` (or `--textGraphics`) or even `-q` (or `--quietTextGraphics`).

If you do want the display, then you need to do X forwarding when you connect via ssh. If you are in Linux/Unix this is easy, just do `-X` and `-Y` when you ssh (e.g., `ssh -X -Y server`).

If you use Windows, then you need an X server running and set your ssh client (e.g., Putty) with X forwarding. For example, check [this page](https://superuser.com/questions/119792/how-to-use-x11-forwarding-with-putty) and [this video](https://www.youtube.com/watch?v=vwZXhTykSis).

Also, if you are using Windows hooked up into Linux (WSL or WSL2), you need to properly resolve the IP Address seen by Linux. For example, under Ubuntu bash, add this to your `~/.bashrc`:

```shell
export DISPLAY=$(cat /etc/resolv.conf | grep nameserver | awk '{print $2}'):0
```


Then install the [VCXSRV](https://sourceforge.net/projects/vcxsrv/files/vcxsrv/) X-server. Run xLaunch and "Disable access control". And add a new inbound rule in Windows Firewall for TCP Port 6000.  Use the ssh command as above.

As you can see, all this can be too complicated for no benefit. For development, **we strongly suggest** to clone your repo locally on your machine and work there (e.g., using PyCharm, Visual Code Studio).

## Cannot run Pacman due to problems with Tkinter: "`ImportError: No module named Tkinter`"

Install Tkinter in your system. If you are running `conda`:

```bash
$ conda install tk
```

Now it should be installed, so you should not get this error. But please try the code below, it should not trigger any error:

```bash
[eXXXXX@foo~]$ scl enable rh-python36 bash
[eXXXXX@foo~]$ python
Python 3.6.9 (default, Sep 11 2019, 16:40:19)
[GCC 4.8.5 20150623 (Red Hat 4.8.5-16)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> import tkinter
>>>
>>>
[eXXXXX@foo~]$
```

## Error module 'cgi' has no attribute 'escape' when running autograder.pt

You are probably not using Python 3.6 but a higher version. Check [this post](https://piazza.com/class/kbsmlzxg3k7418?cid=28).

## Can't fit the Pacman window in my screen, can I resize it?

The Pacman windows cannot be resized once open. However, you can use the option `-z <float>` (or `--zoom <float>`) to scale the window. For example, using `-z 0.5` will scale down the window by half. Using this option you should be able to fit the entire window in the screen.

## Cannot compile Metric-FF in MacOS

Some Mac users have reported this error when compiling [Metric-FF](https://fai.cs.uni-saarland.de/hoffmann/metric-ff.html) planner:

![bad-graphics](img/ff-compile-mac.png)

The problem seems to be that the default `gcc` in Mac is set to be `clang`. So, you first neeed to install standard `gcc` on using command `brew install gcc@7`  (must use version 7, newest version 10 won't work) and instead of just `make`, you need to run:

```bash
make CC=/usr/local/bin/gcc-7
```

Thanks Banhao from AI'20!

## One of the many tests is failing, how can I just run one question or even one particular test only?

Use the `-q n` option for running just one question (e.g., `-q q3` to run Question 3 only) or `-t` to run only a specific test (e.g., `-t test_cases/q1/graph_bfs_vs_dfs`).

## My X algorithm (e.g. A* search) works but it takes too long, what's the best way to work out why it's taking so long/work out how to optimise it?

Fundamentally there are two ways of approaching this, empirically or theoretically.

Empirically you can profile your code and see which sections are taking the longest. If you have a particular section that you suspect might be the issue, you can use the time module to check manually. However probably the better way is to use pythons inbuilt `cprofile` tool. This works well, especially when paired with [Snakeviz](https://stackoverflow.com/a/49173782). There is also
[line_profiler](https://github.com/pyutils/line_profiler) which profiles line by line showing line time, total line time and number of calls.

Theoretically, you can use your algorithms and analysis skills to try to figure out the time complexity of your algorithm. If your code matches the book, it should have a similar time complexity, but you may want to dig a bit deeper into each individual line of code. What is the time complexity of popping from a priority queue in python? What about a list? What about adding a node to the frontier, or visited data structure?

In general, before spending a lot of time doing experimental analysis, look at your implementation conceptually in a very, I repeat, _very_, critical way and perform the (theoretical) analysis of it. Think where the problem could be and whether you can suspect of something that is not well done. It's like being a detective, and good detectives are critical and meticulous!

## How can I debug my system?

While you may want to do some print outs here and there, eventually using a debugger is the way to go. Check [this video](https://www.youtube.com/watch?v=w8QHoVam1-I) for a quick guide to debugging python in VSCode (you can do similar things in PyCharm or other editors as well). This is far more flexible and reliable than print messages. :-)

## Can I change the pacman infrastructure at run-time?

**Absolutely no!** You should never tamper with the Pacman codebase infrastructure in any project, neither at the source code level nor at run-time. That is not allowed for any project: your agent systems should alter anything in the infrastructure, even at runt-time, unless you have been given explicit permission in writing.

As a general rule, reading properties of the infrastructure is OK and you will need to do so indeed. But **modifying the infrastructure at run-time in any way is not OK**. First it is poor technical approach to rely on that. Second, it may _unfairly_ give you an advantage, and in the contest project, may even affect other teams; for example by making them fail!

For example, doing this in the contest project:

```python
Actions._directions.pop('Stop', None)
```

will delete the action `Stop` from the set of legal directions. That is of course NOT allowed as you are tampering with the infrastructure, not just with your own code. Instead, you should do something like this:

```python
# Get legal actions from the agent and remove "Stop"
actions = gameState.getLegalActions(self.captureAgent.index)
actions.remove(Directions.STOP)
```

Here is another example that interferes badly with the infrastructure:

```python
agent.configuration.direction = "North"
```

This is setting a property of the agent: that is done by the infrastructure as part of the simulation and you should not interfere.

Even a more serious one would be to override `makeObservation` or any other function or class in the infrastructure. Never ever do that.

In fact, tampering with the infrastructure could be considered as dishonest behavior to get an unfair advantage. If you are in doubt, then ASK, never assume. Not asking before tampering with the codebase is in fact very worrying, even more for an advance course like AI.

We have specialized checks to test that the infrastructure is kept unchanged.

So please, remove absolutely every code that modifies, changes, or alter, even minimally, any part of the infrastructure and make sure you play _fair_ and don't make Pacman cry...

## Can I use catch all exceptions in my code, or exceptions from the infrastructure?

**Absolutely no!** It is first a very [bad practice](https://www.learnpython.dev/03-intermediate-python/40-exceptions/70-best-practices/#:~:text=Catching%20BaseException%20is%20a%20really,Don't%20do%20it.), as stated in PEP-8 and so many pages around:

> When catching exceptions, mention specific exceptions whenever possible instead of using a bare `except:` clause.

So, instead of doing:

```python
try:
    import platform_specific_module
except:
    platform_specific_module = None
```

you should instead do

```python
try:
    import platform_specific_module
except ImportError:
    platform_specific_module = None
```

You can see there that I am catching the specific `ImportError` exception (not any exception!), which is what could happen when I execute the `import` statement.

For the same reason, you should never catch `Exception` or `BaseException`, or any exception raised by the Pacman infrastructure itself (as the ones used for tracking timeouts). This would amount to tampering with the Pacman infrastructure, which is pretty bad (check question above on that).

Most solutions won't require catching any exception, but if you happen to do/need so, you must catch specific exceptions and not the ones of the Pacman infrastructure.

-----------------
# Project 0

## Do we have to handle edge cases? For example, for the `shopSmart` function, what should we do if a fruit is _not_ present in one of the shops?

For this project only (Project 0), since it is just designed to get you warmed up with python and git, you do not need to consider edge cases which are not mentioned in the project spec.

Specifically:

* for Q2, you should handle the case where the price list does not contain a fruit in the order, and return `None` as specified.
* for Q3, you do not need to handle the case where the shop does not contain one of the fruits in the order - you can assume _all_ shops will have all relevant fruit.

Having said that, for your own benefit, this is a great question to be thinking of, and you should feel free to handle the edge case if you would like. This is a great bonus activity that introduces you to some of the subtleties inherent in working with existing code-bases.

Note that, for all future projects you should consider edge cases carefully and handle them appropriately, even if we do not say so explicitly in the project spec. This is a critical skill for programming and will really test your detailed knowledge of the underlying algorithms that you will see in this course.

**Note:** in principle, a shop that misses one item in the order would just need to be ignored and not considered. However, this would mean that code in `shop.py` would have to be altered (which goes against what UC's specification!), because the predefined shop class contains its own function `getPriceOfOrder`, which does _not_ handle missing fruit in the way that Q2 requires.

One could import the function from Q2 and use that instead, but the function signatures then won't match, so one needs to create a wrapper in Q2 anyway, and it all gets a bit messy. Fundamentally if you use `getPriceOfOrder`, it will give wrong results for any shops which don't stock all your fruit, but that does seem to be the intended solution.
