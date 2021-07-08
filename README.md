# Relational Database Management System - C++

This project implements a toy relational database management system. I wrote it when I was the TA for CMPS181 - Database Management Systems II during spring quarter 2016 at UC Santa Cruz.

The system consists of the following components:

* Paged File Manager (PFM)
* * Allows reading and writing entire pages at once based on a page index.
* * Under PDFs, see Project 1 for more details.
* Record Based File Manager (RBFM)
* * Given data and a record format, writes the data to disk as a record.
* * Records are indexed by a page number and a slot number within a page.
* * Under PDFs, see Projects 1 and 2 for more details.
* Relation Manager (RM)
* * Manages tables, including column information.
* * Used to define the record format used by the RBFM.
* * Ensures changes to RBFM layer are reflected in associated Indexes
* * Under PDFs, see Projects 2 and 4 for more details.
* Index Manager (IX)
* * Given a table and a column from that table, creates an index to allow quick lookups and in order traversals.
* * Index is implemented as an on-disk B+ tree.
* Query Engine (QE)
* * Implements query operations such as Filter, Project, and Join (equality only for join condition)
* * Under PDFs, see Project 4 for more details.

I'm currently rewriting this project in Rust here: https://github.com/coy-humphrey/RDBMS-Rust
