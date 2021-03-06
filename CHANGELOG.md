4.4.4 update: Fixed MEMO corruption bug:
Fixed an if-then statement that checks if the index link list contained a cycle.
Fixed an if-then statement that updates the last written block's index pointer to the block that is represented by EOF.  This statement only executes if there are no more free blocks in the file.  When writing the EOF index, it might right pad the index with an incorrect number of spaces, which may result in a corrupted index, which may result in data corruption.

4.4.3 update: added SELECT columns functionability when retrieving record(s)
bug fixed with isTable()
renamed sortAndBuild() to sort(); left placeholder for sortAndBuild() for backwards compadibility

4.4.2 update: query results cached
memo file's first unused block cached
more bugs fixed
rewrote memo functions; same process
tdb::sendError now can use custom error handlers
TDB_ERROR_INCLUDE_ORIGIN constant added
TDB_PRINT_ERRORS constant added
tdb::define_error_handler();
TDB Errors are assigned Error numbers and include the line the error was generated on

4.4.1 update: sortAndBuild() clears record reference cache
minor bug fixed in removeTable()
minor bug fixed in listRec()
debugging code removed from memo functions

4.4.0 update: NOT COMPADABLE WITH PREVIOUS VERSIONS
Separated memo's into blocks
Added readMemo(), writeMemo(), and deleteMemo(); removed rewriteMemo()
Changed record deletion and storage method; multiple functions affected;
Added the extention ".ta" to the main table file.
Added Db's name to tables' names to allow multiple Dbs to exist in one directory
Added descriptions to functions
check() now validates workingDir, Db, and Fp

4.3.5 update: added rewriteMemo()

4.3.4 update: added support for memo field in query()

4.3.3 update: added $start and $howmany in query()
added editField() and removeField()

4.3.2 update: limited file locking
fixed bug with removing databases
added '<' '>' usage in query()

4.3 update: all chars are allowed in string fields now
header buffering
wrote new query() algorithm increasing query speeds over 3 times

4.2 update: removed $start and $howmany from basicQuery()
added query()