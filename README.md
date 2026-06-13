# EMSC2010 – Week 10 Practical 1: Fourier Analysis and Filtering

This repository contains the template Jupyter notebooks for **Week 10 Practical 1** of *EMSC2010: Data Science for Earth System Scientists* at the Australian National University.

The session introduces **Fourier analysis** — decomposing a signal into its constituent sinusoids and representing it as a frequency spectrum — and **frequency-domain filtering**. Students build up these tools using synthetic signals before applying them to a real palaeoclimate record to identify Milankovitch orbital cycles.

---

## Notebooks

### Notebook 1 – Building Sinusoids (`NB1`)

This notebook introduces the building blocks of Fourier analysis. Students generate sinusoids and explore how changing their **frequency**, **amplitude**, and **phase** affects their shape. Several sinusoids of different frequency and amplitude are then summed together to create a more complex composite signal — motivating the central question of the practical: given a complicated signal, how can we recover the characteristics of the sinusoids that make it up?

**Key concepts:** Sinusoids, frequency, amplitude, phase, signal superposition

**Libraries:** `numpy`, `matplotlib`

---

### Notebook 2 – The Fourier Transform and Filtering (`NB2`)

Building on the composite signal from NB1, this notebook introduces the **Fourier transform** (via `np.fft.rfft`) to convert a signal from the time domain into a frequency spectrum, revealing the frequencies and amplitudes of its component sinusoids. Students then explore **low-pass filtering** — zeroing out high-frequency components in the frequency spectrum and using the inverse Fourier transform to reconstruct a smoothed version of the signal in the time domain — and experiment with how the choice of cutoff frequency affects the result.

**Key concepts:** Fourier transform, frequency spectra, interpolation onto uniform sampling, low-pass filtering, inverse Fourier transform

**Libraries:** `numpy`, `matplotlib`

---

### Notebook 3 – Milankovitch Cycles in the LR04 Record (`NB3`)

**Dataset:** LR04 benthic oxygen isotope (δ¹⁸O) stack spanning the last 800,000 years (`LR04.xlsx`).

This notebook applies Fourier analysis to a real palaeoclimate record. Students calculate the frequency spectrum of the raw δ¹⁸O data, then detrend the record using a polynomial fit (`np.polyfit`) to remove the dominant long-term trend and reveal the underlying cyclicity. With the detrended frequency spectrum, students identify the **Milankovitch orbital cycles** — eccentricity, obliquity, and precession — and use low-pass, high-pass, and band-pass filters to isolate each cycle individually in the time domain.

**Key concepts:** Detrending, frequency spectra of real data, low-pass/high-pass/band-pass filtering, Milankovitch cycles (eccentricity, obliquity, precession)

**Libraries:** `numpy`, `matplotlib`, `pandas`

> **Note:** The `LR04.xlsx` data file must be uploaded to the Colab file space before running this notebook.

---

### Notebook 4 – Challenge: The Older LR04 Record (`NB4`)

**Dataset:** LR04 δ¹⁸O record spanning 1.5–2.5 million years ago (`LR04_old.xlsx`).

This is an open-ended challenge notebook. Using the workflow developed in NB3 as a template, students independently apply Fourier analysis, detrending, and filtering to an older portion of the LR04 record to investigate how the dominant orbital cycles (and their relative strengths) differ from the more recent record.

**Key concepts:** Independent application of Fourier analysis and filtering, comparison of orbital forcing across geological time

**Libraries:** As needed (students build their own solution)

> **Note:** The `LR04_old.xlsx` data file must be uploaded to the Colab file space before running this notebook.

---

## Data Files

| File | Description |
|---|---|
| `LR04.xlsx` | LR04 benthic δ¹⁸O stack, 0–800 ka (used in NB3) |
| `LR04_old.xlsx` | LR04 benthic δ¹⁸O stack, 1.5–2.5 Ma (used in NB4) |

Both files are included in this repository and must be uploaded to the Colab file space when running the relevant notebooks.

---

## Getting Started

This is a **template repository**. To begin working on the notebooks:

1. Click **"Use this template"** at the top of this page to create a copy of the repository in your own GitHub account.
2. Open any notebook from your copy of the repository and click the **"Open in Colab"** badge at the top of the notebook to launch it in Google Colab.
3. Before submitting, replace the `uXXXXXXX` placeholder in the filename with your ANU student UID.

---

## Repository Structure

```
EMSC2010-W10-P1/
├── EMSC2010_W10_P1_NB1_uXXXXXXX.ipynb   # Building sinusoids
├── EMSC2010_W10_P1_NB2_uXXXXXXX.ipynb   # The Fourier transform and filtering
├── EMSC2010_W10_P1_NB3_uXXXXXXX.ipynb   # Milankovitch cycles in the LR04 record
├── EMSC2010_W10_P1_NB4_uXXXXXXX.ipynb   # Challenge: the older LR04 record
├── LR04.xlsx                              # LR04 record, 0-800 ka
├── LR04_old.xlsx                          # LR04 record, 1.5-2.5 Ma
├── LICENSE
└── README.md
```

---

## Course Information

| | |
|---|---|
| **Course** | EMSC2010 – Data Science for Earth System Scientists |
| **Institution** | Australian National University (ANU) |
| **Week** | 10 |
| **Session** | Practical 1 |
| **Topic** | Fourier Analysis and Filtering |

---

## License

This repository is released under the [MIT License](LICENSE).
