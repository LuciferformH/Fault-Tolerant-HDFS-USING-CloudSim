# Fault-Tolerant HDFS using CloudSim

## Project Overview

**Group**: G3  
**Course**: CSE468 - Cloud Computing (Unit 4)  
**Industry Scenario**: Scientific Research Archive (Data)  
**Tool**: CloudSim 3.0.3

---

## Project Description

This project implements a Fault-Tolerant HDFS (Hadoop Distributed File System) simulation using CloudSim. It demonstrates:
- 4 regionally distributed Data Centers
- 80 VMs (20 VMs per Data Center)
- 5000 Cloudlets per hour workload
- HDFS 3x replication factor
- Failure event simulation (5 VM shutdown)
- Resource allocation policy comparison

---

## Infrastructure

| Parameter | Value |
|-----------|-------|
| Data Centers | 4 (US-East, US-West, EU, Asia-Pacific) |
| VMs per DC | 20 |
| Total VMs | 80 |
| Workload | 5000 Cloudlets/hour |
| HDFS Replication | 3x |
| Block Size | 128 MB |

---

## Results

### Policy Comparison

| Policy | Avg Response (ms) | Throughput (ops/s) |
|--------|-------------------|-------------------|
| Round Robin | 250.00 | 1.39 |
| Throttled | 180.50 | 1.85 |

**Improvement**: 27.8% faster response, 33.1% more throughput

---

## Role Contributions

- **Role A (Infrastructure Lead)**: VM provisioning & host mapping
- **Role B (Storage & Data Architect)**: HDFS replication (3x)
- **Role C (Performance Analyst)**: Response time optimization
- **Role D (Sustainability)**: Cost-benefit analysis

---

## How to Run

### In Eclipse:
1. Import project: `File → Import → General → Projects from Folder or Archive`
2. Add CloudSim JAR: Right-click project → Build Path → Add External JARs
3. Run: Right-click `HDFSResearchArchive.java` → Run As → Java Application

### In Command Line:
```bash
javac -cp "lib/cloudsim-3.0.3.jar" -d "build/classes" src/HDFSResearchArchive.java
java -cp "lib/cloudsim-3.0.3.jar:build/classes" HDFSResearchArchive
```

---

## Project Structure

```
Group_G3_Fault_Tolerant_HDFS_CSE468/
├── src/
│   └── HDFSResearchArchive.java
├── lib/
│   └── cloudsim-3.0.3.jar
├── config/
│   └── hdfs-config.properties
├── .classpath
├── .project
└── README.md
```

---

## References

- CloudSim Documentation: https://github.com/Cloudslab/cloudsim
- HDFS Architecture: https://hadoop.apache.org/

---

**License**: Academic Project - CSE468 Cloud Computing