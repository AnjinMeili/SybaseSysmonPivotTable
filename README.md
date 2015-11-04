# SybaseSysmonPivotTable
A dataengine should never be a black box.  This tool chain shows one way of integrating the engines metrics with the OS view.
-----------------------
This is an example case of a Sybase server that struggled under load.  As the load increased, its struggles turned to thrashing with out a clear cause.  As the various groups pointed fingers, it was only when agile methods were applied to unifying the metrics from Sybase, OS, and Storage that the reasons became clear.  

Thats right, I am saying a pretty picture drawn with all the parts in view, saved the day.  With a side benefit of delivering a view of metrics that everyone could play with.  From Developers, DBAs, Admins, and Managers.. All could coax useful information from the spread sheet based pivot tables.

These parsers take the point in time snapshot reports from Sybase, and combine them with other point in time metrics.  The trick is really simply that the Sybase reports are in human readable form, so need a lot of filtering to allow them to be combined into a pivottable on time.

The scripts were written by me after a very frustrating day.  An evenings work to build a tool that could extract, stack, and build a spreadsheet in one.  Server side bits that dictionary the data, and macros in excel to generate the view.  But the results were immediate, and we used this tool with continued success for a few years.

In this case, the data shows a table that gets filled faster then it can index.  The data engines response is full table scans of a fast moving target from that point on.  Shown by graphing reads to writes, tada!  A simple view of data already right in front of you, can give one the key.  Having the skill to fold it means more then all the swags taken without it.

James Hutchinson
