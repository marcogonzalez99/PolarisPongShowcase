# PolarisPong Changelog

## [v1.0.0] - 2025-08-30  
### Release  
- **Achievements System**:  
  - Added full achievement unlock tracking, including thresholds for rallies, total wins, and individual game modes.  
  - Implemented final **Pong Legend** achievement, awarded when all others are unlocked.  
  - Results screen now shows newly unlocked achievements with name and description.  

- **Results Scene**:  
  - Refactored to load save data and check achievements on `on_enter`, ensuring fresh data every time.  
  - Reset `new_achievements` on entry to avoid stale unlocks.  
  - Displays player summary (wins, mode-specific wins, highest rally) consistently.  

- **General**:  
  - Background music now plays on entry with fade effect.  
  - Various polish and consistency improvements across scene flow.  

---

## [v0.9.0] - 2025-08-29
### Refactor
- **GameScene**:
  - Replaced inline ball reset logic with dedicated `add_point` and `apply_gamemode_effects` methods for clarity.
  - Introduced `POINTS_TO_WIN` constant, removing hardcoded win score of 5.
  - Extracted winner handling into `set_winner` for cleaner save/stat updates.
  - Consolidated end-game logic so highest rally and wins always save consistently.
  - Corrected variable naming (`ract` → `rect`) for speed display.

- **Ball**:  
  - Fixed velocity clamping to handle both positive and negative values (±30).
  
---

## [v0.8.6] - 2025-08-28
### Gameplay & Physics  
- **Ball Physics**:  
  - Replaced `apply_gamemode_speed` with new `apply_angle_and_speed` method.  
  - Ball bounce angle now scales based on hit position relative to paddle center.  
  - In **speed mode**, both `x` and `y` velocity scale with rally count using `SPEED_INCREASE_FACTOR`.  
  - In **power mode**, both `x` and `y` velocity scale with paddle’s `power` value.  
  - Added wall-clamp logic to prevent the ball from sticking to the top/bottom edges.  
  - Paddle collision now clamps ball position to paddle edge to prevent phasing through.  

- **Opponent AI**:  
  - Refactored AI movement to use proportional movement capped by speed instead of rigid steps.  
  - Added smoothed error offset (linear interpolation toward randomized target offset).  
  - AI behavior now feels more human-like, avoiding sudden jerks and snaps.  

---

## [v0.8.5] - 2025-08-27
### Refactor  
- **CustomizeScene**:  
  - Unified `categories`, `option_keys`, and `selected_indices` into a single `customization_data` structure.  
  - Updated navigation and save logic to use unified data.  
  - Refactored `draw_customization_options` to render directly from `customization_data`.  

- **CreditsScene**:  
  - Replaced parallel lists (`headers`/`body`) with a single list of dicts for safer credits storage.  
  - Converted layout to use percentage-based constants (`OPTIONS_Y_START_PCT`, `OPTIONS_TITLE_X_PCT`, etc.).  
  - Standardized helper text positioning to bottom-left.  

- **AchievementsScene**:  
  - Replaced all magic numbers with percentage-based constants (`STARTING_Y_PCT`, `ACHIEVEMENT_SPACING_PCT`, `OFFSET_X_PCT`).  
  - Modularized drawing into helper methods (`draw_achievements_list`, `draw_page_counter`, `draw_selected_achievement`).  
  - Centered preview image dynamically with rects and stacked name/description below with scalable offsets (`NAME_OFFSET_PCT`, `DESC_OFFSET_PCT`).  
  - Added polish for locked achievements with darkened overlay.  
  - Cleaned navigation and scrolling logic with bounds checks and selection reset on page switch.  

## [v0.8.4] - 2025-08-26
### Refactor
- Standardized **PauseScene**, **SettingsScene**, **ResultsScene**, and **TitleScene** to use percentage-based layout (`*_PCT`) across all UI elements.  
- Cleaned up **draw methods** in each scene for clarity and consistency (`draw_helper_text`, `draw_save_summary`, `draw_achievements`, etc.).  
- Replaced hardcoded pixel offsets with scalable spacing constants.  
- Unified color usage with `WHITE`, `GRAY`, `GOLD`, and `SELECTED_GREEN` from `config`.  
- Simplified **PauseScene** logic to rely on explicit key prompts (`[Q]`, `[B]`, `[M]`), removing need for highlight states.  
- Refactored **save summary** in `ResultsScene` into a clean loop, reducing duplication.  

## [v0.8.3] - 2025-08-25
### Refactor
- Standardized **screen percentage constants** (`*_PCT`) for all scenes to eliminate magic numbers.
- Updated **IntroScene** to use percentage-based layout with clear named constants (e.g., `LOGO_Y_PCT`, `INTRO_TEXT_Y_PCT`, `EDGE_PCT`).
- Broke down `IntroScene` rendering into helper methods (`draw_logo`, `draw_center_text`, `draw_helper_text`) for clarity.
- Refactored resolution handling: `config.set_resolution()` is now called at startup, ensuring `SCREEN_WIDTH`, `SCREEN_HEIGHT`, and `SCALE` are always initialized properly.
- AssetManager now references `config` directly instead of importing frozen values, fixing `NoneType` issues.
- Cleaned up **font scaling** using `config.SCALE` for consistent visuals across 720p, 1080p, and 4K.
- Began standardizing UI positioning ratios across scenes for consistent layout logic.

### Changed
- Improved fullscreen handling logic; resolution is now detected automatically from monitor size.
- Reorganized layout constants: global anchors (e.g., `CENTER_X_PCT`, `EDGE_PCT`) live in `config`, while scene-specific percentages (e.g., `LOGO_Y_PCT`) live per scene.

---
## [v0.8.2] - 2025-08-15
### Refactor
- Refactor all of Ball, grouped paddles into a PaddleBlock class, grouping functions together. Refactored out magic numbers. Fix Intro, Settings and Pause

## [v0.8.1] - 2025-08-11
### Changed
- Changed names of all gamemodes (Classic, Speed Rush, Power Cycle, Paddle Morph and Paddle Overdrive)

## [v0.8] - 2025-08-10
### Added
- Add placeholder badges for all achievements (minus winning without losing a point)
- Add new gamemode **Paddle Speed Shuffle**


## [v0.7.1] - 2025-08-09
### Docs
- Update README to match the showcase document.
- Create Changelog to maintain and track updates

---

## [v0.7.0] - 2025-08-07
### Changed
- **Power Mode:** randomizes power levels.
- Refactor draw methods for cleaner rendering.
- Add hover effect to **Mode Select**.

---

## [v0.6.9] - 2025-07-28
### Changed
- Improve **Title Screen** animations.
- Update **Shuffle Mode** logic.

---

## [v0.6.8] - 2025-07-27
### Changed
- Minor updates to **Achievements**.

---

## [v0.6.7] - 2025-07-26
### Added
- **ResultsScene** for post‑match summaries.
- **Rally Tracking** system (enables rally-based achievements).
### Changed
- Improve detection logic for **Wins** and **Rally** achievements.

---

## [v0.6.6] - 2025-07-25
### Changed
- Make **menu music** consistent across scenes.
- Minor polish and cleanup.

---

## [v0.6.5] - 2025-07-24
### Changed
- Game modes now pass data correctly to **save file**; update save data format.

---

## [v0.6.4] - 2025-07-23
### Changed
- General **Achievements** updates.

---

## [v0.6.3] - 2025-07-21
### Added
- **Achievements Scene** preview panel.
- Additional **achievement badges**.

---

## [v0.6.2] - 2025-07-20
### Added
- **Achievements** and **Badge** support (base system).

---

## [v0.6.1] - 2025-07-15
### Changed
- Integrate fonts more cleanly; standardize screen width/height.
- Update some assets; switch to improved Pong font.
- Further **Achievements** logic improvements.

---

## [v0.6.0] - 2025-07-02
### Added
- More assets (paddles, fields).
- **Customize Scene** updates and asset loader improvements.

---

## [v0.5.1] - 2025-07-01
### Added
- **Grassy Soccer Field** background.

---

## [v0.5.0] - 2025-06-30
### Added
- **CustomizationScene** now saves user preferences.

---

## [v0.4.0] - 2025-06-29
### Added
- New scenes: **Credits**, **Settings**, **Customization**, **Achievements**.

---

## [v0.3.0] - 2025-06-24
### Changed
- Migrate project to **PolarisKit v2.0**.

---

## [v0.2.0] - 2025-06-12
### Added
- Implement **music** and **SFX**.
### Changed
- Update **IntroScene** and **TitleScene**.

---

## [v0.1.1] - 2025-06-10
### Changed
- Update **IntroScene** visuals/logic.

---

## [v0.0.0] - 2025-06-04
### Added
- Initial commit: **Pong powered by PolarisKit**.
