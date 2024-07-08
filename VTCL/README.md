# VTCL: Visual Text Contrastive Learning for Abnormal Behavior Recognition

## Overview
VTCL (Visual Text Contrastive Learning) is an innovative framework designed to enhance the detection of abnormal behaviors in campus environments using a multimodal contrastive learning approach. This repository contains the official implementation of VTCL, demonstrating its efficacy in robust abnormal behavior detection through both traditional and zero-shot learning methods.

## Features
- **Multimodal Learning:** Integrates visual and textual data to improve detection accuracy and system robustness.
- **Cross and Multi-frame Analysis:** Enhances spatial and temporal understanding of video data within the visual branch.
- **Innovative Prompting Technique ($PW_1PW_2L$):** Utilizes context-rich prompts in the textual branch to enhance the semantic understanding of behaviors.
- **Zero-Shot Prediction:** Capable of identifying unseen abnormal behaviors, thereby facilitating applications in dynamic environments without the need for retraining.

## Results
VTCL has been tested on multiple datasets, including CABR50 and UCF-101, and has achieved top-tier accuracies:
- **Top-1 Accuracy:** 86.92% on CABR50
- **Top-5 Accuracy:** 98.14% on CABR50
- Demonstrated competitive zero-shot performance on additional datasets like CABRZ6 and UCF-101.

## Computational Efficiency
Maintains competitive computational efficiency, making it suitable for real-time applications in various settings.

## Usage
The codebase is designed to be user-friendly and is structured for easy integration into existing projects. Detailed usage instructions will be provided for setting up and running the model, including how to load data, train, test, and evaluate the results.

## Contributing
We welcome contributions from the community. Please refer to our contribution guidelines for more information on how to submit issues, propose bug fixes, or improve the code.

## License
This project is released under the [MIT License](LICENSE).

## Citation
If you find this work useful, please consider citing it in your publications. Citation details are provided in the `CITATION.md` file.

