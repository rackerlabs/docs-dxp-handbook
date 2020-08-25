.. _write_runbook:

===============
Write a runbook
===============

A runbook is an optional document that contains mutually agreed-upon actions
that Rackspace should take on your production environment each time there is
an alert. The purpose of a runbook is to return your system to service as
quickly as possible. After your system returns to service, you can work with
Rackspace to perform root cause analysis to determine the cause of the alert.

.. note::
   Runbook procedures do not apply to non-production environments,
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

Without a runbook, Rackspace can take much longer to diagnose an issue
and return your system to service.


Runbook contents
----------------

During the runbook creation process, Rackspace performs the following
activities:

* Develops an operations runbook following the transition plan that
  complies with the following conditions:

  * Where a change in law affects a change in policy, both parties discuss
    this change in good faith.
  * The parties shall develop and follow specific procedures, which are
    described in the operations runbook, during the term of the contract.
  * The operations runbook describes the procedures the both parties use to
    perform the services.
  * The operations runbook conforms to Rackspace policies and, where
    reasonably possible, your policies. If there is any discrepancy between the
    operations runbook and this Service Description, the terms of the runbook
    prevail.
  * You and Rackspace jointly use the operations runbook to enable close
    cooperation and communication between the parties.
  * The operations runbook includes checkpoint reviews, testing, acceptance,
    and other procedures to ensure the quality of Rackspace performance.

* Performs the services according to your approved operations runbook.


The operations runbook contains the following items, at a minimum:

.. list-table::
   :header-rows: 1

   * - Item
     - Description
     - Example
   * - Hours of use
     - The hours that you primarily use this application
     - 24x7x365

       09:00 - 17:30 Monday to Friday
   * - Business criticality
     - On a scale of Tier 1 (critical) to Tier 4 (non-critical), what tier
       is this application?
     - Tier 1 - Critical
   * - Support hours
     - Any agreed support hours that we must adhere to
     - 24x7x365

       08:00 - 18:00 Monday to Friday
   * - Allowable maintenance window
     - Any pre-agreed maintenance time for this platform or application
     - On your agreement, only or third (3rd) Sunday of the month
   * - Incident management process
     - Standard incident management process and major incident management
       process
     - A hyperlink to the pre-agreed standard and major incident management
       processes
   * - Change management process
     - Standard and emergency change advisory board (ECAB) change management
       processes
     - A hyperlink to the pre-agreed change and ECAB processes
   * - Escalation contacts
     - Agreed platform and escalation processes

       .. note::
          Ensure that you provide an after-hour contact, the times the
          contact is available, and the time zone.
     - A hyperlink to the pre-agreed platform and application escalation contacts
   * - Application owner
     - The application owner
     - Named contact
   * - Business owner
     - The business owner
     - Named contact
   * - Logical view
     - A description of the platform or application
     - The DummyTest application runs a total of six VM servers between LON5 and
       LON3 data centers with a physical MSSQL backend database based in LON3
       as active, LON5 as failover.
   * - Application dependencies
     - Any known application dependencies
     - If application A doesn't function, the search engine in application B
       doesn't function.
   * - Infrastructure scope
     - Identified and documented infrastructure used within the platform or
       application
     - 12345-dummyapp1.company.co.uk

       23456-dummyapp2.company.co.uk
   * - Monitoring configuration
     - Documented URL, port, and server monitoring configuration set up and
       implementation
     - A hyperlink to the configuration set up for URL, port, and server
       monitoring configuration and implementation
   * - Customer-supplied high-level design (HLD)
     - Any additional design documentation supplied by you
     - An application or platform design document
   * - Disaster Recovery (DR) process
     - If the platform or application has DR, a link to the DR process that is
       maintained by you
     - A hyperlink to the DR process
