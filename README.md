# Rescue-Flow
Disaster Relief Coordination System is a C program that simulates aid dispatch to disaster zones. It manages inventory, tracks zones' severity and weather, and prioritizes aid using a queue system. Dijkstra’s algorithm calculates the shortest route from the aid center, optimizing disaster response.


# 🌍 Disaster Relief Coordination System

This C program simulates a disaster relief coordination system that optimizes the dispatch of aid to various disaster zones. The system efficiently manages inventory, tracks disaster zones, prioritizes aid distribution based on severity and weather factors, and uses Dijkstra's algorithm for route optimization.

---

## 📚 Table of Contents
1. [🛠️ System Overview](#-system-overview)
2. [⚙️ Key Features](#-key-features)
   - [📦 Inventory Management](#-inventory-management)
   - [🏙️ Zone Management](#-zone-management)
   - [🚚 Aid Dispatching](#-aid-dispatching)
   - [🖥️ User Interface](#-user-interface)
3. [💻 Code Structure](#-code-structure)
   - [📦 AidPackage Structure](#-aidpackage-structure)
   - [🏙️ Zone Structure](#-zone-structure)
   - [🗃️ Queue Structure](#-queue-structure)
   - [🛠️ HashTable Structure](#-hashtable-structure)
4. [⚡ Algorithms](#-algorithms)
   - [🧑‍💻 Dijkstra’s Algorithm](#-dijkstras-algorithm)
   - [📍 Shortest Path Calculation](#-shortest-path-calculation)
5. [📝 How to Use](#-how-to-use)
6. [📂 License](#-license)

---

## 🛠️ System Overview

The Disaster Relief Coordination System is a C-based program aimed at providing a streamlined solution for disaster relief operations. The program efficiently simulates the coordination between an aid center and multiple disaster zones, managing inventory, aid dispatching, and ensuring the shortest route for aid delivery using a combination of data structures and algorithms.

---

## ⚙️ Key Features

### 📦 Inventory Management

The system maintains an inventory of essential relief items (food, medical supplies, tents) using a hash table. The inventory is updated as aid is dispatched to zones, ensuring the available stock is always up-to-date.

### 🏙️ Zone Management

Zones (representing cities or disaster areas) are managed using a `Zone` structure. Each zone has:
- **Severity Level**: The priority of the disaster.
- **Weather Factor**: Adjustments for delays due to weather conditions (normal, rain, snow, storm).
- **Required Aid Packages**: The relief items needed by each zone.

### 🚚 Aid Dispatching

Aid is dispatched using a queue system based on zone severity and weather conditions. The program employs **Dijkstra's algorithm** to calculate the shortest paths from the aid center to various zones, ensuring efficient resource delivery.

### 🖥️ User Interface

A menu-driven interface allows the user to:
1. View inventory.
2. Add aid requests to zones.
3. Process aid calls and dispatch relief materials.
4. Restock inventory.

---

## 💻 Code Structure

### 📦 AidPackage Structure

```c
typedef struct AidPackage {
    char itemName[50];  // Name of the relief item
    int quantity;       // Quantity of the item required
} AidPackage;
