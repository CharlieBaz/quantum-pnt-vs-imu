# Navigation Project: Conventional IMU vs. Quantum PNT

This repository contains a Python notebook outlining how rapidly navigation errors build when estimating position through conventional smartphone inertial sensors, compared to an idealised zero-drift quantum (PNT) sensor.

## Core Methodology

* **Strapdown Navigation:** Processes raw IMU measurements through static bias correction, 3D coordinate transformation, and explicit gravity compensation.
* **Numerical Integration:** Utilizes trapezoidal double integration of linear acceleration to estimate velocity and trajectory over time.
* **Error Quantification:** Compares the integrated IMU trajectory against interpolated smartphone GPS ground truth to calculate absolute 3D position and velocity error.
* **Theoretical Benchmarking:** Contrasts empirical inertial drift against a theoretical quantum PNT model defined as $E_{quantum}(t) \approx 0$.

## Data Collection

To run this with custom data, export walking sessions from the phyphox app containing Accelerometer, Gyroscope, Magnetometer, and Location CSVs at ~100 Hz. Ensure a ~5 second stationary window in order to calibrate zero-offsets. Place these CSVs in the data/ directory
