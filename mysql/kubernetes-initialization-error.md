## Initialization errors

When running into 137 exit codes for MySQL containers in Kubernetes,
be sure to add the following code to `/etc/mysql/conf.d`:

```[conf]
[mysqld]
skip-host-cache
skip-name-resolve
```

The settings above deactivate MySQL's DNS that doesn't play nice
with Kubernetes's DNS.

