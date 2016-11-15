## New features in PE 

### PE 2016.4: long-term support release

PE 2016.4 is the next consecutive release following PE 2016.2. PE 2016.4 has been designated as a long-term support release for customers who require longer testing periods between PE upgrades. PE 2016.4 will be fully supported (security releases, critical bug fixes, and full customer support) for 24 months from its general availability date.

### Corrective change reporting in the PE console

This release introduces corrective change reporting in the PE console. PE now differentiates between changes driven by updates to Puppet code (“intentional changes”) and changes made by Puppet to return a system to the desired state as defined by Puppet code (“corrective changes”). Use the console’s Overview page to quickly identify nodes that received corrective changes on the last Puppet run, and view details of corrective change events on the Reports page. Corrective change reporting is available only for Puppet agents running PE 2016.4.

### Puppet data collection

In order to better understand how you, our customers, are using PE, Puppet Server automatically collects basic data about your PE installation and sends it to Puppet. This data (click here to see what we collect) helps us improve our products and make decisions about the future of PE. If you wish to opt out of sending data to Puppet, see Opting out of Puppet Enterprise analytics.

### No-op mode run statuses in the PE console

Reporting in the PE console provides more granularity and context about no-op mode run performance. The Overview page now offers a breakdown of the run status of each node run in no-op mode on the last Puppet run. Filtering by no-op mode run status has also been added to the Reports page. No-op mode reporting is available only for Puppet agents that are running PE 2016.4.