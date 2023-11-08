observability.md

# Observability


## Links

- log-level hierarchy
	- [log-levels](https://sematext.com/blog/logging-levels/#:~:text=You%20can%20expect%20the%20TRACE,with%20parameters%20in%20your%20code.&text=INFO%20%E2%80%93%20the%20standard%20log%20level,entered%20a%20certain%20state%2C%20etc.)

- Metrics vs logs vs traces: 
	- [logsvsmetricsvstrace](https://microsoft.github.io/code-with-engineering-playbook/observability/log-vs-metric-vs-trace/)
	- ```text
	Metrics
The purpose of metrics is to inform observers about the health & operations regarding a component or system. A metric represents a point in time measure of a particular source, and data-wise tends to be very small. The compact size allows for efficient collection even at scale in large systems. Metrics also lend themselves very well to pre-aggregation within the component before collection, reducing computation cost for processing & storing large numbers of metric time series in a central system. Due to how efficiently metrics are processed & stored, it lends itself very well for use in automated alerting, as metrics are an excellent source for the health data for all components in the system.

Logs
Log data inform observers about the discrete events that occurred within a component or a set of components. Just about every software component log information about its activities over time. This rich data tends to be much larger than metric data and can cause processing issues, especially if components are logging too verbosely. Therefore, using log data to understand the health of an extensive system tends to be avoided and depends on metrics for that data. Once metric telemetry highlights potential problem sources, filtered log data for those sources can be used to understand what occurred.

Traces
Where logging provides an overview to a discrete, event-triggered log, tracing encompasses a much wider, continuous view of an application. The goal of tracing is to following a program’s flow and data progression.

In many instances, tracing represents a single user’s journey through an entire app stack. Its purpose isn’t reactive, but instead focused on optimization. By tracing through a stack, developers can identify bottlenecks and focus on improving performance.

A distributed trace is defined as a collection of spans. A span is the smallest unit in a trace and represents a piece of the workflow in a distributed landscape. It can be an HTTP request, call to a database, or execution of a message from a queue.

When a problem does occur, tracing allows you to see how you got there:

Which function.
The function’s duration.
Parameters passed.
How deep into the function the user could get.
	```
