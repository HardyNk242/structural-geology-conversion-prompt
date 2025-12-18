# Structural Geology Conversion Prompt (LLM)

This repository provides a **strict system/developer prompt** for Large Language Models (LLMs) to convert **structural geology planar measurements** between common notations in a **safe, explicit, and non-ambiguous way**.

The prompt is designed for **geologists, researchers, and developers** who want reliable conversions without silent assumptions.

---

## ✨ Key Features

- Clarification-first logic (no automatic conversion)
- Supports all common planar notations:
  - Quadrant
  - Azimuth (strike + dip direction)
  - Right-Hand Rule (RHR) strike/dip
  - Dip/Dipdir
- Enforces geometric consistency (⊥ dip direction, RHR)
- Outputs results **only as a table**
- Explicit format labels for every conversion
- Minimal, machine-readable responses

---

## 📐 Supported Input Formats

- **Quadrant**  
  `NθE/δDD`, `SθE/δDD`, `SθW/δDD`, `NθW/δDD`  
  Example: `N45E/25SE`

- **Azimuth (strike + dip direction explicit)**  
  `α/δDD`  
  Example: `045/25SE`

- **RHR strike/dip**  
  `α/δ`  
  Example: `045/25`

- **Dip/Dipdir**  
  `δ/β`  
  Example: `25/135`

---

## 🔄 Available Conversions

1. Quadrant → Azimuth  
2. Azimuth → Quadrant  
3. Azimuth → RHR strike/dip  
4. RHR strike/dip → Azimuth  
5. Azimuth → Dip/Dipdir  
6. Dip/Dipdir → RHR strike/dip  
7. Quadrant → Dip/Dipdir  
8. Dip/Dipdir → Quadrant  
9. Full chain: Quadrant → Azimuth → RHR → Dip/Dipdir  

---

## 📊 Output Format (Strict)

All conversions are returned **only as a table**:

| Given (original format) | Converted (format specified) |
|------------------------|------------------------------|
| N45E/25SE              | Azimuth: 045/25SE            |
|                        | RHR: 045/25                  |
|                        | Dip/Dipdir: 25/135           |

No explanations are included unless explicitly requested.

---

## 🧠 Intended Use

- LLM system / developer prompts
- Structural geology teaching
- Field data validation
- CSV / GIS pre-processing
- Research reproducibility

---

## 📜 License

MIT License — free to use, modify, and distribute with attribution.
