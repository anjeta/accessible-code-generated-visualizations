# Accessible Code-Generated Visualizations

> Practical guidelines and reproducible examples for creating more accessible data visualizations in **Python** and **R**.

This repository accompanies the document **_Guidelines for Accessible Code-Generated Visualizations in Computer Science Education_** and provides ready-to-run examples for common graph types in Python and R.

The materials are intended for teaching, demonstrations, and self-study and were developed with the needs of blind and visually impaired learners in mind.. The central idea is that accessibility should be considered **while the visualization is being created**, rather than added only after a figure has already been produced.

These materials were prepared in the context of the Erasmus+ project [Access2CS](https://ascnet.ie/access2cs/), which focuses on improving accessibility and inclusion in Computer Science education.

---

## ✨ What is included?

The repository contains:

- 📘 **Accessibility guidelines** for code-generated visualizations
- 🐍 **Python/Jupyter examples** using Matplotlib
- 📊 **R/Jupyter examples** using ggplot2
- 🧩 Reusable plotting templates
- 📝 Examples of structured textual graph descriptions
- 🤖 Examples of automatic graph description with **MatplotAlt**
- 💬 Examples of generating descriptions for existing PNG graphs with **Chatlas + Gemini**
- 🔊 A **STRAUSS sonification** example for representing data through sound

---

## 🎯 Accessibility goals

The examples in this repository follow four main principles described in the accompanying guidelines:

1. **Prioritize semantic meaning**  
   A visualization should clearly communicate what variables and relationships are represented.

2. **Preserve computational context**  
   Students should be able to understand how the graph relates to the code, data, parameters, and transformations that generated it.

3. **Support reproducibility**  
   Source code is provided so that graphs can be inspected, modified, and recreated.

4. **Support non-visual exploration**  
   Whenever possible, visualizations should be complemented with textual descriptions, structured data, or alternative modalities such as sonification.

---

## ♿ Accessibility-aware plotting

Across both Python and R examples, the plotting code emphasizes:

- meaningful axis labels
- measurement units where appropriate
- descriptive titles
- readable font sizes
- high-contrast and colorblind-friendly palettes
- redundant visual encodings such as line style + markers
- useful but non-intrusive grid lines
- reduced visual clutter
- semantic interpretation of the resulting graph

Color should **not** be the only way information is communicated.

---

## 📈 Graph types

Equivalent examples are provided in both Python and R.

| Graph type | Typical purpose |
|---|---|
| **Line graph** | Trends and change over continuous variables |
| **Scatterplot** | Relationships, correlations, and clusters |
| **Histogram** | Distributions, spread, and skewness |
| **Box plot** | Median, quartiles, variability, and outliers |
| **Heatmap** | Matrix relationships, correlations, and magnitude |

Each graph-specific notebook contains:

1. a short explanation of what the graph is used for
2. guidance on making that graph more accessible
3. an accessible example
4. a reusable template
5. structured descriptions of the graph

---

## 🗂 Repository structure

```text
accessible-code-generated-visualizations/
├── README.md
├── LICENSE
├── CITATION.cff
├── CONTRIBUTING.md
├── requirements.txt
│
├── guidelines/
│   └── Guidelines for Accessible Code-Generated Visualizations
│       in Computer Science Education.pdf
│
├── python/
│   ├── line_graph_accessible.ipynb
│   ├── scatterplot_accessible.ipynb
│   ├── histogram_accessible.ipynb
│   ├── box_plot_accessible.ipynb
│   ├── heatmap_accessible.ipynb
│   ├── chatlas_gemini_alt_text.ipynb
│   └── strauss_sonification.ipynb
│
├── R/
│   ├── line_graph_accessible_R.ipynb
│   ├── scatterplot_accessible_R.ipynb
│   ├── histogram_accessible_R.ipynb
│   ├── box_plot_accessible_R.ipynb
│   └── heatmap_accessible_R.ipynb
│
└── images/
    ├── line_graph_accessible.png
    └── bar_graph_accessible.png
```

---

# 🐍 Python examples

The Python graph examples use **Matplotlib**.

The examples deliberately encode important information through more than color alone.

---

## 📝 MatplotAlt descriptions

The Python notebooks also demonstrate **MatplotAlt**, which can extract semantic information from Matplotlib figures and generate structured textual descriptions.

The notebooks organize descriptions into four levels:

| Level | Focus |
|---|---|
| **1** | Chart type, axes, labels, and basic structure |
| **2** | Important values and statistical details |
| **3** | Trends, relationships, or patterns |
| **4** | Broader contextual interpretation |

Levels 1–3 can be generated from the plot structure with MatplotAlt's rule-based functionality.

Level 4 may require an API-enabled model and is therefore optional depending on the user's environment and available API access.

> Automated descriptions should supplement good visualization design rather than replace it. A description can only interpret information that is meaningfully encoded in the graph.

---

# 📊 R examples

The R notebooks recreate the same accessible graph examples with **ggplot2**. 

The R notebooks follow the same teaching structure as the Python versions. Because MatplotAlt is Python-specific, the R notebooks include the four description levels as templates rather than calling MatplotAlt directly.

---

# 🚀 Getting started

## Python environment

A simple Conda environment can be created with:

```bash
conda create -n accessible-viz python=3.12
conda activate accessible-viz
```

For the basic graph examples:

```bash
pip install matplotlib jupyter
```

Install MatplotAlt, Chatlas, or STRAUSS only if you plan to run the corresponding notebooks.

---

## R environment

One option is to create a dedicated Conda environment:

Start R:

```bash
R
```

Then install the R Jupyter kernel:

```r
install.packages("IRkernel")

IRkernel::installspec(
  name = "r-env",
  displayname = "R (r-env)"
)
```

If required, install ggplot2 directly from R:

```r
install.packages("ggplot2")
```

---

# 🖼 Describing existing graph images

The repository also includes an example using **Chatlas with Gemini** to generate natural-language descriptions from graphs that have already been saved as PNG images.

```text
Existing PNG graph
        │
        ▼
     Chatlas
        │
        ▼
      Gemini
        │
        ▼
Accessible natural-language description
```

This is useful when an existing image needs an additional semantic explanation.

> To run the Chatlas + Gemini, you need a valid **Gemini API key**. Configure the key in your environment before running the notebook, do not input API credentials directly into the scripts.

---

# 🔊 Sonification with STRAUSS

Accessibility does not have to rely only on text.

The repository also includes an example using **STRAUSS**, where numerical data is represented through sound.

Data can be mapped to auditory dimensions such as:

- pitch / frequency
- volume / amplitude
- duration
- timbre
- spatial position
- temporal progression

The included example demonstrates explicit mappings between data variables and auditory channels.

---

# 🧭 How to use these materials

### For students
Run the examples, inspect the code, change the data, and observe how visualization design affects interpretation.

### For instructors
Use the notebooks as teaching examples when discussing visualization, accessibility, data analysis, or reproducible computational workflows.

### For developers
Use the reusable templates as starting points for accessibility-aware visualizations in new projects.

---

## ✅ Accessibility checklist

Before publishing a code-generated visualization, consider the following:

- [ ] Does the graph have a descriptive title?
- [ ] Are both axes clearly labeled?
- [ ] Are measurement units included where appropriate?
- [ ] Is the text large enough to read comfortably?
- [ ] Does the graph remain understandable without relying only on color?
- [ ] Are high-contrast or colorblind-friendly colors used?
- [ ] Are markers, line styles, labels, or other redundant encodings used where appropriate?
- [ ] Is unnecessary visual clutter avoided?
- [ ] Can the underlying data or source code be accessed?
- [ ] Is a textual description available?
- [ ] Could another modality, such as sonification, improve access?

---

# 📘 Guidelines

The full rationale, design recommendations, examples, accessibility tools, and teaching considerations are described in:

> **Guidelines for Accessible Code-Generated Visualizations in Computer Science Education**

The document should be treated as the primary reference for the examples in this repository.

---

# 🤝 Contributions

Contributions that improve accessibility, clarity, reproducibility, or educational usefulness are welcome.

Examples include:

- additional accessible graph types
- equivalent examples in other programming languages
- improved textual-description approaches
- non-visual interaction methods
- accessibility testing
- teaching exercises and examples

When contributing a new visualization, please aim to include:

1. a clear explanation of the graph's purpose
2. accessibility considerations
3. a worked example
4. a reusable template
5. a textual interpretation of the result

---

# 📄 License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

## 🎯 Final principle

> **Accessibility should be part of visualization design from the beginning—not an afterthought.**

A well-designed accessible visualization should help users understand not only **what the graph looks like**, but also **what the data means, how the visualization was generated, and what relationships or patterns it communicates**.

## Repository status

> These materials provide practical accessibility-oriented examples for educational use. They are intended to support accessible visualization practice, but they should not be interpreted as a complete accessibility compliance standard.
