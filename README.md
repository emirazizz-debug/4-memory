# 4 MEMORY 🧠🎵

[![GitHub license](https://shields.io)](LICENSE)
[![PRs Welcome](https://shields.io)](http://makeapullrequest.com)

A sleek, responsive, and minimalist audio-visual memory game inspired by the classic arcade game *Simon*. Built completely from scratch using vanilla web technologies, this game challenges players to memorize and replicate an ever-increasing sequence of flashes and electronic tones.

🎮 **[Play the Live Game Here](https://github.io)** *(Remember to update this link with your live GitHub Pages URL!)*

---

## ✨ Features

- **Web Audio API Integration:** Generates pure, retro-style triangle wave harmonics directly in the browser—no heavy external audio assets or network requests required.
- **Responsive Dark Mode UI:** A clean, modern aesthetic with rich glow effects (`box-shadow` mapping) that fluidly scales across mobile screens, tablets, and desktops.
- **Dynamic Input Locking:** Built-in safeguards automatically freeze user inputs during sequence playback to ensure a fluid, bug-free gameplay rhythm.
- **High Score Tracking:** Keeps track of your best run during the session via local session variables so you can continuously challenge your memory limits.

---

## 🕹️ How to Play

1. Click the central **START** button to generate the first signal.
2. Watch the sequence of color flashes and listen to their associated musical tones.
3. Once the computer finishes, repeat the pattern exactly by clicking the colored pads.
4. Each successful round appends one random new signal to the existing sequence.
5. If you press the wrong pad, a low-frequency game-over buzzer sounds, displaying your final score. Hit **RETRY** to try again!

---

## 🛠️ Technical Stack & Implementation

- **HTML5:** Structured semantic markup and document object hierarchy.
- **CSS3:** Custom 2x2 grid layout, flexbox centering, active-state filters, and responsive mobile-first sizing.
- **JavaScript (ES6+):** Advanced asynchronous timing loops (`setInterval` execution buckets) and procedural synthesiser control.

```javascript
// Example of how the game synthesizes sound on-the-fly using code
const osc = audioCtx.createOscillator();
osc.type = 'triangle'; // Classic chip-tune arcade profile
osc.frequency.setValueAtTime(frequencies[color], audioCtx.currentTime);
```

---

## 🚀 Local Setup & Development

If you want to run, test, or tweak this project locally on your machine:

1. **Clone the repository:**
   ```bash
   git clone https://github.com
   ```
2. **Navigate into the project directory:**
   ```bash
   cd YOUR-REPO-NAME
   ```
3. **Launch the game:**
   Simply double-click the `index.html` file to open it directly in any modern web browser (Chrome, Safari, Firefox, Edge). Turn up your volume and start playing!

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome! Feel free to check the issues page if you want to add difficulty multipliers, continuous scoreboard memory (`localStorage`), or custom soundboard themes.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request
