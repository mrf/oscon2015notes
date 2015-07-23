# Speeding up the web with PHP 7
- Some Rasmus dude, seems to know a lot about PHP
- Original Intention "A C api for the web"
  - Turns out people are lazy and wanted to do everything in the templating language
- Symlink prod /var/www/a /var/www/b swap case, shared opcache php8 figures it out
- Most fatals turned to exceptions!! Finally! But have to remember to litter your code with try/catch
- A lot of PHP4 stuff finally dropped completely so be hesitant about upgrading really old code


# You Code Like A Sysadmin
- Imposter Syndrome
- Started out in middle of nowhere with little access to tech
- Went to college not ready to come head to head with tech
- A Turbo Pascal class later with a dash of C, thought he'd never be a programmer
  - Got picked to write the docs for his OS class
- Long story short, he became a sysadmin
  - picked up perl and shell scripting
- Wrote a really long perl hell comedy sports troup app
  - BUT it works and people still use it 10 years later
- BUT all the sudden a windows sysadmin job becomes a rails dev job
  - ended up writing a lot of small tools to solve internal needs
    - because nature abhors a vacuum

- Standards for being GOOD are really really high
- Why to keep building with such high standards if you know / think you suck?
- What if code is means, not the end
- If code ends up being useful you'll get a chance to fix it
- If you prematurely optimize it you'll never ship it
- Unwritten code helps no one
- But wait, if you have the ability USE IT
- Good code better than bad code bad code better than no code
- Decide who you want to listen to, users or haters


# Stope Writing Javascript Frameworks
- Google guy, will mostly only make fun of google supported frameworks
- follow up to his blog post of the same name
  - this ^ created an internet firestorm (yay hacker news!)

- Argument 1 browsers have gotten enough better that you don't need the frameorkw for browser support
- Argument 2 all the other stuff
  - Abstractions are abstract what do they do for you?
- Presentation pro tip: Use kids to draw pictures for you

- A few lines of code and you can import JS into any html page
  - HTML becomes your templating language core JS becomes your "framework"
- Custom elements not hard to do in modern browsers
- Whoa all the JS you wanted to write in 2004 now works!
- Not convinced that this doesn't just bloat into a framework per project
  - maybe if everyone writing the js was a google engineer
- Libraries are still ok, but small purposeful libraries, not frameworks
- https://gist.github.com/jcgregorio/7fa68cdced1181416559
- https://github.com/polymer


# Reactive Frontend
- Not about Functional Reactive Programming
- why go functional?
 - because immutable state which aligns well with parallelism
 - no side effects, impossible if it done properly and only ever supposed to do 1 thing
 - but its possible to have too much of a good thing
 - too much array map filter reduce == explosion
 - solution =https://github.com/Reactive-Extensions/RxJS observables
    - observables a streamed collection of all events over time
    - simply a pattern to start a stream emit messages tear down stream
