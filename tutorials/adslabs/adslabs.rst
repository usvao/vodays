.. vodays documentation file
.. include:: ../../references.rst

:tocdepth: 1

.. _tutorial_adslabs:
   
ADS Labs: The Next Generation Data/Literature Search Tool(s)
============================================================

.. contents:: 

Science Story
-------------

One begins to search the literature for many reasons during ones research:
when one is looking for new data or new collaborations or learning a new
field.  Here are a couple of ways ADS and `ADS Labs`_ might be used for some
of the :ref:`sci_stories`:

.. topic:: Questions

    * What are people reading about accretion regulated rotation or 
      disk / magnetic field connections? (:ref:`sci_ysos`)
    * What are other papers on black holes in NGC 3393?  Signatures of 
      galaxy mergers?  (:ref:`sci_mergers`)
    * How is a blazar not a quasar? (:ref:`sci_blazars`)


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

.. topic:: Filters, Facets, Future

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
`streamlined search form <http://adslabs.org/ui>`_.

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
   
   Consider the science story, :ref:`sci_mergers`:  has the lead author,
   G. Fabbiano, written other papers on this subject? What is the scope of the
   literature for the targeted object, `NGC 3393`_?

Topic Search: Blazars
---------------------

Let’s now go to a topic search and consider one of our original science
questions about blazars. 

.. note:: The ADS Labs user interface supports many different rankings of
   results, some of which are not straightforward. Let’s go over some of them as
   part of this exercise.

#. We are interested in papers published on “blazars.” In this case, we don’t
   want to see results ranked by publication date, but rather see the papers that
   best match the input term, so we select ``Most relevant`` as the ranking method
   and submit the query.

#. We get a list of 200 papers, and under the option ``View as...`` we select
   the ``Author Network`` associated with them to understand what the different
   groups of collaborators working on this topic are.

#. We use the slider to remove some of the complexity in the network and see
   that one of the most prolific authors is Ghisellini; we select this author and
   its immediate co-authorship nodes (``alt + shift`` or use the proper selector in
   the author network screen).
   
#. We apply the selection back to the list of records in our result set and are now down to 55 records.

#. Let us now see what archives have data related to these articles; if we
   open the ``Archives`` tab we see that there are data in different places; we
   notice that there are 33 papers in the original list which have datasets
   available from HEASARC; if we click on this facet our list of results shrinks
   to 11 papers.        
  
.. topic:: Exercise

   As an exercise, can you guess what the “paper network” option does to
   visualize the selected set of papers? What do you think it could be useful for?

Let us try a different approach to our problem. Let us say that we are
entirely new to the field of blazars and want to read review articles as an
introduction to the subject.  

.. note:: While the first column of search options provide **"Sort by"** capability,
   the second, **"Explore the field"** provide additional second order operators
   to the search itself. 

#. Type “blazars” in the search field, select “Reviews and introductory papers” and submit.

#. We find a list of 200 papers, but we want to restrict ourselves to reviews
   written in the last 3 years, so use the slider under the ``Dates`` facet to
   manipulate the histogram and select the proper range of dates.

#. The remaining list shows the paper 
   `2010arXiv1006.5048B <http://labs.adsabs.harvard.edu/ui/abs/2010arXiv1006.5048B>`_ 
   up top. We can’t really tell if this is a review paper from the title, but look! 
   We see links under the record saying ``matches in abstract`` and 
   ``matches in preprint`` which allow us to take a peek inside the paper.
   Click on the abstract link and find that, in fact this is a recent review 
   of the field.

#. We want to find out which objects in the sky these papers are studying;
   thanks to `SIMBAD <http://simbad.u-strasbg.fr/simbad/>`_, we can open 
   the corresponding facet and select first a class
   of objects, then a set of object names within that class.    
   
#. As an alternative, we can use a sky map visualization of the list of 
   SIMBAD objects to perform a selection based on position and object type; 
   as an example, select “other objects” and then box the cluster of objects 
   near (ra=200, dec=-45), then click on ``Apply to facets``.

#. We are left with one paper: 2010ApJ...719.1433A; we click on the link to see the full abstract page.

.. note:: Notice that the list of authors is truncated to a reasonable amount,
   but which can be expanded to the complete list, and the affiliations can be
   displayed in-line as an option.

.. topic:: Exercise

   Perform a search using keywords describing your field of study. Can you guess
   what type of results are returned if one selects the search options labeled
   “what people are reading” and “what experts are citing”? First you should find
   out more by clicking on the icon next to the label to understand how the
   search is structured, then try each option and see if the results make sense
   to you.

AstroExplorer
-------------

The next, next generation tool, `AstroExplorer <http://labs.adsabs.harvard.edu/semantic/>`_, 
is further integrating aspects of the data and the literature.  Go ahead and
log on, along the way try and save queries, publications, and datasets.

#. Type in blazars into search box on publications page. See the 10 results
   autocomplete as keywords but larger set of 37 when you hit ESC to remove the
   autocomplete.

#. See top keywords, active people, most studied CDS objects, targets (mention
   combining these). Click in left on B1101+384 object, one of the most studied.
   
#. Choose the one that has chandra mission. Note that it also has data with FUSE.  

#. Pivot on QSO B1101+384, notice Schull as main author, and Sembachs on proposals. 

#. Go to Observations tab, type in and autocomplete QSO B1101+384. 

.. topic:: Exercise

   Repeat these steps for the `3C273`_ object that will be used in other of
   today's tutorials.