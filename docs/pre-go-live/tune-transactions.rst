.. _tune_transactions:

==========================
Tune business transactions
==========================

Your application monitoring solution relies on you and the RAS Digital
Experience team to identify the critical business transactions that you want
to monitor. When you come on board as a RAS Digital Experience customer, you
can choose to use either AppDynamics or New Relic as your application
performance monitoring tool. Critical business transactions are the set of
pages on your site that are more important than others.

For example, you might want to receive a notification when the
**Add to Cart** page
doesn't load properly for a customer. Because this page is directly tied
to revenue, it's critical for you to know when it isn't available. Other
important pages include the **Login** page and the **Search Results** page.

For pages associated with a critical business transaction, the RAS Digital
Experience team can:

* Add custom alert thresholds that monitor page response time and error rates.

  When the defined threshold is exceeded, the RAS Digital Experience team
  automatically receives a ticket, and they consult the runbook for
  instructions on how to proceed.

* Configure a custom dashboard that displays business transaction metrics.

* Document runbooks that outline procedures to follow when responding to
  custom alerts.


.. note::
   To prevent alert fatigue, limit the number of monitored business
   transactions to 10.


As you continue to develop your application and add critical business
transactions, ensure that you communicate to the RAS Digital Experience team
about the changes you make.
