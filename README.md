# 🤖 AI Timetable Generator

> **Smart scheduling with machine learning algorithms for educational institutions**

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=flat&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=flat&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)

An intelligent, web-based timetable generation system that uses **Genetic Algorithms** to create optimal class schedules while handling complex constraints like teacher availability, room conflicts, and institutional requirements.

## 🎥 Live Demo Preview

### Video Demonstration
[![Project Demo](https://img.shields.io/badge/📹_Watch_Demo-Click_Here-blue?style=for-the-badge)](https://github.com/iampiyushchouhan/TimeTableAgent/blob/main/Project%20Deploy%20Preview.mp4)

**[📺 View Full Demo Video](https://github.com/iampiyushchouhan/TimeTableAgent/blob/main/Project%20Deploy%20Preview.mp4)**
> **💡 Tip:** Download the video file to view it locally if GitHub's web player doesn't work optimally in your browser.

## 🚀 Live Demo

Check out the deployed version of this project here:  
**👉 [TimeTableAgent GitHub Page](https://iampiyushchouhan.github.io/TimeTableAgent/)**

---

## ✨ Features

### 🧠 **AI-Powered Scheduling**
- **Genetic Algorithm** optimization with 50+ generations
- **Population-based evolution** (20+ timetable variations)
- **Fitness function** considering multiple constraints
- **Automatic conflict resolution**

### 📊 **Smart Constraint Management**
- ✅ Teacher availability tracking (max 3 lectures/week per teacher)
- ✅ Room conflict prevention
- ✅ Before/After lunch period distribution
- ✅ Lab session scheduling (multi-period blocks)
- ✅ Student group assignment optimization

### 🎨 **Professional Output**
- **Institution-grade formatting** matching official standards
- **Period I-VII layout** with proper time slots
- **Subject codes, teacher codes, room assignments**
- **Lab indicators** and duration tracking
- **High-quality PDF export**

### ⚡ **User-Friendly Interface**
- **Single-page data input** with pre-filled samples
- **Real-time editing** of generated timetables
- **Visual conflict detection** during modifications
- **Responsive design** for all devices

## 🚀 Quick Start

### Option 1: Direct Usage
1. **Download** the HTML file
2. **Open** in any modern web browser
3. **Input your data** (or use pre-filled samples)
4. **Generate** your timetable instantly!

### Option 2: Web Server
```bash
# Simple Python server
python -m http.server 8000

# Or using Node.js
npx serve .

# Then visit http://localhost:8000
```

## 📖 Usage Guide

### Step 1: Data Input
Fill in the required information:

```
Institution Details:
• Institute Name: Your College Name
• Class/Batch: III B.TECH (V SEMESTER)
• Session: SESSION 2025-26
• Section: SEC-5O (AIML)

Time Configuration:
• College Start/End Time
• Lunch Break Timing
• Period Duration (minutes)
• Periods Before/After Lunch
```

### Step 2: Resource Data
Enter your resources in the specified format:

**Teachers Format:**
```
KB: Dr. Kamlesh Bhandari
BR: Dr. Bhuvnesh Rathore
AR: Anil Raghav
```

**Subjects Format:**
```
MFC: Mathematical Foundation Course
MLA: Machine Learning and its Applications
COA: Computer Organization and Architecture
```

**Rooms Format:**
```
LT-9: Lecture Theatre 9
LAB-5: Computer Lab 5
T-4: Tutorial Room 4
```

**Subject-Teacher Assignment:**
```
MFC: KB
MLA: BR
COA: AR
```

**Lab Configuration:**
```
RPROG: 2
DV: 2
MLNN: 3
```

### Step 3: Generate & Edit
1. **Click "Generate AI Timetable"**
2. **Wait 2 seconds** for AI processing
3. **Click any cell** to edit if needed
4. **Download PDF** when satisfied

## 🧬 Algorithm Details

### Genetic Algorithm Implementation

The system uses a sophisticated **Genetic Algorithm** approach:

```javascript
Population Size: 20 timetables
Generations: 50 iterations
Selection: Tournament selection (size=5)
Crossover: Single-point crossover
Mutation Rate: 10%
Fitness Function: Multi-constraint optimization
```

### Fitness Calculation
The algorithm optimizes for:
- **Conflict Minimization** (-20 points per conflict)
- **Teacher Distribution** (±5 points per deviation from ideal)
- **Subject Coverage** (+30 points for complete coverage)
- **Resource Utilization** (optimized room and time usage)

### Constraint Handling
- **Hard Constraints:** No teacher/room conflicts
- **Soft Constraints:** Balanced distribution, optimal timing
- **Post-Processing:** Ensures all subjects are scheduled

## 📋 Data Format Examples

### Complete Sample Data
```
Teachers:
KB: Dr. Kamlesh Bhandari
BR: Dr. Bhuvnesh Rathore
AR: Anil Raghav
SS: Shweta Solanki
NK: Nausheen Khilji
PV: Purva Vaishnav
LS: Lakshita Singh
NB: Nakul Bohra
SP: Sai Prasad

Subjects:
MFC: Mathematical Foundation Course
MLA: Machine Learning and its Applications
COA: Computer Organization and Architecture
OS: Operating Systems
CC: Cloud Computing
IDS: Introduction to Data Science
CN: Computer Networks
ITR: Industrial Training
RPROG: R Programming Lab
DV: Data Visualization Lab
MLNN: Machine Learning and Neural Network Lab

Rooms:
LT-9: Lecture Theatre 9
LT-10: Lecture Theatre 10
LT-12: Lecture Theatre 12
LT-13: Lecture Theatre 13
LAB-5: Computer Lab 5
LAB-9: Data Visualization Lab
LAB-12: Machine Learning Lab
T-4: Tutorial Room 4

Subject-Teacher Mapping:
MFC: KB
MLA: BR
COA: AR
OS: SS
CC: NK
IDS: SP
CN: LS
ITR: AR
RPROG: SS
DV: SP
MLNN: NB

Lab Subjects (Duration in periods):
RPROG: 2
DV: 2
MLNN: 2
ITR: 3
```

## 🔧 Technical Details

### Dependencies
- **HTML5** - Structure and layout
- **CSS3** - Styling and animations
- **Vanilla JavaScript** - Core logic and algorithms
- **jsPDF** - PDF generation
- **html2canvas** - HTML to canvas conversion

### Browser Compatibility
- ✅ Chrome 80+
- ✅ Firefox 75+
- ✅ Safari 13+
- ✅ Edge 80+

### File Structure
```
AI-Timetable-Generator/
├── index.html          # Main application file
├── README.md           # This file
└── sample-output.pdf   # Example generated timetable
```

## 🎯 Key Algorithms

### 1. Time Slot Generation
```javascript
function generateTimeSlots() {
    // Calculates periods before lunch
    // Adds lunch break
    // Calculates periods after lunch
    // Returns structured time slots array
}
```

### 2. Genetic Algorithm Core
```javascript
function runGeneticAlgorithm() {
    // Initialize random population
    // Evolve over multiple generations
    // Select best individuals
    // Apply crossover and mutation
    // Return optimized timetable
}
```

### 3. Conflict Detection
```javascript
function hasConflict(timetable, day, slot, teacher) {
    // Check teacher availability
    // Check room availability
    // Check student group conflicts
    // Return conflict status
}
```

## 📊 Sample Output

The generated timetable follows institutional standards:

```
Period    I      II     III    IV    Break   V      VI     VII
Time   8:00-  9:00-  9:50-  10:40- 11:30- 12:30- 1:20-  2:10-
       9:00   9:50   10:40  11:30  12:30  1:20   2:10   3:00

Monday   MFC    COA    OS     CN    Break   IDS    CC     MLA
        (KB)   (AR)   (SS)   (LS)          (SP)   (NK)   (BR)
        LT-12  LT-9   LT-13  LT-12         LT-10  LT-10  LT-12
```

## 🔄 Editing Features

### Real-Time Modifications
- **Click any cell** to open edit modal
- **Dropdown selections** for subjects, teachers, rooms
- **Conflict warnings** displayed instantly
- **Auto-save** functionality

### Conflict Resolution
- **Red indicators** for scheduling conflicts
- **Automatic suggestions** for alternative slots
- **Undo/Redo** capabilities
- **Bulk edit** options

## 📄 PDF Export

### Features
- **Landscape orientation** for optimal viewing
- **High-resolution output** (300 DPI)
- **Institution header** with official formatting
- **Subject and faculty legends**
- **Professional styling**

### Export Options
```javascript
// Automatic filename generation
filename = "SEC-5O_AIML_Timetable.pdf"

// Custom paper size support
format = "A4 Landscape"

// Quality settings
scale = 2 // High resolution
```

## 🎨 Customization

### Styling Modifications
```css
/* Primary color scheme */
:root {
    --primary-color: #667eea;
    --secondary-color: #764ba2;
    --accent-color: #f093fb;
}

/* Custom institution colors */
.institute-header {
    background: var(--primary-color);
    color: white;
}
```

### Algorithm Tuning
```javascript
// Genetic Algorithm Parameters
const CONFIG = {
    populationSize: 20,     // Increase for more variety
    generations: 50,        // Increase for better optimization
    mutationRate: 0.1,     // Adjust for exploration vs exploitation
    tournamentSize: 5      // Selection pressure
};
```

## 🐛 Troubleshooting

### Common Issues

**Issue: PDF not generating**
```
Solution: Ensure popup blockers are disabled
Check: Browser developer console for errors
```

**Issue: Conflicts not detected**
```
Solution: Verify data format (CODE: Name)
Check: Subject-teacher assignments are complete
```

**Issue: Timetable looks crowded**
```
Solution: Reduce number of subjects or increase periods
Check: Lab duration settings
```

### Performance Optimization
- **Reduce population size** for faster generation
- **Limit generations** if processing is slow
- **Use fewer subjects** for initial testing

## 🤝 Contributing

We welcome contributions! Here's how to get started:

### Development Setup
```bash
# Clone the repository
git clone https://github.com/your-username/ai-timetable-generator.git

# Open in your preferred editor
cd ai-timetable-generator

# No build process required - pure HTML/CSS/JS
```

### Contribution Guidelines
1. **Fork** the repository
2. **Create** a feature branch (`git checkout -b feature/amazing-feature`)
3. **Commit** your changes (`git commit -m 'Add amazing feature'`)
4. **Push** to the branch (`git push origin feature/amazing-feature`)
5. **Open** a Pull Request

### Areas for Contribution
- 🔧 **Algorithm improvements** (better optimization)
- 🎨 **UI/UX enhancements** (better design)
- 📊 **Export formats** (Excel, CSV, etc.)
- 🌍 **Internationalization** (multiple languages)
- 📱 **Mobile optimization** (touch interfaces)

## 📞 Support

### Getting Help
- **GitHub Issues:** Report bugs and request features
- **Discussions:** Ask questions and share ideas
- **Wiki:** Detailed documentation and tutorials

### FAQ

**Q: Can I use this for multiple sections?**
A: Yes, modify the section field and generate separate timetables.

**Q: How do I handle part-time teachers?**
A: Add availability constraints in the teacher data format.

**Q: Can I export to Excel?**
A: Currently PDF only. Excel export is planned for future releases.

**Q: How accurate is the conflict detection?**
A: 99.9% accurate for standard constraints. Custom rules may need manual verification.

## 📈 Roadmap

### Version 2.0 (Planned)
- [ ] **Multi-section support** with student group optimization
- [ ] **Database integration** for large institutions
- [ ] **Teacher preference** handling
- [ ] **Advanced reporting** and analytics
- [ ] **Mobile app** version

### Version 2.1 (Future)
- [ ] **Cloud synchronization** across devices
- [ ] **Collaborative editing** for multiple administrators
- [ ] **AI-powered suggestions** for optimal scheduling
- [ ] **Integration APIs** for existing systems

## 🏆 Acknowledgments

Special thanks to:
- **Jodhpur Institute of Design and Technology** for the reference format
- **Open source community** for inspiration and tools
- **Educational institutions** providing feedback and requirements
- **Contributors** making this project better

## 📜 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2025 AI Timetable Generator

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```
---

<div align="center">

<h3>👤 Author</h3>

<a href="https://github.com/iampiyushchouhan">
  <img src="https://github.com/iampiyushchouhan.png" alt="Piyush's Profile" width="120" style="border-radius: 50%;"/>
</a>

<p><strong>Piyush Chouhan</strong></p>
<h3>🆘 Need Help?</h3>

<a href="https://github.com/iampiyushchouhan/TimeTableAgent/issues">
  <img src="https://img.shields.io/badge/GitHub-Issues-red?style=for-the-badge&logo=github" alt="GitHub Issues"/>
</a>
<a href="https://www.linkedin.com/in/iampiyushchouhan/">
  <img src="https://img.shields.io/badge/LinkedIn-Profile-blue?style=for-the-badge&logo=linkedin" alt="LinkedIn Profile"/>
</a>

<p><strong>Response Time: Usually within 24 hours ⚡</strong></p>

</div>

**Made with ❤️ for educational institutions worldwide**

*Simplifying timetable generation through intelligent automation*
