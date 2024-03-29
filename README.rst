`schedule <https://schedule.readthedocs.io/>`__
===============================================


.. image:: https://github.com/dbader/schedule/workflows/Tests/badge.svg
        :target: https://github.com/dbader/schedule/actions?query=workflow%3ATests+branch%3Amaster

.. image:: https://coveralls.io/repos/dbader/schedule/badge.svg?branch=master
        :target: https://coveralls.io/r/dbader/schedule

.. image:: https://img.shields.io/pypi/v/schedule.svg
        :target: https://pypi.python.org/pypi/schedule
        pymsa/tests/test_score.py

Python job scheduling for humans. Run Python functions (or any other callable) periodically using a friendly syntax.

- A simple to use API for scheduling jobs, made for humans.
- In-process scheduler for periodic jobs. No extra processes needed!
- Very lightweight and no external dependencies.
- Excellent test coverage.
- Tested on Python and 3.6, 3.7, 3.8, 3.9

Usage
-----

.. code-block:: bash

    $ pip install schedule

.. code-block:: python

    import schedule
    import time

    def job():
        print("I'm working...")

    schedule.every(10).seconds.do(job)
    schedule.every(10).minutes.do(job)
    schedule.every().hour.do(job)
    schedule.every().day.at("10:30").do(job)
    schedule.every(5).to(10).minutes.do(job)
    schedule.every().monday.do(job)
    schedule.every().wednesday.at("13:15").do(job)
    schedule.every().minute.at(":17").do(job)

    while True:
        schedule.run_pending()
        time.sleep(1)
        
        #The Job is 
        import pandas as pd
        # Through pandas read any number of fasta file
        a=pd.read_fasta('sequence(2)')
        b=pd.read_fasta('sequence(3)')
        c=pd.read_fasta('sequence(4)')
        import pymsa pm
        #Through Pymsa alignment at each worker processor take place, also called as job in this coding section
        #for sample unitest of multiple alignment Go to :pymsa/tests/test_score.py
        

Documentation
-------------

Schedule's documentation lives at `schedule.readthedocs.io <https://schedule.readthedocs.io/>`_.


Meta
----


https://github.com/ishaqafridi/at
