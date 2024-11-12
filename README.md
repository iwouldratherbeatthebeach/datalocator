A simple app (dashboard) meant to quickly identify logs across large swaths of data.

## Details

The underlying query used by DataLocator uses the "tstats" command with one or more TERM() clauses specified by the user.

The use of TERM() matches whatever is inside the parentheses as a single term in the index, even if it contains characters that are usually recognized as minor segmenters, such as periods or underscores. This can affect results returned due to the way Splunk uses Major/Minor segmenters to tokenize and index events.
<a href="en-US/app/splunkdocs/UseCASEandTERMtomatchphrases">Using CASE and TERM</a>

An example of how this can affect results is searching for an IP address. Many of the indexes/sourcetypes will have Major segementers for events containing IP addresses; however, the <i>iptables</i> sourcetype requires the IP address be prepended with either "SRC=", "DST=", or "*" (e.g. "*8.8.8.8"). 
