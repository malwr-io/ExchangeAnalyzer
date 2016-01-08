#Exchange Analyzer

Exchange Analyzer is a PowerShell tool that scans an Exchange Server 2013 or 2016 organization and reports on compliance with best practices.

Exchange Analyzer is a community project, and is currently a beta release seeking feedback and results from real world environments.


###Table of Contents

- [Background and Purpose](#background-and-purpose)
- [Installing Exchange Analyzer](#installing-exchange-analyzer)
- [Running Exchange Analyzer](#running-exchange-analyzer)
- [Exchange Analyzer Output](#exchange-analyzer-output)
- [Wiki Home Page](https://github.com/cunninghamp/ExchangeAnalyzer/wiki)
	- [Exchange Analyzer Tests](https://github.com/cunninghamp/ExchangeAnalyzer/wiki/Exchange-Analyzer-Tests)
	- [Draft Tests](https://github.com/cunninghamp/ExchangeAnalyzer/wiki/Draft-Tests)
	- [Development Overview](https://github.com/cunninghamp/ExchangeAnalyzer/wiki/Development-Overview)
	- [How to Contribute](https://github.com/cunninghamp/ExchangeAnalyzer/wiki/How-to-Contribute)
- [Credits](#credits)
- [License](#license)

##Background and Purpose

Historically, Microsoft has provided tools to scan an Exchange Server organization to check its configuration against known "Best Practices". Exchange 2007 and 2010 included these Best Practice Analyzers (BPA) within the the server software itself, while Exchange 2013's version was shipped externally.

For more information on the previous versions of BPA see the links below:

* [Exchange 2010 BPA](http://blogs.technet.com/b/exchange/archive/2010/07/28/3410533.aspx) 
* [Exchange 2013 BPA](http://blogs.technet.com/b/exchange/archive/2013/10/01/beta-of-microsoft-office-365-best-practices-analyzer-for-exchange-server-2013-now-available.aspx)

The Exchange 2013 BPA requires an Office 365 tenant or Azure AD login, and remains in a Beta state. Exchange 2016 was released in early October 2015 and does not yet have a BPA. The Exchange Analyzer tool serves to fill the void by providing an on-premises best practices analyzer that is developed and maintained by the community.

The Exchange Analyzer tool scans your Exchange Server 2013/2016 organization and evaluates it for compliance with both the [Preferred Architecture](http://blogs.technet.com/b/exchange/archive/2015/10/12/the-exchange-2016-preferred-architecture.aspx) (Microsoft's high-level design recommendations) as well as various recommended practices from the Microsoft MVP and MCM community.

##Installing Exchange Analyzer

Exchange Analyzer consists of a series of PowerShell scripts, PowerShell modules, and XML data files. Installation is performed manually using the following steps.

1. Copy the following files and folders to a computer that has the Exchange 2013/2016 management shell installed. For example, place all of the files and folders in a C:\Scripts\ExchangeAnalyzer folder.

	- Run-ExchangeAnalyzer.ps1
	- Data
	- Modules
	- Tests

2. Copy the folders in the Modules folder to C:\Windows\System32\WindowsPowerShell\v1.0\Modules\
3. Open a new Exchange Management Shell console.

##Running Exchange Analyzer

To run the Exchange Analyzer open an Exchange management shell, navigate to the folder with the script files (e.g. C:\Scripts\ExchangeAnalyzer) and run:

```
.\Run-ExchangeAnalyzer.ps1
```

To see verbose output run:

```
.\Run-ExchangeAnalyzer.ps1 -Verbose
```

##Exchange Analyzer Output

Internet Explorer will automatically open the HTML report when the script has finished. THe report contains information about the tests that were performed, and their results (such as "Passed" or "Failed"). Links to more information is provided for most tests.

![Exchange Analyzer Sample Report](https://github.com/cunninghamp/ExchangeAnalyzer/blob/master/Examples/exchange-analyzer-example-report-01.png)

##Credits

- Paul Cunningham ([Blog](http://exchangeserverpro.com) | [Github](https://github.com/cunninghamp) | [Twitter](https://twitter.com/exchservpro))
- Mike Crowley
- Michael B Smith
- Brian Desmond
- Damian Scoles

##License

Exchange Analyzer is released under the MIT license (MIT). Full text of the license is available [here](https://github.com/cunninghamp/ExchangeAnalyzer/blob/master/LICENSE).