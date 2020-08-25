.. _development_best_practices:

==========================
Development best practices
==========================

Because applications evolve as your business evolves, your development team
is critical for running and maintaining your web applications. To ensure
success, approach application development in a structured, systematic fashion.

When you plan your application development and deployment strategies, think
about your application from a governance perspective. Ensure that the
governance plan includes policies for the following DevOps areas:

* Source control and branch management
* Development tools (for example, VS, VS Code, and so on)
* Team communication
* Deployment tools and release management packaging, continuous integration,
  continuous delivery, blue/green, monitoring, and rollback)
* Deployment targets (don’t test in production)
* Testing methods (user, load, smoke, sanity, and regression)
* Infrastructure management (infrastructure as code, ARM templates)
* Escalation points (internal and external)
* DataOps and DevSecOps integration
* External integrations and APIs
* Rollback plan (for example, backup databases before deployment, redeploy
  previous code)

This section includes best practices for each of the following DevOps
development lifecycle phases:

* Planning and design
* Build
* Testing
* Release and deployment
* Monitor


Planning and design
-------------------

Consider the following guidelines during the planning and design phase of
your project:

**Pick your coding methodology**: A coding methodology is a framework and
set of processes that organize the development process. These methodologies
provide guidance about:

* How you gather requirements
* How you make decisions
* How the cycles of software development flow into each other and influence
  your choice of branching strategy and team structure.

While many development methodologies are available, Agile, Lean,
Waterfall, and Scrum are the most common methodologies IT organizations use
to manage their projects. Keep in mind that every methodology has its pros and
cons. A methodology that fits your project and available resources becomes a
driving factor in steering your team toward success.

Decide on your branching strategy: When you start or revamp a development
process, consider which branching strategy is right for your team and
project. Consider how large the development team is, whether multiple teams or
a single team develop the code, and how often the code changes. While hybrid
strategies are tempting, they are often more difficult to implement. All
effective branching strategies include source-code management tools, such
as GitHub.

The following image illustrates a sample GitHub branching workflow:

.. image:: _images/github-workflow.png


**Standardize your environment**: After you identify a strategy, you should
standardize the development environment and processes that developers use
when coding. We recommend that your developers use the same integrated
development environment (IDE) to enable team collaboration. By using the same
IDE, developers use the same linting process that identifies code errors. When
developers use the same IDE and linting process, you ensure that the
application has a consistent quality level.

Build
-----

Consider the following guidelines when you plan your application build
processes:

**Incorporate unit testing**: Unit tests operate on a software component to
test basic functionality independent of other factors. For example, a common
requirement for many web applications is to calculate sales tax. A sales tax
unit test verifies that the calculated tax rate is correct. Other separate
unit tests ensure that items added to the cart are visible in the cart and
that the credit card information is valid. As opposed to a large, single test
that incorporates all of your site’s functionality, unit tests can save
development time because they help you to identify defective code efficiently.
Unit tests also encourage modular coding, making it easier for you
to reuse and make updates to your code.

**Automatic builds**: It is useful to configure automatic builds in
non-production environments so that a build runs whenever a developer checks
in code. In addition to automating a step, which allows developers to use their
time more effectively, automated builds provide real-time feedback if the
code introduces a significant error.

**Continuous integration/Continuous deployment**: Continuous integration (CI)
and Continuous deployment or delivery (CD) are often linked together in modern
software development methodologies. Continuous integration refers to the
process of frequently merging code updates back into the main branch, often
several times throughout the day, when developers address discrete features or
defects. By frequently merging or integrating code, your developers’ local
repositories are kept in sync, which reduces the time required to complete
each merge operation. CD commonly refers to continuous deployment,
a build process where deployments are performed automatically as developers
check in code throughout the day. CD can also refer to continuous delivery,
which is similar to continuous deployment in that the main branch can always
be deployed, but it does not necessarily get deployed each time a developer
merges code. The automation that enables CI/CD is called a CI/CD pipeline.


Testing
-------

Consider the following guidelines when you plan your application testing
strategy:

**Automate testing**: You can use a tool like Selenium to run your smoke
tests. Selenium automates much of the testing work and has the added benefit
of performing the final, post-deployment checks on your production
environment. This final check quickly catches issues during the coding
process before they impact your users. Because Selenium automates testing,
your QA team can perform more thorough tests than they otherwise have time
to conduct.

**Load testing**: After you update the application, you should perform load
tests that identify performance bottlenecks. Apache® JMeter is an application
that enables you to load test your application and identify issues that are
only visible when the system is under a high load, such as during a sale or
other peak times.

**Code reviews**: Automated tests are an essential part of software
development, but collaboration between developers remains an important activity
that should be encouraged. Working with colleagues and mentors via code
reviews not only decreases defect rates for a low investment but also
provides valuable team building, employee growth, and camaraderie.


Release and deployment
----------------------

Consider the following guidelines when you plan your release and deployment
strategy:

**Deployment**: You, our Named Application Engineers, and our Application
Support Engineers collaboratively determine the steps to take during a
deployment.

* By using the requirements gathered during discussions with your team, our
  Named Application Engineers develop the automation jobs required for your
  deployments.
* The Application Support Engineers use the automation jobs and high-level
  processes to define deployment templates that provide detailed deployment
  steps.
* The Application Support Engineers use the deployment templates to create
  maintenance plans for each deployment.
* Another ASE reviews the templates to ensure their quality and that there
  are no anticipatable issues.
* An ASE works with your team to deploy your application.


**Rollback plan**: If a deployment fails, it is important that you have a
documented and tested rollback plan in place. Deployments can fail for
any of the following issues:

* A coding error
* A bug or undocumented behavior of a library
* An incorrect assumption
* An issue with the vendor

Rollback plans ensure that you can restore the application to a functional
state, reducing the impact on your end users and preserving your brand image.

**Use multiple environments**: In addition to a production environment, most
organizations maintain a development (DEV) environment and a quality
assurance (QA) environment. As you promote code or other changes between
the environments, you should test at each stage.

* Developers working in their local environment or workstation should test
  their changes before pushing the code to the development environment.
* Thoroughly test the application in the development environment before you
  promote it to the QA environment.
* Within the QA environment, the QA team should perform regression testing on
  every aspect of the application. Regression testing ensures that the new
  features work and that they don't negatively impact existing functionality.
* After you promote the new version to the production environment, perform
  one final test to ensure that your end users don’t experience any issues.


Monitor
-------

To ensure that your application is always available and performing as
expected, continually monitor the application for critical production
issues, application performance issues, and the end-user experience.


As a best practice, use APM tooling and synthetic monitoring to monitor the
application. While RAS Digital Experience is not a monitoring team, we are
happy to use our tooling to help you achieve your monitoring goals. When the
RAS Digital Experience team instruments your environment with our APM tool, we
can create default alerts for the production environment. Those default
alerts cover many common situations that indicate a performance issue
or that could lead to a failure situation. However, because you are an expert
in your application, you should discuss additional monitoring needs
with us based on your knowledge of past issues and application requirements.


Communicate your development timeline
-------------------------------------

It is critical that you communicate with us about your development pipeline
and deployment cycles.

* If you schedule your releases (preferred), we can add the release schedule
  to the runbook.
* If you cannot develop a scheduled release cycle, coordinate with
  the RAS Digital Experience team to develop a method by which you
  communicate when you release changes.


.. note::
   Pushing out changes to your environment can trigger multiple alerts. If we
   are not aware of your deployment schedule and we actively monitor your
   environment, we might spend support hours trying to identify the source
   of the alert.


When your runbook contains detailed information of the transactions we
monitor and the steps we take to remedy any triggered alerts, Rackspace ASEs
function as your first-tier response. RAS Digital Experience can effectively
triage and remediate many issues, which frees your team up to focus on
improving your business.
