# OpenTelemetry Collector on Render

This Blueprint deploys a GRPC-listening oltp metrics collector, and a Prometheus instance that
receives and stores periodically the events collected. This allows a monitoring setup where
the monitoring deployment does not need any knowledge of its targets, and without needing to
expose a "Service Discovery" unit either.

These 2 advantages make it really easy to "just" point monitored services to this deployment
to enable metrics, even if you have Render autoscaling active which creates/kills instances
arbitrarily.


## Usage

- Each monitored service should use a OTLP metrics-enabled library, pushing GRPC payloads to
  the URL of the otelcol service.
