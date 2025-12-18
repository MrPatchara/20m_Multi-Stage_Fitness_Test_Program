# 🏃 20m Multi-Stage Fitness Test (Beep Test) Program

<div align="center">

![Python](https://img.shields.io/badge/Python-3.x-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Platform](https://img.shields.io/badge/Platform-Windows-lightgrey.svg)

**A comprehensive desktop application for conducting the 20-meter Multi-Stage Fitness Test (Beep Test) with real-time tracking, player management, and VO₂max calculation.**

[Features](#-features) • [Installation](#-installation) • [Usage](#-usage) • [Screenshots](#-screenshots) • [Contributing](#-contributing) • [License](#-license)

</div>

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Features](#-features)
- [Requirements](#-requirements)
- [Installation](#-installation)
- [Usage](#-usage)
- [VO₂max Calculator](#-vo₂max-calculator)
- [Project Structure](#-project-structure)
- [Contributing](#-contributing)
- [Contact](#-contact)
- [License](#-license)

---

## 🎯 Overview

The **20m Multi-Stage Fitness Test (Beep Test)** is a widely used fitness assessment tool that measures cardiovascular endurance and aerobic capacity. This application provides a digital solution for conducting the test with:

- ⏱️ **Real-time tracking** of levels, shuttles, speed, and distance
- 👥 **Multi-player support** (up to 10 players simultaneously)
- 🔊 **Audio beep signals** for accurate timing
- 📊 **VO₂max calculation** using the Léger et al. (1988) formula
- 🎨 **Modern, user-friendly interface**

---

## ✨ Features

### 🎮 Core Functionality

- **Automated Test Execution**: Runs the beep test protocol with 21 levels
- **Real-time Display**: Shows current level, shuttle number, speed (km/h), elapsed time, and total distance
- **Audio Cues**: Plays beep sounds at the correct intervals for each shuttle
- **Countdown Timer**: 10-second countdown before test begins
- **Start/Stop Controls**: Easy-to-use controls for test management

### 👥 Player Management

- **Multi-Player Tracking**: Support for up to 10 players simultaneously
- **Individual Results**: Track each player's completion level, shuttle, and distance
- **Result Display**: Real-time results panel showing all player completions
- **Completion Marking**: One-click button to mark when a player fails to complete a shuttle

### 📊 VO₂max Calculator

- **Accurate Calculation**: Uses the scientifically validated Léger et al. (1988) formula
- **Personalized Results**: Takes into account age, sex, level, and shuttle number
- **Fitness Rating**: Provides rating categories (Excellent, Good, Average, Below Average)
- **Easy Access**: Available through the Tools menu

### 🎨 User Interface

- **Dark Theme**: Modern dark color scheme for comfortable viewing
- **Responsive Layout**: Clean, organized interface with intuitive navigation
- **Menu System**: Accessible tools, help, and developer information
- **Visual Feedback**: Color-coded buttons and status indicators

---

## 📦 Requirements

### Software Dependencies

- **Python 3.x** (3.6 or higher recommended)
- **tkinter** (usually included with Python)
- **Pillow (PIL)** - For image handling
- **pygame** - For audio playback

### Required Files

- `beep.mp3` - Audio file for beep signals
- `book.png` - Image for help section
- `pic.png` - Developer profile image

---

## 🚀 Installation

### Step 1: Clone the Repository

```bash
git clone https://github.com/YourUsername/Beep-test-Program.git
cd Beep-test-Program
```

### Step 2: Install Dependencies

```bash
pip install pillow pygame
```

Or using `requirements.txt` (if available):

```bash
pip install -r requirements.txt
```

### Step 3: Verify Required Files

Ensure the following files are present in the project directory:
- `cal.py` (main application file)
- `beep.mp3` (audio file)
- `book.png` (help image)
- `pic.png` (developer image)

---

## 📖 Usage

### Starting the Application

Run the main Python file:

```bash
python cal.py
```

### Running a Test

1. **Prepare Players**: Ensure all players are ready at the starting line
2. **Click "Start Test"**: The application will show a 10-second countdown
3. **Follow Audio Cues**: Players run between the 20-meter lines following the beep signals
4. **Mark Completions**: When a player fails to complete a shuttle, click their "Complete" button
5. **View Results**: Results are displayed in real-time in the Results panel
6. **Stop Test**: Click "Stop Test" to end the test at any time

### Using the VO₂max Calculator

1. Navigate to **Tools → VO₂max Calculator**
2. Enter the following information:
   - **Age**: Player's age
   - **Sex**: Select Male or Female
   - **Level**: Final level reached (1-21)
   - **Shuttles**: Number of shuttles completed in that level (0-16)
3. Click **"Calculate VO₂max"**
4. View the calculated VO₂max value and fitness rating

### Menu Options

- **Tools → VO₂max Calculator**: Calculate VO₂max from test results
- **Help → How to use?**: View detailed usage instructions
- **Developer → Contact**: View developer contact information
- **Exit**: Close the application

---

## 🧮 VO₂max Calculator

The application uses the **Léger et al. (1988)** formula for VO₂max calculation:

```
VO₂max = 31.025 + (3.238 × Level) - (0.156 × Age) - (0.646 × Sex Factor)
```

Where:
- **Level**: The final level reached (1-21)
- **Age**: Player's age in years
- **Sex Factor**: 1 for Male, 0 for Female

### Rating Categories

- **Excellent**: VO₂max > 60 ml/kg/min
- **Good**: VO₂max > 50 ml/kg/min
- **Average**: VO₂max > 40 ml/kg/min
- **Below Average**: VO₂max ≤ 40 ml/kg/min

---

## 📁 Project Structure

```
Beep-test-Program/
│
├── cal.py                 # Main application file
├── beep.mp3              # Audio file for beep signals
├── book.png              # Help section image
├── pic.png               # Developer profile image
├── README.md             # This file
├── LICENSE               # MIT License
│
├── V.1.0/                # Version 1.0 build files
│   └── dist/             # Compiled executable
│
└── V.1.1/                # Version 1.1 build files
    └── dist/             # Compiled executable
```

---

## 🎯 Test Protocol

The application follows the standard 20m Beep Test protocol with 21 levels:

| Level | Shuttles | Speed (km/h) |
|-------|----------|--------------|
| 1     | 7        | 8.0          |
| 2     | 8        | 9.0          |
| 3     | 8        | 9.5          |
| 4     | 9        | 10.0         |
| 5     | 9        | 10.5         |
| ...   | ...      | ...          |
| 21    | 16       | 18.5         |

Each shuttle requires running 20 meters between two lines.

---

## 🤝 Contributing

Contributions are welcome! If you'd like to contribute to this project:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)
4. **Push to the branch** (`git push origin feature/AmazingFeature`)
5. **Open a Pull Request**

### Areas for Contribution

- 🐛 Bug fixes
- ✨ New features
- 📝 Documentation improvements
- 🎨 UI/UX enhancements
- 🧪 Testing improvements

---

## 📞 Contact

**Developer**: Mr. Patchara Al-umaree

- 📧 **Email**: Patcharaalumaree@gmail.com
- 💻 **GitHub**: [@MrPatchara](https://github.com/MrPatchara)
- 📱 **Phone**: +66-96-061-4238

---

## ⚠️ Important Notes

- ⚠️ **This program is for educational purposes only**
- ⚠️ **Not intended for commercial use**
- ⚠️ **Always ensure proper supervision during fitness testing**
- ⚠️ **Consult with healthcare professionals before conducting fitness tests**

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

- **Léger et al. (1988)** - For the VO₂max calculation formula
- **Multi-Stage Fitness Test Protocol** - Standard beep test protocol
- **Open Source Community** - For the amazing tools and libraries

---

<div align="center">

**Made with ❤️ for fitness enthusiasts and educators**

⭐ **Star this repo if you find it useful!** ⭐

</div>
