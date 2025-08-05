# Context-Aware Smart Building Sensor Placement Optimization Using PSO-GA Hybrid

## Contributors:

1st Chao Meng

2nd Oluwadamifola Ademoye

3rd Quang Thong Phung

4th Suhas Sunder

---

Our project utilizes the HouseExpo dataset found in this GitHub repository: https://github.com/TeaganLi/HouseExpo 

---

This repository implements a two-phase optimization framework for smart indoor environments. The system uses a hybrid Particle Swarm Optimization (PSO) and Genetic Algorithm (GA) to determine:

1. Optimal static placement of motion sensors over a 2D floor layout (Phase One)
2. Time-aware binary activation schedules for energy-efficient monitoring (Phase Two)

Sensor layouts are generated based on polygonal room geometry extracted from the HouseExpo dataset. Activity-aware activation masks are computed using synthetic occupancy weights informed by real-world behavior patterns.

---

## Demo Video

A live demonstration of the system is available on YouTube: https://youtu.be/jTwuYmSXz6c

pso_ga_demo_video.mp4 is also avilable within this repo itself, however, due to GitHub's size limitations the video had to be compressed and includes a watermark. Therefore, I would recommend viewing the YouTube video instead.

---

## Phase Overview

### Phase One: PSO + GA Sensor Placement

- Optimizes sensor coordinates \((x, y, r)\) to maximize layout coverage.
- Penalizes redundant coverage and excessive sensor radius.
- Outputs are saved to `phase1_sensors.json`.

### Phase Two: PSO + GA Activation Scheduling

- Uses fixed sensor layout from Phase One.
- For each of four time blocks (Morning, Afternoon, Evening, Night), computes a binary activation mask.
- Optimization balances weighted occupancy coverage vs. active sensor cost.
- Outputs are saved to `phase2_results.json`.

---

## How to Run

### Prerequisites

- Python 3.7+
- `numpy`, `matplotlib`

Install with:

```bash
pip install numpy matplotlib pprintpp
```

If using Jupyer Lab or Google Colab, the code can be run directly within the application using the 'run' button.
<img width="1062" height="209" alt="image" src="https://github.com/user-attachments/assets/2722177d-72b3-4dbb-aa46-2d54112d2451" />

The code files can also be copied into a .py file and run directly.

Run the phase one code file first then, after successful complection, run phase 2. Please refer to the video for further instructions: https://youtu.be/jTwuYmSXz6c 

### Execution

This project runs in:
- **JupyterLab** (recommended)
- **Google Colab** (with minor path adjustments)
- **Standard Python** by converting notebooks or cells to `.py` scripts


