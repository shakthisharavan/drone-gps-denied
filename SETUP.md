# Drone Dev Kit – Setup Guide
#SITL AND MAVPROXY setup
## 1. Update System
```bash
sudo apt update
sudo apt upgrade
```

---

## 2. Install Required Packages
```bash
sudo apt install git python3-pip python3-venv
```

---

## 3. Clone ArduPilot
```bash
git clone https://github.com/ArduPilot/ardupilot.git
cd ardupilot
```

---

## 4. Install ArduPilot Prerequisites
```bash
./Tools/environment_install/install-prereqs-ubuntu.sh -y
```

---

## 5. Install Python Dependencies
```bash
pip install -r requirements.txt
```

---

## 6. Install MAVProxy(inside venv)
### Install venv Package
```bash
sudo apt install python3-venv
```
###Example create a project folder
```bash
python3 -m venv venv
```

```bash
pip install mavproxy
```

---

## 7. Run SITL
```bash
sim_vehicle.py -v ArduCopter --console --map
```

---

## Troubleshooting

### Error: pymavlink not found
```bash
pip install pymavlink
```
