📘 Firstock Trading Flowcharts (Equity & Options)

This repository contains complete trading process flowcharts for the Firstock platform.
All diagrams are written in Mermaid format and cover Equity and Options trading scenarios, including POA, CDSL, RMS, Exchange, Intraday, and Delivery logic.

These flowcharts are used for:

QA Test Case Creation

Automation planning

Backend/OMS/RMS logic understanding

Developer onboarding

Documentation & audits

📂 Folder Structure
firstock-trade-flows/
│
├── diagrams/
│   ├── equity-buy-flow.mmd
│   ├── equity-sell-flow/
│   │     ├── ES01–NoHold-NoToday.mmd
│   │     ├── ES03–TodayBuyOnly.mmd
│   │     ├── ES04–POATrue.mmd
│   │     ├── ES07–NewCDSL.mmd
│   │     ├── ES08–MixedQty-CDSLAlready.mmd
│   │     ├── ES09–MixedQty-NewCDSL.mmd
│   │     ├── ES12–PartialCDSL-SellMore.mmd
│   │     ├── ES13–PartialCDSL-SellWithin.mmd
│   │     └── <all other ES flows>
│   │
│   ├── option-buy-flow.mmd
│   ├── option-sell-close-long.mmd
│   ├── option-writing-new-short.mmd
│   │
│   └── README-diagrams.md (optional future extension)
│
├── README.md
└── .vscode/
    └── settings.json

🧭 Available Flowcharts
📈 Equity Flows
Flow	Description
equity-buy-flow.mmd	Full Equity Buy (CNC/MIS) flow with RMS, Exchange, Order/Position updates
equity-sell-flow/*.mmd	All ES01–ES13 Sell scenarios separated clearly
ES12	POA False → Partial CDSL → Sell more than authorized
ES13	POA False → Partial CDSL → Sell within authorized qty
📉 Option Flows
Flow	Description
option-buy-flow.mmd	Option BUY: New LONG + SHORT Cover logic
option-sell-close-long.mmd	Option SELL: Closing LONG (Square-off)
option-writing-new-short.mmd	Option SELL: Writing/creating new SHORT position

All diagrams follow Top → Bottom (TD) layout for clarity.

🛠 How to Preview Mermaid in VS Code

Install these extensions:

Markdown Preview Mermaid Support

(Optional) Mermaid Markdown Syntax Highlighting

Open any .mmd file
Example:

diagrams/option-buy-flow.mmd


Open preview:

Press Ctrl + Shift + V

OR Right-click → Open Preview to the Side

🧪 Sample Diagram Block
flowchart TD
  A([Start]) --> B{Logged in?}
  B -- Yes --> C[Home]
  B -- No --> D[Login Screen]

📝 Notes

All flows use error-free Mermaid syntax

All branches include:

Frontend validation

Backend RMS/margin checks

Exchange acceptance/rejection

Order Book & Position updates

Equity Sell includes:

POA TRUE / POA FALSE

CDSL/E-DIS

Mixed quantities (holdings + today buy)

Partial CDSL logic (ES12, ES13)