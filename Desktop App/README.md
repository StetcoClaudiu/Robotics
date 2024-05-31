
# Desktop Application Development with Tauri Framework
## Overview
The desktop application is built using the Tauri framework, combining React for the frontend and Rust for the backend. Its primary function is to facilitate communication between the computer and the transceiver connected to it, allowing data retrieval and storage into an SQLite database.

## Features
Data Communication: The application manages communication with the transceiver, enabling data retrieval from the robot and subsequent storage in the database.
Database Integration: Utilizing SQLite, the application stores incoming data for further analysis and visualization.
Scatter Charts: The app generates scatter charts to visually represent the distribution of plants in the field, aiding in analysis and decision-making processes.
Comparative Analysis: Users can compare different scatter charts side by side, enabling them to observe field variations and assess progress over time. Additionally, the application provides metrics such as the number of good and bad plants in each chart.
## Technologies Used
1. Tauri Framework: Provides the foundation for building cross-platform desktop applications, leveraging web technologies alongside Rust for enhanced performance.
2. React: Used for frontend development, enabling the creation of dynamic user interfaces for seamless interaction.
3. Rust: Employs Rust for backend functionalities, ensuring robustness, speed, and security in data handling and communication processes.
4. SQLite: Serves as the database management system, offering lightweight, self-contained storage for efficient data management.
## Database tables
1. Plant:
   -id
   -x_position
   -y_position
   -category
   -scan_id
2. Scan:
   -id
   -date
