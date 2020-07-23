.. _identify_deployment:

============================================
Use APM to identify when deployment occurred
============================================

In both New Relic and AppDynamics, you can set release points that enable you
to compare application performance between releases. For example, if the
checkout process is slower or generates more errors after you deploy changes
to your environment, the APM tooling helps you identify precisely when and
what kind of change you deployed. If required, you can use the APM tooling
to roll back to a previous release.

To enable deployment tracking, create a ticket to request that we enable
deployment tracking.

For AppDynamics, you can add an API call to your deployment process, which
creates a custom even to track performance across multiple deployments.
For more information, see
`Using AppDynamics to track performance between releases <https://developer.rackspace.com/blog/Using-AppDynamics-to-Track-Performance-Between-Releases>`_.
