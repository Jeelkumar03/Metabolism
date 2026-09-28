# 🧬 Metabolism in Motion

An interactive, visual learning tool for understanding **cellular metabolism** through animated biochemical pathways, step-by-step reactions, molecular changes, cofactors, energy balance, regulation, narration, and real-time pathway simulation.

> **Learn metabolism by watching it happen.**

---

## ✨ Overview

**Metabolism in Motion** is a browser-based educational visualization designed to make complex metabolic pathways easier to understand.

Instead of presenting metabolism as static textbook diagrams, the application turns each pathway into an interactive animation. Users can move through individual reactions, observe substrates becoming products, track ATP/NADH and other cofactors, and explore how metabolic regulation changes pathway activity.

The application currently includes:

* Glycolysis
* Gluconeogenesis
* Krebs / TCA cycle
* Electron Transport Chain
* Metabolic Regulation Lab

Everything runs directly in the browser with **HTML, CSS, and vanilla JavaScript**.

---

## 🚀 Features

### 🔬 Interactive Metabolic Pathways

Each pathway is represented as an interactive SVG diagram containing:

* Metabolite nodes
* Enzyme labels
* Reaction connections
* Cofactors
* Carbon and phosphate representations
* Control-point indicators
* Reaction direction
* Step-by-step pathway progression

Clicking a molecule or enzyme jumps directly to the corresponding reaction step.

---

### ▶️ Step-by-Step Learning

Every pathway provides interactive controls:

* **Play** — automatically progress through the pathway
* **Back** — return to the previous reaction
* **Next** — advance one reaction
* **Reset** — return to the pathway overview
* **Overview** — return to the beginning
* **Summary** — view the pathway's final summary
* **Animation speed** — `0.5×`, `1×`, `1.5×`, or `2.5×`

Keyboard interaction is also supported for navigating the pathway.

---

### 📊 Running Cofactor Ledger

The application maintains a live balance of important metabolic molecules.

Depending on the pathway, the ledger tracks molecules such as:

* ATP
* ADP
* GTP
* GDP
* NADH
* NAD⁺
* FADH₂
* FAD
* H₂O
* CO₂
* H⁺
* Pᵢ
* CoA-SH
* O₂

The balance updates as reactions are completed, making energy and redox changes easier to follow.

---

## 🧪 Included Pathways

### 1. Glycolysis

Glycolysis is presented as the conversion of:

**Glucose → 2 Pyruvate**

The visualization contains all **10 glycolytic reactions**, including:

1. Hexokinase
2. Phosphoglucose isomerase
3. Phosphofructokinase-1
4. Aldolase
5. Triose phosphate isomerase
6. Glyceraldehyde 3-phosphate dehydrogenase
7. Phosphoglycerate kinase
8. Phosphoglycerate mutase
9. Enolase
10. Pyruvate kinase

The application highlights ATP investment, ATP payoff, NADH production, reaction reversibility, and major regulatory points.

The modeled overall balance is:

```text
Glucose + 2 NAD⁺ + 2 ADP + 2 Pᵢ
→
2 Pyruvate + 2 NADH + 2 H⁺ + 2 ATP + 2 H₂O
```

The application summarizes glycolysis as a net gain of **2 ATP and 2 NADH per glucose**.

---

### 2. Gluconeogenesis

The gluconeogenesis module visualizes glucose synthesis from pyruvate while highlighting the bypasses around glycolysis's irreversible reactions.

It covers:

* Mitochondrial pyruvate transport
* Pyruvate carboxylase
* Mitochondrial malate dehydrogenase
* Malate transport
* Cytosolic malate dehydrogenase
* PEP carboxykinase
* Reverse glycolytic reactions
* Fructose-1,6-bisphosphatase
* Glucose-6-phosphatase

The visualization also shows the mitochondrial matrix and cytosol.

The modeled energy cost per glucose is:

```text
4 ATP + 2 GTP + 2 NADH
```

---

### 3. Krebs Cycle / TCA Cycle

The Krebs cycle is presented as a circular mitochondrial pathway.

It includes:

* Acetyl-CoA
* Oxaloacetate
* Citrate
* cis-Aconitate
* Isocitrate
* α-Ketoglutarate
* Succinyl-CoA
* Succinate
* Fumarate
* Malate

The visualization emphasizes:

* Carbon loss as CO₂
* NADH generation
* FADH₂ generation
* GTP production
* Regeneration of oxaloacetate

The application models the running balance per acetyl-CoA and displays the cycle as occurring in the **mitochondrial matrix**.

---

### 4. Electron Transport Chain

The ETC module visualizes electron flow through the inner mitochondrial membrane.

It includes:

* **Complex I — NADH dehydrogenase**
* **Complex II — Succinate dehydrogenase**
* **Complex III**
* **Complex IV**
* **ATP synthase / Complex V**
* Ubiquinone `Q / QH₂`
* Cytochrome c
* Electrons
* Protons
* Oxygen
* ATP / ADP

The visualization demonstrates how electron transport generates a proton gradient and how proton flow through ATP synthase drives ATP production.

The application also represents proton pumping and electron movement using animated SVG elements.

---

## ⚙️ Regulation Lab

The **Regulation Lab** provides an interactive simulation of metabolic regulation.

Users can manipulate cellular conditions using sliders and presets.

The simulation considers signals including:

* Insulin
* Energy / ATP state
* Acetyl-CoA
* Citrate
* NADH
* Calcium
* Glucose-6-phosphate

The system calculates activity levels for important control enzymes and displays them using:

* Activity percentages
* Circular gauges
* Activity bars
* Pathway flux
* Animated particles
* Hormonal signaling cascades
* Dynamic explanations

---

### 🔄 Hormone Relay

The regulation lab visualizes the relay:

```text
cAMP
  ↓
PKA
  ↓
PFK-2
  ↓
Fructose 2,6-bisphosphate
  ↓
PFK-1
```

This allows users to see how hormonal signals influence glycolysis and gluconeogenesis.

---

### ⚖️ Metabolic Balance

The regulation simulator determines whether the system is primarily:

* Breaking down glucose
* Producing glucose
* Idling
* Running a futile cycle

It also reports whether the Krebs cycle is relatively fast or braked based on the simulated conditions.

---

## 🎨 Visualization System

The application uses **SVG** for its biochemical diagrams.

Molecules are visually represented using:

* Carbon markers
* Phosphate markers
* CoA groups
* Cofactor indicators
* Reaction arrows
* Enzyme labels
* Animated particles
* Proton/electron representations

A color-coded legend is provided for the major biochemical components.

---

## 🔊 Audio & Narration

The application includes two audio systems.

### Sound Effects

The application generates synthesized sound effects using the browser's **Web Audio API**.

Different reaction events can produce different sounds, including:

* ATP usage
* ATP production
* Redox reactions
* Water-related reactions
* Gas release
* Selection feedback

Sound effects can be enabled or disabled from the top navigation.

### Voice Narration

Where supported by the browser, the application uses the **Web Speech API** to narrate pathway steps.

Narration describes:

* Current reaction
* Enzyme
* Substrate
* Product
* Cofactor usage
* Reaction explanation

Narration can also be enabled or disabled.

---

## 🌗 Theme Support

The interface supports:

* Light mode
* Dark mode
* System color-scheme preference

The selected theme is persisted using:

```text
localStorage
```

The application uses CSS custom properties extensively so the complete visualization adapts to the selected theme.

---

## 📱 Responsive Design

The UI is designed for different screen sizes.

On smaller screens:

* The two-column pathway layout becomes a single-column layout.
* Navigation becomes horizontally scrollable.
* The pathway visualization remains horizontally scrollable when necessary.
* Controls adapt to the available width.
* The regulation laboratory switches to a stacked layout.

The application also respects:

```text
prefers-reduced-motion
```

to reduce animation for users who request reduced motion.

---

## ♿ Accessibility

Accessibility considerations include:

* Semantic buttons
* Keyboard navigation
* `aria-label` attributes
* Focus-visible styling
* Keyboard activation for interactive SVG elements
* Live regions for changing information
* Hidden narration control when speech synthesis is unsupported
* Reduced-motion support

Interactive pathway molecules and enzyme labels can be activated using the keyboard.

---

## 🛠️ Technology Stack

This project intentionally uses a lightweight browser-native stack.

| Technology         | Purpose                                       |
| ------------------ | --------------------------------------------- |
| HTML5              | Application structure                         |
| CSS3               | Layout, theming, responsive UI and animations |
| Vanilla JavaScript | Application logic and interaction             |
| SVG                | Metabolic pathway visualization               |
| Web Audio API      | Synthesized sound effects                     |
| Web Speech API     | Voice narration                               |
| `localStorage`     | Theme persistence                             |
| Google Fonts       | Typography                                    |

No JavaScript framework or frontend build system is required.

---

## 📁 Project Structure

The current implementation is a standalone HTML document:

```text
metabolism-in-motion/
└── index.html
```

The file contains:

```text
index.html
├── HTML structure
├── CSS styles
└── JavaScript application logic
    ├── Cofactor definitions
    ├── Glycolysis data
    ├── Gluconeogenesis data
    ├── Krebs cycle data
    ├── ETC data
    ├── Audio engine
    ├── Narration engine
    ├── SVG rendering
    ├── Pathway controller
    ├── Regulation simulator
    ├── Router
    └── Theme controller
```

---

## ▶️ Getting Started

### Requirements

A modern web browser with support for:

* ES6+ JavaScript
* SVG
* CSS custom properties
* Web Audio API
* Web Speech API for optional narration

Recommended browsers include recent versions of:

* Google Chrome
* Microsoft Edge
* Mozilla Firefox
* Safari

---

### Run Locally

Because the application is client-side and self-contained, no Node.js, Python server, npm installation, or build process is required.

Simply open the HTML file in a modern browser:

```text
index.html
```

For a local development server, any static HTTP server can also be used.

For example, with Python:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

---

## 🧭 Navigation

The application uses hash-based client-side routing.

Available routes:

```text
#/glycolysis
#/gluconeogenesis
#/krebs
#/etc
#/regulation
```

The default route is:

```text
#/glycolysis
```

The browser title changes automatically according to the active module.

---

## 🧠 How the Application Works

The application stores biochemical pathways as structured JavaScript data.

Each reaction contains information such as:

```javascript
{
  enzyme: "Hexokinase",
  ec: "EC 2.7.1.1",
  cls: "Kinase",
  loc: "Cytosol",
  in: [["ATP", 1]],
  out: [["ADP", 1]],
  what: "...",
  more: "...",
  reg: "..."
}
```

The visualization engine reads this data and dynamically creates:

1. Metabolite nodes
2. Reaction edges
3. Enzyme labels
4. Cofactor labels
5. Timeline controls
6. Running ledgers
7. Animation states
8. Narration text

This keeps the pathway information separate from the rendering logic.

---

## 🧮 Reaction Ledger

The pathway engine calculates the running biochemical balance from the reaction definitions.

For each completed reaction:

```text
Input cofactors → decrease
Output cofactors → increase
```

Reactions can also specify a multiplier when a pathway reaction occurs multiple times per substrate.

For example, the payoff phase of glycolysis occurs twice per glucose molecule.

---

## 🔬 Regulation Engine

The Regulation Lab converts user-controlled physiological conditions into normalized signals.

The simulator derives signals such as:

```text
ATP
ADP
AMP
Insulin
Glucagon
cAMP
PKA
Fructose 2,6-bisphosphate
```

Enzyme activity is then calculated from the defined regulatory effects.

The resulting activities drive:

```text
Enzyme gauges
      ↓
Pathway flux
      ↓
Animated particles
      ↓
Metabolic verdict
      ↓
Dynamic biological insights
```

---

## 🔗 Pathway Relationships

The application connects major metabolic pathways conceptually:

```text
                  ┌─────────────────────┐
                  │   Gluconeogenesis  │
                  │       ↑            │
                  │      Glucose       │
                  └───────┬─────────────┘
                          │
                    Glycolysis
                          │
                       Pyruvate
                          │
                    Acetyl-CoA
                          │
                    Krebs Cycle
                          │
                       NADH
                      FADH₂
                          │
                          ▼
              Electron Transport Chain
                          │
                          ▼
                         ATP
```

The Regulation Lab provides an interactive view of how cellular signals influence these pathways.

---

## 🎓 Educational Goals

The project is designed to help learners understand:

* How glucose is metabolized
* Where ATP is consumed and produced
* How NADH and FADH₂ carry reducing equivalents
* How the Krebs cycle generates reducing power
* How the ETC establishes a proton gradient
* How ATP synthase converts proton-motive force into ATP
* Why glycolysis and gluconeogenesis are regulated independently
* How hormones influence metabolic pathways
* How energy status changes metabolic flux
* How different metabolic pathways are interconnected

---

## ⚠️ Scope

This project is an **educational visualization and simulation**.

The regulation laboratory uses simplified mathematical representations of biochemical regulation to make pathway behavior interactive and understandable. It should not be interpreted as a quantitative physiological model of a real organism or cell.

Likewise, the animations are conceptual representations of biochemical mechanisms rather than molecular-scale simulations.

---

## 🔮 Possible Future Improvements

Potential extensions include:

* More metabolic pathways
* Pentose phosphate pathway
* Fatty acid β-oxidation
* Fatty acid synthesis
* Amino acid metabolism
* Urea cycle
* Glycogen metabolism
* Interactive pathway comparison
* Quiz mode
* Progress tracking
* More detailed molecular structures
* Mobile-specific interaction improvements
* Additional narration voices
* Exportable pathway diagrams

---

## 📄 License

No explicit license is defined in the provided source code.

If this project is published publicly, add an appropriate license file such as:

```text
LICENSE
```

and update this section accordingly.

---

## 👨‍💻 Project

**Metabolism in Motion**

An interactive approach to learning cellular metabolism through:

> **Pathways → Reactions → Cofactors → Regulation → Visualization**

Built with browser-native technologies and designed to make metabolic biochemistry more interactive, visual, and understandable.
