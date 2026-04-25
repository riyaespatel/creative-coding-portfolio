# Creative Coding & Digital Art Showcase
### Curriculum & Examples from Ohlone College (2022-2024)

![p5.js](https://img.shields.io/badge/p5.js-ED225D?style=for-the-badge&logo=p5.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

This repository contains a collection of interactive sketches and digital art used during my time as a **Digital Literacy & Creative Coding Mentor** at Ohlone College. My workshops focused on teaching students how to use **p5.js** to explore the intersection of mathematics, data science, and visual design.

## 🌟 Featured Projects

### 1. Perlin Noise Nebula
**Simulating fluid dynamics and stellar gas clouds using 2D Perlin noise**

![Nebula Preview](https://img.shields.io/badge/Status-Live-success?style=flat-square)

**Concept:** This project demonstrates how natural phenomena like nebulae and fluid flows can be simulated using Perlin noise—a type of gradient noise that produces organic, flowing patterns. The sketch creates thousands of particles that follow a dynamically generated flow field, resulting in mesmerizing, cloud-like formations.

**Learning Objectives:**
- Understanding non-linear randomness vs. pure randomness
- Working with vector fields and force-based particle systems
- Implementing efficient particle systems with object-oriented programming
- Real-time user interaction with physics simulations

**Key Features:**
- 🎨 Interactive color palette switching (Nebula Blue / Plasma)
- ⚡ Adjustable flow speed, noise scale, and particle count
- 🖱️ Mouse interaction to disturb particle flow
- 💫 Smooth trail rendering with alpha compositing

**Technical Highlights:**
```javascript
// Flow field generation using Perlin noise
let angle = noise(xoff, yoff, zoff) * TWO_PI * 4;
let v = p5.Vector.fromAngle(angle);
```

[**View Live Demo**](perlin-nebula.html) | [**View Source Code**](perlin-nebula.html)

---

### 2. Algorithmic Symmetry
**Generative art utilizing trigonometric identities to create complex geometric forms**

![Symmetry Preview](https://img.shields.io/badge/Status-Live-success?style=flat-square)

**Concept:** This piece explores the mathematical beauty of symmetry groups and harmonic oscillation. By layering trigonometric functions and applying rotational symmetry, the sketch generates hypnotic, kaleidoscopic patterns that evolve over time.

**Learning Objectives:**
- Mapping mathematical functions to visual properties (position, color, stroke)
- Understanding polar coordinates and their relationship to Cartesian space
- Exploring symmetry groups (cyclic rotational symmetry C_n)
- Creating layered compositions with transparency and blending

**Key Features:**
- 🔄 Adjustable symmetry order (3-24 fold symmetry)
- 🎭 Four preset patterns: Rosette, Mandala, Spirograph, Fractal Bloom
- 🌈 Dynamic color cycling based on HSB color mode
- 🎯 Mouse-driven phase shifting for interactive exploration

**Technical Highlights:**
```javascript
// Parametric pattern generation in polar coordinates
let r = amplitude * (1 + 0.5 * sin(complexity * t));
let x = r * cos(t);
let y = r * sin(t);
```

[**View Live Demo**](algorithmic-symmetry.html) | [**View Source Code**](algorithmic-symmetry.html)

---

### 3. Data-Driven Particle Systems
**Interactive system where particle behavior is dictated by real-time data inputs**

![Particles Preview](https://img.shields.io/badge/Status-Live-success?style=flat-square)

**Concept:** This sketch demonstrates how simple rules and data inputs can create emergent complexity. Each particle is an independent agent with its own physics properties, yet when combined with attractor forces and neighbor connections, complex swarm behaviors emerge.

**Learning Objectives:**
- Integrating Data Science principles with real-time rendering
- Object-oriented programming with particle classes
- Implementing physics simulations (gravity, attraction, collision)
- Real-time statistics tracking and visualization

**Key Features:**
- 📊 Live system statistics (particle count, average speed, energy, connections)
- 🧲 Dynamic attractor system with mouse interaction
- 🎮 Four behavior modes: Swarm, Orbit, Chaos, Flow
- 🔗 Proximity-based particle networking
- 💥 Particle burst generation

**Technical Highlights:**
```javascript
// Class-based particle with encapsulated physics
class Particle {
    applyForce(force) {
        let f = p5.Vector.div(force, this.mass);
        this.acc.add(f);
    }
    
    applyAttractor(attractor) {
        let force = p5.Vector.sub(attractor.pos, this.pos);
        let distance = constrain(force.mag(), 5, 100);
        let strength = (attractor.strength) / (distance * distance);
        force.setMag(strength);
        this.applyForce(force);
    }
}
```

[**View Live Demo**](data-particles.html) | [**View Source Code**](data-particles.html)

---

## 🛠️ Skills Demonstrated

### Languages & Frameworks
- **JavaScript (ES6+)** - Modern syntax, arrow functions, classes
- **p5.js** - Creative coding library built on Processing
- **HTML5 Canvas** - Low-level graphics rendering
- **CSS3** - Modern layout with Flexbox/Grid, custom properties, animations

### Mathematical Concepts
- **Trigonometry** - Sin, cos, tangent for circular motion and oscillation
- **Vector Mathematics** - Vector addition, normalization, dot/cross products
- **Perlin Noise** - Coherent noise functions for natural randomness
- **Polar Coordinates** - Converting between polar and Cartesian systems
- **Harmonic Oscillators** - Creating periodic motion with sin/cos waves

### Programming Paradigms
- **Object-Oriented Programming** - Classes, inheritance, encapsulation
- **Functional Programming** - Pure functions, immutability where applicable
- **Event-Driven Programming** - Mouse/keyboard interaction handling
- **Real-time Systems** - 60fps animation loops, performance optimization

### Version Control
- **Git** - Branching, commits, merging
- **GitHub** - Repository management, GitHub Pages deployment

### Teaching Philosophy
- Breaking down complex algorithms into digestible visual components
- Providing interactive controls for experimental learning
- Emphasizing the connection between mathematics and art
- Encouraging creative exploration through parameter manipulation

---

## 🚀 Getting Started

### Local Development

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/creative-coding-portfolio.git
cd creative-coding-portfolio
```

2. **Open any HTML file in your browser:**
```bash
# Using Python 3
python -m http.server 8000

# Using Node.js
npx http-server

# Or simply open index.html in your browser
```

3. **Navigate to:**
```
http://localhost:8000
```

### Deployment

This site is designed to work seamlessly with GitHub Pages:

1. Push to your repository
2. Go to Settings → Pages
3. Select your branch (usually `main`)
4. Your site will be live at `https://yourusername.github.io/creative-coding-portfolio/`

---

## 📚 Learning Resources

### p5.js Documentation
- [p5.js Reference](https://p5js.org/reference/)
- [p5.js Tutorials](https://p5js.org/learn/)
- [The Coding Train](https://thecodingtrain.com/) - Excellent video tutorials by Daniel Shiffman

### Mathematical Art
- [The Nature of Code](https://natureofcode.com/) - Physics simulations in processing
- [Generative Design](http://www.generative-gestaltung.de/) - Visualizing code
- [Tyler Hobbs on Generative Art](https://tylerxhobbs.com/essays)

### Creative Coding Communities
- [OpenProcessing](https://openprocessing.org/) - Share and discover creative code
- [Shadertoy](https://www.shadertoy.com/) - Fragment shader art
- [Dwitter](https://www.dwitter.net/) - JavaScript code golf

---

## 🎓 Workshop Series Context

These sketches were developed as part of a comprehensive Creative Coding curriculum at Ohlone College. The workshops covered:

**Week 1-2:** Introduction to p5.js, basic shapes, and color theory  
**Week 3-4:** Animation loops, transforms, and coordinate systems  
**Week 5-6:** Object-oriented programming and particle systems  
**Week 7-8:** Physics simulations and vector mathematics  
**Week 9-10:** Perlin noise and organic motion  
**Week 11-12:** Trigonometry and generative patterns  
**Week 13-14:** Data visualization and final projects

Each project in this repository represents a culmination of multiple weeks' worth of concepts.

---

## 🤝 Contributing

While this is primarily a portfolio/educational repository, I welcome suggestions and improvements:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/improvement`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/improvement`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License - see below for details:

```
MIT License

Copyright (c) 2024 [Your Name]

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📧 Contact

**Created by:** [Your Name]  
**Role:** Digital Literacy & Creative Coding Mentor  
**Institution:** Ohlone College  
**Period:** 2022-2024

- 🌐 Portfolio: [yourwebsite.com](https://yourwebsite.com)
- 💼 LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)
- 📧 Email: your.email@example.com
- 🐙 GitHub: [@yourusername](https://github.com/yourusername)

---

## 🙏 Acknowledgments

- **Ohlone College** - For providing the platform to teach creative coding
- **Daniel Shiffman** - For The Coding Train and Nature of Code
- **Processing Foundation** - For creating and maintaining p5.js
- **My Students** - For their creativity, curiosity, and feedback

---

<div align="center">

**⭐ If you found this helpful, please consider starring the repository! ⭐**

Made with ❤️ and JavaScript

</div>
