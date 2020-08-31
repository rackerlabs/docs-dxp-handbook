.. _define_monitor:

==========================
Define a synthetic monitor
==========================

A synthetic monitor is a NodeJS script that mimics the steps of a user
transaction and tests for the success or failure of that transaction. Common
synthetic monitor transactions include a search transaction, a login
transaction, and an ecommerce transaction. If any step of a transaction
fails, the monitor can help identify where the problem originated.

For example, the synthetic monitor can reveal a problem with the command that
writes a record to a database or that the tax calculated during the
**Add to Cart** step isn't correct. *Synthetic monitors can identify
problems with your site before they negatively affect your business*.

A synthetic monitor runs 12 times each hour, 24 hours per day. You can run
synthetic monitors in different geographic locations (except Antarctica),
depending on the location of your user base. You can check multiple
geographies simultaneously. If there is an error in any of the 288 daily
transactions, the monitor automatically creates an **Emergency** ticket.
After Rackspace acknowledges the ticket and tests the Internet
connections, Rackspace consults the runbook for guidelines.

.. note::
   Collaborating with Rackspace to write a runbook is extremely
   important.


The user transactions that you want to test are up to you, based on your
business requirements. Rackspace relies on you to identify the transactions
you want to test and to provide the steps of each transaction. Rackspace
sends a ticket requesting that you define your synthetic monitors.

Refer to the following example when you provide Rackspace with documentation
about the synthetic monitors that you want to create:

**Synthetic monitor name**: Add Item to Cart

**Result of transaction**: By the end of this transaction, the user has
searched for and added an item to the cart.

**Steps**:

   1. Open a browser and navigate to **acme.com**.
   2. On the top navigation bar, click **Products > Shirts**.
   3. Review the list of available shirts.
   4. Select a shirt and click **Add to Cart**.
   5. To begin the purchasing process, click **Cart**.
   6. Click **Checkout**.


After you provide the detailed steps to Rackspace, Rackspace creates a
NodeJS script that includes the steps you have documented.

The following NodeJS example includes the steps identified above:

.. code::

   /** BEGINNING OF SCRIPT **/// Step 1
   .then(function() {
     log(1.1, 'Browse to site.');
     return $browser.get("Url");
   })// Step 2
   .then(function() {
     log(2, 'Click PRODUCTS list');
     $browser.findElements(By.linkText("PRODUCTS"))
     .then(function(elements) { elements[0].click(); });
   })// Step 3
   .then(function() {
     log(3, 'Click SHIRTS');
     $browser.findElements(By.linkText("SHIRTS"))
     .then(function(elements) { elements[0].click(); });
   })// Step 4
   .then(function() {
     log(4, 'Click "ADD TO CART".');
     $browser.switchTo().defaultContent();
     return $browser.waitForAndFindElement(By.id("btn-addtocart"), DefaultTimeout)
     .then(function (el) { el.click(); });
   })// Step 5
   .then(function() {
     log(5, 'Click CART.');
     return $browser.waitForAndFindElement(By.linkText("CART"), DefaultTimeout)
     .then(function (el) { el.click(); });
   })// Step 6
   .then(function() {
     log(6, 'Click CHECKOUT.');
     return $browser.waitForAndFindElement(By.id("CHECKOUT"), DefaultTimeout)
     .then(function (el) { el.click(); })
   }).then(function() {
     log(lastStep, '');
     console.log('Browser script execution SUCCEEDED.');
   }, function(err) {
     console.log ('Browser script execution FAILED.');
     throw(err);
   });/** END OF SCRIPT **/


You can sign off on the script before Rackspace deploys it. After you
approve, Rackspace tunes the script to remove popup messages.

Rackspace is responsible for the ongoing maintenance of the script. As you make
changes to the user interface of your site, ensure that you coordinate with
Rackspace so that Rackspace updates your synthetic monitors.
