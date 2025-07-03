# 🏠 Residential Network Architecture

This repository documents the design and implementation of a hybrid home network infrastructure optimized for performance, coverage, redundancy, and workstation management. Built from the ground up by Allen Bartley, this setup reflects a practical integration of consumer-grade devices with enterprise-level planning.

---

## 🌐 Core Network Topology

### 🧩 ISP & Entry Point
- **Fiber Connection** → **Arris NVG443B Modem/Router**
  - **Port 1:** Direct to Gaming PC (LAN)
  - **Port 2:** TP-Link Powerline Adapter (Primary wired extension)
  - **Port 3:** PoE Injector powering Ruckus R730 Access Point

### ⚡ Powerline Expansion
- **TP-Link TL-WPA7617KIT:** Dual-band Wi-Fi extender used for wireless coverage on far end of house
- **TP-Link TL-PA9020P KIT:** Ethernet-to-unmanaged-switch bridge used in study room

---

## 📡 Wireless Coverage Zones

| Device | Location | Role |
|--------|----------|------|
| **Ruckus R730 AP** | Central hallway (PoE powered) | Main access point for home Wi-Fi |
| **TL-WPA7617KIT** | Bedroom zone | Secondary Wi-Fi coverage for remote rooms |

---

## 🖥️ Wired Endpoint Layout

### 🎮 Gaming Workstation (Direct LAN)

| Component | Specification |
|-----------|----------------|
| OS | Windows 11 Pro 64-bit |
| CPU | Intel Core i7 12700K |
| GPU | NVIDIA RTX 3060 12GB |
| RAM | 32GB DDR5 @ 5600MHz |
| Motherboard | MSI MAG B760 TOMAHAWK WIFI |
| Monitors | Dual: 4K Sceptre + HP 27mq |
| Storage | ~25TB across SATA, NVMe, USB |
> *Role:* Primary endpoint for gaming, image generation, and high-throughput tasks.

---

### 🖥️ Study Workstation (Powerline + Switch)

| Component | Specification |
|-----------|----------------|
| OS | Windows 10 Home 64-bit |
| CPU | Intel Core i5 6500 |
| GPU | NVIDIA RTX 2060 SUPER |
| RAM | 32GB DDR4 |
| Storage | 1.8TB HDD + 953GB SSD |
> *Role:* Productivity and research node. Connected via unmanaged switch and shared through a KVM setup.

---

### 🖥️ Auxiliary Study Workstation (KVM Node)

| Component | Specification |
|-----------|----------------|
| OS | Windows 11 Pro 64-bit |
| CPU | AMD Ryzen 3 3200U |
| GPU | AMD Vega 3 |
| RAM | 20GB DDR4 |
| Storage | 2TB HDD + 2TB SSD + 119GB USB |
> *Role:* Secondary access point via KVM switch. Supports backup tasks and image generation workflows.

---

### 💻 Main Laptop (Remote Access Node)

| Component | Specification |
|-----------|----------------|
| OS | Windows 11 Pro 64-bit |
| CPU | AMD Ryzen 3 3200U |
| GPU | AMD Vega 3 |
| RAM | 20GB DDR4 |
| Storage | 2TB HDD + 2TB SSD + 119GB USB |
> *Role:* Portable control node using VPN and remote access tools to connect to the gaming workstation and internal network services.

---

### 📱 Compact Touchscreen Laptop (Field Node)

| Component | Specification |
|-----------|----------------|
| OS | Windows 11 Pro 64-bit |
| CPU | Intel Celeron @ 1.80GHz |
| RAM | 12GB DDR4 |
| Storage | 2TB SATA SSD |
> *Role:* Ultra-mobile interface for light diagnostics, documentation, and fieldwork. OS manually reinstalled for security assurance.

---

## 🔌 Peripheral & Print Management

- **Dual Monitor KVM Switch**: Shares input/output between three active desktops
- **USB 3-Port Hub**: Front-mounted access at desk level for portable drives and peripherals
- **Canon imageCLASS MF273dw**: Wireless monochrome multifunction printer in study zone

---

## 🧠 Smart Home & Entertainment Ecosystem

| Device | Location | Role |
|--------|----------|------|
| Google Nest Display | Kitchen | Smart assistant & visual dashboard |
| Google Home Mini | Bathroom | Voice-controlled smart speaker |
| Roku TV + Google TV Stick + PS4 | Bedroom | Wireless media and entertainment hub |
| Smart Bulbs | Throughout | Voice and app-controlled lighting |
| Multiple Wi-Fi Endpoints | Various | Seamless coverage across residence |

---

## ✅ Project Highlights

- **Hybrid Topology**: Combines fiber input, powerline Ethernet, and Wi-Fi for multi-zone connectivity
- **Peripheral Switching**: Efficient device access across systems via KVM and USB hub
- **Redundancy Planning**: Multiple remote access tools and mirrored workstations
- **DIY Expertise**: Custom-built gaming PC and manually configured devices
- **Security Awareness**: Reinstalled OS on imported devices to eliminate potential risks

---

> Maintainer: Allen Bartley  
> Repo Created: July 2025  
> Status: Active Infrastructure  
