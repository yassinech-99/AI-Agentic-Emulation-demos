
# Network Configuration and Emulation Platform

A comprehensive platform for planning, executing, and testing network configurations with realistic device emulation.

## Overview

This project combines two powerful capabilities:
1. **Network Configuration Planning**: Converts natural language instructions into device-specific command sequences
2. **Router Emulation**: Provides realistic Cisco IOS XE/XR router emulation for command execution and testing

Together, these components create a complete environment for network automation, testing, and learning.

## Key Components

### 1. Command Planning System
- **Planner Agent**: Transforms natural language requirements into step-by-step network configuration commands
- **Task Management**: Tracks task execution and provides status updates
- **Plan Execution**: Automatically runs generated commands on the emulated device

### 2. Device Emulation System
- **Router Emulation**: Supports both Cisco IOS XE and XR with realistic responses
- **CLI Emulation**: Generates authentic command-line interface responses
- **API Emulation**: Optional RESTCONF API response emulation
- **State Management**: Tracks and updates device configuration state

### 3. Common Infrastructure
- **State Representation**: Flexible state objects for device configuration
- **Interactive GUI**: Chainlit-based user interface with multiple interaction modes
- **Workflow Engine**: LangGraph-powered processing pipeline

## Interaction Modes

### Planning Mode
- Enter natural language instructions (e.g., "Configure OSPF on all interfaces with a loopback address")
- Receive a step-by-step command plan
- Execute the plan with progress tracking
- Review command outputs
- Save the resulting device state

### Direct Device Mode
- Interact directly with the emulated device
- Enter standard CLI commands
- Receive realistic device responses
- View the current device state
- Save, load, and modify state snapshots

## Use Cases

- **Network Automation**: Test automation scripts in a safe environment
- **Configuration Prototyping**: Quickly develop and test complex configurations
- **Training**: Learn network configuration through natural language instructions
- **Documentation**: Generate configuration guides with verified command sequences
- **Testing**: Validate configurations before deployment on physical devices

## Features

- **Natural Language Interface**: Generate network commands from plain English
- **Multi-Device Support**: Emulate different IOS versions and device types
- **State Persistence**: Save and load device states between sessions
- **Task Tracking**: Monitor execution progress with task-based UI
- **Realistic Emulation**: Accurate responses matching real Cisco devices

## Dependencies

- LangChain
- LangGraph
- Chainlit
- OpenAI GPT models (or alternative LLMs)
- Pydantic

## Extending the System

This platform can be extended in several ways:
1. **Additional Device Types**: Add support for more network vendors and OSes
2. **New Command Types**: Extend the planner to support additional protocols or features
3. **Enhanced State Tracking**: Add more detailed state representation
4. **Integration with External Tools**: Connect to physical devices or network simulators
5. **Custom Prompt Types**: Create specialized prompts for specific network tasks
