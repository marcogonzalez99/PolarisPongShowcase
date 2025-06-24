# 🎮 PolarisPong v1.0 (WiP)

**PolarisPong** is the first game built using **PolarisKit**, a lightweight modular starter kit for building 2D games with Pygame.  
PolarisPong is designed to be fully replayable, polished, and fun, a complete example of what PolarisKit can power.

This project serves both as a *complete game* and as a **showcase of PolarisKit's core features**, including its **Achievements system** and **Save/Load system**.

---

## To Add
- Add a PolarisKit splash Scene (KitScene)

## 🏓 Current Features

✅ Classic **Pong gameplay** (Player vs CPU)  
✅ **Skin customization** (Paddle + Ball skins)  
✅ **Pause menu** (ESC to pause from anywhere)  
✅ **Title screen**  
✅ Basic **sound effects** (Paddle hit, Wall hit, Point scored)  
✅ Built-in **debug overlay** (TAB to toggle)  
✅ **Achievements system** (unlockable badges + progress tracking)  
✅ **Stats system** (Games Played, Games Won, Longest Rally)  
✅ **Save/load system** (Skins, Stats, Achievements)

---

## 🏆 Achievements System

PolarisPong includes a built-in **Achievements system**, powered by PolarisKit:

- **First Win** → Win your first match  
- **5 Wins** → Win 5 matches total  
- **Shutout Win** → Win a match without allowing a single point  
- **Longest Rally 10** → Reach a rally of 10 hits  
- **Longest Rally 25** → Reach a rally of 25 hits  
- **Longest Rally 50** → Reach a rally of 50 hits  
- **Fast Win** → Win a match in under 2 minutes  
- **Comeback Win** → Win a match after trailing by 3+ points  

Achievements are unlocked through gameplay and tracked between sessions.

---

## 💡 Why Pong?

**Pong is simple**, but a great test case:

- It tests your scene system, asset loading, input flow, save/load patterns, and now the **Achievements framework**.
- Forces a complete game loop: Title → Game → Pause → Match End → Achievements → Back to Title.

**PolarisPong proves that PolarisKit can ship a small, polished game with save/load and achievements.**

---

## 🚀 Planned Features (Next Steps - v1.x)

- [ ] More **Achievements** (edge cases, mastery challenges)  
- [ ] **Match End screen** (You Win! / CPU Wins!)  
- [ ] **Background music** (looped)  
- [ ] **Stats screen** (view progress + achievements in a dedicated scene)  
- [ ] Additional **skins** (unlockable through achievements or milestones)

---

## Built on PolarisKit v2.1

PolarisKit currently provides:

✅ Direct **scene management stack system** (Title, Game, Pause, Achievements, Match End)  
✅ Global **pause system** (ESC key from anywhere)  
✅ **Achievements system** with visual badges and persistent progress  
✅ Simple **asset + sound loader** (images, SFX, fonts)  
✅ Clean and scalable **folder structure**  
✅ Scene lifecycle: **on_enter()**, **on_exit()**  
✅ Built-in **save/load system** for Stats and Achievements

---

## Notes

**PolarisPong** is intentionally simple:

- First goal: ship a complete small game built with PolarisKit v2.1  
- Second goal: demonstrate clean **Save/Load**, **Stats**, and **Achievements** using PolarisKit patterns  
- Third goal: establish a clean example of how PolarisKit can power **small retro games** for the **Polaris branch** and the **M64 console** project  

---

## 🔒 Code Access

> The codebase is currently **private**.  
> This repository is a **project showcase** highlighting features, screenshots, and development direction.  
> Interested in early access or collaboration?  
> Reach out via [LinkedIn](https://www.linkedin.com/in/marco-a-gonzalez99).

---

## Built By

Marco @ **SB Studios**  
[GitHub](https://github.com/marcogonzalez99) · [LinkedIn](https://www.linkedin.com/in/marco-a-gonzalez99)
