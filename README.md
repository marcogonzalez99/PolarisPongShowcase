# 🏓 PolarisPong v0.7.1 (Work in Progress)

**PolarisPong** is the first game built using **PolarisKit**, our lightweight, modular starter kit for developing 2D games with Pygame.  
It’s designed to be **fully replayable**, **polished**, and a **complete example** of what PolarisKit can deliver.

This project is **still in development**, and now showcases key PolarisKit features like **Scene Management**, **Asset Management**, **Save Management**, and **Audio Management** as it evolves toward **v1.0**.

[![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/J3J41IBU2Y)
---

## 📜 Why Pong?

Pong is **simple** and **classic**, making it the perfect first test case for PolarisKit.  

It requires:
- A complete game loop with clear transitions
- Scene stack handling
- Asset loading
- Input flow
- Save/load persistence

**PolarisPong proves that PolarisKit can deliver a small, polished game with persistent save/load, multiple game modes, customization, and achievements.**

---

## ✅ Current Features (v0.7.1)

- **Achievements System**
  - Fully functional and saved between sessions
  - Includes win counts, rally challenges, mode-specific wins, and customization milestones

- **Game Modes**
  - Regular
  - Speed Ball *(included in v0.7.1)*
  - Paddle Size Shuffler *(included in v0.7.1)*
  - Power Ball Shuffler *(included in v0.7.1)*
  - **Paddle Speed Shuffler** *(upcoming in v0.8)*

- **Customization**
  - **Ball Skins:** Blue, Green, Purple, Red, Shaded Blue, Shaded Green, Shaded Purple, Shaded Red
  - **Paddle Skins:** Black, White, Blue, Cloud Pattern, Cyan, Galaxy, Green, Red, Purple, Neon Variants
  - **Backgrounds:** Black, White, Grassy Soccer, Soccer, Basketball

- **Save System**
  - Stores skins, stats, achievements, and settings
  - Saves persist between sessions

- **Scenes**
  - Intro Scene
  - PolarisKit Splash Scene
  - Title Scene w/ Mode Select, Achievements, Customize, Settings
  - Settings Scene (Create/Delete Save, Toggle FPS, Credits)
  - Achievements Scene
  - Main Gameplay Scene (Player vs CPU)
  - Pause Menu (Quit, Resume, Back)

- **Audio**
  - Ball bounce, paddle hit, score sounds
  - Main menu music
  - Music and SFX manager built into PolarisKit

---

## 🏆 Achievements List (Draft)

- **First Win** – Win your first match  
- **5 Wins** – Win 5 matches total  
- **10 Wins** – Win 10 matches total  
- **25 Wins** – Win 25 matches total  
- **Longest Rally 10** – Reach a rally of 10 hits  
- **Longest Rally 25** – Reach a rally of 25 hits  
- **Longest Rally 50** – Reach a rally of 50 hits  
- **Longest Rally 100** – Reach a rally of 100 hits  
- **Win 5 Normal Mode** games *(planned)*  
- **Win 5 Speed Ball Mode** games *(planned)*  
- **Win 5 Power Ball Mode** games *(planned)*  
- **Win 5 Paddle Size Randomizer** games *(planned)*  
- **Win 5 Paddle Speed Shuffler** games *(planned)*
- **Shutout Win** – Win a match without allowing a single point  
- **Achievement Hunter** – Unlock all other achievements  

---

## 🚀 Planned Features for v1.0

- Finalize all **5 game modes**
- Expanded **Customization Options**:
  - Ball skins: Soccer ball, Baseball, Basketball, Classic Pong, more
  - Paddle skins: Wooden, Hockey stick, Tech paddle
  - Backgrounds: Hockey rink, Dirt field, Grass field, Tech grid
- Gameplay Enhancements:
  - Match End screen (Win/Loss display)
  - Stats screen (Games Played, Wins, Longest Rally)
- Additional achievements tied to new content
- Visual polish and menu improvements

---

## 🛠 Built on PolarisKit v2.0

PolarisKit currently provides:

- **SceneManager stack system** (Intro, Title, Game, Pause, Achievements, Match End)
- **Global pause system** (ESC from anywhere)
- **Asset + Sound loader** for images, SFX, fonts
- **Scene lifecycle** methods: `on_enter()` / `on_exit()`
- **Save/Load system** for stats, skins, achievements
- **Audio Manager** for SFX and Music
- **Clean, scalable folder structure**

---

## 🔒 Code Access

> The codebase is currently **private**.

---

## 👤 Built By

Marco @ **SB Studios**  
[GitHub](https://github.com/marcogonzalez99) · [LinkedIn](https://www.linkedin.com/in/marco-a-gonzalez99) · [Ko-fi](https://ko-fi.com/sbstudios)

---
