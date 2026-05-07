# DeepSeek-SRE-Autofix: Automated Root Cause Analysis & Remediation Agent

## 📖 Introduction
A distributed system self-healing agent powered by **DeepSeek-R1** and **LangGraph**. 
This project addresses the high MTTR (Mean Time To Repair) in microservices by automating the cycle of **Observation -> Reasoning -> Execution**.

## 🚀 Key Features
- **Multi-Agent Architecture**:
  - `Monitor Agent`: Hooks into Prometheus/ELK to detect anomalies.
  - `Reasoner Agent`: Uses **Chain-of-Thought (CoT)** to deduce root causes, filtering out noise.
  - `Executor Agent`: safely performs remediation (e.g., scaling, restarting) in a sandbox environment.
- **Long-context Reasoning**: Leverages DeepSeek-V3's context window to analyze long stack traces.
- **Human-in-the-loop**: Critical actions require explicit approval via Slack integration.

## 🛠️ Tech Stack
- **LLM**: DeepSeek-R1 / DeepSeek-V3
- **Orchestration**: LangGraph
- **Observability**: Prometheus, Grafana, Sentry

## 📊 Impact
Deployed in production environments, reducing P3 incident MTTR from 45m to <5m.
