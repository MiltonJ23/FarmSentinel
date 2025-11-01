**Mandate:** Propose a severe, reliable, and secure color palette and font scheme for **FarmSentinel** that evokes the authority of a critical utility, suitable for serious adult users (farmers, authorities). The target aesthetic is **Unwavering Reliability and Trust**, not superficial friendliness.

This proposal is based on established principles of professional design and color psychology associated with safety, data integrity, and mission-critical systems.

---

## 1. Font Palette: Authority, Readability, and Unambiguous Data

The choice of typeface must prioritize legibility across all map, data, and alerting interfaces, regardless of screen quality or user age. The selection must project the technical rigor of the distributed system.

| Usage | Font Family | Style Mandate | Rationale (Fact-Based) |
| :--- | :--- | :--- | :--- |
| **Primary (Body Text, Data Labels)** | **IBM Plex Sans** | Regular, Semibold, Light | Designed to be highly legible for complex UIs and data visualization. Its open-source nature and modern, professional geometry project technical credibility without being overly decorative. Excellent for dense data tables and map labels. |
| **Secondary (Headlines, Alerts)** | **Source Sans 3** (or similar Humanist Sans-Serif) | Semibold, Black | A clean, high-contrast typeface that works well at large sizes. It maintains a serious, neutral tone, ensuring that critical alerts (pests/diseases) have maximum visual impact and immediate readability. |
| **Monospace (Code, Logs, Status Codes)** | **IBM Plex Mono** | Regular | Essential for a distributed systems project. Provides clear differentiation for any status logs, technical outputs, or debugging console views, maintaining a severe, factual aesthetic. |

---

## 2. Color Palette: Security, Grounding, and Actionable Data

The palette is constructed around a dark, authoritative primary color (deep green/blue) that grounds the app in agriculture and data security, complemented by a single, high-contrast action color for alerts.

### Primary Palette: Security and Stability (The Trustworthy Uncle)

| Color Name | Hex Code | Usage | Rationale |
| :--- | :--- | :--- | :--- |
| **Primary Base (Authority)** | **\#003D2E** (Deep Forest Green) | Backgrounds, Sidebars, Primary Navigation. | Evokes soil, agriculture (Green), combined with stability and data depth (Deep Blue/Black). It is severe, non-distracting, and anchors the system as a serious tool. |
| **Surface/Card Color** | **\#F5F5F5** (Near White) | Content Panels, Data Cards, Input Fields. | Provides maximum contrast for text readability (WCAG AAA contrast). Clean white surface for reports and data. |
| **Text/Icon Primary** | **\#1A1A1A** (Dark Black) | All primary body text, titles, essential icons. | Unambiguous, high-contrast black for all factual data and text. |

### Semantic Palette: Status and Action (The Emergency Call)

These colors are reserved strictly for data status and alerts, ensuring their meaning is immediate and non-negotiable. **Do not use these for decoration.**

| Color Name | Hex Code | Usage | Rationale |
| :--- | :--- | :--- | :--- |
| **Positive/Success** | **\#008000** (Pure Green) | Report Submission Success, Field Boundary Confirmation (Low Threat). | Universal sign of success and health. |
| **Alert/Warning** | **\#FFA500** (Deep Orange) | High-Priority Outbreak Area, Threat Level 'Moderate' (US 9). | Projects caution and immediate attention, without inducing panic. |
| **Critical/Danger** | **\#CC0000** (Severe Red) | **Real-Time Outbreak Alert** (The PEST/DISEASE signal), System Failure Status. | Reserved exclusively for immediate action or high-threat events, fulfilling the severity mandate. |
| **Interactive Accent** | **\#0066CC** (Trust Blue) | Primary button calls-to-action, active selection states, map markers for non-outbreak data (fields). | Projects efficiency, professionalism, and reliability (The "true" color of technology and data integrity). |