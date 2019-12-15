# httpimp-topdesk

These two tools are created in order to send HTTPrequests in batch to TOPdesk.
Also works on SAAS!


## str-httpimp-topdesk
 
Use this script to send HTTPrequests in batch to TOPdesk
Suitable for sending single strings.
Written by Rogier Visser (Laansloot IT), 15 december 2019.

Usage:
1. Set variables url and user (see below)
2. Set the first part of the HTTPrequest in file str1-card.
3. Set the last part of the HTTPrequest in file str2-string
4. Set the array of variables in file str3-var
5. Run the script. If SAAS, answer Y to question "New architecture? (y/n)"

Example:

str1-card:		branch?status=1&action=edit&lookup=naam&lookupValue=
str2-string:	&field0=website&value0=1234
str3-var:		TOPdesk UK
				TOPdesk Nederland
	

## csv-httpimp-topdesk
 
Use this script to send HTTPrequests in batch to TOPdesk
Suitable for sending complex strings, based on a csv source file.
Written by Rogier Visser (Laansloot IT), 15 december 2019.

Usage:
1. Set variables url and user (see below)
2. Set the first part of the HTTPrequest in file csv1-card.
3. Csv-file with headers is file csv2-source.
4. Refer to linked tables in the header with / (for example vestigingid/naam)
5. Run the script. If SAAS, answer Y to question "New architecture? (y/n)"

Example:

csv1-card:		branch?status=1&action=
csv2-source:	naam;debiteurennummer;vrijeopzoek1/naam
				TOPdesk UK;1;1 - Lineair
				TOPdesk Nederland;2;1 - Lineair
