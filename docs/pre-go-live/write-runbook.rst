.. _write_runbook:

===============
Write a runbook
===============

A runbook is an optional document that contains mutually agreed-upon actions
that Rackspace should take on your production environment each time there is
an alert. The purpose of a runbook is to return your system to service as
quickly as possible. After your system returns to service, you can work with
Rackspace to perform root cause analysis to determine the cause of the alert.

.. note:: Runbook procedures do not apply to non-production environments,
including test, development, and staging environments.


Why you should write a runbook
------------------------------

You should write a runbook because Rackspace can return your system to service
much more quickly than without a runbook. Because a runbook contains known
issues that result in alerts firing, Rackspace engineers can skip some
required diagnostic steps.

If you choose not to write a runbook, Rackspace uses the following prescribed
set of steps each time an alert fires:

* Determine if the traffic rate has increased over the last few hours or days
* Determine if the error rate and response times have increased
* Review warning violations that could point to a transaction or group of
  URLs that might have higher response times
* Investigate individual transactions and determine if any method calls take a
  long time to return
* Check the database to determine which queries are running and how much CPU
  time the queries require

Without a runbook, it can take Rackspace much longer to diagnose an issue
and return your system to service.


Runbook contents
----------------

During the runbook creation process, Rackspace

* Develops an operations runbook in accordance with the transition plan that
  complies with the following conditions:

  * Where a change in law affects a change in policy, this change is discussed
    between both parties in good faith.
  * The parties shall develop and follow specific procedures, which are set
    out in the operations runbook, during the term of the contract.
  * The operations runbook describes the procedures to be used to perform the
    services.
  * The operations runbook conforms to Rackspace policies and, where
    reasonably possible, your policies. If there is any discrepancy between the
    operations runbook and this Service Description, the terms of the runbook
    prevail.
  * Rackspace and you jointly use the operations runbook to enable close
    cooperation and communication between the parties.
  * The operations runbook includes checkpoint reviews, testing, acceptance,
    and other procedures to ensure the quality of Rackspace performance.

* Performs the services in accordance with your approved operations runbook.


The operations runbook contains the following items, at a minimum:

.. list-table::
   :header-rows: 1

   * - Item
     - Description
     - Example
   * - Hours of Use
     - The hours that this application is primarily used by you
     - 24x7x365

       09:00 - 17:30 Monday to Friday
   * - Business Criticality
     - On a scale of Tier 1 (critical) to Tier 4 (non-critical), what tier
       is this application?
     - Tier 1 - Critical
   * - 
