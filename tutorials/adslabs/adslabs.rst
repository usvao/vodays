.. vodays documentation file
.. include:: ../../references.rst

:tocdepth: 1

.. _tutorial_adslabs:
   
ADS Labs: The Next Generation Data/Literature Search Tool(s)
============================================================

.. contents:: 

Science Story
-------------

.. topic:: Questions

    * ?


Tools and Files
---------------
.. image:: /logo/adslogo_labs.jpg
   :align: right
   
This tutorial uses the 
  * `ADS Labs`_ web application
  
Overview of ADS Labs
--------------------

`ADS Labs`_ is an experimental interface incorporating new search capabilities,
and result visualizations. Not all functionality from “classic” ADS is 
available yet and search limitations exist (only 200 records appear in the 
facets). 

.. note:: For best results users should be 
    `logged into ADS <http://adsabs.harvard.edu/cgi-bin/nph-manage_account?man_cmd=login>`_; 
    this login is shared with ADS Labs. 
    Simply click on the ``Sign on`` link on the top-right of the screen.

.. sidebar:: Filters, Facets, Future

   There are a couple of interesting points about Filtering, Facets and the
   Future of `ADS Labs`_:

   * Each facet category is orthogonal to others (and performs an AND);
   * Facet values within a category are combined using OR;
   * Any of the visualizations create a rendering of (some property of) the 
     articles currently selected, and selection within the visualization can 
     be reapplied back to the results in ADS Labs using a filter similar to 
     what a facet selection would do.
   * The current system is limited to displaying (and manipulating) the top 
     200 papers returned by a query, so facets are built exclusively on 
     this partial list.  This limitation will be removed in the near future.


Author Based Queries
--------------------

Author searches are the most popular searches in ADS. We all want to see what
our favorite {collaborators|competitors|friends} have been up to. Let’s walk
through a typical author search in ADS Labs, starting from the ADS Labs' 
`streamlined search form <http://adslabs.org/ui>`_

#. We’re interested in papers by Steve Murray. Let’s find out what papers he
   wrote as first author. Click on “first author” link and enter: “Murray, S”
   
   .. note:: Did you know that you could request first-author papers only?    

   .. note:: a long list of results, some by “Murray, Sophie” etc.

#. Go back to search form, enter full first name: “Murray, Stephen”
#. Look at results, now many fewer. Click on ``Authors`` facet for “Murray, S” 
   and show all name variations.
#. Tick off only the author names in the ``Authors`` facet that 
   correspond to Steve (whose middle initial is S).

   .. note: ``Keywords`` facet are associated with papers, but some records 
             don’t have keywords associated with them.
             
#. Click on the ``View as...`` tab and pull up a ``Word cloud``, 
   which is generated from all words in the title and abstract of the papers.
   
   * Select “ACIS,” “HRC” words and click ``View papers for selected words`` 
     to facets to show a list of Chandra observing proposals.  
     
     .. note:: Yes, ADS has records for many observing proposals, including Chandra ones. 
        You will see more of this in the second part of this tutorial.
        
#. Click on first record in result list (about observations on `Abell 2199`_), 
   and follow links to Chandra data.

.. topic:: Exercise

   As an exercise, try searching for your own publications (or your adviser’s, if
   you only have a few), and then visualize the results via the word cloud. Is
   there anything that jumps out at you? Select a few words and then filter
   papers by clicking on “view papers for selected words.”

Topic Search
------------

AstroExplorer
-------------
  