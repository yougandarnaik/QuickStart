## Enhancements in PE

### Puppet orchestrator enhancements

* You can now directly enforce change to selections of your infrastructure with the Puppet orchestrator. This version of PE adds the ability to run orchestrator jobs against the following targets:
        
        Nodes derived from a Puppet Query Language (PQL) query.

        A specific node or list of nodes.

        A single instance or all instances of an application in an environment.

* Puppet Application Orchestration and the orchestration service are now enabled by default in PE.

### Platform enhancements

* The MCollective metadata refresh cron job has been improved so that when it’s created, it’s created with a random minute. Previously the cron job was created with a fixed runtime of 0, 15, 30, or 45 minutes. Now the load of running the job is spread evenly across time. If you are upgrading from a   previous version of PE you can expect to see most agents change this cron resource.

* When installing PE agents on *nix-based systems, you can pass parameters to the install script to specify configuration settings for inclusion in custom_attributes and extension_requests sections of csr_attributes.yaml. See Passing configuration parameters to the install script for an example.
  
### Console enhancements

* On the Nodes > Classification page, a hierarchical view replaces the previous alphabetical list.

* Timestamps in the console can be displayed in local time, with UTC time shown on hover.

* The Overview page provides a count of nodes on which one or more resources were enforced during the last Puppet run in no-op mode. Enforced resources are created when the noop => false metaparameter setting is used on no-op mode runs.

### Code Manager and r10k enhancements

* We’ve improved support for managing non-module content, such as Hiera data, with Code Manager and r10k. The Puppetfile includes an install_path option you can set for any Git repository you declare. This allows you to declare non-module content in your Puppetfile, and then use the install_path      option to install it in your environment outside of the “modules” directory.

* This release adds the ability to track a control repo branch relative to the environment your Puppetfile is in. This means that when you create new branches from an existing branch of your control repo, you can have environment-specific content directed by the Puppetfile without having to edit      the new Puppetfile.

* The puppet-code command now supports Windows and OSX systems. See puppet-code documentation for usage details.

* For r10k, you can specify the levels at which r10k purges unmanaged content during deployment. See the purge_levels parameter for details.

### PE client tools enhancements

* You can now run PE client tools on Windows and OS X. See the client tools installations instructions for more information.

### API enhancements

* When generating an authentication token, you can affix a plain-text, user-specific label to the token. Use this label to more readily refer to the token when working with RBAC API endpoints, or when revoking your own token.

* The DELETE /roles/<rid> endpoint in the v1 RBAC service API no longer requires the use of the Content-Type header.
