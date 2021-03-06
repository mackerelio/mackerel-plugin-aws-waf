mackerel-plugin-aws-waf
=======================

AWS WAF custom metrics plugin for mackerel.io agent.

## Synopsis

```shell
mackerel-plugin-aws-waf -web-acl-id=<aws-waf-web-acl-id> [-access-key-id=<id>] [-secret-access-key=<key>] [-region=<region>] [-tempfile=<tempfile>]
```

## AWS IAM Policy
the credential provided manually or fetched automatically by IAM Role should have the policy that includes an action, 'cloudwatch:GetMetricStatistics'

## Installation
- `mkr plugin install mackerelio/mackerel-plugin-aws-waf`
- Or download binary in Github Releases

## Example of mackerel-agent.conf

```
[plugin.metrics.aws-waf]
command = "/path/to/mackerel-plugin-aws-waf -web-acl-id=your-web-acl-id"
```
