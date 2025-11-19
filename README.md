📘 Firstock Trading Flow Diagrams

This repository contains Mermaid-based flowcharts for Firstock’s Equity and Options trading lifecycle.
These diagrams are useful for:

QA manual + automation test case design

Developer workflows

Backend + OMS + RMS decision mapping

Documentation & knowledge transfer

Visualizing POA/CDSL, margin checks, RMS, exchange acceptance, order status flow

📂 Folder Structure
firstock-trade-flows/
├── diagrams/
│   ├── equity-buy-flow.mmd
│   ├── equity-sell-flow.mmd
│   ├── option-buy-flow.mmd
│   └── option-sell-flow.mmd
├── .vscode/
│   └── settings.json
└── README.md

🗂️ Flow Diagrams
📈 Equity

Equity Buy Flow
diagrams/equity-buy-flow.mmd

Equity Sell Flow
diagrams/equity-sell-flow.mmd

📉 Options

Option Buy Flow
diagrams/option-buy-flow.mmd

Option Sell Flow (Square-off + Writing / Shorting)
diagrams/option-sell-flow.mmd

Each of these is a left-to-right Mermaid flowchart, with vertical branching at each decision node.

🛠️ VS Code Setup for Mermaid Preview

To preview .mmd Mermaid diagrams:

1. Install the extension

Go to VS Code → Extensions (Ctrl + Shift + X) → search:

Markdown Preview Mermaid Support


Install it → Reload VS Code.

2. Open any .mmd file

Example: equity-buy-flow.mmd

3. Open preview

Press:

Ctrl + Shift + V


Or right-click → Open Preview to the Side

Now your flowchart will render visually on the right.

📝 What’s Included in the Diagrams
Equity Buy Flow covers:

Login → Symbol selection → Buy form

Frontend validation

OMS/Backend checks (Funds, Margin, RMS, Market status)

Exchange acceptance

Partial/Full Fill logic

Order Book & Position update

Equity Sell Flow covers:

Delivery Sell (POA True/False)

CDSL/eDIS check

Intraday Sell (MIS)

Short Sell logic

Order Book & Position update

Option Buy Flow covers:

Option contract selection

Premium debit

RMS + Margin checks

Open/Pending/Partial/Full execution

LONG position creation

Option Sell Flow covers:

Square-off LONG positions

Option Writing (SHORT position creation)

SPAN + Exposure margin checks

RMS rejection handling

Order Book & Position updates