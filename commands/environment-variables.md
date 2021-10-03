# Environment variables

Environment variables are used to control various behaviours within the sfpowerscripts orchestrator, including Git author details and logging of metrics.  To learn how to set an environment variable, refer to the documentation of your shell. 

| Name | TYPE | Default | Description |
| :--- | :--- | :--- | :--- |
| `SFPOWERSCRIPTS_GIT_USERNAME` | String | sfpowerscripts | Set the username of commit author and tagger in git config  |
| `SFPOWERSCRIPTS_GIT_EMAIL` | String | sfpowerscripts@dxatscale.io | Set the email of commit author and tagger in git config |
| `SFPOWERSCRIPTS_ARTIFACT_PACKAGE` | String | 04t1P000000ka9mQAA | Set the subscriber package version ID of the Sfpowerscripts Artifact package that is installed in pooled scratch orgs |
| `SFPOWERSCRIPTS_STATSD` | Bool | false | Enable logging of metrics through StatsD |
| `SFPOWERSCRIPTS_STATSD_HOST` | String |  | Host address of StatsD agent  |
| `SFPOWERSCRIPTS_STATSD_PORT` | Num | 8125 | Port number of StatsD agent |
| `SFPOWERSCRIPTS_STATSD_PROTOCOL` | String | udp | Set the transport layer protocol \(tcp/udp\) of the StatsD agent |
| `SFPOWERSCRIPTS_DATADOG` | Bool | false | Enable logging of metrics through native Datadog API |
| `SFPOWERSCRIPTS_DATADOG_HOST` | String |  | Host address of Datadog API endpoint |
| `SFPOWERSCRIPTS_DATADOG_API_KEY` | String |  | API key for authorization to the Datadog API endpoint |
| `SFPOWERSCRIPTS_NEWRELIC` | Bool | false | Enable logging of metrics through native New Relic API |
| `SFPOWERSCRIPTS_NEWRELIC_API_KEY` | String |  | API key for authorization to the New Relic API endpoint |



