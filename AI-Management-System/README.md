# AI Management System - 24/7 Autonomous Operation

A comprehensive AI-powered self-management system designed for 24/7 operation on your ASUS Vivobook Go (Intel i3-N305, 8GB RAM) with full PyCharm integration and autonomous learning capabilities.

## 🎯 Features

### ✅ Core Capabilities
- **24/7 System Monitoring**: Real-time CPU, memory, disk, temperature tracking
- **AI Task Management**: Automated execution of ML/AI workloads
- **Self-Learning**: Adaptive behavior based on system patterns
- **PyCharm Integration**: Automated development environment management
- **Resource Optimization**: Intelligent performance tuning
- **Health Monitoring**: Proactive alerts and auto-recovery

### 🔧 System Requirements
- **OS**: Windows 10/11
- **Python**: 3.11+ (you have 3.13.7 ✅)
- **RAM**: 8GB (optimal for your setup ✅)
- **Storage**: 500GB+ available (you have ~1TB ✅)
- **Network**: Stable internet connection ✅

## 🚀 Quick Start

### 1. Installation
```powershell
# Navigate to your Lexar drive
cd E:\Code\AI-Management-System

# Create virtual environment
python -m venv ai_env

# Activate environment
ai_env\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```

### 2. Initial Setup
```powershell
# Run the system
python main.py
```

## 💾 Drive Execution Layout

- **Drive F:\\ (Lexar NS100)** hosts the live codebase, automation scripts, and log pipelines. All orchestration jobs (`main.py`, schedulers, monitoring daemons) should be launched from this drive so they benefit from its write throughput and free space.
- **Drive E:\\** stores the durable datasets, SQLite databases, and any cross-system artifacts that must persist between drive swaps. When a job needs long-lived I/O (metrics snapshots, trading exports, backup bundles), point it to the E drive paths defined in the config files.
- Before starting a session, mount both drives and verify the paths in `.env.production` / `config/*.json` still reference `E:\\...` and `F:\\...`. The system expects this dual-drive layout; if either drive is missing, jobs will pause until both are available.

### 3. Access Control Panel
- **Web Interface**: http://localhost:8000
- **API Documentation**: http://localhost:8000/docs
- **Metrics Dashboard**: http://localhost:8000/metrics

## 📊 System Architecture

```
AI-Management-System/
├── main.py                 # Core system orchestrator
├── requirements.txt        # Dependencies
├── config/                 # Configuration files
├── data/                   # System metrics and logs
├── logs/                   # Application logs
├── models/                 # AI models storage
└── README.md              # This file
```

## 🎮 Usage Examples

### Basic Monitoring
```python
# Check system health
curl http://localhost:8000/metrics

# Get recent performance history
curl http://localhost:8000/metrics/history

# View active alerts
curl http://localhost:8000/alerts
```

### AI Task Execution
```python
# Run data analysis
curl -X POST "http://localhost:8000/tasks/execute?task_type=data_analysis" \
     -H "Content-Type: application/json" \
     -d '{"scope": "system_performance"}'

# Trigger system optimization
curl -X POST "http://localhost:8000/system/optimize"

# Train predictive models
curl -X POST "http://localhost:8000/tasks/execute?task_type=model_training" \
     -H "Content-Type: application/json" \
     -d '{"model_type": "performance_predictor"}'
```

## 🧠 AI Learning Capabilities

### Adaptive Monitoring
- **Pattern Recognition**: Learns your usage patterns
- **Predictive Alerts**: Forecasts potential issues
- **Auto-Tuning**: Adjusts monitoring frequency based on activity

### Performance Optimization
- **Resource Allocation**: Intelligent memory and CPU management
- **Process Prioritization**: Automatic priority adjustment
- **Cache Optimization**: Smart cache management for faster operations

### Self-Improvement
- **Model Updates**: Continuous model retraining
- **Parameter Tuning**: Automatic hyperparameter optimization
- **Behavior Adaptation**: Learns from system feedback

## 🔧 PyCharm Integration

### Automated Features
- **Project Configuration**: Auto-setup of development environment
- **Code Quality**: Integrated linting and type checking
- **Template Generation**: Smart code template creation
- **Inspection Rules**: Automated code quality enforcement

### Development Workflow
1. **Auto-Setup**: System configures PyCharm project automatically
2. **Smart Templates**: Generates code templates for common AI tasks
3. **Quality Checks**: Runs automated code inspections
4. **Performance Monitoring**: Tracks development environment performance

## 📈 Performance Monitoring

### Real-Time Metrics
- **CPU Usage**: Multi-core monitoring with alerts
- **Memory Tracking**: RAM usage with garbage collection optimization
- **Disk I/O**: Read/write performance monitoring
- **Network Activity**: Traffic analysis and optimization
- **Temperature**: Thermal monitoring for stable 24/7 operation

### Historical Analysis
- **Trend Detection**: Long-term performance patterns
- **Anomaly Detection**: Unusual behavior identification
- **Performance Prediction**: Forecasting resource needs

## 🛠️ Configuration

### System Thresholds
```json
{
  "cpu_max": 85.0,
  "memory_max": 80.0,
  "disk_max": 90.0,
  "temperature_max": 75.0
}
```

### Monitoring Intervals
- **Real-time**: Every 30 seconds
- **Detailed Analysis**: Every hour
- **Model Training**: Daily
- **System Optimization**: As needed

## 🔒 Security & Reliability

### 24/7 Operation Features
- **Auto-Recovery**: Automatic restart on failures
- **Health Checks**: Continuous system validation
- **Resource Limits**: Prevents system overload
- **Safe Mode**: Degraded operation during issues

### Data Protection
- **Local Storage**: All data stored on your E: drive
- **Encrypted Logs**: Sensitive information protection
- **Backup System**: Automatic data backup
- **Privacy First**: No external data transmission

## 📱 Integration Options

### GenX_FX Trading System
- **Market Data Analysis**: AI-powered trading insights
- **Performance Correlation**: Trading activity impact analysis
- **Resource Scheduling**: Optimal resource allocation during trading hours

### External APIs
- **Trading Platforms**: MT4/MT5 integration ready
- **Data Sources**: Multiple market data provider support
- **Alert Systems**: SMS/Email notifications (configurable)

## 🚀 Advanced Usage

### Custom AI Tasks
```python
# Add your own AI task
async def custom_analysis_task(self, params):
    """Custom AI analysis implementation"""
    # Your AI logic here
    return {"status": "completed", "insights": [...]}
```

### Custom Monitoring
```python
# Add custom metrics
def monitor_trading_activity(self):
    """Monitor GenX_FX trading activity"""
    # Your monitoring logic
    return trading_metrics
```

## 🐛 Troubleshooting

### Common Issues
1. **High CPU Usage**: System automatically optimizes
2. **Memory Leaks**: Built-in garbage collection
3. **Network Issues**: Automatic retry logic
4. **Disk Space**: Automatic cleanup routines

### Logs Location
- **System Logs**: `E:\Code\AI-Management-System\logs\`
- **Error Logs**: Check daily log files
- **Performance Data**: `E:\Code\AI-Management-System\data\`

## 📞 Support & Maintenance

### Self-Maintenance
- **Automatic Updates**: Self-updating capability
- **Health Checks**: Daily system validation
- **Performance Tuning**: Continuous optimization
- **Log Rotation**: Automatic log cleanup

### Manual Maintenance
```powershell
# Check system status
python -c "from main import AIManagementSystem; print('System OK')"

# Force optimization
curl -X POST "http://localhost:8000/system/optimize"

# View recent alerts
curl "http://localhost:8000/alerts"
```

## 🎯 Next Steps

1. **Run the system**: `python main.py`
2. **Open web interface**: http://localhost:8000
3. **Monitor performance**: Check metrics dashboard
4. **Customize settings**: Edit config files as needed
5. **Integrate with GenX_FX**: Connect to your trading system

---

**Optimized for your ASUS Vivobook Go with Intel i3-N305 and 8GB RAM**
**Perfect for 24/7 AI/ML hosting while keeping your main laptop free!** ✨