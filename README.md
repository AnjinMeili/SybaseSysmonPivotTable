# SybaseSysmonPivotTable
A data engine should never be a black box.  This tool chain shows one way of integrating the engine's metrics with the OS view.
-----------------------
This is an example case of a Sybase server that struggled under load.  As the load increased, its struggles turned to thrashes without a clear cause.  As the various groups pointed fingers, it was only when agile methods were applied to unifying the metrics from Sybase, OS, and Storage that the reasons became clear.  

That's right, I'm saying a pretty picture drawn with all the parts in view saved the day.  With a side benefit of delivering a view of metrics that everyone could play with, from Developers, DBAs, Admins, and Managers.. All could coax useful information from the spreadsheet-based pivot tables.

These parsers take the point-in-time snapshot reports from Sybase and combine them with other point-in-time metrics.  The trick is simply that the Sybase reports are in human readable form, so a lot of filtering is needed to allow them to be combined into a pivottable on time.

I wrote the scripts after a very frustrating day.  It took an evening's work to build a tool that could extract, stack, and build a spreadsheet in one with server side bits which dictionary the data, and macros in Excel to generate the view.  The results were immediate, and we used this tool with continued success for a few years.

In this case, the data shows a table that gets filled faster than it can index.  The data engine's response is full table scans of a fast moving target from that point on.  Shown by graphing reads to writes, tada!  A simple view of data already right in front of you can provide the key.  Having the skill to fold it means more than all the swags taken without it.

James Hutchinson
