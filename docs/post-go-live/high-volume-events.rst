.. _high_volume_events:

==============================
Prepare for high volume events
==============================

Use the following considerations and recommendations to plan for high seasonal
traffic. Your Rackspace Account team and RAS Digital Experience team can work
with you to understand and implement these recommendations. They come up with a
Seasonal Readiness Plan for your environment to ensure that your end users
are not impacted by poor performance during peak seasonal traffic
periods.

General guidelines:

* Limit code deployments leading up to peak traffic periods to minimize
  changes in the environment.
* Consider limiting or disabling back-end administrative functionality, such as
  imports, catalog updates, and so on, during peak traffic periods.
* Consider scheduling regular, short touchpoints with all appropriate parties
  throughout the peak period.

Two to four months before peak traffic begins
---------------------------------------------

**Perform load testing**: Engage the Rackspace Customer Success team, RAS, and
Network Security to participate in load testing to observe, analyze, and
take action on the results.

Depending on your environment's size and complexity, use marketing analytics
data to calculate the expected peak flow of traffic and perform load testing.
Refer to the following guidelines when you plan for and execute application
load testing:

* Many environments can expect a 20-30 percent increase in traffic year over
  year.
* Develop a load testing plan that tests all application functions and tests
  for at least 125 percent of expected peak traffic.
* Use a load-testing tool that incorporates realistic *think time* to gauge
  the impact of real users more acurately. If you do not have a preferred
  vendor or tool, Rackspace has load testing partners with whom you can
  engage.
* Test against an environment that uses the same codebase and is as close to
  production as possible. Modern, complex applications do not scale linearly,
  and you cannot always accurately extrapolate real-world performance.
* Use metrics to establish the success or failure of a test. For example, a
  test is successful when at least 95 percent of transactions complete without
  errors.
* You might need to pconduct multiple load tests to ensure that you can iterate
  through the results and achieve stability at peak user traffic levels.

One to two months before the peak traffic period
------------------------------------------------

**Integration points review**: Work with the RAS team to review integration
points approximately one to two months before the peak traffic period. Include
internal and external integrations such as search, payment gateways, OMS,
inventory, mobile, and so on.

* Ensure that load testing includes integration points.
* Where possible, review integration point architectures to determine if they
  are highly available.
* Understand the impact on users if the integration service is degraded or
  unavailable.

**Configuration review**: Work with the RAS team to proactively review your
environment's configuration and APM metrics, including the application, web
servers, caching layers, databases, and so on. This review can uncover
bottlenecks that developed during load testing.

Ensure that you allow for time to make changes and then test again.

**APM configuration review**: During the APM configuration review, engage with
the Rackspace team to:

* Review baselines
* Review business transactions configurations
* Ensure that you configure health rules appropriately for the environment
* Review dashboards to reduce troubleshooting time in the event of issues

Two to four weeks before the peak traffic period
------------------------------------------------

**Network layer review**: Engage the Rackspace Account team and Network
Security team to review performance of firewalls, load balancers, and any
inline devices, such as IDS, to ensure that they can handle increased traffic.

**CDN and caching tuning**: Engage the Rackspace Account team and RAS to
ensure as many static assets as possible are cached. Ideally, the CDN or
cache layer should take as much traffic as possible, which reduces calls back
to the application.

One to three weeks before the peak traffic period
-------------------------------------------------

**Schedule jobs review**: Engage the RAS team to review any scheduled jobs,
such as cron jobs, scheduled tasks, and backups, to minimize impact during
peak hours.

**Review URL monitoring**: Engage Rackspace RAS to ensure synthetic
transactions are in place to monitor the availability and functionality of
critical business paths (for example, add to cart, checkout, search, and
so on).

**Review account guidelines**: Engage the Rackspace Account team to verify
that escalation paths, return-to-service instructions, and runbooks are
up-to-date and technically valid.
