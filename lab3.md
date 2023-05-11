# Lab Report 3  
  
## grep examples:

1) using the -r option to search recursively within a directory. Found with ChatGPT
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
  
2) using -v option to inverse-search, which will exclude any phrase I want and print the rest to the terminal. Found with ChatGPT
```
$ grep -v "a" technical/plos/journal.pbio.0020001.txt





        serious problems not only for the scientific community in the developing countries, but for






        2002).








        regions.
        In
        However, publishing in


        world.




        built.



```
  
Here I used '^$' to get rid of all the empty lines: (Source: ChatGPT)
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
  
3) using -A num option to get num amount of lines after the matching phrase. Found with ChatGPT
```
$ grep -A 3 "criminal" technical/government/Media/Advocate_for_Poor.txt 
landlord-tenant disputes and even criminal cases are the specialty
of his East New York Legal Services Corp. on New Lots Ave.
The office, in a former bodega, was Mazzariello's idea, and he
got some help from high places early on.
```
  
```
$ grep -A 2 "children" technical/government/Media/A_helping_hand.txt 
affects children. Mintie noticed that health-care professionals
were graduating with staggering debts and also couldn't afford to
work with the poor.
```
  
4) using -i to ignore case. Found with ChatGPT
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

```
$ grep -i "foundation" technical/911report/chapter-2.txt
            THE FOUNDATION OF THE NEW TERRORISM
                allowed to dissolve. They established what they called a base or foundation (al
                Foundation in Sarajevo, which supported the Bosnian Muslims in their conflict with
```
