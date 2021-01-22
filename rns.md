- [DB Upgrade Service Configuration](#_DB_Upgrade_Service)
  - [DBUS Configuration: 1.0.188](#_DBUS_Configuration:_1.0.188)
  - [DBUS Configuration: 1.0.164](#_DBUS_Configuration:_1.0.164)
  - [DBUS Configuration: 1.0.147](#_DBUS_Configuration:_1.0.147)
  - [DBUS Configuration: 1.0.146](#_DBUS_Configuration:_1.0.146)
  - [DBUS Configuration: 1.0.140](#_DBUS_Configuration:_1.0.140)
  - [DBUS Configuration: 1.0.136](#_DBUS_Configuration:_1.0.136)
  - [DBUS Configuration: 1.0.132](#_DBUS_Configuration:_1.0.132)
  - [DBUS Configuration: 1.0.132](#_DBUS_Configuration:_1.0.132)
  - [DBUS Configuration: 1.0.128](#_DBUS_Configuration:_1.0.128)
  - [DBUS Configuration: 1.0.108](#_DBUS_Configuration:_1.0.108)
  - [DBUS Configuration: 1.0.80](#_DBUS_Configuration:_1.0.80)
  - [DBUS Configuration: 1.0.73](#_DBUS_Configuration:_1.0.73)
  - [DBUS Configuration: 1.0.59](#_DBUS_Configuration:_1.0.59)
  - [DBUS Configuration: 1.0.51](#_DBUS_Configuration:_1.0.51)
  - [DBUS Configuration: 1.0.46](#_DBUS_Configuration:_1.0.46)
  - [DBUS Configuration: 1.0.22](#_DBUS_Configuration:_1.0.22)
- [DB Upgrade Service](#_DB_Upgrade_Service_1)
  - [DBUS Version: 1.0.224](#_DBUS_Version:_1.0.224)
  - [DBUS Version: 1.0.222](#_DBUS_Version:_1.0.222)
  - [DBUS Version: 1.0.214](#_DBUS_Version:_1.0.214)
  - [DBUS Version: 1.0.207](#_DBUS_Version:_1.0.207)
  - [DBUS Version: 1.0.189](#_DBUS_Version:_1.0.189)
  - [DBUS Version: 1.0.181](#_DBUS_Version:_1.0.181)
  - [DBUS Version: 1.0.164](#_DBUS_Version:_1.0.164)
  - [DBUS Version: 1.0.157](#_DBUS_Version:_1.0.157)

|
# **DB Upgrade Service Configuration**
 |
| --- |
|
## DBUS Configuration: 1.0.188
**December 15, 2020** |
| **Agile Studio reference** | **Enhancement** |
| _US-387268_ | Unify DBUS deployment |
| _US-375517_ | Remove RDS CA Certificate update |
|
## DBUS Configuration: 1.0.164
**July 3, 2020** |
| **Agile Studio reference** | **Change or enhancement** |
| _BUG-554926_ | Changed flow to execute rolling restart after upgrade |
|
## DBUS Configuration: 1.0.147
**January 28, 2020** |
| **Agile Studio reference** | **Change or enhancement** |
| _US-342791_ | Modified exceptions handling raised by get-instances lambda |
|
## DBUS Configuration: 1.0.146
**January 21, 2020** |
| _US-342407_ | Modify timeout to 5s for curl in docker-check-health  |
| _US-338670_ | Refactor subflow versioning |
|
## DBUS Configuration: 1.0.140
**January 7, 2020** |
| _ISSUE-70975_ | A dry run doesn&#39;t check Pega environment health |
| _US-341368_ | Introduced 5 retries on Pega health check verification after ASG has been enabled |
| _US-341368_ | Minor timeout changes  |
|
## DBUS Configuration: 1.0.136
**December 25, 2019** |
| _US-330553_ | Reducing the number of AWS API calls to the AWS autoscaling API |
|
##  DBUS Configuration: 1.0.132
  **December 16, 2019** |
| _US-337246_ | Modified pega-health subflow to perform additional checks  |
|
## DBUS Configuration: 1.0.128
**December 12, 2019** |
| _BUG-528250_ | **Bugfix** : Fixed script for PostGIS check/removal |
| _BUG-527559_ | **Bugfix** : Improved Pega Health check script |
|
## DBUS Configuration: 1.0.108
**December 5, 2019** |
| _US-336869_ | Support for an upgrade to PG 11.5 from PG 9.4.20,9.6.11,11.1,11.4 |
| _-_ | Upgrades to PG 11.5 were extended for change of the RDS certificate |
| _-_ | Dry run functionality for PG 11.5 has been extended to verify if the environment has ForceSSL set and if true if the version is at least 2.14 (  **Note that the service is unable to distinguish between 2.14.1 and 2.14.3**  )
 |
| _-_ | Dry run has been extended to perform actual Pega Ping to verify the health of the environment before the upgrade
 |
| _US-321554_ | All upgrade flows have been divided into a collection of smaller flows (subflows) |
| _-_ | Extended error reporting by marking failed subflows in a service API response
 |
| _-_ | Even after a failed upgrade, the Autoscaling processes are enabled
 |
| _-_ | Additional verification has been implemented that verity&#39;s if the enabled autoscaling processes (and the instance replacement potentially caused by it) did not move the environment into a healthy state
 |
| _-_ | With the introduction of subflows logging streams in CloudWatch logs have been reorganized
 |
| As part of _SR-D66017_ | **Bugfix:**  Creating downtimes in DD monitoring has been deployed
 |
| DBUS Configuration: 1.0.85
**November 22, 2019** |
| _BUG-521280_ | **Bugfix:**  Log sending from script failed |
| _BUG-527559_ | **Bugfix:**  DBUS marks the instance as unhealthy after upgrade too soon |
|
##  DBUS Configuration: 1.0.80
**November 6, 2019** |
| _US-330556_ | Kafka&#39;s health is verified after DB Upgrade  |
|
##  DBUS Configuration: 1.0.73
  **November 1, 2019** |
| _US-329902_ | Block DB upgrades to Postgres 11.4 from PG 9.4.20 and 9.6.11 on cloud infrastructure 2.12 |
| _US-329902_ | Upgrades to Postgres 11.4 from PG 9.4.20 and 9.6.11 available on cloud infrastructure 2.13 |
| _US-329924_ | Checking RDS version after every upgrade |
| _US-330557_ | Improved pega health-check on post-DB upgrade actions |
| _BUG-518262_ | **Bugfix: **&quot;Check if Postgis plugin installed&quot; returns accurate exit code |
|
## DBUS Configuration: 1.0.59
**October 1, 2019**   |
| _US-326328_ | Added support of PG11 for Pega 7.2 and Pega 7.3 |
| _ISSUE-66494_ | Correction of Data sync pipeline |
|
## DBUS Configuration: 1.0.51
**September 6, 2019**
  |
| **-** | Added support for Hong Kong Region
 |
| _ISSUE-65221_ | Pg stat statements added after upgrade to 11.1 in upgrade flow 9.4.20 to 11.4 and 9.6.11 to 11.4 |
| _ISSUE-65221_ | Added new fail state for failing PG plugin update in upgrade 9.4.20 to 11.4 |
|
##  DBUS Configuration: 1.0.46
**August 15, 2019** |
| _ISSUE-64474_ | Moved flow integration tests execution from a pipeline to a script |
| _ISSUE-64704_ | **Bugfix** : Fix &quot;invalid option name&quot; message in SSM script |
|
## DBUS Configuration: 1.0.22
**August 13, 2019** |
| _ISSUE-64633_ | Added production deployment pipeline |
| _ISSUE-64472_ | Added timeouts to Jenkins pipelines |
| _ISSUE-64053_ | Send email notification when a master build fails |
| _ISSUE-63912_ | Changed version to 1.0.x |

|
# **DB Upgrade Service**
 |
| --- |
|
## CC-104863
** ** DBUS Version: 1.0.264
**December 30, 2020 - ** |
| Agile Studio reference | **Change or enhancement** |
| _ **US-387268** _ | Unify DBUS deployment |
| _ **US-375517** _ | Remove RDS CA Certificate update |
|
##  CC-88711 DBUS Version: 1.0.236
**July 3 2020** |
| _ **BUG-554926** _ | Added PeRollingRestart lambda to allow rolling restarts of tiers + fixing Sonar issues |
|
## DBUS Version: 1.0.224
**February 12, 2020****   ****SR-D78308** |
| _ **US-342791** _
 | Added instances state filtering to get-instances lambda  |
| Error statuses replaced with exceptions raised |
| _**US-342773)**_ | Introduce new deliveryTimeout variable |
|
## DBUS Version: 1.0.222
**January 20, 2020** |
| _ **ISSUE-70647** _ | Log info about unhealthy instances and set healthy state just before resuming autoscaling processes  |
| _ **US-341437** _ | Validate if each of environment&#39;s SCE is healthy before starting the DB upgrade |
| _ **US-338670** _ | Refactor subflow versioning |
|
##  DBUS Version: 1.0.214
**December 25, 2019** |
| _ **US-330553** _ | Reducing the number of AWS API calls to the AWS autoscaling API |
| _ **BUG-527140** _ | **Bugfix** : Read correct cause and error for UpgradeStatusEvent, when execution timed out |
| _ **BUG-527065** _ | **Bugfix** : Pass dryRun parameter as a boolean to AWSStepFunctions to detect unhealthy environments |
| _ **BUG-525141** _ | **Bugfix** : Wait until RDS becomes available before cleanup in integTests |
|
## DBUS Version: 1.0.207
**December 9, 2019** |
| _ **US-321565** _ | Added support of sub-flows to db-upgrade lambda |
| _ **US-321554** _ | Use sub-flows in db-upgrade service  |
| _ **ISSUE-69427** _ | Integrate US-320945 (replace instances by ASG) into new subflows |
| _ **US-336869** _ | DB Upgrade service changes the certificate during an upgrade to 11.5 |
| _ **BUG-521275** _ | **Bugfix** : Wrong script logging in restart pega web containers task |
| _ **BUG-492548** _ | **Bugfix** : Retain logs in case of PE build failure  |
| _ **BUG-520373** _ | **Bugfix** : Email notifications are not sent when new PE is built |
|
## DBUS Version: 1.0.189
**November 6, 2019** |
| _ **US-328334** _ | Set minimal access rights set on all db-upgrade service lambdas |
| _ **US-329924** _ | Check database version directly from RDS  |
| _ **ISSUE-65480** _ | Added SonarQube to db-upgrade service  |
|
## DBUS Version: 1.0.181
**September 24, 2019** |
| | Added support for Hong Kong Region |
| _ **ISSUE-65786** _ | Move the SOP document from git to Pega Box |
| _ **ISSUE-65970** _ | Corrected validation service bucket name in research |
|
## DBUS Version: 1.0.164
**August 13, 2019** |
| _ **ISSUE-64482** _ | Log to stdout using AWS&#39;s Lambda appender instead of CloudWatchAppender |
| _ **ISSUE-64053** _ | Send email notification when a master build fails |
| _ **US-312998** _ | Added CFN to supported-db-target lambda, added SupportedDbTargets to outputs of SCE |
| _ **ISSUE-63912** _ | Changed version to 1.0.x |
| _ **BUG-503990** _ | **Bugfix** : Throttling exception handling fixed |
| _ **BUG-503703** _ | **Bugfix** : Lambda upgradeDb creates logs in an incorrect region |
|
##  DBUS Version: 1.0.157
**August 7, 2019** |
| _ **US-314129** _ | Improved UpgradeEnvironmentDbStatus error messages |
| _ **ISSUE-63852** _ | Improved throttling handling |
| _ **ISSUE-63762** _ | Added configurationVersion to flow parameters and UpdateStatus |
| _ **ISSUE-63204** _ | Added State Machnie ARN logging |
| _ **BUG-499419** _ | **Bugfix** : UpgradeEnvironmentDbStatus API not returning flowErrorCause  |
