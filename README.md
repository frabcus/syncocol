Syncocol
========

A proposed simple specification for syncing tabular data via JSON transaction logs.


HTTP endpoint
-------------

XXX todo


Wire protocol
-------------

JSON representing part of the transaction log of changes to the tabular data.

<pre>
{ 
    seq: 10, 
    id: "07acde3002cb1f62a08de5469160b912", 
    deleted: false, 
    data: { first_name: "Ryan", last_name: "Pitts", employer: "The Spokesman-Review" } }
</pre>

* seq - the sequence in the transaction log
* id - unique identifier of the row
* deleted - if present and true, means the row is being deleted by the transaction
* data - new data for the row, should not be present if deleted is true


Data format
-----------

Just strings, integers or floats in normal Javascript.

XXX dates

XXX lat/lng?



