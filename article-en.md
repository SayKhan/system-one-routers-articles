# The Rise of Intelligent Networks: What Happens When Every Router Can Run System One Models

## Introduction

In 2026 a new class of AI models called **System One** (or System 1) models appeared. Unlike traditional large language models that generate text token by token, System One models return typed, probabilistic decisions in a single forward pass. They are designed for fast classification, scoring, routing and extraction tasks.

This architectural difference makes them dramatically faster and cheaper for decision workloads. The natural next question is: what happens if we put these models not only in the cloud, but directly onto network routers — and eventually onto every hop in the path?

## What Are System One Models?

System One models (starting with TypeSafe AI’s Jev and followed by open alternatives such as Laya, basal and others) specialise in structured decisions:

- Choice (pick one option from a list)
- Score (rate on a scale)
- Noul (yes/no with probability)
- Extraction of typed values

Because they skip autoregressive text generation, typical end-to-end latency is 70–500 ms on hosted APIs and can drop to tens of milliseconds for small quantised open models running locally. Independent benchmarks often show 3–10× speedups versus small LLMs and higher gains versus frontier models on pure decision tasks.

## Running System One Models on Routers

Modern routers are not powerful enough for large generative models, but they are increasingly capable of running lightweight decision models:

- Home and CPE routers can host very small quantised classifiers.
- Enterprise, SD-WAN and ISP edge devices have enough compute (or NPUs) for practical System One-style models.
- Lightweight traffic classification models already achieve sub-20 ms inference on constrained hardware.

The models would not sit in the pure data plane (packet forwarding still happens in hardware at microsecond speeds). They would operate at the flow and control-plane level: classifying sessions, applying policies, scoring urgency and making routing or QoS decisions.

## Opportunities When Every Hop Can Decide

If new routers across the entire path (home → ISP → backbone → destination) can run System One models, several new capabilities emerge:

### 1. End-to-End Application-Aware QoS
Every hop can consistently recognise and prioritise traffic types (gaming, video calls, real-time control, bulk downloads). Priority is no longer lost after the first router. Under congestion this can meaningfully reduce latency and jitter for latency-sensitive applications.

### 2. Intent-Based Networking
Users or applications declare high-level goals (“low latency for this game”, “prioritise this video call”). Fast decision models translate and enforce those intents across domains without constant human configuration.

### 3. Adaptive Path Selection
Routers can choose routes not only by traditional metrics but by current application requirements, measured congestion, cost or privacy constraints. Multi-WAN and SD-WAN become significantly smarter.

### 4. Distributed Security and Filtering
Anomaly detection, malware scoring and content classification can happen closer to the source, reducing load on central systems and improving reaction time.

### 5. Intelligent Routing of AI Traffic
Inference requests can be steered to the nearest suitable edge or cloud location based on model availability, current load and latency budgets.

### 6. More Local Decisions, Better Privacy and Resilience
A larger share of classification and policy decisions can be made on-device or on-premises, reducing round-trips and exposure of metadata.

### 7. New Service Offerings
ISPs and enterprises can offer “guaranteed experience” tiers for specific applications, dynamic SLAs that the network can actually enforce, and premium intelligent connectivity products.

## Limitations and Realism

- Raw bandwidth does not increase.
- Packet forwarding remains hardware-accelerated; AI assists policy and flow decisions.
- Full consistency across operators requires standards and trust.
- Home routers will only run the lightest models; heavier decisions stay on stronger nodes.
- The transition is evolutionary, not overnight.

## Conclusion

Deploying System One models on routers does not magically make the internet faster in megabits. It makes the network **smarter**. When decision capability exists at every hop, the internet can become application-aware and intent-driven. Interactive traffic (games, calls, real-time control) becomes more stable under load, operators gain new service possibilities, and a larger portion of intelligence moves closer to the edge.

This is the practical path toward AI-native networking.

---

*Article based on discussions around System One models (2026) and their potential application in networking infrastructure.*
