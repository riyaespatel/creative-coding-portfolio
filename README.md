# Creative Coding & Digital Art Showcase
### Curriculum & Examples from Ohlone College (2022-2024)

![p5.js](https://img.shields.io/badge/p5.js-ED225D?style=for-the-badge&logo=p5.js&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)

This repository contains a collection of interactive sketches and digital art used during my time as a **Digital Literacy & Creative Coding Mentor** at Ohlone College. My workshops focused on teaching students how to use **p5.js** to explore the intersection of mathematics, data science, and visual design.

## Featured Projects

### 1. Perlin Noise Nebula
**Simulating fluid dynamics and stellar gas clouds using 2D Perlin noise**

![Nebula Preview](https://img.shields.io/badge/Status-Live-success?style=flat-square)

**Concept:** This project demonstrates how natural phenomena like nebulae and fluid flows can be simulated using Perlin noise—a type of gradient noise that produces organic, flowing patterns. The sketch creates thousands of particles that follow a dynamically generated flow field, resulting in mesmerizing, cloud-like formations.

**Main Learning Objectives:**
- Understanding non-linear randomness vs. pure randomness
- Working with vector fields and force-based particle systems
- Implementing efficient particle systems with object-oriented programming
- Real-time user interaction with physics simulations

**Key Features:**
-  Interactive color palette switching (Nebula Blue / Plasma)
-  Adjustable flow speed, noise scale, and particle count
-  Mouse interaction to disturb particle flow
-  Smooth trail rendering with alpha compositing

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

**Main Learning Objectives:**
- Mapping mathematical functions to visual properties (position, color, stroke)
- Understanding polar coordinates and their relationship to Cartesian space
- Exploring symmetry groups (cyclic rotational symmetry C_n)
- Creating layered compositions with transparency and blending

**Key Features:**
-  Adjustable symmetry order (3-24 fold symmetry)
-  Four preset patterns: Rosette, Mandala, Spirograph, Fractal Bloom
-  Dynamic color cycling based on HSB color mode
-  Mouse-driven phase shifting for interactive exploration

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

**Main Learning Objectives:**
- Integrating Data Science principles with real-time rendering
- Object-oriented programming with particle classes
- Implementing physics simulations (gravity, attraction, collision)
- Real-time statistics tracking and visualization

**Key Features:**
-  Live system statistics (particle count, average speed, energy, connections)
-  Dynamic attractor system with mouse interaction
-  Four behavior modes: Swarm, Orbit, Chaos, Flow
-  Proximity-based particle networking
-  Particle burst generation

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

##  Skills Demonstrated

### Languages & Frameworks
- **JavaScript (ES6+)** - Modern syntax, arrow functions, classes
- **p5.js** - Creative coding library built on Processing
- **HTML5 Canvas** - Low-level graphics rendering
- **CSS3** - Modern layout with Flexbox/Grid, custom properties, animations

### Programming Paradigms
- **Object-Oriented Programming** - Classes, inheritance, encapsulation
- **Functional Programming** - Pure functions, immutability where applicable
- **Event-Driven Programming** - Mouse/keyboard interaction handling
- **Real-time Systems** - 60fps animation loops, performance optimization

### Teaching Philosophy
- Breaking down complex algorithms into digestible visual components
- Providing interactive controls for experimental learning

---


##  Contact

**Created by:** [Riya Patel]  
**Role:** Digital Literacy & Creative Coding Mentor  
**Institution:** Ohlone College  
**Period:** 2022-2024

- email: riyaespatel@gmail.com

