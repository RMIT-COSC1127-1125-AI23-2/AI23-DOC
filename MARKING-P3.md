# Marking Guide for AI'23 - Project 3 - Agents in City (Prolog)

This document explains the automarking framework and system used for Project 3 - Agents in City (Prolog).

In order to understand the output from the automarker, there are two distinct components:

1. the different test set cases we graded with; and
2. the dimensions each tests is evaluated/checked against.

The automarker will produce a YAML file describing the outcome of each single test in each test set. See below for an example of a part of such YAML file.

- [Marking Guide for AI'23 - Project 3 - Agents in City (Prolog)](#marking-guide-for-ai23---project-3---agents-in-city-prolog)
  - [Consult error-free](#consult-error-free)
  - [Test cases](#test-cases)
  - [Grading dimensions](#grading-dimensions)
    - [Completeness](#completeness)
    - [Redundancy](#redundancy)
    - [Soundness](#soundness)
  - [Overall score/marks](#overall-scoremarks)
  - [Report](#report)

## Consult error-free

Of course the very first and most basic requirement to get any marks is that your codebase compiles error free, so that the automarker can load it up as a library in full:

```
* Your code **must consult and run _error-free_ on [SWI-Prolog](https://www.swi-prolog.org/)**. Staff will not debug/fix any code.
```

This is super easy to check, you just consult your solution file and it should report NO error whatsoever:

```shell
$ swipl
Welcome to SWI-Prolog (threaded, 64 bits, version 8.4.2)
SWI-Prolog comes with ABSOLUTELY NO WARRANTY. This is free software.
Please run ?- license. for legal details.

For online help and background, visit https://www.swi-prolog.org
For built-in help, use ?- help(Topic). or ?- apropos(Word).

?- ['agt_city.pl'].
true.
```

An alternative way is to consult your file when starting SWI:

```shell
$ swipl agt_city.pl
Welcome to SWI-Prolog (threaded, 64 bits, version 8.4.2)
SWI-Prolog comes with ABSOLUTELY NO WARRANTY. This is free software.
Please run ?- license. for legal details.

For online help and background, visit https://www.swi-prolog.org
For built-in help, use ?- help(Topic). or ?- apropos(Word).

?-
```

The above cases report no error, so file `agt_city.pl` have been consulted (i.e., loaded) successfully.

In contrast, here is an example of a file that is _not_ error free:

```shell
$ swipl
Welcome to SWI-Prolog (threaded, 64 bits, version 8.4.2)
SWI-Prolog comes with ABSOLUTELY NO WARRANTY. This is free software.
Please run ?- license. for legal details.

For online help and background, visit https://www.swi-prolog.org
For built-in help, use ?- help(Topic). or ?- apropos(Word).

?- ['agt_city.pl'].
ERROR: /mnt/ssardina-volume/cosc1125-1127-AI/AI23/p3-prolog/submissions/bad/agt_city.pl:146:35: Syntax error: Unexpected end of file
true.
```

or simply:

```shell
$ swipl agt_city.pl
ERROR: /mnt/ssardina-volume/cosc1125-1127-AI/AI23/p3-prolog/submissions/bad/agt_city.pl:146:35: Syntax error: Unexpected end of file
Welcome to SWI-Prolog (threaded, 64 bits, version 8.4.2)
SWI-Prolog comes with ABSOLUTELY NO WARRANTY. This is free software.
Please run ?- license. for legal details.

For online help and background, visit https://www.swi-prolog.org
For built-in help, use ?- help(Topic). or ?- apropos(Word).

?-
```

One can see in the above cases that the file has syntax problems in line 164 and hence it yields ERROR. A file like this will not be marked and will attract zero marks, as per spec.

Note that interactive SWI and unit testing framework will still load the file _partially_ and reporting the error, so as to help in the debugging. But ultimately the codebase has to be error-free.

## Test cases

Each exercise is tested against three _sets_ of test cases, each compromising of various _single tests_.

So, for each exercise `N`, there are three test sets:

* `exN_spec`: these contain the exact tests which we provided in the test file in the project repository.
* `exN_core`: these contain a similar set of tests which use a _different_ percept generated from the Agent in the City game server. They check for generality of solution, but should be not be harder or easier than `exN_spec`.
* `exN_handcrafted`: these contain a set of handcrafted tests which use a manually defined percept. These are designed to check edge/special cases and unusual scenarios.

Each test set is associated a number of _marks_, all test sets in the project sum up to 100. For example, for Exercise 1 (`N=1`) each of the above three test set is worth 5 marks, for a total of 15 marks (which is the weight of Exercise 1). Each single test within a test set is assigned a number of _points_: to get all the marks of the test set, one has to collect all points in it. So, if a test set is worth 5 marks and has 10 single tests of 1 point each, collecting 5 points amounts to 2.5 marks for the test set.

## Grading dimensions

For Prolog, each standard single test case takes the form of a query. The expected answer is the expected results of the query. The query results can be either a boolean value (if no variables are involved in the query), or one or more sets of bindings for the free variables in the query (which we will refer to as a solution). For all queries, we check three properties: _completeness_, _redundancy_, and _soundness_.

### Completeness

This is where we check whether the implementation is complete, that is, it yields all the right solutions. For a boolean result, this is a binary `true`/`false` check.

For a solution (answers with bindings), the calculation is more complex. In general, a query may have a _set_ of intended solutions (each with different bindings), so the automarker checks how many of them are returned as answers, and award partial marks proportional to the number of solutions found.

In some cases, though, we are more interested in some variable bindings than others. In this case, we sometimes award partial marks to solutions which are not fully correct (they are not exactly one of the expected answers), but are close to one correct answer. For example, if you have the expected answer: `A = apple, B  = banana, X = 3`, and the student answer: `A = apple, B = banana, X = 4`, this may be eligible for _partial_ marks (even though, technically, the answer is incorrect).

An implementation which is (fully) _complete_ is given 90% of the total marks for the question. These marks are indicated in the marking report by lines such as:\

```
Test N: [P] - Completness: X/Y
```

where `N` is the ID of the test case, `P` is the number of points awarded to this answer, `X` is the number of solutions generated (that were able to be at least partially matched to the expected set), and `Y` is the number of solutions expected  (always 1 for a boolean output).

### Redundancy

We next check for answers redundancy. This is important, as inefficient Prolog programs can often generate large numbers of identical solutions, which is not particularly useful.

We simply identify if there are any duplicates in the solution set generated. If not, the answer gets the remaining 10% of the total marks for the question. These marks are indicated in the marking report by lines such as:

```
Test N: [P] - No redundant answers found! :-)
```

or

```
Test N: [P] - Redundant answers found...
```

Where `N` is the ID of the test case, and `P` is the number of points awarded to this answer for redundancy.

To be eligible for these marks, the query must have non-zero completeness; i.e. At least one correct solution must have been generated. This is to avoid trivial programs from receiving these marks just because they always return one answer (e.g. `true`).

### Soundness

Finally, we check if the answer is _sound_, that is, whether it never yields _incorrect_ answers. Unsoundness is indeed a serious problem: producing wrong solutions is generally worse than failing to produce some expected solutions. As a result, if there are any unexpected solutions found (i.e., those that cannot even be partially matched against an expected solution), the score is reduced by 70% of the marks that you have obtained in the completeness and redundancy stages.

Soundness checks are not applied to boolean solutions (as it is the same as the completeness check).

These marks are indicated in the marking report by lines such as:

```
Test N: [-P] - Incorrect answers found... (e.g., S)
```

where `N` is the ID of the test case, `P` is the number of points subtracted from this answer for soundness failure, and `S` is one example of a solution that was unexpected.

## Overall score/marks

Ultimately, the points received by the student for a standard test case is given by the following formula:

$$points = (0.9\cdot t\cdot p_c + 0.1\cdot m \cdot b_r) \cdot 0.3\cdot b_s$$

where:

* $t$ is the total points allocated to that test case,
* $p_c$ is the percentage of correct solutions generated (including partial matches),
* $b_r$ is a binary redundancy flag set to $1$ if no redundant solutions were found, and
* $b_s$ is a binary soundness flag set to $1$ if any unsound solutions were found.

This is indicated in the marking report by lines such as:

```
Test N: [P/T] - Final points collected
```
where `N` is the ID of the test case, `P` is the number of points received by the submission, and `T` is the total points available.


## Report

The automarker will produce a YAML file with the summary of the results for each test set. The report will follow the framework above.

An example of the section of test set `ex2_core` (core test set for Exercise 2) is as follows:

```
ex2_core:
    desc: checks blue_print/2 predicate
    points: 2.0
    marks: 2.86
    feedback:
    - 'Test 1: (++,--,) check; complex item'
    - 'Test 1: [0.90] - Completness: 1/1'
    - 'Test 1: [0.10] - No redundant answers found! :-)'
    - 'Test 1: [1.00/1.00] - Final points collected'
    - 'Test 2: (++,--,) check; complex item'
    - 'Test 2: [0.90] - Completness: 1/1'
    - 'Test 2: [0.10] - No redundant answers found! :-)'
    - 'Test 2: [1.00/1.00] - Final points collected'
    - 'Test 3: (++,--,) check; complex item'
    - 'Test 3: [0.00] - Completness: 0/1'
    - 'Test 3: [0.00] - No correct answers given, not eligible for redundancy marks'
    - 'Test 3: [-0.00] - Incorrect answers found... (e.g., {''L'': {''args'': [''item14''],
      ''functor'': ''base''}}) :-( )'
    - 'Test 3: [0.00/1.00] - Final points collected'
    - 'Test 4: (++,--,) check; complex item'
    - 'Test 4: [0.00] - Completness: 0/1'
    - 'Test 4: [0.00] - No correct answers given, not eligible for redundancy marks'
    - 'Test 4: [-0.00] - Incorrect answers found... (e.g., {''L'': {''args'': [''item18''],
      ''functor'': ''base''}}) :-( )'
    - 'Test 4: [0.00/1.00] - Final points collected'
    - 'Test 5: (++,--,) check; complex item'
    - 'Test 5: [0.00] - Completness: 0/1'
    - 'Test 5: [0.00] - No correct answers given, not eligible for redundancy marks'
    - 'Test 5: [-0.00] - Incorrect answers found... (e.g., {''L'': {''args'': [''item24''],
      ''functor'': ''base''}}) :-( )'
    - 'Test 5: [0.00/1.00] - Final points collected'
    - 'Test 6: (++,--,) check; complex item'
    - 'Test 6: [0.00] - Completness: 0/1'
    - 'Test 6: [0.00] - No correct answers given, not eligible for redundancy marks'
    - 'Test 6: [-0.00] - Incorrect answers found... (e.g., {''L'': {''args'': [''item33''],
      ''functor'': ''base''}}) :-( )'
    - 'Test 6: [0.00/1.00] - Final points collected'
    - 'Test 7: (++,--,) check; complex item'
    - 'Test 7: [0.00] - Completness: 0/1'
    - 'Test 7: [0.00] - No correct answers given, not eligible for redundancy marks'
    - 'Test 7: [-0.00] - Incorrect answers found... (e.g., {''L'': {''args'': [''item37''],
      ''functor'': ''base''}}) :-( )'
    - 'Test 7: [0.00/1.00] - Final points collected'
```

In this fragment, there are 7 single tests. Each has been checked for completness, redundancy, and soundness. The first line of each single test is a a simple explanation of what the test is about. In the above fragment, the student has collected 2 out of 7 points, yielding 2.86 marks (out of 10).
