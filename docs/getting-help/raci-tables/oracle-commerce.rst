.. _oracle_commerce:

===============
Oracle Commerce
===============

The following table lists service relationships (roles and responsibilities)
for Oracle Commerce (ATG):

.. list-table::
   :header-rows: 1

   * - Tasks
     - RAS Digital Experience: Application installation and configuration
     - RAS Digital Experience: Experts only
     - RAS Digital Experience: Application operations
     - Customer/SI
   * - Share guidance from Oracle Commerce Platform architect and engineering
       team
     -
     - R, A
     - R, A
     -
   * - Provide 24x7x365 access to a team of Application Support Engineers,
       including highly technical .NET experts who:
          * Are experienced in infrastructure management
          * Provide active monitoring of the complete environment
     -
     -
     - R, A
     -
   * - Provide consultation on Oracle Commerce Platform architecture best
       practices
     -
     - R, A
     - R, A
     -
   * - Determine environment sizing,
       including:
          * Number and name of environments (DEV, QA, PROD)
          * Number of nodes
          * Virtual machine CPU and RAM requirements
          * Amount of disk space needed
     -
     - C, I
     - C, I
     - R, A
   * - Verify compatibility with Oracle Commerce Platform-supported
       environments matrix, including:
          * OS
          * Application server
          * JVM
          * Virtualization
     - R, A
     - R, A
     - R, A
     - C, I
   * - Define and document initial OS-level requirements,
       including:
          * Server naming conventions
          * Drive mount point names and sizing
          * Users and permissions
          * Sudo management
          * User groups
     -
     - C, I
     - C, I
     - R, A
   * - Define initial J2EE application server configuration,
       including:
          * JVM heap sizing
          * Garbage collection tuning parameters
          * Server instance layout
          * Session timeout values (if not defined in the application)
          * Port configurations and instance naming conventions
     - R, A
     -
     -
     - C, I
   * - Provide consultation on the Oracle Commerce-specific disaster recovery
       implementations and high-availability approaches
     -
     - R, A
     - R, A
     - C, I
   * - Develop application code,
       including:
          * Custom components and templates
          * Client libraries
          * Custom workflows
          * Source control
          * Endeca application
          * ATG configuration layer (ATG-DATA)
          * Custom code
     -
     -
     -
     - R, A
   * - Migrate legacy content
     -
     -
     -
     - R, A
   * - Consult and advise on Oracle Commerce Platform best practices and
       standards
     -
     - R, A
     - R, A
     -
   * - Install the Oracle Commerce Platform application
     - R, A
     -
     -
     -
   * - Install BCC
     - R, A
     -
     -
     -
   * - Install and configure Ant, Jenkins, and Weblogic or JBOSS (if needed)
     - R, A
     -
     -
     -
   * - Apply recommended hotfixes and service packs
     - R, A
     -
     -
     -
   * - Apply specific customer-requested hotfixes
     - R, A
     -
     -
     - C, I
   * - Configure and test Oracle Commerce Platform disaster recovery process
       (failover testing)
     - R, A
     -
     -
     -
   * - Configure Oracle Commerce Platform user administration,
       including:
          * User and group creation and management
          * SSO
          * Access control policy management
     -
     -
     -
     - R, A
   * - Configure advanced synthetic and static URL monitoring\*
     -
     -
     - R, A
     -
   * - Install application performance management (APM) tools\*
     -
     -
     - R, A
     -
   * - Provide read access to APM data\*
     -
     -
     - R, A
     -
   * - Configure SMS or robocall option for alerts\*
     -
     -
     - R, A
     -
   * - Provide an environment runbook template,
       including:
          * Contacts
          * Rackspace hosting
          * Customer
          * Vendors
          * Environment description
          * Application server configuration
     -
     - R, A
     - R, A
     -
   * - Add information to the customer runbook regarding procedures,
       including\*:
          * Build process
          * Monitoring configuration
          * Application deployment process
          * Standard deployment
          * Rollback procedure
          * Incident reporting
     -
     -
     - R, A
     -
   * - Populate the environment runbook
     -
     -
     -
     - R, A
   * - Create and migrate content
     -
     -
     -
     - R, A
   * - Define workflow management
     -
     -
     -
     - R, A
   * - Install and manage third-party plug-ins
     -
     -
     -
     - R, A
   * - Deploy custom code,
       including\*:
          * Deploy code (EAR file) to production by using an automated
            deployment tool
          * Roll back code by using an automated deployment tool
          * Deploy Endeca artifacts and initial baseline
          * Deploy static content to web servers (if defined and automated)
          * Perform basic site validation
     -
     -
     - R, A
     - C, I
   * - Define digital asset management policies
     -
     -
     -
     - R, A
   * - Conduct application smoke testing and quality assurance
     -
     -
     -
     - R, A
   * - Conduct performance load testing
     -
     - C, I
     - C, I
     - R, A
   * - Escalate Oracle Commerce Platform application issues to Oracle
     -
     - C, I
     - C, I
     - R, A
   * - Troubleshoot application server issues
     -
     - R, A
     - R, A
     -
   * - Provide guidance and insight with APM tool data,
       including\*:
          * Java profile (Heap, CPU, replication queues)
          * Application performance
          * Faster root-cause analysis
          * Business transaction errors
          * Bottleneck identification
          * Average response-time metrics
     -
     -
     - R, A
     -
   * - Provide tuning recommendations based on Oracle Commerce Platform
       best practices
     -
     - R, A
     - R, A
     -
   * - Provide recommendations on new Oracle Commerce Platform service packs
       and hotfixes
     -
     - R, A
     - R, A
     -
   * - Provide environment trend data for capacity planning\*
     -
     -
     - R, A
     -
   * - Provide reporting around the customer experience,
       including:
          * Understand how pages, Ajax requests, and iframes are performing
            over time
          * Gain insight into the performance of individual pages and requests
            as experienced by end users
          * Find the worst performing pages by using multiple common metrics
     -
     -
     - R, A
     -
   * - Provide application performance management software,
       with\*:
          * The ability to profile Java and .NET
          * An application performance dashboard
          * Bottleneck identification
     -
     -
     - R, A
     -

\* Not available without tools
