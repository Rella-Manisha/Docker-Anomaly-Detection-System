# Docker Anomaly Detection System

A Python-based system that automatically monitors Docker 
container logs and detects anomalous behaviour using 
log parsing and machine learning techniques.

## Problem it solves
Manually checking Docker logs is slow and unreliable 
at scale. This system automates the detection process 
and flags unusual patterns instantly — no manual review needed.

## How it works
```
Docker Container → Log Output → Parser → ML Model → Flag Anomaly
```

## Features
- Parses raw Docker container log files automatically
- Detects unusual patterns using ML-based anomaly detection
- Flags suspicious log entries for further review
- Lightweight and runs locally without cloud dependency

## Technologies
| Technology      | Purpose                        |
|-----------------|--------------------------------|
| Python          | Core programming language      |
| Docker          | Container log source           |
| Log Parsing     | Extract structured data        |
| Scikit-learn    | Machine learning model         |
| Pandas          | Data processing                |

## Project Structure
```
docker-anomaly-detection/
│
├── anomaly_detector.py   # Main detection script
├── log_parser.py         # Parses raw Docker logs
├── model.py              # ML model training & prediction
├── requirements.txt      # Python dependencies
├── .gitignore            # Files to ignore
└── README.md             # Project documentation
```

## How to run

### 1. Clone the repo
```bash
git clone https://github.com/Rella-Manisha/Docker-Anomaly-Detection-System.git
cd Docker-Anomaly-Detection-System
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Collect Docker logs
```bash
docker logs CONTAINER_NAME > logs/container.log
```

### 4. Run the detector
```bash
python anomaly_detector.py
```

## Sample output
```
[INFO]  Log file loaded: 1200 entries found
[OK]    Entry 001 — Normal
[OK]    Entry 002 — Normal
[ALERT] Entry 047 — ANOMALY DETECTED (confidence: 91%)
[OK]    Entry 048 — Normal
[ALERT] Entry 103 — ANOMALY DETECTED (confidence: 87%)

Summary: 2 anomalies detected out of 1200 log entries.
```

## Results
- Automatically flags anomalous log entries
- Reduces manual log review time significantly
- Works on any Docker container log output

## Future improvements
- Add real-time log monitoring (live streaming)
- Build a simple dashboard to visualize anomalies
- Support multiple containers simultaneously
- Send email/Slack alert when anomaly is detected

## Author
**Rella Manisha**  
B.Tech CSE (Cyber Security) — Vignan's Institute of Engineering for Women  
[LinkedIn](https://www.linkedin.com/in/rella-manisha-597943288) | [GitHub](https://github.com/Rella-Manisha)
