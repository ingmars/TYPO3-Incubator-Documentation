==============================
Indexing
==============================


How indexing is called and how the file is processed by DAM

What does "Indexing" mean?
==========================

IMO Indexing means that an media record in DAM is automatically filled with as much information as possible.

Indexing is called in the following situations:

*A file is uploaded and indexing is set to auto ("normal" case)*
DAM is using a TCE hook to call the controller and pass over the file object:
$this->indexingController = t3lib_div::makeInstance('Tx_Dam_Controller_IndexingController');
$this->indexingController->indexAction($file);

*A file is manually indexed because auto indexing is set to off*
For that case a DAM indexing button is registered in Vidi. Clicking this button also generates and indexingController instance and passes over the file for indexing as described above.

A file is replaced
When a file is replaced, the IndexingController is called as above. Depending on the TSconfig certain actions are performed or not, e.g. if 
tx_dam.indexing.replaceFile.reindexingMode = 3 (see below), the whole metadata is replaced by new data.

A bunch of files is mass indexed
In a yet to be planned backend module it should be possible to mass index files. Depending on TCA configuration, fields can be prefilled by user defined value, e.g. the user can choose a category for all the files being indexed.



Indexing is the process of automatically extracting meta data from the file and 