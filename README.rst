**********
msplit
**********

Splits mbox files into smaller mbox files.

Sometimes an mbox file (UNIX mailbox file) grows up too large to read with an email client.
This tool splits the large file per the given number of emails.

=============
Requirements
=============

* Ruby 1.9.3 or greater
* Rubygem Keybreak_

.. _Keybreak: https://github.com/hashimoton/keybreak

=============
Setup
=============

1. Copy msplit into your convenient directory.

  - Windows users need to copy msplit.bat into the same directory.
  - \*nix users may need executable permission (chmod +x msplit). 
  
2. Include the directory in PATH.

=============
Usage
=============

::

  $ msplit -h
  Usage: msplit [options] MBOX_FILE [MBOX_FILE...]
  
  Options:
      -c=NUM                           Number of emails in a splitted file (10)
      -n                               Dry-run (does not save splitted files)
  
I recommend to run::

  $ grep -cE "^From " large.mbox

before msplit in order to count emails in the file.


==============
License
==============

Public Domain

==================
Another Solution
==================

If you have GNU csplit::

  $ csplit large_mbox '/^From /'

may help you (but for me, the above command line didn't as expected).


.. EOF

