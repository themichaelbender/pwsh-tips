# Tips from the Twitterverse
Here are the reply from the orgin posting on [Twitter](https://twitter.com/MichaelBender/status/1095394513500205056?s=20

@bpkrothgeek
It's far more -v than bash, but typed vars leads to some nice tab compl opts and built in ops (eg: date funcs) in pipelines. Get-Help (man), Get-Command (with globs around a *searchterm*, it's similar to apropos), etc. to help get started. Install the PSReadline module!

@BenDumke
The ADAC was a huge help with user management. Seeing how #PowerShell commands fit together for a single user, made it easier to expand those ideas to manage multiple users.
Also, sample scripts. I've cobbled together pieces of code from multiple sources to build scripts that meet my needs. When you can see how a similar problem is solved or just see how nested If-Then-Else statements are formatted, it's a huge help to understanding.

@AndyKorth
I start my class by getting them into the right mindset to learn PowerShell.  Understanding up front that it will be confusing at first but stick with it and the clouds WILL part and you will be set from then on.  "Learn once, apply everywhere" is a great ROI and pro of PS IMO

@Ehrnst
Now. If we where to talk about modern it pro or ops, I would try to focus on stuff you can do with web apis. Azure management etc. These things are often unknown territory for ops, but if they know a little PS it's quickly known material

@secprentice
[Blacklisted PowerShell commands for Blue Teams](https://github.com/secprentice/PowerShellBlacklist)

@MarkCroloff
What I did early on, and need to get back into the habit of, was running "Get-Help about_ | Get-Random" once a day. 

Gets you comfortable reading the built-in docs and exposes you to some new concepts.

Add in Profile

@MrThomasRayner
select-object (incl. -expandproperty)
get-member
$thing.gettype()
get-command
get-help (-online)

@mobileck
came here to say these things, and add where-object, and focus on about_ in the docs - they are the real guidelines for how to use powershell instead of just what powershell is

@MSAdministrator
Also get-member -Force and i would also add “understanding quotes (single/double)” and also expressions (grouping & invoking). E.g. ($someVar) and $($someVar)

@nclinch
Set-exectionpolicy unrestricted
Get-process |gm

@nakedpowershell
Jeffrey has several videos out called Windows PowerShell Unplugged

@coderomnipotens
-WhatIf is a huge command line PoC help. Also understand piping and object streams, filtering using -Where. And the super awesome aliases: ?{},&{},%{}

@HerbMartin
Use #PowerShell to teach yourself PowerShell: 
help, gcm, gm
Maybe fl, gettype()
I build whole classes around these & REALLY knowing how to  read the results.
Along this line teach the #PowerShell workhorses for DOINGstuff in the pipeline which breaks the string habit some:
Where, ForEach, Select, Sort, ft, & the overlooked Group-Object
Yes, teach that way, but the need Format-List for exploration to supplement the primary Get-Member.
When you get to the pipeline workhorse you explicitly show the problems with Format-Table within scripts etc.
I'm usually starting with admins not programmers who learned solo

@sinclairinator
Pipe everything
Invoke-WebRequest
Start-Job
Format-Table/Format-List
PSCustomObject
@{ }
@( )
Get-Command/Get-Member
ConvertFrom-Json/ConvertTo-Json
[XML]$somexmlstring
Start-Transcript/Stop-Transcript
$someobject | gm

@jeremymurrah
I know it's kind of a cop out, but "CMD /c <some dos command>" has helped people I've worked with. Knowing that they don't have to throw away all their batch files and rewrite them all in Powershell on day one has really helped.

[Registry to PowerShell Converter](https://reg2ps.azurewebsites.net/)

@ctmcisco
"Operators"  "Operators"  "Operators"

@mrhodes
get-help, get-command, get-member
I also start every workshop with “Take a couple of minutes to think about a problem, job or task you have at work, that you repeat all the time and that just chews up time.   Got one?  Is there any reason you can’t automate it?”

@GuyGregory
For those more comfortable with a GUI interface and WinForms dialog boxes, I like to show them an ‘Out-GridView Sandwich™’. e.g. Get-Process | Out-GridView -PassThru | Stop-Process

@SeanPMassey
There is one thing that would have helped me better, and it wasn’t specifically a PowerShell thing. It’s making sure you understand the processes you’re automating and making sure they’re well documented. Including the exceptions.

The second thing is to not worry about making the code elegant and efficient at first. Automate the task first, and then work on refactoring your code to make it elegant. Spend time getting a working product first and then streamline it.

@Jawz_84
I've seen so many great answers! My 2cts: a metaphor i like when explaining the powershell pileline is the fence. Picture movers passing items over a fence. Empty a truck and fill a house. A house has rooms. The receiving mover might be absent (no pipeline input), dumb...

dumb (ValueFromPipeline), or smart (ValuefromPipeLineByPropertyName). Items may come in in labeled boxes, or as loose, unlabeled items. Depending on your mover, your stuff gets moved to the correct room (parameter) or not.
Start with explaining just the fence first, expand later.

@drewjAnderson
Make sure people understand how and why they should only run their shells as an unprivileged user and not Domain/Enterprise Admin...

and how to use a credential object on cmdlets

@mikemaccana
From a Unix background:

  select, where and get-member

Enough to make me genuinely realise this is all just keys and values and I don't need to scrape everything

@RobertoMoir
-WhatIf, giving both new starter and experienced veterans a chance to check their work with confidence.

A reminder that get-whatever is non-destructive, and that -ft / -fl can do great things with output.

@finickyadm
How to make a module - at the end of the beginnings for that “and here’s how you make code once and reuse it.”
How to use Git for code mgmt.
How to implement and manage jobs for parallel processing - because ain’t no one got time for serial.
How to document code inline.
VSCode.

@vexx32
[PowerShell Koans](https://github.com/vexx32/PSKoans)

@ChrisGardner
I think I'd avoid teaching Format-* except as a warning that it only looks pretty in the console and you shouldn't pass that out to csv or whatever. So many people run into issues because their useful object became format object and then don't become csvs like they expected.

@Jason_Krause_CO
Don't try to learn PowerShell. Try to learn to do your current job using PowerShell.

@AndiKrueger_DE
I think of learning PS like learning woodworking. There’s so much to know from tools to understanding the different types of wood.
Beginners should get familiar with:
1. tools: 
@code
 , source control, ISE
2. Data types & functions
and then start practicing syntax & craftsmanship.

@MSAdministrator
[Let's Automate Blog Post](https://t.co/1uA4SIqWe2)

@SeguraOSD
[PowerShell Verbs at docs.com](https://t.co/tFreYwsx9h)

