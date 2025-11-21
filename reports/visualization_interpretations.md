# Visualization Interpretations

Generated: 2025-11-21 00:56:46Z UTC

## Dataset Summary

- **Shape**: Rows: 250000, Columns: 14
- **Numeric columns**: cpu_utilization_percent, memory_utilization_percent, storage_utilization_percent, network_throughput_gbps, active_sessions, requests_per_second, avg_response_time_ms, cache_hit_ratio_percent
- **Categorical columns**: edge_node_id, city, application, operator, load_status

## Dataset Column Descriptions

- **edge_node_id**: Unique identifier for the edge node (string; e.g., EDGELAG04).
- **operator**: Telecom operator managing the node (e.g., MTN, Airtel, Glo, 9mobile).
- **city**: City where the edge node is located (category; e.g., Lagos, Abuja).
- **application**: Workload/application category running on the node (e.g., video_analytics, cdn, gaming, ai_inference, ar_vr, iot_processing, content_caching).
- **timestamp**: UTC timestamp when the measurement was recorded (datetime).
- **load_status**: Discrete load class label (low, medium, high).
- **cpu_utilization_percent**: CPU utilization in percent [0–100].
- **memory_utilization_percent**: Memory utilization in percent [0–100].
- **storage_utilization_percent**: Storage utilization in percent [0–100].
- **network_throughput_gbps**: Observed network throughput in gigabits per second.
- **active_sessions**: Concurrent active user/device sessions (count).
- **requests_per_second**: Requests handled per second (rate).
- **avg_response_time_ms**: Average response latency in milliseconds.
- **cache_hit_ratio_percent**: Cache hit ratio in percent [0–100].

## Target Distribution (load_status)

- **low**: 124720 (49.888%)
- **medium**: 98416 (39.366%)
- **high**: 26864 (10.746%)

## Metric Trends vs load_status (median)

- **cpu_utilization_percent**: non-monotonic (low→high: 87.460 → 63.630)
- **memory_utilization_percent**: non-monotonic (low→high: 70.100 → 52.480)
- **storage_utilization_percent**: decreasing (low→high: 55.320 → 54.980)
- **network_throughput_gbps**: non-monotonic (low→high: 25.460 → 25.400)
- **active_sessions**: non-monotonic (low→high: 2753.500 → 1408.000)
- **requests_per_second**: non-monotonic (low→high: 5047.000 → 5038.500)
- **avg_response_time_ms**: increasing (low→high: 27.380 → 27.480)
- **cache_hit_ratio_percent**: non-monotonic (low→high: 77.535 → 77.500)

## Categories with Highest High-Load Share

- **operator** (top 10):
  - 9mobile: 0.395
  - Airtel: 0.395
  - Glo: 0.394
  - MTN: 0.391
- **city** (top 10):
  - Kano: 0.399
  - Port Harcourt: 0.394
  - Lagos: 0.392
  - Ibadan: 0.392
  - Abuja: 0.392
- **application** (top 10):
  - iot_processing: 0.399
  - ar_vr: 0.396
  - ai_inference: 0.394
  - gaming: 0.393
  - content_caching: 0.392
  - cdn: 0.392
  - video_analytics: 0.389
- **edge_node_id** (top 10):
  - EDGEKAN11: 0.420
  - EDGEPOR16: 0.420
  - EDGEKAN18: 0.418
  - EDGEABU08: 0.417
  - EDGEIBA16: 0.411
  - EDGEKAN03: 0.410
  - EDGEABU10: 0.409
  - EDGELAG08: 0.409
  - EDGELAG09: 0.406
  - EDGEKAN20: 0.406

## Peak High-Load Windows

- **Hours** with highest high-load share:
  - Hour 16: 0.675
  - Hour 13: 0.673
  - Hour 11: 0.670
  - Hour 9: 0.669
  - Hour 17: 0.667
  - Hour 12: 0.667
  - Hour 15: 0.667
  - Hour 14: 0.666
  - Hour 10: 0.664
  - Hour 18: 0.578
- **Days** with highest high-load share:
  - Mon: 0.397
  - Thu: 0.395
  - Tue: 0.394
  - Wed: 0.394
  - Fri: 0.393
  - Sun: 0.392
  - Sat: 0.391

## Correlation Highlights (Pearson)

- cpu_utilization_percent ↔ memory_utilization_percent: 0.762
- memory_utilization_percent ↔ active_sessions: 0.696
- cpu_utilization_percent ↔ active_sessions: 0.690
- avg_response_time_ms ↔ cache_hit_ratio_percent: -0.006
- network_throughput_gbps ↔ cache_hit_ratio_percent: 0.005
- storage_utilization_percent ↔ cache_hit_ratio_percent: 0.005
- requests_per_second ↔ cache_hit_ratio_percent: 0.004
- cpu_utilization_percent ↔ storage_utilization_percent: 0.004
- active_sessions ↔ cache_hit_ratio_percent: 0.003
- cpu_utilization_percent ↔ cache_hit_ratio_percent: 0.002
- cpu_utilization_percent ↔ requests_per_second: -0.002
- memory_utilization_percent ↔ network_throughput_gbps: 0.002
- network_throughput_gbps ↔ avg_response_time_ms: 0.001
- active_sessions ↔ avg_response_time_ms: 0.001
- cpu_utilization_percent ↔ network_throughput_gbps: -0.001

## Operator-Focused Insights

### Operator load_status distribution (proportions)

- **9mobile**: high: 10.731%, low: 49.746%, medium: 39.523%
- **Airtel**: high: 10.580%, low: 49.939%, medium: 39.481%
- **Glo**: high: 10.808%, low: 49.797%, medium: 39.395%
- **MTN**: high: 10.864%, low: 50.070%, medium: 39.067%

### Per-operator peak high-load windows

- **9mobile**:
  - Hour 9: 0.679
  - Hour 12: 0.677
  - Hour 10: 0.675
  - Hour 13: 0.674
  - Hour 16: 0.672
  - Days: Tue (0.404), Mon (0.399), Thu (0.396), Sat (0.394), Wed (0.394), Fri (0.391), Sun (0.386)
- **Airtel**:
  - Hour 11: 0.682
  - Hour 16: 0.678
  - Hour 10: 0.677
  - Hour 15: 0.669
  - Hour 13: 0.668
  - Days: Thu (0.403), Mon (0.402), Sun (0.397), Sat (0.395), Fri (0.392), Tue (0.389), Wed (0.388)
- **Glo**:
  - Hour 11: 0.673
  - Hour 16: 0.673
  - Hour 15: 0.671
  - Hour 12: 0.671
  - Hour 17: 0.669
  - Days: Wed (0.402), Mon (0.398), Tue (0.395), Fri (0.395), Sat (0.391), Sun (0.389), Thu (0.386)
- **MTN**:
  - Hour 13: 0.684
  - Hour 16: 0.677
  - Hour 17: 0.677
  - Hour 14: 0.668
  - Hour 9: 0.666
  - Days: Sun (0.395), Thu (0.394), Fri (0.393), Wed (0.391), Mon (0.390), Tue (0.387), Sat (0.384)

### Per-operator metrics with largest low→high increase (median)

- **9mobile**:
  - active_sessions: 337.000 → 1412.000 (319.0%)
  - memory_utilization_percent: 32.800 → 52.380 (59.7%)
  - cpu_utilization_percent: 39.980 → 63.740 (59.4%)
  - requests_per_second: 5014.000 → 5066.000 (1.0%)
  - avg_response_time_ms: 27.380 → 27.630 (0.9%)
- **Airtel**:
  - active_sessions: 337.000 → 1405.000 (316.9%)
  - memory_utilization_percent: 32.690 → 52.405 (60.3%)
  - cpu_utilization_percent: 40.020 → 63.580 (58.9%)
  - avg_response_time_ms: 27.310 → 27.515 (0.8%)
  - cache_hit_ratio_percent: 77.420 → 77.765 (0.4%)
- **Glo**:
  - active_sessions: 338.000 → 1416.000 (318.9%)
  - memory_utilization_percent: 32.740 → 52.630 (60.8%)
  - cpu_utilization_percent: 39.830 → 63.630 (59.8%)
  - storage_utilization_percent: 55.140 → 55.075 (-0.1%)
  - cache_hit_ratio_percent: 77.185 → 77.050 (-0.2%)
- **MTN**:
  - active_sessions: 339.000 → 1396.000 (311.8%)
  - memory_utilization_percent: 32.810 → 52.510 (60.0%)
  - cpu_utilization_percent: 39.890 → 63.590 (59.4%)
  - requests_per_second: 5022.500 → 5042.000 (0.4%)
  - avg_response_time_ms: 27.510 → 27.610 (0.4%)

### Per-operator top cities and applications by high-load share

- **9mobile**:
  - Cities: Kano (0.404), Port Harcourt (0.396), Abuja (0.393), Lagos (0.392), Ibadan (0.392)
  - Apps: iot_processing (0.407), ai_inference (0.401), video_analytics (0.395), cdn (0.393), content_caching (0.391)
- **Airtel**:
  - Cities: Kano (0.403), Ibadan (0.397), Port Harcourt (0.394), Abuja (0.391), Lagos (0.389)
  - Apps: content_caching (0.397), iot_processing (0.396), gaming (0.396), ar_vr (0.396), cdn (0.395)
- **Glo**:
  - Cities: Lagos (0.400), Abuja (0.394), Port Harcourt (0.394), Ibadan (0.391), Kano (0.391)
  - Apps: ar_vr (0.397), ai_inference (0.396), cdn (0.396), iot_processing (0.396), content_caching (0.393)
- **MTN**:
  - Cities: Kano (0.398), Port Harcourt (0.392), Abuja (0.388), Ibadan (0.388), Lagos (0.388)
  - Apps: ar_vr (0.399), gaming (0.399), iot_processing (0.395), ai_inference (0.389), content_caching (0.387)

## Operator-Level Conclusions

- **High-load share varies slightly by operator**: 39.067% (MTN) to 39.523% (9mobile).
- **Peak high-load hours cluster in the evening**: 9:00–13:00 across operators.
- **Metrics that rise most from low→high**: active_sessions (~311.8%→319.0% increase), memory_utilization_percent (~59.7%→60.8% increase), cpu_utilization_percent (~58.9%→59.8% increase).
- **Recurring city hotspots**: Kano (3 ops), Lagos (1 ops).
- **Recurring application hotspots**: ar_vr (2 ops), iot_processing (1 ops).