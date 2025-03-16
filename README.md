# 🎉 Tailwind Animations Plugin

An easy-to-use, ready-made animation library for Tailwind CSS. Quickly apply beautiful animations directly via Tailwind utility classes.

---

## 📖 Overview

This Tailwind CSS plugin offers a collection of ready-to-use, creative, and smooth CSS animations, categorized for easy use:

- Attention Seekers
- Back Entrances & Exits
- Bouncing Entrances & Exits
- Fading Entrances & Exits
- Flippers
- Lightspeed Effects
- Rotating Entrances & Exits
- Special Effects
- Zooming Entrances & Exits
- Sliding Entrances & Exits

## 🚀 Installation

Install via npm:

```bash
npm install tailwind-animations-plugin
```

---

## 📌 Setup

After installation, include the plugin in your `tailwind.config.js`:

```js
 // tailwind.config.js
module.exports = {
  content: [
    "./resources/views/**/*.blade.php",
    "./resources/js/**/*.js",
    // add your project paths here
  ],
  plugins: [
    require('tailwind-animations-plugin'),
  ],
};
```

### 📌 Dynamic class usage

If you're dynamically creating class names via JavaScript, you should explicitly include these classes in the `safelist`: Optional (Recommended)

```js
 // tailwind.config.js
module.exports = {
  content: [
    "./resources/views/**/*.blade.php",
    "./resources/js/**/*.js",
  ],
  safelist: ["animate-bounceC", "animate-flash", "animate-pulseC" /* all animation classes you use dynamically */],
  plugins: [
    require('your-plugin-name'),
  ],
};
```
⚠️ Important Note: Dynamic Class Usage in JavaScript

When using Tailwind classes in JavaScript, you must ensure that class names appear as full, clean strings in your code for Tailwind to recognize them. If classes are dynamically generated using template literals (animate-${animation}), Tailwind will not detect them during compilation.

✅ Correct way (Tailwind detects it):
```javascript
const element = document.getElementById("box");
element.classList.add("animate-bounceC", "text-red-500");
```
------------------------------------------------------------

❌ Incorrect way (Tailwind won't detect this dynamically generated class):
```javascript
const animation = "bounceC";
const element = document.getElementById("box");
element.classList.add(`animate-${animation}`); // Tailwind cannot see this class in static analysis
```
✅ Solution: If you need dynamic classes, either add all possible animation classes to safelist in tailwind.config.js or use explicit class names in your JS code


## 🚀 Usage

Once configured, use the animation utility classes in your markup:

### HTML example (Blade, React, Angular):

```html
<div class="animate-flash animate-duration-1000ms animate-iteration-infinite">
  Flash Animation
</div>
```

### ✅ Animation Duration, Delay, Iteration

You can customize your animation:

```html
<div class="animate-bounceC animate-duration-1500ms animate-delay-2s animate-iteration-infinite">
  Bounce Animation (Custom duration and delay)
</div>
```

---

## 📖 Available Animations

**Attention Seekers**:

- `animate-bounceC`, `animate-flash`, `animate-pulseC`, etc.

**Bouncing Entrances/Exits:**

- `animate-bounceIn`, `animate-bounceOut`, etc.

**Fading Entrances/Exits:**

- `animate-fadeIn`, `animate-fadeOut`, etc.

... and many more!

(Full list available in `tailwind.config.js`)

---

## 🚀 Examples

Include example HTML:

```html
<!-- Bounce Animation -->
<div class="animate-bounceC animate-duration-750ms">
  Bouncing in!
</div>

<!-- Fade animation example -->
<div class="animate-fadeInUp animate-duration-1500ms">
  Fading In!
</div>
```

---

## ⚙️ Installation (NPM)

```bash
npm install tailwind-animations-plugin
```

---

## 📦 Requirements

- Tailwind CSS `^3.x`

---

## 🙌 Contributing

Feel free to contribute new animations or improvements.

---

## 📜 License

MIT © Joe Nassar All rights reserved

