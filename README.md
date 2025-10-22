# 🌐 EdgeNodeX

[![Build Status](https://img.shields.io/github/actions/workflow/status/<usuario>/prod-edgenodex-edge-go/build.yml?branch=main)](https://github.com/<usuario>/prod-edgenodex-edge-go/actions)
[![Coverage](https://img.shields.io/codecov/c/github/<usuario>/prod-edgenodex-edge-go)](https://codecov.io/gh/<usuario>/prod-edgenodex-edge-go)
[![License](https://img.shields.io/github/license/<usuario>/prod-edgenodex-edge-go)](LICENSE)
[![Go](https://img.shields.io/badge/Go-1.21-blue)](https://golang.org/)

---

## 🚀 Overview

**EdgeNodeX** é um **nó de processamento distribuído para edge computing**, projetado para:

- Executar **tasks computacionais localmente**, reduzindo latência  
- Integrar-se a **CloudFlow Orchestrator, EventHubX e TraceMatrix**  
- Fornecer **observabilidade, monitoramento e segurança** em ambientes distribuídos  
- Escalar horizontalmente em clusters de edge nodes

Ideal para arquiteturas **IoT, 5G e edge-native**, fornecendo **processamento em tempo real próximo da origem dos dados**.

---

## 🏗 Architecture

```mermaid
graph TD
    Sensors[IoT / Edge Devices] -->|Data Streams| EdgeNodeX[Edge Node]
    EdgeNodeX -->|Process| Tasks[Local Tasks / Computation]
    EdgeNodeX -->|Publish Events| EventHubX[EventHubX / GoBridge]
    EdgeNodeX -->|Metrics| TraceMatrix[TraceMatrix / Prometheus]
    EdgeNodeX -->|Config & Secrets| CoreVault[CoreVault]
