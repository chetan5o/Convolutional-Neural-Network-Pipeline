# Convolutional-Neural-Network-Pipeline
Implemented a hardware CNN pipeline in SystemVerilog for a 1024×1024 input, featuring 4×4 convolution, Leaky ReLU activation, and 2×2 average pooling. The design interfaces with DRAM, handles fixed-point arithmetic, padding, and truncation, and is fully verified and synthesized.
## 📂 Documentation

[**📄 View Project Specification**](https://github.com/chetan5o/Convolutional-Neural-Network-Pipeline/blob/main/ece564_Project2025_spec.pdf?raw=true)

## 📂 Design Approach/Challenges
1. Need to process the inputs and write back with 1.25x of read cycles.
2. Synthesis should run under 30min.

Read the design_approach for more details like 
1. what should be size of the buffer
2. optimize pattern to slize
3. how to store the processed data
* [**Design Approach (PDF)**](https://github.com/chetan5o/Convolutional-Neural-Network-Pipeline/blob/main/design_approach_pdf.pdf?raw=true)

### 🎥 Dataflow Visualization
To understand the dataflow for convolution, I have created an animation that illustrates how the data moves through the pipeline:
* [**View Dataflow Animation (PDF)**](https://github.com/chetan5o/Convolutional-Neural-Network-Pipeline/blob/main/data_path_slidiing_pdf.pdf?raw=true)
* [**Download Editable Design PPTX**](https://github.com/chetan5o/Convolutional-Neural-Network-Pipeline/blob/main/design_approach.pptx?raw=true) — Added my powerpoint here. If you have a better architecture you can use this template.


### 📊 High-Level Architecture & Performance Metrics 
1. Highlevel data flow architecture diagram.
2. Pipelined MAC to reduce the critical path.
3. Included Area, Synthesized clock and simulation time to calculate performace
* [**View Architecture & Metrics (PDF)**](https://github.com/chetan5o/Convolutional-Neural-Network-Pipeline/blob/main/CNN_architecture_metrics.pdf?raw=true)

