# pulse-doppler-forge-MATLAB-radar
# MatlabRadarModeling: End-to-End Radar System Simulation

A comprehensive, open-source MATLAB simulation suite for modeling, designing, and analyzing radar systems. This repository provides foundational scripts, link budget calculators, and signal processing chains to simulate radar performance across diverse environments.

## 🚀 Features

*   **Radar Link Budget Calculator:** Model the radar equation, atmospheric losses, and target Radar Cross Sections (RCS).
*   **Waveform Generation & Processing:** Simulate Linear Frequency Modulation (LFM), pulsed waveforms, matched filtering, and stretch processing.
*   **Detection & Estimation:** Implements Constant False Alarm Rate (CFAR) processors (CA-CFAR, OS-CFAR) and Doppler processing.
*   **Target & Environment Models:** Includes Swerling target fluctuation models, clutter modeling, and ground/atmosphere path attenuation.

## 📁 Repository Structure

├── core_equations/       # Analytical models, link budgets, and range equations
├── waveforms/            # LFM, Barker codes, and ambiguity functions
├── signal_processing/    # Matched filtering, FFTs, Pulse-Doppler processing, and CFAR
├── examples/             # Pre-configured simulation scenarios (e.g., automotive FMCW)
└── README.md             # Project documentation
## 🛠️ Prerequisites & Installation

To run these simulations, you will need:
*   **MATLAB** (R2022a or newer recommended)
*   *Optional:* **Radar Toolbox** & **Signal Processing Toolbox** (Standard MATLAB implementations are provided in the `core_equations/` directory for users without toolbox licenses).

### Getting Started
1. Clone this repository:
   ```bash
   git clone https://github.com
   ```
2. Open MATLAB and navigate to the project root folder.
3. Run `examples/run_basic_simulation.m` to see a Pulse-Doppler radar simulation example.

## 📊 Quick Start Example

```matlab
% Simple Radar Range Equation Example
pt = 1e3;        % Peak Power (Watts)
gain = 30;       % Antenna Gain (dB)
freq = 10e9;     % Operating Frequency (10 GHz)
rcs = 1;         % Target RCS (sq meters)
snr_min = 15;    % Minimum detectable SNR (dB)

% Run the calculator
max_range = radar_range_calculator(pt, gain, freq, rcs, snr_min);
fprintf('Maximum Detection Range: %.2f km\n', max_range / 1000);
```

## 📚 References & Technical Sources
*   *Radar Systems Analysis and Design Using MATLAB* by Bassem R. Mahafza.
*   MathWorks Official [Radar Toolbox Documentation](https://mathworks.com).

## 📄 License
This project is licensed under the MIT License - see the LICENSE file for details.
