
A case against TDD and unit-testing-first

disclaimer; heavily opinionated, based on current understanding of
software development, and current experience in JavaScript/CoffeeScript on node.js,
and C++, C on GNU/Linux and bare metal.

testing serves primarily one purpose:
ensuring a system does what it is supposed to,
even when the underlying implementation is being changed
secondarily it may have other benefits,
like helping design good interfaces
like making it easy to find out

tests are code too, and code has costs
each line of code added is ones that have
to be written and maintained
If you have as much test code than implementation code,
not much by TDD-standards, that is twice as much

if you have to change the tests when refactoring,
then who-tests-the tests
TDD says first writen broken test (to ensure test work),
but if you refactor

test how 
BDD, is more in this style
though concept usually means behavior as seen from end-user perspective
extended notion, is that it is the behavior of the (sub)'system',
as seen from the entity that uses said system.
system may then be a JS library, and the user the developer and software
that incorporates the library
or a HTTP server with a RESTful JSON api, the user the developer and
software which makes api calls to this server

have to keep your promises
make as few promises as possible
make sure that your API is comprehensive,
enough to understand and debug

TDD claims testing-first informs design decisions
this is true, but design of units is much less important
than design of interfaces between system components,
and overall system architecture

