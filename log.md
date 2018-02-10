# 100 Days Of Code - Log - Tommy Williams

[@twwilliams on Twitter](https://twitter.com/twwilliams) |
[@twwilliams on GitHub](https://github.com/twwilliams) |
[LinkedIn](https://www.linkedin.com/in/twwilliams/)

## Day 0: 06 February 2018

### Today's Progress

- Figured out how the rules of #100DaysOfCode work and got my cloned repo and
  the log set up.
- Enabled stricter Code Analysis rules and handled warnings.
- Switched from string to enum for number type parameter.

### Learning Activities

- Watched [Vaidehi Joshi](https://dev.to/vaidehijoshi)'s [video on Linked Lists](https://dev.to/vaidehijoshi/linked-lists--basecs-video-series--2le8)
  in the BaseCS Video Series.
    - It is indeed very basic but she also teaches the concepts clearly. I wish
      the video player on dev.to had a way to change the playback speed.

### Thoughts

- Still trying to work out my own style guide. After spending so much time with
  Python this summer and the strict line-length requirements of PEP8, it's
  strange to go back to C# and VS where such constraints were never enforced.
  It's clear that 80 characters is way too short. I tried 90 for a while but
  that feels constrained, too. At the same time, 120 feels like I would just be
  abusing the system, so I'm going to aim at 100 in my C# projects for a while
  and see how that works. Just glad I'm not working with a team as I reformat
  files around these experiments.
- I have always liked enums. I love the extra bit of checking that the editor
  and compiler can do when using enums instead of strings. It does mean changes
  are a bit harder.
- I hate that code analysis rules fight so hard against default parameters. I
  find them so much more intuitive and elegant than a bunch of method overloads.
  [CA1026: Default parameters should not be used](https://docs.microsoft.com/en-us/visualstudio/code-quality/ca1026-default-parameters-should-not-be-used)

### Link to work
[ConsoleEx](https://github.com/twwilliams/ConsoleEx)

---

## Day 1: 07 February 2018

### Today's Progress

- 10 min. Experimented with JotForm API with C# from LINQPad.
- 10 min. Created a VS Code snippet to generate the template for each day's
  entry in this log. Published as
  [a gist](https://gist.github.com/twwilliams/5a4b3716d81e4dab81cc690a2f89a54b).
- 20 min. Created an Airtable database for my wife to use as part of her class.
- 10 min. Refactored integer tests to allow for testing of verbose flag.
- 10 min. Add tests to check for behavior of verbose flag.

### Thoughts

- I should probably just submit a pull request to add the month and day name
  variables but I thought I would at least log it while I investigate how much
  work it would be to create it and submit it.

### Learning Activities

- Looking into the [JotForm API](https://api.jotform.com/docs/) as an option for
  handling game submissions for [GFGR 2018](http://gfgr.org). Would have to pay
  for an account but we could get a non-profit discount. With that API, I could
  enhance my schedule management tool to at least put stuff into place
  conditionally automatically and then I could adjust manually if I needed to.
  Still need a way to check the registration data--but maybe we'll have that if
  we move away from the WordPress-based add-in we have today.

### Link to work

- [Visual Studio Code template for daily log entry](https://gist.github.com/twwilliams/5a4b3716d81e4dab81cc690a2f89a54b)
- No link to the Airtable database: it's private
- [ConsoleEx](https://github.com/twwilliams/ConsoleEx)

---

## Day 2: 08 February 2018

### Today's Progress

- 2 hours+. Set up Bootstrap 4 page, found template, modified it, re-minified
  stuff with gulp, set up private Git repo, and pushed to site.

### Thoughts

- Still need to create a script to copy changed files from repository to live
  site, or at least to another local directory where I can then upload over SFTP.
  I wonder what the scp experience is like on Windows now thanks to WSL.

### Investigations

### Link to work

- https://twwilliams.com

---

## Day 3: 09 February 2018

### Today's Progress

- [5 min] Set up ssh keys for ssh access to twwilliams.com.
- [10 min] Refactor some shared test functions for PromptDecimal tests.
- [40 min] Tried to work around bug in Visual Studio Pro 2017 15.5.6 when I
  have more than one class in my test project.
- [10 min] Add a few more tests and refactor TestFx back to my original design
  since I can't work around this VS bug any other way.
- [20 min] Maybe there's a problem with the way XUnit is handling the Console
  class redirecting I'm doing when there are multiple test classes since this
  problem happens with the XUnit console runner and when I use JetBrains
  Rider. I wanted to avoid mocking the Console class and thought I could make
  redirecting Console.StdIn and Console.StdOut work, but I'm stuck with one
  class and the sense that this is a cargo-cult response since I don't know
  **why** a single class works but multiple classes don't. Running the tests
  through the debugger didn't reveal anything.

### Thoughts

### Investigations

- Discovered [Codela](https://www.codela.io/challenges) and completed a few
  challenges. [LinqPad](https://www.linqpad.net/) is a fantastic tool. And some
  of the challenges are absurdly easy, at least when working in C#, but they
  don't have high success rates. 61% for comparing two strings?
- Looking into the video production gear that
  [mpj (Mattias Petter Johansson)](https://www.youtube.com/watch?v=HnvKQScJ_ho)
  uses. Thinking about doing something for absolute beginners, or even people
  who are interested in software development but have no experience with it.

### Link to work

---
