# Residential Network Architecture

![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=flat-square)
![Network](https://img.shields.io/badge/Network-Hybrid_Setup-blue?style=flat-square)
![Coverage](https://img.shields.io/badge/Coverage-Multi_Zone-orange?style=flat-square)
![Difficulty](https://img.shields.io/badge/Difficulty-Intermediate-yellow?style=flat-square)

## 🎯 Project Overview

This project documents the home network setup I designed and implemented to solve coverage and connectivity issues in a house with challenging layout and construction. The solution combines fiber internet, powerline adapters, enterprise Wi-Fi equipment, and multiple endpoints to provide reliable connectivity throughout the property.

The network serves multiple computers, smart home devices, and provides the infrastructure for my various IT lab projects and learning environments.

---

## 🏠 The Challenge

**House Layout Issues:**
- Long, narrow house with rooms spread across significant distance
- Dense wall construction (hardwood paneling) that interfered with Wi-Fi signals
- Need to connect multiple work areas with reliable internet
- Mix of wired and wireless devices requiring different connection types

**Requirements:**
- Reliable internet for remote work and lab projects
- Good Wi-Fi coverage throughout the house
- Wired connections for high-performance workstations
- Support for smart home devices and streaming

---

## 🌐 Network Design

### Internet Connection
- **ISP:** Fiber connection through Arris NVG443B modem/router
- **Speed:** Gigabit service providing sufficient bandwidth for all uses

### Core Infrastructure
- **Main Router:** ISP-provided Arris unit serving as DHCP server and gateway
- **Primary Connections:** Three key connections from main router:
  - Direct ethernet to gaming workstation (high performance)
  - Powerline adapter for extending wired network
  - PoE injector for enterprise access point

### Network Extensions
- **Powerline Network:** TP-Link adapters to extend ethernet over existing electrical wiring
- **Enterprise Wi-Fi:** Ruckus R730 access point for better coverage than consumer equipment
- **Wi-Fi Extender:** Additional TP-Link unit for far end of house coverage

---

## 🖥️ Connected Systems

### Primary Workstation (Direct Ethernet)
- **System:** Custom gaming PC (i7-12700K, RTX 3060, 32GB RAM)
- **Connection:** Direct gigabit ethernet for best performance
- **Purpose:** Primary work system, AI projects, gaming, 3D printing management

### Study Area Network
- **Connection Method:** Powerline adapter to unmanaged switch
- **Systems:** Two desktop computers sharing KVM switch
- **Purpose:** Secondary work area, research, backup systems

### Mobile Devices
- **Laptops:** Multiple systems for portable work and field use
- **Connection:** Wi-Fi through enterprise access point or extenders
- **Purpose:** Flexible access throughout house and property

---

## 📡 Wireless Coverage Strategy

### Enterprise Access Point
- **Model:** Ruckus R730 (early Wi-Fi 6 model)
- **Power:** PoE injector from main router
- **Location:** Central hallway for optimal coverage
- **Configuration:** Solo firmware (standalone operation)

### Coverage Extension
- **Secondary Wi-Fi:** TP-Link extender in bedroom area
- **Smart Devices:** Google Home/Nest devices throughout house
- **Entertainment:** Roku TV and gaming systems on wireless

---

## 🔧 Implementation Challenges & Solutions

### Ruckus Access Point Setup
**Challenge:** R730 model didn't support standard Unleashed firmware
**Root Cause:** Early Wi-Fi 6 chipset with limited firmware options
**Solution:** Researched and installed Solo firmware for standalone operation

### Powerline Network Reliability
**Challenge:** Electrical wiring quality affecting powerline performance
**Solution:** Selected higher-quality TP-Link adapters and tested multiple outlet locations
**Result:** Stable connection sufficient for office work and general internet use

### Wi-Fi Dead Zones
**Challenge:** House construction blocking wireless signals
**Solution:** Strategic placement of enterprise AP plus consumer extender
**Result:** Reliable coverage in all rooms and work areas

---

## 🔒 Network Security Improvements

### DNS Security
- **Primary DNS:** Quad9 (9.9.9.9) for malware/phishing protection
- **Secondary DNS:** 149.112.112.112 for redundancy
- **Benefit:** Network-level protection against known malicious domains

### Endpoint Hardening
- **Registry Modifications:** Applied consistent Windows privacy/security settings
- **Scope:** All Windows systems including VMs and workstations
- **Changes:** Disabled unnecessary telemetry, Cortana, Bing integration
- **Goal:** Reduce attack surface and improve privacy across all systems

---

## ✅ Current Network Performance

**Coverage Results:**
- ✅ Reliable internet access in all rooms and work areas
- ✅ High-performance wired connections where needed
- ✅ Good Wi-Fi performance for mobile devices and smart home equipment
- ✅ Stable connections for video calls and streaming

**Capacity Handling:**
- Multiple simultaneous video streams
- VPN connections for remote lab access
- File transfers and backup operations
- Smart home device management

---

## 📚 Skills Demonstrated

**Network Planning:**
- Site survey and coverage analysis for challenging building layout
- Selection of appropriate equipment for specific use cases
- Integration of consumer and enterprise networking equipment

**Implementation:**
- Powerline networking setup and optimization
- Enterprise access point configuration and firmware management
- Multi-zone coverage planning with various wireless technologies

**Troubleshooting:**
- Firmware compatibility research and resolution
- Performance optimization for mixed wired/wireless environment
- Security configuration across diverse endpoint types

---

## 🚀 Future Improvements

**Potential Upgrades:**
- **pfSense Router:** Replace ISP router with more capable open-source solution
- **Managed Switches:** Add VLANs for network segmentation
- **Additional APs:** Expand enterprise Wi-Fi coverage if needed
- **Network Monitoring:** Add tools for performance tracking and troubleshooting

**Learning Opportunities:**
- VLAN configuration and network segmentation
- Advanced firewall rules and traffic shaping
- Network monitoring and performance analysis tools

---

## 💡 Key Lessons

**Equipment Selection:**
- Enterprise equipment can be worth the investment for challenging environments
- Powerline adapters work well when implemented correctly
- Don't underestimate the impact of building construction on wireless signals

**Planning Approach:**
- Map out coverage needs before purchasing equipment
- Consider both current and future bandwidth requirements
- Test equipment in actual environment before final installation

**Practical Implementation:**
- Sometimes non-standard firmware solutions are necessary
- Network security improvements should be applied consistently
- Document configurations for future troubleshooting

---

## 🔗 Related Projects

- [`ruckus-r730-home-deployment`](https://github.com/Allen-Bartley/ruckus-r730-home-deployment) - Detailed AP setup documentation
- [`windows-server-ad-lab`](https://github.com/Allen-Bartley/windows-server-ad-lab) - Lab environment running on this network
- [`personal-pc-build-2024`](https://github.com/Allen-Bartley/personal-pc-build-2024) - Primary workstation on this network

---

> **Project Status:** Active production network  
> **Implementation Date:** 2025  
> **Current Performance:** Meeting all requirements reliably  
> **Skills Focus:** Network design, mixed equipment integration, coverage optimization