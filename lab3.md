# Lab Report 3  

  note: all commands were found with ChatGPT, this lab report includes a section at the bottom containing all input and output to ChatGPT used.
## grep examples:

1) using the `grep -r <String> <path to directory>` command to search recursively within a directory. Found with ChatGPT  
- this command looks through a whole directory and get all files that contain the String you searched for, then for each file, gives the line of text where the String appeared on.  
- If you don't know what files contain a certain String in a directory, this will be useful to find which files have that String. Additionally, if you are looking for a particular file and only remember one String from it, this command gives you all the files that match the String, and the line that they appear on for context.
```
$ grep -r "strategy" technical/government/About_LSC
technical/government/About_LSC/commission_report.txt:is a survival strategy, permitting them to survive their periods of
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:most difficult part of our strategy to move our grantees into new
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:most attention (both good and bad)-is the State Planning strategy
technical/government/About_LSC/ONTARIO_LEGAL_AID_SERIES.txt:"most important strategy".
technical/government/About_LSC/Progress_report.txt:experts on evaluations will create a national evaluation strategy
technical/government/About_LSC/State_Planning_Report.txt:the primary strategy for achieving these goals. In December 2000,
technical/government/About_LSC/State_Planning_Report.txt:public communications strategy and a grassroots support network.
technical/government/About_LSC/State_Planning_Report.txt:community legal education strategy;
technical/government/About_LSC/State_Planning_Report.txt:and a multiyear strategy to help the public understand their rights
technical/government/About_LSC/State_Planning_Report.txt:part of a coordinated web information delivery strategy involving
technical/government/About_LSC/Strategic_report.txt:document as LSC's key strategy to achieve the goals stated
technical/government/About_LSC/Strategic_report.txt:strategy for fulfilling the mandate of Strategic Directions
technical/government/About_LSC/Strategic_report.txt:later, in 1998, state planning became a key LSC strategy to achieve
technical/government/About_LSC/Strategic_report.txt:primary strategy for enhancing client access to services. We have
```  
- In the above output, I searched recursively in the technical/government/About_LSC directory to find which files contain the phrase "strategy".
The terminal output is all the files in that directory that contain "strategy", for each file, it gives the line that "strategy" appeared on. If it appeared multiple times in one file, it repeats the file name and gives the line it appeared on for each instance.
```
$ grep -r "SCI" technical/plos
technical/plos/journal.pbio.0020001.txt:        (SCI). North America and Europe clearly dominate the number of scientific publications
technical/plos/journal.pbio.0020001.txt:        is a statistical bias on the part of the SCI as a bibliometric database, since it
technical/plos/journal.pbio.0020001.txt:        Using the SCI databases produced by the Institute for Scientific Information (ISI), as
technical/plos/journal.pbio.0020001.txt:        picked up by the SCI in relation to the number of scientists in a particular country, also
technical/plos/journal.pbio.0020001.txt:        scientific community? We used SCI 2001 data to examine the proportion of publications in
technical/plos/journal.pbio.0020001.txt:        developed regions are listed by the SCI than similar journals from developing regions
technical/plos/journal.pbio.0020156.txt:        open-access publication, the American Society for Clinical Investigation (ASCI) has since
technical/plos/journal.pbio.0020156.txt:        author charges and other means,” John Hawley, the executive director of the ASCI writes,
```  
- In the above output, I searched recursively in the technical/plos directory to find which files contain the phrase "SCI".
The terminal output is all the files in that directory that contain "strategy", for each file, it gives the line that "strategy" appeared on.  
  
2) using `grep -v <String> <file path>` command to inverse-search, which will exclude any phrase I want and print the rest to the terminal. Found with ChatGPT
- this command returns all the lines from the file that don't contain a particular phrase, including blank lines. 
- It could be useful, if for example, I have a file with some data on different college majors and I wanted to examine data on all majors except for CSE majors. I could use `grep -v` to return all data except for CSE major data. (note: '>' used to indicate empty line due to markdown to html issues).
```
$ grep -v "a" technical/plos/journal.pbio.0020001.txt
>
>
>
>
>
serious problems not only for the scientific community in the developing countries, but for
>
>
>
>
>
>
2002).
>
>
>
>
>
>
>
>
regions.
In
However, publishing in
>
>
world.
>
>
>
>
built.
>
>
>
```  
- in the above output, I used the -v option to exclude all lines of text with "a" in the file, technical/plos/journal.pbio.0020001.txt.
It returned all the lines without "a".
```
$ grep -v '^$' technical/government/Media/5_Legal_Groups.txt 
5 Legal Groups at 1 Locale To Serve the February 3, 2002
Vulnerable
Salt Lake City Tribune
BY EDWARD MCDONOUGH
Five independent Salt Lake organizations that provide legal
services to the poor, ethnic minorities, seniors and people with
disabilities have joined together to acquire a west-side downtown
building where they will have their offices. The new Community
Legal Center at 205 N. 400 West is a project of "And Justice for
All," which, until this venture, has been a joint fund-raising
campaign by an alliance of the non-profit providers of free legal
services. "And Justice for All," which solicits donations primarily
from Utah lawyers and foundations, was the first joint fund-raising
campaign of legal services agencies in the country, and the
Community Legal Center is the first joint office project of public
service law groups.
The Legal Aid Society of Salt Lake, the Disability Law Center,
the Multi-Cultural Legal Center, the Senior Lawyer Volunteer
Project and Utah Legal Services will share the new facility, and
last Wednesday their board members were given a tour of the
Community Legal Center hosted by staff members of the five
agencies. All of the agencies can share the same reception area and
client waiting room. The building is close in, across the street
from West High and two blocks from the Gateway. It has its own
parking, something that's hard to find downtown and which has been
a problem for staff as well as clients. Owning and sharing the
building and not paying rent times five will save the non-profit
agencies about $375,000 each year. My assistant, Charity
Christenson, pointed out that the shared facility will also be
efficient for those needing legal services. No longer will a woman
desperate for a protective order, for example, have to run all over
town trying to find the right agency.
After the tour, we found Jaye Olafson at the cookies and
brownies reception on the first floor. Jaye and her husband, Erik,
own Tomax Technologies and were the sellers of the building. Jaye
explained how much of the renovation had been merely uncovering
what was already there. The hardwood floors, wooden ceilings and
brick and stone interior walls were all hidden behind coverings and
old paint. She loves the building, and they only moved out because
the business had outgrown the space. So they renovated the old
Sweet Candy Company building for Tomax. The Olafsons are delighted
with the new owners. The building had been like home, she
explained, and so it was important who would be living there. I
noted on the donor list that the couple, through Olafson Group, had
become one of the major supporters of the project.
Stewart Ralphs, the executive director of the Legal Aid Society,
explained that the Community Legal Center Campaign still has a long
ways to go, with a bit more than half of the $4 million projected
cost received so far. There still needed to be furnishings and
office equipment and such. He promised that they would be getting
in touch with us later on the subject.
```  
- in the above output, I used `'^$'` to get rid of all the empty lines: (Source: ChatGPT). I used the inverse searach on technical/government/Media/5_Legal_Groups.txt and it returned all the lines excluding the empty lines.  
  
3) using `grep -A <num> <String> <File path>` command to get num amount of lines after the matching String. Found with ChatGPT
- this could be useful when searching a long text file for information on a topic. For example, if I had a book as a text file, and I wanted to quickly look for a the definition of a term, but the difinition is more than one line long, I can use `grep -A 4` to get the whole definition (with a bigger number if the definition was longer than 4 lines).
```
$ grep -A 3 "criminal" technical/government/Media/Advocate_for_Poor.txt 
landlord-tenant disputes and even criminal cases are the specialty
of his East New York Legal Services Corp. on New Lots Ave.
The office, in a former bodega, was Mazzariello's idea, and he
got some help from high places early on.
```  
- In the above output, I searched the technical/government/Media/Advocate_for_Poor.txt file for the word "criminal" and the 3 lines after that, and it outputed the line with "criminal" and the 3 lines after.
```
$ grep -A 2 "children" technical/government/Media/A_helping_hand.txt 
affects children. Mintie noticed that health-care professionals
were graduating with staggering debts and also couldn't afford to
work with the poor.
```  
- In the above output, I searched the technical/government/Media/A_helping_hand.txt file for the word "children" and the 2 lines after that. It outputed the line with "children" and then 2 lines after that.  
  
4) using `grep -i <String> <File path>` to ignore case. Found with ChatGPT
- this is useful to find if a file contians words regardless of case. For example, if I wanted to find where I wrote a specific word, but can't remember if I capitalized it or not, I can use this option to see if a file had the word.
```
$ grep -i "el" technical/government/Media/A_helping_hand.txt
A helping hand for helping hands
Linda Samels Ceballos entered Loyola Law School in Los Angeles
she took a job at the Inner City Law Center in Los Angeles, a firm
... There was no way I could make that payment. I barely make it
only were there fewer attorneys entering the field of poverty law,
Catholic Worker soup kitchen on skid row in Los Angeles. She lived
to the field of poverty law.
Mintie also started to ask questions about the medical field.
Award" from Oprah's Angel Network, a nonprofit organization that
awards money to those who help others. Mintie said that all of the
She is trying to get religious organizations to sponsor
Mintie's religious convictions.
She said she hopes that religious organizations see the link
between their beliefs and her work.
religious community and the work lawyers do for the poor. The work
Uncommon Good has a few religious sponsors, including her
recipients grew up poor and want to give back, while others feel
of $1,200. She works as the head physician at the Los Angeles
two jobs as a physician's assistant and supports his elderly
model for other professions.
-- the closest legal aid office is in El Monte and represents
700,000 poor people throughout the San Fernando, San Gabriel and
Services of Los Angeles County, the legal aid office in El Monte.
```  
- in the output above, I searched for the String "el" and with the ignore case option. Each line in the output contains "el" or "EL" or "El" or "eL".
```
$ grep -i "foundation" technical/911report/chapter-2.txt
            THE FOUNDATION OF THE NEW TERRORISM
                allowed to dissolve. They established what they called a base or foundation (al
                Foundation in Sarajevo, which supported the Bosnian Muslims in their conflict with
```  
- in the output above, I searched for the word "foundation". It returned all lines with "foundation" regardless of case. You can see the first line returned had "FOUNDATION" while the second line had "foundation" and the third had "Foundation".  

## ChatGPT input and output:  
My input: `what does grep do in bash?`  
ChatGPT output:  
```
n Bash, grep is a command-line utility that is used for pattern matching and searching for specific text within files or streams of data. The name "grep" stands for "global regular expression print." It is a powerful tool commonly used in Unix-like operating systems, including Linux.

The basic syntax of grep is as follows:
grep [options] pattern [file...]
Here's a breakdown of the components:

options: Optional flags that modify the behavior of grep. For example, you can use the -i option to perform a case-insensitive search or the -r option to search recursively in directories.
pattern: The regular expression or text pattern you want to search for.
file: Optional parameter specifying the file(s) to search. If not provided, grep reads from standard input (e.g., data piped from another command).
When grep is executed, it reads the input data line by line and searches for matches based on the specified pattern. If a line contains the pattern, grep will print the entire line by default, although there are options to modify the output format.

Here are a few examples to illustrate how grep can be used:

Search for a specific pattern in a file:
grep "apple" fruits.txt
This command searches for the word "apple" in the file fruits.txt and prints all matching lines.

Perform a case-insensitive search:
grep -i "banana" fruits.txt
The -i option ignores case, so this command will match "banana," "Banana," "BANANA," and so on.

Search recursively in files within a directory:
grep -r "keyword" /path/to/directory
The -r option instructs grep to search recursively within all files in the specified directory and its subdirectories for the given keyword.

These are just a few basic examples of what grep can do. It offers a wide range of options and supports complex pattern matching using regular expressions, making it a versatile and powerful tool for searching and filtering text in the Bash shell.
```  
- here I asked ChatGPT to simply tell me what grep does, as a refresher, but it already gave me some useful options `-i` and `-r`, which I decided to use for this lab report.  
  
My input: `can you give me some more useful options for grep`  
ChatGPT output:  
```
Certainly! Here are a few more useful options for the grep command:

-v or --invert-match: This option inverts the match, i.e., it selects lines that do not match the specified pattern. It can be handy when you want to exclude certain lines from the output.

-l or --files-with-matches: This option prints only the names of files that contain at least one match, rather than displaying the matching lines themselves. It is useful when you want to find files that contain a specific pattern without displaying the actual matches.

-c or --count: Instead of printing the matching lines, this option prints only the count of matching lines for each file. It can be helpful when you're interested in the number of occurrences rather than the actual content.

-w or --word-regexp: With this option, grep matches only whole words that match the pattern. It ensures that the pattern is not part of a larger word. For example, searching for -w "cat" will match the word "cat" but not "catch" or "scat".

-A num or --after-context=num: This option displays num lines of context after each match. It can be useful for showing additional lines of context around the matching lines.

-B num or --before-context=num: Similar to -A, this option displays num lines of context before each match.

-C num or --context=num: This option combines -A and -B to display num lines of context both before and after each match.

These are just a few examples of useful options. There are many more available, and you can explore them further by referring to the grep command's documentation or using the man grep command in the terminal to access the manual page for grep.
```  
- here I asked for some more useful options, and ChatGPT gave me a long list. I felt `-A num` and `-v` where the most interesting ones that I didn't remember seeing in class, so I used them for my lab report.  

My input: `what if i want to exclude all empty lines with -v?`  
ChatGPT output:
```
If you want to exclude all empty lines using the -v option in grep, you can use the pattern ^$ to match empty lines. Here's an example:

Let's say we have a file called data.txt with the following contents:

apple
banana

cherry
date


elderberry
To exclude all empty lines from the output, you can use the following grep command:


grep -v '^$' data.txt
The output will be:


apple
banana
cherry
date
elderberry
In this case, the lines containing only whitespace characters or nothing at all (empty lines) are excluded from the output.

The pattern ^$ uses regular expressions to match the start (^) and end ($) of a line with nothing in between, representing an empty line.

By using this pattern with the -v option, grep will select all lines that do not match the empty line pattern, effectively excluding the empty lines from the output.

Note that grep treats empty lines as lines that contain no characters or only whitespace characters.
```
- I used the suggestion from ChatGPT to use the `-v` option and `^$` in order to exclude all empty lines for my second example of `grep -v`. I wanted to do this because the `-v` option might return many empty lines as it did in my first example. So this might be useful in conjunction with any inverse search if you want more consise output. 
- *Of course, I made sure to thank ChatGPT for helping me :)*
