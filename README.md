A simple app (dashboard) meant to quickly identify logs across large swaths of data.

## Details

The underlying query used by DataLocator uses the "tstats" command with one or more TERM() clauses specified by the user.

The use of TERM() matches whatever is inside the parentheses as a single term in the index, even if it contains characters that are usually recognized as minor segmenters, such as periods or underscores. This can affect results returned due to the way Splunk uses Major/Minor segmenters to tokenize and index events.
<a href="en-US/app/splunkdocs/UseCASEandTERMtomatchphrases">Using CASE and TERM</a>

If you modify index or sourcetype via a search time extraction, you will not be able to choose the source from the dropdown nor use your modified name, as the logic works on indexed fields only.
