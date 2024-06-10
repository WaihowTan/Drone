# Drone Fleet Rental Management System 

## Functional Requirements
1. **Storage of Map Data**:
   - The system must be able to store map data for use in drone missions.

2. **Real-time Tracking of Drones**:
   - The system must track the status and location of all drones in the fleet in real-time.

3. **Data Collection by Drones**:
   - Drones must be able to collect various types of data (e.g., imagery, videos, sensor data) during missions.

4. **Generation of Detailed Reports**:
   - The system must generate detailed reports on drone missions, including flight logs, data collected, and any anomalies encountered.

5. **Drone Registration**:
   - Managers should be able to register new drones with detailed information.

6. **Drone Detail Retrieval**:
   - Workers should be able to check the details of a drone by providing specific information such as the drone’s name, date registered, date created, last use, last service, drone ID number, drone brand, and drone capacity.

7. **Real-time Monitoring of Drone Status**:
   - Workers should be able to monitor the real-time status (battery levels, condition, location) of drones.

8. **Mission Scheduling**:
   - Workers should be able to create and schedule drone missions for parcel delivery.

9. **Integration with External Map Service**:
   - The system should integrate with an external map service (e.g., Google Maps) for map data.

## Non-Functional Requirements
1. **Low Latency**:
   - The maximum allowable latency for data transmission from the drone to the server and from the server to the computer should not exceed 100 milliseconds in 95% of the transactions.

2. **High Success Rate**:
   - The data transfer should have a 99.9% success rate to ensure consistent and reliable communication.

### Scalability
- **Storage**:
  - 10TB of storage per week of high-resolution map data, including satellite images, topographic maps, and 3D terrain models.

### Throughput
- **Data Processing**:
  - The system should handle processing of up to 1 TB of map data daily, including uploads, updates, and analysis tasks.

## Software Architecture
The Drone Fleet Management System will utilize a client-server architecture. The server will manage data storage, real-time tracking, mission scheduling, and reporting. Clients (desktop or tablet applications) will interact with the server to access real-time drone data, manage missions, and view reports.

## Technological Stack
- **Backend**:
  - **Language**: Python
  - **Framework**: Flask
  - **Database**: PostgreSQL
  - **Real-time Communication**: WebSocket
  - **External Map Service Integration**: Google Maps API

- **Frontend**:
  - **Framework**: React.js
  - **State Management**: Redux
  - **Mapping**: Leaflet.js

- **Infrastructure**:
  - **Cloud Hosting**: AWS
  - **Containerization**: Docker
  - **Orchestration**: Kubernetes

- **Monitoring and Logging**:
  - Prometheus for monitoring metrics
  - ELK stack (Elasticsearch, Logstash, Kibana) for logging and visualization.
