# 100 Days Of Code - Log - Tommy Williams

[@twwilliams on Twitter](https://twitter.com/twwilliams) |
[@twwilliams on GitHub](https://github.com/twwilliams) |
[LinkedIn](https://www.linkedin.com/in/twwilliams/)

## Day 12: 18 February 2018

### Today's Progress

- *[30 min]* Investigated options for REST services for currency conversions,
  command-line parsing libraries (they're all so complicated in C# compared to
  Python and JavaScript), and trying to avoid writing my own filesystem cache
  for the values (but, again, the available options are all incredibly heavy-
  weight.)
- *[40 min]* Start a basic persistance class to store data from the Web service
  in a file and only update it once a day.

### Thoughts

- One of the big problems that .NET Core is going to face is how complicated
  the available packages are compared to what Ruby, Python, Node.js, and other
  devs on Unix-based systems are used to. I mean, sure, when your needs are
  complicated, it's good to have a tool that can operate there, but there's a
  **huge** complexity gap between rolling everything yourself out of the BCL to
  what's available from the community.
- There's also a giant documentation gap. I've been looking at command-line
  argument parsing libraries for .NET today and have been appalled at how
  weakly they are documented compared to options for Python. Even where I can
  find some sort of getting started examples, they're poorly done and not nearly
  complete enough. Once I select a library to use regularly myself, I'm going to
  submit some pull requests to make the docs better.

### Learned or Discovered

### Link to work

---

## Day 11: 16 February 2018

### Today's Progress

- *[60 min+]* Experimented with a few different forms of pure Dependency
  Injection (no IoC container) and tried to simplify down to examples that could
  be easily understood. Still need to do more work on this.

### Thoughts

### Learned or Discovered

### Link to work

---

## Day 10: 15 February 2018

### Today's Progress

- *[10 min]* Created simple example of basic uses of ref and out parameters
  based on Twitter conversation.
- *[5 min]* Updated to show that while C# passes by value by default, the value
  that is passed with a reference type (like a custom class) is the reference,
  not a deep copy of the object.
- *[60 min]* Went through a bunch of edge cases with built-in C# types with some
  programs written in LINQPad. Not real projects but cemented (for a while,
  anyway) a much more solid understanding of some aspects of C# that I have
  always just glossed over and taken for granted. It's kind of tedious at times
  but worth what I have learned.
- *[5 min]* Updated gist **again** to show what happens with ref params and
  reference types.

### Thoughts

- Biggest takeaway about ref vs. out params, to me, is the idea that with a
  `ref` param, you can pass information out of **and** into a function via the
  parameter. With an `out` param, you can only get information out of the
  function. Hence the name.

### Learned or Discovered

### Link to work

- [Condensed example of basics of ref and out parameters](https://gist.github.com/twwilliams/ebfc12fdde6385eb496e29a584a6dc28)

---

## Day 9: 14 February 2018

### Today's Progress

- *[20 min]* Bit more project housekeeping and basic JSON processing in Holidays
- *[50 min]* More challenges in the ASP.NET course

### Thoughts

### Learned or Discovered

### Link to work

- [Holidays](https://github.com/twwilliams/Holidays)

---

## Day 8: 13 February 2018

### Today's Progress

- *[30 min]* Created a "Hello world" Azure Function in C# and changed it to
  return the response as JSON instead of XML.
- *[10 min]* Looked into REST services to get holidays for a little app to tell me
  how many days until the next holidays in the year. Unfortunately, they're all
  pay services (for future data) and the rates are pretty large, so I'm just
  going to build it with a local JSON file until I find a better alternative.
- *[10 min]* Created JSON file with holidays for 2018 in Montana.
- *[15 min]* Wrote basic code to read file and then fought with VS and .NET Core
  2.0 to produce a stupid damned console EXE and there doesn't appear to be any
  way to get the Publish profile to do that. I only get a choice of a Portable
  application. .NET Core 2.0 continues to be nothing but a pain in the ass every
  time I try to use it. Just a huge waste time.
- *[5 min]* Finally figured out I need to edit the .csproj file directly and add
  a `<RuntimeIdentifier>win10-x64</RuntimeIdentifier>` tag, then create a Publish
  profile that uses that identifier. But it generates a directory with 216 files
  that is nearly 63MB. This continues to be just crazy. Or, if I'm willing to
  call my app with `dotnet path\to\my.dll` to run it, I only need 13 files and
  1MB on disk. Ugh.

### Thoughts

### Learned or Discovered

### Link to work

---

## Day 7: 12 February 2018

### Today's Progress

- *[40 min]* Implemented a demonstration of using a DateTime2 column in SQL
  Server and querying it with SqlClient using the naive approach, which ends up
  truncating data, then created a `SqlParameter` with SqlDbType of
  `SqlDbType.DateTime2`. Had to be sure to use a date earlier than 1773 to show
  the effect. See
  https://docs.microsoft.com/en-us/dotnet/framework/data/adonet/sql/date-and-time-data#datetime2-example
- *[20 min]* Added remaining tests from PromptIntegerTests to
  PromptDecimalTests (and renamed the class and file from PromptDigitalTests--
  that was a typo from when I was trying to solve the parallel classes problem).

### Thoughts

- Wondering how important it is to know how to manually work with data structures
  linked lists and binary trees when environments like .NET already have great
  implementations. Or where there are packages with well-tested implementations
  in the rare cases that there isn't one in the box. Case in point:
  [SortedDictionary](https://docs.microsoft.com/en-us/dotnet/api/system.collections.generic.sorteddictionary-2?view=netframework-4.7.1)
  instead of building your own binary tree from scratch. You still get O(log N)
  performance on searches and inserts and you know it's been tested a **lot**
  more than code you write on your own.
- I think knowing design patterns--and, particularly, when and how to use them--
  is a lot more valuable.

### Learned or Discovered

### Link to work

- [ConsoleEx](https://github.com/twwilliams/ConsoleEx)

---

## Day 6: 11 February 2018

### Today's Progress

- *[15 min]* Radio Button Challenge from DevU C# Fundamentals course. Most of
  that spent watching the video to get the requirements of the challenge.
- *[45 min]* Papa Bob's Pizza Challenge from DevU C# Fundamentals course. Took a
  while to get all the buttons and special formatting set up. Code is messy
  because I'm trying not to use stuff we haven't covered in the course yet. But
  I couldn't help myself and I created a `[Flags] Enum` for the toppings and
  used `Enum.HasFlag()` to handle the special deal.

### Thoughts

### Learned or Discovered

- Figured out that I could keep IIS Express up between builds by disabling
  "Edit and Continue" in the project properties. That way, I can use Ctrl+F5 to
  start **without** debugging. That makes it much faster when iterating on a
  Web Forms project.

### Link to work

- [Papa Bobs Pizza Challenge](https://github.com/twwilliams/Challenges.PapaBobsPizza)

---

## Day 5: 10 February 2018

### Today's Progress

- [15 min] Discovered the source of the bug from last night and refactored the
  tests back into separate classes. Also hit the VS bug below for sure and
  verified the workaround for me and tweeted about it.
- [60 min] Played around with ASP.NET Web Forms just for the nostalgia of it. I
  had forgotten how much I remembered about it. Nothing uploaded since I was
  just playing with all the toolbox items and seeing the code that was rendered
  and changing it up both in code and with VS properties. I had honestly
  forgotten that this is the way we used to build Web sites with ASP.NET.
- [20 min] Complete a simple calculator challenge in the DevU C# Fundamentals
  with ASP.NET course. Doing stuff with the WebForms designer is so incredibly
  tedious, and yet it is also discoverable. Had to try hard not to use language
  features I know how to use that haven't already been discussed in the course.

### Thoughts

- Turns out the problem from last night was due to XUnit running separate
  classes in parallel and hitting a problem with my test code not being
  thread-safe. Fixed by putting both classes into the same XUnit collection:
  [Running Tests in Parallel](https://xunit.github.io/docs/running-tests-in-parallel.html)
- Found [an answer on StackOverflow](https://stackoverflow.com/a/29325370/240398)
  that roughly describes the process of making these calls to `Console.SetIn()`
  and `Console.SetOut()` thread safe. Might be a nice exercise to implement.
- Or, I could change my approach and just mock the Console class. It would give
  me a chance to choose and learn a mocking framework--there are just so many
  from which to choose.
- I am hitting the
  [bug in VS 2017 15.5.*](https://developercommunity.visualstudio.com/content/problem/158160/unable-to-fetch-source-information-for-test-method.html)
  with Dotnet Extensions for Test Explorer

### Investigations

- [How to mock a `System.Console` dependency](https://stackoverflow.com/a/13406010/240398)
- [C# Fundamentals Via ASP.NET Web Applications](https://devu.com/courses/cs-fundamentals-via-asp-net-web-applications/lessons/cs-asp-003-building-your-first-web-app)

### Link to work

- [ConsoleEx](https://github.com/twwilliams/ConsoleEx)

---

## Day 4: 09 February 2018

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

- [ConsoleEx](https://github.com/twwilliams/ConsoleEx)

---

## Day 3: 08 February 2018

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

## Day 2: 07 February 2018

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

## Day 1: 06 February 2018

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
