0x06. Regular expression
Resources📚
Read or watch:

Regular expressions - info
Regular expressions - basics
Regular expressions - advanced
Rubular is your best friend
Use a regular expression against a problem: now you have 2 problems
Learn Regular Expressions with simple, interactive exercises
Learning Objectives💡
For this project, you have to build your regular expression using Oniguruma, a regular expression library that which is used by Ruby by default. Note that other regular expression libraries sometimes have different properties.

Because the focus of this exercise is to play with regular expressions (regex), here is the Ruby code that you should use, just replace the regexp part, meaning the code in between the //:

#!/usr/bin/env ruby
puts ARGV[0].scan(/127.0.0.[0-9]/).join
0. Simply matching Holberton
Requirements:

The regular expression must match Holberton

Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

1. Repetition Token #0
Requirements:

Find the regular expression that will match the above cases

Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

2. Repetition Token #1
Requirements:

Find the regular expression that will match the above cases

Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

3. Repetition Token #2
Requirements:

Find the regular expression that will match the above cases

Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

4. Repetition Token #3
Requirements:

Find the regular expression that will match the above cases

Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

5. Not quite HBTN yet
Requirements:

The regular expression must be exactly matching a string that starts with h ends with n and can have any single character in between

Using the project instructions, create a Ruby script that accepts one argument and pass it to a regular expression matching method

6. Call me maybe
This task is brought to you by Holberton mentor Neha Jain, Senior Software Engineer at LinkedIn.

Requirement:

The regular expression must match a 10 digit phone number

7. OMG WHY ARE YOU SHOUTING?
Requirement:
The regular expression must be only matching: capital letters
8. Textme
This exercise was prepared for you by Guillaume Plessis, VP of Infrastructure at TextMe. It is something he uses daily. You can thank Guillaume for his project on Twitter.
For this task, you’ll be taking over Guillaume’s responsibilities: one afternoon, a TextMe VoIP Engineer comes to you and explains she wants to run some statistics on the TextMe app text messages transactions.

Requirements:

Your script should output: [SENDER],[RECEIVER],[FLAGS]

   The sender phone number or name (including country code if present)
   The receiver phone number or name (including country code if present)
   The flags that were used
You can find a log file here.

Example:

$ ./100-textme.rb 'Feb 1 11:00:00 ip-10-0-0-11 mdr: 2016-02-01 11:00:00 Receive SMS [SMSC:SYBASE1] [SVC:] [ACT:] [BINF:] [FID:] [from:Google] [to:+16474951758] [flags:-1:0:-1:0:-1] [msg:127:This planet has - or rather had - a problem, which was this: most of the people on it were unhappy for pretty much of the time.] [udh:0:]'
Google,+16474951758,-1:0:-1:0:-1
$
$
$ ./100-textme.rb 'Feb 1 11:00:00 ip-10-0-64-10 mdr: 2016-02-01 11:00:00 Receive SMS [SMSC:SYBASE2] [SVC:] [ACT:] [BINF:] [FID:] [from:+17272713208] [to:+19172319348] [flags:-1:0:-1:0:-1] [msg:136:Orbiting this at a distance of roughly ninety-two million miles is an utterly insignificant little blue green planet whose ape-descended] [udh:0:]'
+17272713208,+19172319348,-1:0:-1:0:-1
$
$ ./100-textme.rb 'Feb 1 11:00:00 ip-10-0-64-11 mdr: 2016-02-01 11:00:00 Sent SMS [SMSC:SYBASE1] [SVC:backendtextme] [ACT:] [BINF:] [FID:] [from:18572406905] [to:14022180266] [flags:-1:0:-1:-1:-1] [msg:136:Far out in the uncharted backwaters of the unfashionable end of the western spiral arm of the Galaxy lies a small unregarded yellow sun.] [udh:0:]'
18572406905,14022180266,-1:0:-1:-1:-1
$
$
$ ./100-textme.rb 'Feb 1 11:00:00 ip-10-0-64-11 mdr: 2016-02-01 11:00:00 Sent SMS [SMSC:SYBASE1] [SVC:backendtextme] [ACT:] [BINF:] [FID:] [from:12392190384] [to:19148265919] [flags:-1:0:-1:-1:-1] [msg:99:life forms are so amazingly primitive that they still think digital watches are a pretty neat idea.] [udh:0:]'
12392190384,19148265919,-1:0:-1:-1:-1
$
9. Pass LinkedIn technical interview level0
One way to get started in getting a Software Engineering job at LinkedIn is to solve their regex puzzle.

Requirements:

Solve LinkedIn regex puzzle: https://engineering.linkedin.com/puzzle

Provide as an answer file a screenshot of the “Congratulations” screen with the date and time of completion

Author
Robinson Montes - mecomonteshbtn
