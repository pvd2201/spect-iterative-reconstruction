# Iterative Reconstruction for SPECT Imaging

## Overview
This project investigates iterative image reconstruction methods for simulated SPECT (Single Photon Emission Computed Tomography) imaging data.

The project focuses on the simulation of projection data, Poisson noise modeling, image reconstruction, and quantitative evaluation of reconstructed images.

Maximum Likelihood Expectation Maximization (MLEM) is used as the baseline iterative reconstruction method and is compared with Filtered Back Projection (FBP). Improved reconstruction approaches based on the Median Root Prior (MRP) and Ordered Subsets Expectation Maximization (OSEM) are also investigated.

## Objectives
The main objectives of this project are:
* Generate and process different imaging phantoms.
* Simulate projection data using the Radon transform.
* Model photon-counting noise using a Poisson distribution.
* Implement MLEM image reconstruction.
* Compare MLEM with FBP.
* Investigate MLEM with a Median Root Prior (MRP).
* Investigate OSEM combined with MRP.
* Evaluate reconstruction quality under different photon-count levels.

## Reconstruction Methods
The following reconstruction methods are investigated:

### Filtered Back Projection (FBP)
FBP is used as an analytical reconstruction method and serves as a reference for comparison with iterative reconstruction.

### Maximum Likelihood Expectation Maximization (MLEM)
MLEM is used as the baseline iterative reconstruction algorithm. The method estimates the image by maximizing the likelihood of the measured projection data under a Poisson statistical model.

### MLEM-MRP
MLEM is improved by incorporating a Median Root Prior (MRP) to introduce prior information into the reconstruction process and reduce noise while preserving important image structures.

### OSEM-MRP
Ordered Subsets Expectation Maximization (OSEM) is investigated to accelerate the iterative reconstruction process. The MRP prior is incorporated into the reconstruction framework.

## Phantom and Data Simulation
Two types of phantoms are used in this project:
* NEMA phantom
* Grayscale phantom

Projection data are generated using the Radon transform. Poisson noise is subsequently simulated to represent the statistical nature of photon counting in nuclear medicine imaging.
Different photon-count levels can be investigated to study the effect of statistical noise on reconstruction quality.

## Image Quality Evaluation
The reconstructed images are evaluated using several quantitative metrics:
* Root Mean Square Error (RMSE)
* Peak Signal-to-Noise Ratio (PSNR)
* Structural Similarity Index Measure (SSIM)
* Log-likelihood
These metrics are used to investigate reconstruction accuracy, image quality, and convergence behavior.

## Repository Structure
SPECT-Iterative-Reconstruction/
│
├── README.md
│
└── notebooks/
    │
    ├── phantoms/
    │   ├── phantom_NEMA.ipynb
    │   └── phantom_grayscale.ipynb
    │
    ├── reconstruction/
    │   └── MLEM_FBP.ipynb
    │
    └── improved_methods/
        ├── MLEM_MRP.ipynb
        └── OSEM_MRP.ipynb

### Notebook Description
| Notebook                  | Description                                        |
| ------------------------- | -------------------------------------------------- |
| `phantom_NEMA.ipynb`      | Generation and processing of the NEMA phantom      |
| `phantom_grayscale.ipynb` | Generation and processing of the grayscale phantom |
| `MLEM_FBP.ipynb`          | Reconstruction and comparison of MLEM and FBP      |
| `MLEM_MRP.ipynb`          | MLEM reconstruction with the Median Root Prior     |
| `OSEM_MRP.ipynb`          | OSEM reconstruction with the Median Root Prior     |

## Requirements
The project is implemented in Python and uses the following main libraries:

* NumPy
* SciPy
* scikit-image
* Matplotlib
* pandas
* Jupyter Notebook

## Installation
Clone the repository:
git clone https://github.com/USERNAME/SPECT-Iterative-Reconstruction.git
cd SPECT-Iterative-Reconstruction

Install the required Python packages:
pip install -r requirements.txt

## Usage
The notebooks can be executed in the following order:
1. Generate the NEMA and grayscale phantoms.
2. Generate projection data and simulate Poisson noise.
3. Perform MLEM and FBP reconstruction.
4. Perform MLEM-MRP reconstruction.
5. Perform OSEM-MRP reconstruction.
6. Evaluate and compare the reconstructed images using the selected image quality metrics.

## Results
Representative reconstruction results and quantitative comparisons will be added as the project develops.
The results are intended to demonstrate the effects of photon-count level, statistical noise, iterative reconstruction, and prior information on reconstructed image quality.

## References
Relevant references for SPECT imaging, iterative reconstruction, MLEM, OSEM, and prior-based reconstruction methods are provided in the project documentation.

**Project status:** Ongoing research project.
