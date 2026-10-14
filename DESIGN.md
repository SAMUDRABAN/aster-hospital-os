---
name: Aster Hospital OS
description: Calm precision for connected hospital work
colors:
  primary: "#09685e"
  canvas: "#f5f7f7"
  paper: "#ffffff"
  ink: "#1b3033"
  muted: "#617477"
  metadata: "#566c65"
  border: "#e1e8e7"
  teal-soft: "#edf6f3"
typography:
  headline:
    fontFamily: "Geist, sans-serif"
    fontSize: "28px"
    fontWeight: 600
    lineHeight: 1.3
  body:
    fontFamily: "Geist, sans-serif"
    fontSize: "14px"
    fontWeight: 400
    lineHeight: 1.5
  patient-body:
    fontFamily: "Geist, sans-serif"
    fontSize: "16px"
    lineHeight: 1.5
rounded:
  control: "6px"
  panel: "12px"
spacing:
  compact: "8px"
  group: "16px"
  section: "24px"
  page: "32px"
components:
  button-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.paper}"
    rounded: "{rounded.control}"
    padding: "9px 13px"
  panel:
    backgroundColor: "{colors.paper}"
    rounded: "{rounded.panel}"
---

## Overview

**Creative North Star: "Calm precision"**

A working hospital deserves a quiet interface that makes its next action visible. Mineral surfaces, graphite text and deep teal actions form the approved visual world. This is an Operate surface: task clarity takes priority over decoration.

**Key Characteristics:**
- Connected workflows with inspectable consequences.
- Restrained semantic colors and explicit status text.
- Patient-facing typography larger than staff metadata.

## Colors

Teal carries primary actions; pale teal marks related context. White panels sit on the mineral canvas with fine separators. Muted ink supports descriptions; the darker metadata tone improves small operational text. Amber and red accompany written states, never replace them.

**The Named State Rule.** Every status has a readable label alongside its color.

## Typography

Self-hosted Geist supports headings, data and controls. Main headings use compact tracking; numerals are tabular. Staff body text is fourteen pixels, metadata generally eleven to thirteen. Patient-facing paragraphs and actions use sixteen pixels. Clinical data does not animate numerically.

## Layout

Desktop has a persistent 216px navigation rail and content capped at 1700px. Overview columns stack at narrower widths. Below 800px, navigation becomes a drawer and the Today attention queue precedes metrics, flow and insight. Task deadlines remain visible. Wide clinical tables scroll inside their region. The companion reflows to a single column on mobile.

**The Next Action Rule.** Assigned work remains ahead of supporting overview content on small screens.

## Elevation & Depth

Most panels are flat and separated by a thin border. Context panels and the patient preview use restrained soft elevation. Shadows do not signal clinical urgency.

## Shapes

Panels use gently curved corners; controls have tighter corners. Small status labels can use compact rounding. The patient preview has a phone-like outline to distinguish the perspective without implying a separate native app.

## Components

Primary buttons use teal with white text; secondary buttons use white with a fine border. Keyboard focus is visible and disabled actions remain identifiable. Navigation uses a pale selected surface. Dialog panels have an explicit accessible heading, Escape dismissal and native focus containment. Messages inside dialogs remain visible in the top layer. Patient actions have at least 44px height.

Motion is brief and contextual; reduced-motion preferences are respected. Dense information stays stationary.

## Do's and Don'ts

- Do keep synthetic data and simulated behavior clearly labeled.
- Do preserve deadlines, source context and review requirements.
- Do use the single Phosphor icon family consistently.
- Don't introduce decorative gradients or invented clinical claims.
- Don't treat role previews as access controls.
