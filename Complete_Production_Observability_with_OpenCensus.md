# Google Cloud Next 2019 Breakout: Complete Production Observability with OpenCensus
#gcp #cloud

- https://www.youtube.com/watch?v=259NX1-jrUQ

* TODO
	* **compare Zipkin vs. Prometheus vs. Jaeger**
* distributed tracing and metrics
	* context and tag propagation
* concerned with sending metrics to backend (exporters)
* can export to multiple backends at once
* will announce production readiness for python this month
	* see picture
![](images/20190411_090707.jpg)

* OpenCensus + OpenTracing merger = ?
	* new name at KubeCon EU
* candidate recommendation for W3C trace context specification
* OC (OpenCensus agent) = collects traces from apps and forwards to OC collector to forward to backends
	* see picture
![](images/20190411_091503.jpg)

* OpenCensus Client Libraries
	* instantiate tracer
	* setup exporter
	* define sampling policy
	* do work
		* create span
		* do actual work
		* end span
* OpenCensus Service
![](images/20190411_092041.jpg)

	* can be deployed as a binary, docker, kube sidecar
	* see picture for service performance
![](images/20190411_092356.jpg)

	* see picture for intelligent sampling
![](images/20190411_092504.jpg)
	* separate traces by
		* all traces
		* errors
* Distributed Tracing Demo
	* distributed hipster store app
		* see picture
![](images/20190411_092938.jpg)

	* construct hipster demo graph entirely from traces
		* see picture
![](images/20190411_093039.jpg)
* https://github.com/census-instrumentation
![](images/20190411_093350.jpg)
