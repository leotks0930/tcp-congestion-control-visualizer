# TCP Congestion Control Visualizer

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://html5.org/)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://javascript.com/)

[中文版本請見 README-zh.md](README-zh.md)

## Introduction

This project is a dynamic visualizer for TCP congestion control algorithms (Tahoe, Reno, CUBIC, BBR) based on HTML5 Canvas and JavaScript. It aims to translate abstract network protocols into visual sequences, helping students understand CWND dynamics and series summation.

## Key Features

* **Multi-algorithm Simulation**: Supports Tahoe, Reno, CUBIC, and Google BBR.
* **Real-time Visualization**: Visualizes throughput via dynamic line charts and Canvas-based image loading grids.
* **Parameter Customization**: Allows users to set `Loss Ceiling`, `Drop Rate`, and `Initial Window`.
* **Mathematical Analysis**: Automatically calculates the series summation ($\sum CWND$) for performance comparison.

## Visualization Logic

The simulator follows the **Piecewise Dynamic Recursive Function** logic:

* **Slow Start**: $CWND_{n+1} = CWND_n \cdot 2$
* **Congestion Avoidance**: $CWND_{n+1} = CWND_n + 1$
* **CUBIC Model**: Uses a cubic function inflection point to optimize bandwidth.
* **BBR Model**: Locks to the Kleinrock Limit for optimal throughput.

## How to Use

Follow these steps to explore the behavior of different network protocols:

1. **Access the Simulator**: Visit the [Live Demo](https://leotks0930.github.io/tcp-congestion-control-visualizer/tcp.hmtml) directly in your web browser.
2. **Configure Parameters**:
   * **Algorithm Selection**: Choose between Tahoe, Reno, CUBIC, or BBR to observe different growth patterns.
   * **Loss Ceiling**: Set the maximum threshold before the algorithm triggers a congestion response.
   * **Drop Rate**: Adjust the probability of packet loss to simulate real-world unstable network conditions.
3. **Run Simulation**: Click the `Start Simulation` button to begin the transmission process.
4. **Analyze Results**:
   * **Line Chart**: Observe how the $CWND$ (Congestion Window) values fluctuate over time.
   * **Canvas Grid**: Monitor the "Image Loading" speed, which serves as a visual proxy for network throughput and latency.
   * **Data Panel**: Review the calculated performance metrics (Total Throughput and Average Latency) provided at the end of the simulation.

## Contributors

* ltks0930

## License

MIT License.
