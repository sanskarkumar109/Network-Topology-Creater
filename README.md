# 🌐 Network Topology Creator

A web-based application for designing, configuring, visualising, and exporting network topologies.  
Built with a **Django REST backend** and an interactive **HTML5/CSS3/JavaScript frontend** using **Konva.js**, it allows network engineers and students to draw devices, establish cable connections, configure pseudowires, group devices, and generate structured **JSON topology data**.

---

## ✨ Features & Enhancements

- 🎨 **Modern Dark UI & Grid Canvas**: Sleek interface featuring a CAD-style engineering grid background, dynamic responsiveness, and clean typography (Inter & Fira Code).
- 💻 **Interactive Devices**: Add Computers, Routers, and Switches with dynamic, editable text labels attached to shapes.
- 🔌 **Smart Cabling & Handle Snapping**: Connect nodes with **1G Ethernet** or **10G Fiber** cables. Draggable handles feature snap-to-shape proximity locking and real-time handle synchronization as devices are moved.
- ⚙️ **Advanced Link Points**: 
  - **LAG Points**: Link Aggregation endpoints sliding dynamically along cable vectors.
  - **CFM Points**: Connectivity Fault Management endpoints constrained to link vectors.
- 🔀 **Pseudowire Emulation**: Connect devices with dashed pseudowire links, configuring protocol, emulated service, and MPLS label attributes.
- 🏷️ **Group Management**: Group connected network nodes, assigning custom protocol (e.g., OSPF, BGP) and transport types. Automatically renders rotated protocol badges along cable paths.
- 💾 **Diagram Persistence & Database Storage**: Save, load, update, and delete diagrams directly to/from the Django SQLite backend database via REST APIs.
- 📋 **Topology JSON Modal & Export**: View formatted topology JSON in a sleek modal with one-click **Copy to Clipboard** and **Download JSON** options.
- 🖼️ **Multi-Format Image & PDF Export**: Export high-resolution diagrams as **PNG**, **JPG**, or **PDF** documents.
- ⌨️ **Keyboard Shortcuts**: Quick shape deletion using `Delete` or `Backspace` keys.

---

## 🚀 Getting Started

### ✅ Prerequisites
- [Python 3.x](https://www.python.org/downloads/)
- [pip](https://pip.pypa.io/en/stable/)

---

### 🔧 Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/sanskarkumar109/Network-Topology-Creater.git
   cd Network-Topology-Creater
   ```

2. **Install dependencies**:
   ```bash
   pip install django
   ```

3. **Run database migrations (optional)**:
   ```bash
   python manage.py migrate
   ```

4. **Start the Django backend server**:
   ```bash
   python manage.py runserver
   ```

5. **Open in Browser**:
   Navigate to 👉 `http://127.0.0.1:8000/`

---

## 📖 Usage Guide

1. **Add Devices & Cables**: Click or drag items from the **Devices & Cables** palette onto the canvas.
2. **Relabel Devices**: Click the inline text box underneath any device to assign custom hostnames (e.g., `dut1`, `router_east`).
3. **Connect Devices**: Drag blue line handles over devices to auto-snap cable endpoints to shapes.
4. **Create Pseudowires**: Select 2 devices and click **Add Pseudowire** to assign MPLS labels and protocol settings.
5. **Add LAG / CFM Points**: Select 2 connected devices, then click **LAG Point** or **CFM Point** to attach fault/aggregation markers onto the cable.
6. **Form Groups**: Select multiple connected shapes and click **Create Group & Properties** to assign group protocols.
7. **Generate & Export JSON**: Click **Generate JSON** to open the interactive JSON inspector modal to copy or download your topology definition.
8. **Export Diagram**: Click **Export PNG**, **Export JPG**, or **Export PDF** in the footer to download diagram images.

---

## 🧰 Tools & Technologies

* **Backend**: Django 5 (Python) + SQLite
* **Frontend**: HTML5, Vanilla CSS3 (Custom Glassmorphic Theme), JavaScript (ES6+)
* **Canvas Engine**: [Konva.js 2D Canvas](https://konvajs.org/)
* **Document Export**: [jsPDF](https://github.com/parallax/jsPDF)

---

## 🤝 Contributing

Contributions, bug reports, and feature requests are welcome! Feel free to open issues or submit pull requests.
