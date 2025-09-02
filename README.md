# medix-shell
this is my jurney to taming an legacy netbeas

# 🐉 NetBeans Monster Inherited, Chaos Modularized

> *How I survived a 40,000-line Java class from hell — and made it behave.*

---

## 📜 Project Summary

This project showcases a **strategic refactor** of an inherited Java-based hospital system, originally built on **NetBeans GUI Builder** with:

- 💀 900+ hardcoded buttons  
- 🔁 15,000+ lines of duplicated access logic  
- 🧟 A monstrous `MainForm.java` class exceeding 40,000 LOC  
- 🧩 300+ libraries with conflicting versions

Rather than rewrite everything, I built **a new modular structure** that preserves critical logic while opening space for future scalability.

---

## 🧠 What I Inherited

| Element           | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| 🔥 Access Logic   | 15,000 lines of nested `if` conditions for permission filters               |
| 🎯 Buttons        | 900+ hardcoded buttons — difficult to search, filter, or extend             |
| 🎩 Monster Class  | `MainForm.java` — ~40K lines, performs everything from layout to logic       |
| 🎢 Libraries      | 300+ JARs, many outdated or incompatible                                     |

---

## 🧩 What I Built

| Solution            | Impact                                                                 |
|---------------------|------------------------------------------------------------------------|
| `MenuKernel.java`   | A new modular UI entry point                                           |
| Keyword Filtering   | Simplified button search using input fields                            |
| Gradual Refactor    | Compatible with legacy behavior while isolating new logic              |
| Category Filtering  | Roadmap-ready — planned for next iteration                             |

---

## 🔁 Code Snapshot: Before vs After

### 💥 Before (Access Logic, Hardcoded)
```java
if (user.equals("admin")) {
    akses.setpenjualan_obatfalse();
    akses.setpermintaanlabfalse();
    akses.setperiksaradiologifalse();
    // ... hundreds more
}
🌱 After (Access Service, Dynamic UI)
kotlin
Copy code
if (AccessManager.has("radiology")) {
    addButton("Radiology", iconRadiology) {
        openRadiologyModule()
    }
}
📁 Project Structure
bash
Copy code
simrs-menu-refactor/
├── assets/
│   ├── mainform-legacy.png
│   └── menukernel-ui.png
├── legacy_snapshots/
│   └── MainForm_fragment.java
├── src/
│   ├── MenuKernel.java
│   └── AppShell.kt
└── README.md
🚧 Roadmap
[✅] Create modular MenuKernel as replacement for frmUtama

[✅] Implement dynamic keyword filtering

[⏳] Plan category-based button grouping

[⏳] Migrate access logic to centralized AccessManager

[⏳] Clean legacy button listener logic

🧨 Dev Philosophy
“I didn’t just refactor. I performed live brain surgery on a monolithic monster — while keeping it alive.”

In systems that matter — like hospitals — rewrite isn't always an option.
My goal is scalable evolution, not reckless heroism.

🤝 Let’s Collaborate
If you're facing a legacy system nightmare — let's talk.

🧠 Mihaaq
📧 mihaaq.arch@gmail.com
🔗 https://github.com/Mihaaq-arch
🔗 https://www.notion.so/NetBeans-Monster-Inherited-Chaos-Modularized-2627eca1f12980ab877ec13b1e64e2f1?source=copy_link

