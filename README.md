# GOsa² Plugin: NIS Netgroups Management

This plugin for GOsa² provides you with a UI to manage LDAP based NIS netgroups.

## Installation Instructions

*Openldap schemas needed:* nis.schema or rfc2307bis.schema

Changes in ``gosa.conf``:

In GOsa's menu definition:

```
    <section name="Administration">
    <plugin...
    <plugin...
    ...
    <plugin acl="netgroup" class="netgroupManagement" />
```

In Tab definitions:

```
  <!-- Netgroup dialog -->
  <netgrouptabs>
    <tab class="netgroup" name="Generic" />
  </netgrouptabs>
```

And in Location definition:

```
<location name="XXXXX"
	...
	...
	...
	userRDN=...
	groupsRDN=...
	netgroupRDN="Your DN or SUBDN for netgroups"
```

If you want to choose the NIS Netgroup of a user from the user interface you also must change this:

```
  <usertabs>
     <tab...
     <tab...
     ...
     <tab class="netgroupAccount" name="NIS Netgroup" />
```

If you want to choose the NIS Netgroup of a system (server, workstation or network device) from the user interface you also must change this:

```
  <servtabs>
     <tab...
     <tab...
     ...
     <tab class="netgroupSystem" name="NIS Netgroup" />
```

```
  <worktabs>
     <tab...
     <tab...
     ...
     <tab class="netgroupSystem" name="NIS Netgroup" />
```

```
  <componenttabs>
     <tab...
     <tab...
     ...
     <tab class="netgroupSystem" name="NIS Netgroup" />
```


## More Information

GIT: https://github.com/gosa-project/gosa-plugins-netgroups/

## Author & Credits

The NIS netgroups plugin has originally been written by Alejandro
Escanero Blanco in 2011 for the Debian Edu project.
