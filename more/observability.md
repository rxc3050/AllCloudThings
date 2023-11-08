observability.md

# Observability & Monitoring
```
Observability - 
Observability refers to the ability to measure and observe the 
internal state of a software system through data like metrics, logs, and traces. 
It provides visibility into a system's behavior to more easily monitor and 
troubleshoot issues.

Monitoring - 
Monitoring involves collecting metrics and data on a system's performance and health. 
It allows detecting problems and setting alerts around critical events. 
Effective monitoring is key for identifying and diagnosing issues promptly.

Logging - 
Logging refers to recording meaningful events within an 
application's code during execution. Logs provide insights into 
system operations, errors, and user activities. Log data is essential 
for monitoring and observability.

Tracing - 
Tracing follows the path of a request through all the microservices, 
servers, and processes that handle parts of that request. 
Tracing distributed transactions helps pinpoint performance bottlenecks and failures.

Metrics - 
Metrics represent measurements and counts of key activities 
and resources within a system. They allow assessing overall health and 
performance over time. Common metrics include response times, 
error rates, resource usage etc.

Alerting - 
Alerting involves getting notifications when certain metrics 
cross defined thresholds. This allows rapid awareness of problems so 
corrective action can be taken. Alerts are triggered by monitoring systems 
based on log, metric, and tracing data.
```

## Logs vs Metrics vs Traces

```text
Metrics:
The purpose of metrics is to inform observers about the health & operations 
regarding a component or system. A metric represents a point in time measure 
of a particular source, and data-wise tends to be very small. 
The compact size allows for efficient collection even at scale in large systems. 
Metrics also lend themselves very well to pre-aggregation within the 
component before collection, reducing computation cost for processing & storing
large numbers of metric time series in a central system. Due to how efficiently 
metrics are processed & stored, it lends itself very well for use in automated 
alerting, as metrics are an excellent source for the health data for 
all components in the system.

Logs:
Log data inform observers about the discrete events that occurred 
within a component or a set of components. Just about every software component 
log information about its activities over time. This rich data tends to be 
much larger than metric data and can cause processing issues, especially 
if components are logging too verbosely. Therefore, using log data to 
understand the health of an extensive system tends to be avoided and 
depends on metrics for that data. Once metric telemetry highlights 
potential problem sources, filtered log data for those sources 
can be used to understand what occurred.

Traces:
Where logging provides an overview to a discrete, event-triggered log, 
tracing encompasses a much wider, continuous view of an application. 
The goal of tracing is to following a program’s flow and data progression.

In many instances, tracing represents a single user’s journey 
through an entire app stack. Its purpose isn’t reactive, but 
instead focused on optimization. By tracing through a stack, 
developers can identify bottlenecks and focus on improving performance.

A distributed trace is defined as a collection of spans. 
A span is the smallest unit in a trace and represents a 
piece of the workflow in a distributed landscape. 
It can be an HTTP request, call to a database, or execution of a 
message from a queue.

When a problem does occur, tracing allows you to see how you got there:

Which function.
The function’s duration.
Parameters passed.
How deep into the function the user could get.
```

## Logging Level

```text
A log level indicates the importance of a log message. 
It allows you to filter critical information from noise. 
Log levels originated in the 1980s with syslog for Unix. 
Syslog defined severity levels like 
-Emergency, 
-Alert, 
-Critical, 
-Error, 
-Warning, 
-Notice, 
-Informational,
-Debug. 
These are now standard log levels used across many programming languages 
and logging frameworks.

Log levels help reduce information overload and alarm fatigue. 
Looking at the severity level first tells you if a log requires immediate action. 
Proper use of log levels separates high priority alerts from routine diagnostic info.

Modern frameworks allow logging data in formats like JSON. 
Logs can be sent to various destinations beyond syslog, like files or Elasticsearch. 
But most retain the concept of log levels to indicate event importance. 
The hierarchy from Emergency to Debug helps flag the most urgent system issues 
versus detailed tracing. 
Appropriate log levels improve monitoring and observability by controlling the 
verbosity and contents of log output.
```

- Log-Level Hierarchy
	- in most logging frameworks following are some of the log levels:
		- TRACE
		- DEBUG
		- INFO
		- WARN
		- ERROR
		- FATAL
		


## Userful Links

- log-level hierarchy
	- [log-levels](https://sematext.com/blog/logging-levels/#:~:text=You%20can%20expect%20the%20TRACE,with%20parameters%20in%20your%20code.&text=INFO%20%E2%80%93%20the%20standard%20log%20level,entered%20a%20certain%20state%2C%20etc.)
```text
Log-Level Hierarchy:
```	

- Metrics vs logs vs traces: 
	- [logsvsmetricsvstrace](https://microsoft.github.io/code-with-engineering-playbook/observability/log-vs-metric-vs-trace/)

