# Overview

Vertice is a Jenkins CLI wrapper

# Requirements

Use the config for setting username. Go Jenkins - Profile - Configure - Show Token.

# Usage

`./vertice -h`

# Examples

`./vertice -r uninstall`

# Job Example

~~~~
RULES='
{
  "rules": [{
	"rule": {
		"url": "https://$JENKINS/eagle/job/$SERVER/job/$REGION/job/$ENV/job/uninstallPackage/build?delay=0sec",
		"parameters": [
			{ "sideState": "active" },
			{ "packageName": "cluster-splunkforwarder-hvc" },
			{ "appId": "cluster-splunkforwarder-hvc" },
			{ "product": "cluster01" },
			{ "tier": "stage" },
			{ "region": "ew1" },
			{ "flow": "uninstallPackage" }
		]
	}
}]
}
'
~~~~

# Author

Alejandro Sanchez Acosta <sancheza@adobe.com>
