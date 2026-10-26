Zip Bomb Lab: Algorithmic Complexity & Denial of Service
An interactive educational visualization demonstrating decompression bombs (also known as ZIP bombs) as an algorithmic-complexity and resource-exhaustion security example.

Overview
A decompression bomb is an archive or compressed input that expands into a disproportionately large amount of data when processed. If an application does not impose appropriate resource limits, processing the archive can exhaust memory, storage, CPU time, or other resources, potentially causing a denial of service (DoS).

Zip Bomb Lab lets learners explore this relationship through a safe mathematical simulation. It does not create, upload, or decompress actual archives.

Learning objectives
By using this application, learners can:

Explain the relationship between compressed size, expansion ratio, and expanded size.
Understand how inexpensive input can trigger expensive processing or resource consumption.
Connect decompression bombs to resource-exhaustion and denial-of-service risks.
Experiment with resource budgets and see why limits matter.
Identify practical defensive measures for archive-processing systems.
Interactive features
Compressed-size slider: Adjust the hypothetical input size from 1 MB to 100 MB.
Expansion-ratio slider: Explore ratios from 1× to 1,000×.
Resource-budget slider: Set a simulated resource budget from 50 MB to 2,000 MB.
Protection toggle: Compare processing with and without a modeled size limit.
Visual comparison: Compare input size, expanded output, and the resource budget.
High-expansion preset: Load a predefined example.
Knowledge check: Answer a multiple-choice question and receive feedback.
Concept explanations: Read about complexity, resource exhaustion, and defensive strategies.
The mathematical model
The application calculates the hypothetical expanded size as:


text
Expanded size = Compressed size × Expansion ratio
For example, a hypothetical 2 MB input with a 1,000× expansion ratio would represent 2,000 MB of expanded output.

This is an illustrative model, not a measurement of a real compression algorithm. The expansion ratio alone does not determine execution time, and actual archive-processing costs depend on the format, data, implementation, and available resources.

How to run
No installation, server, package manager, or external dependency is required.

Download or clone this repository.
Open index.html in a modern web browser.
Move the sliders, toggle protection, and try the quiz.
The application uses standard HTML, CSS, and JavaScript and can run locally in a browser.

Project structure

text
zip-bomb-lab/
├── index.html
├── README.md
└── reflection.md
Defensive takeaways
Real applications that process archives should consider:

Maximum total decompressed bytes.
Maximum per-file expanded size.
Maximum archive-entry count and nesting depth.
CPU-time and wall-clock-time limits.
Safe handling of malformed or suspicious archives.
Isolation and monitoring for resource-intensive processing.
A high compression ratio is not proof of malicious intent. Effective defenses combine explicit resource budgets, validation, and safe failure handling.

Safety statement
This project is designed for education. It does not generate malicious archives, perform decompression, upload files, or execute an attack. All resource usage is represented through arithmetic and visual elements.
