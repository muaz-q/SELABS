# Lab 3 — Component Modelling & Architectural Pattern Selection

## Scenario
Self-Service Coffee Kiosk System.

## Selected Architecture
**Layered Architecture**

### Architecture comparison
| Architecture | Advantages | Disadvantages | Fit |
|---|---|---|---|
| Layered | Simple, clear separation, easy maintenance | Layer coupling / some overhead | **Best fit** |
| Microservices | Independent scaling/deployment, fault isolation | Network latency, operational complexity, consistency issues | Overkill for one kiosk |
| Client-Server | Centralized control and data consistency | Server bottleneck and single point of failure | Less appropriate than layered design |

## Components
1. Touchscreen UI
2. Order Manager
3. Payment Service
4. Menu & Pricing DB
5. Receipt Printer

## Interfaces
1. IOrderSelection — Touchscreen UI → Order Manager
2. IMenuQuery — Order Manager → Menu & Pricing DB
3. IPayment — Order Manager → Payment Service
4. IReceipt — Order Manager → Receipt Printer

## Main flow
Customer selects coffee type and size → UI sends selection to Order Manager → Order Manager queries menu/pricing → Order Manager requests credit-card payment → successful payment triggers receipt printing.

## Submission files
- Diagram/Lab3_Component_Diagram.png
- Diagram/Lab3_Component_Diagram.pdf
- Justification/Lab3_Written_Justification.docx
- Justification/Lab3_Written_Justification.pdf
