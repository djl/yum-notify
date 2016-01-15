# yum-notify

A tiny script to notify you about pending package updates.


## Usage

Basic usage:

    $ yum-notify
    24 package updates available:

    bind-libs-lite
      Summary: Libraries for working with the DNS protocol
      Current: 32:9.9.4-29.el7
      Available: 32:9.9.4-29.el7_2.1
      Changelog: Fix CVE-2015-8000
    bind-license
      Summary: License of the BIND DNS suite
      Current: 32:9.9.4-29.el7
      Available: 32:9.9.4-29.el7_2.1
      Changelog: Fix CVE-2015-8000
    ...

The `-c/--changelog` option will include the first line of the changelog:

    $ yum-notify -c
    24 package updates available:

    bind-libs-lite
      Summary: Libraries for working with the DNS protocol
      Current: 32:9.9.4-29.el7
      Available: 32:9.9.4-29.el7_2.1
      Changelog: Fix CVE-2015-8000


By default `yum-notify` will print to stdout. Use `-m/--mailto` to send it somewhere else:

    $ yum-notify -m root
    $
