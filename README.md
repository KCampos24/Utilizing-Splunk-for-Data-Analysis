<h1>Utilizing Splunk for Data Analysis</h1>

<h2>Description</h2>
In this project I delve into the essential techniques for querying and analyzing data using Splunk, a leading SIEM tool. I perform basic searches within the Splunk interface, focusing on indexing, fields, and search keywords to extract meaningful insights from event data.
<br>
<br>
I'll examine how to identify security issues, such as failed login attempts, by constructing effective search queries. For instance, I'll analyze SSH login failures for the root account, demonstrating how to use wildcards to broaden search results and pinpoint critical events.
<h2>Program Walk-through:</h2>

<h3>1. Perform a Basic Search</h3>
<p align="center">
<img src="https://i.imgur.com/TEwnSbJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<pre>index=main</pre>
<p>
    This search term specifies the index. An index is a repository for data. Here, the index is a single dataset containing events from an index named <strong>main</strong>. Selecting <strong>All Time</strong> will search for all events across all time. Under selected fields are:
</p>
<ul>
    <li><strong>Host:</strong> specifies the name of the network host from which the event originated.</li>
    <li><strong>Source:</strong> indicates the file name from which the event originates.</li>
    <li><strong>Sourcetype:</strong> determines how data is formatted.</li>
</ul>
 
<br/>
 
<h3>2. Search for Failed Login for Root</h3>
<p align="center">
<img src="https://i.imgur.com/UMyA11f.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<pre>index=main host=mailsv fail* root</pre>
<p>
    This query searches for the keyword <strong>"fail"</strong>, utilizing a wildcard to include related terms such as <strong>"failure"</strong> and <strong>"failed."</strong> Additionally, the keyword <strong>"root"</strong> is used to identify any events containing this term. The query results show a total of <strong>346 events</strong>, indicating instances of failed SSH logins for the root account.
</p>


<h2>Conclusion</h2>
In this project, I utilized Splunk to conduct a targeted query for analyzing failed login attempts, specifically focusing on the root account. By leveraging keywords and wildcards, I effectively identified instances of failed SSH logins, resulting in the detection of 346 relevant events. This analysis underscores the importance of monitoring authentication failures, which can be indicative of attempted unauthorized access and potential security breaches. By understanding patterns in failed login attempts, security teams can strengthen access controls, enhance incident response strategies, and ultimately protect sensitive systems and data from malicious activities.
