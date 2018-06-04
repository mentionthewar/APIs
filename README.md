# Web service API usability (for cultural heritage)

I’ve found it difficult to locate what I regard as really relevant and useful resources on API usability. There’s some really interesting stuff out there, such as https://www.codeproject.com/Articles/8707/API-Usability-Guidelines-to-improve-your-code-ease but very little of it seems to me to really relate to web service APIs, the calls people actually make and the data they get back. They are more concerned with aspects of best practice in systems construction which are important but don’t seem to me to be really relevant to the issues at hand.

[Something like https://nordicapis.com/8-keys-to-creating-a-truly-usable-api/ is a bit nearer but still not terribly useful.]

Even after we agree that such APIs should be 'RESTful', this leaves many properties open:
https://en.wikipedia.org/wiki/Representational_state_transfer
even as it is agreed that interfaces should be 'uniform'.

Patrick Smyth offers some suggestions:
https://programminghistorian.org/lessons/creating-apis-with-python-and-flask

See also:
https://www.vinaysahni.com/best-practices-for-a-pragmatic-restful-api#pretty-print-gzip


In comparing web service APIs I suggest the following features are of interest:

<ul>
<li>What is the maximum acceptable rate of requests?
<li>What is the maximum length of a 'page' of returned results?
<li>How is 'paging' handled?
<li>How are composite objects handled?
<li>How are parent/child relationships handled?
<li>Do calls make use of relatively easy to understand expressions linked together in predictable ways or are they hard for humans to read?
<li>What formats are results returnable in?
<li>Are results heavily nested, requiring forensic examination of the tree?
<li>Does the documentation help you get started quickly and relate to the real use cases researchers actually have?

If anyone has any other suggestions regarding this I’d really like to hear them and they can be added to the list. 

<h3> Sins of web apis </h3>

* Fail to escape characters properly so calls are obliged to incorporate %20 or other weirdness.
* not breaking down entities sufficienctly - e.g. AMPAS orgs and people
* not exposting obvious entities (e.g. BFI)
