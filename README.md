Syncocol
========

A proposed simple specification for syncing tabular data via JSON transaction logs.


HTTP endpoint
-------------

TODO


Wire protocol
-------------

JSON representing part of the transaction log of changes to the tabular data.

<pre>
{ 
    seq: 10, 
    id: "07acde3002cb1f62a08de5469160b912", 
    deleted: false, 
    data: { first_name: "Ryan", last_name: "Pitts", employer: "The Spokesman-Review" } 
}
</pre>

* seq - the sequence in the transaction log
* id - unique identifier of the row
* deleted - if present and true, means the row is being deleted by the transaction
* data - new data for the row, should not be present if deleted is true


Data format
-----------

The values in the data dictionary must be one of these types:

* Strings, in quotes
* Numbers, integers or floats
* Dates, a string containing an ISO 8601 date or date/time. Only in UTC no timezones.

TODO: Something about latitude/longitude? Not something recursive, but a
convention saying do something like "start\_lat, start\_lon"




