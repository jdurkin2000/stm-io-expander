\# STM32CubeIDE Project: STM_IO_Expander

AI Slop Readme

This repository contains the \*\*STM32CubeIDE project\*\* for the STM_IO_Expander board.

\## 📂 Project Structure

\- `Core/` → Application code (`main.c`, user code sections, startup files)

\- `Drivers/` → HAL, CMSIS, BSP drivers

\- `Middlewares/` → Optional (FreeRTOS, FatFS, USB, etc.)

\- `.ioc` → STM32CubeMX configuration file (critical for regenerating code)

\- `.project` + `.cproject` → Eclipse project files (needed for CubeIDE import)

## 🚀 Getting Started

1. Open STM32CubeIDE → _File → Import → Existing Projects into Workspace_
2. Select the cloned folder.
3. Ensure **Copy projects into workspace** is unchecked if you want to work directly in the repo folder.

### Build the project

- Select your build configuration (**Debug** or **Release**).
- Click **Project → Build Project**.

### Flash to your STM32 board

- Connect the board via **ST-LINK**.
- Click **Run → Debug** or **Run → Run**.

---

## ✅ Notes

- **Ignored files**: All build artifacts (`Debug/`, `Release/`), `.settings/`, temporary files, and binaries are excluded via `.gitignore`.
- **CubeMX `.ioc` file**: Keep this file tracked; it allows anyone to regenerate HAL code and peripheral configurations.
- **Collaborators**: Anyone cloning this repo can open the project in CubeIDE and build immediately.

---

## ⚡ Optional: Regenerate CubeMX Code

If you modify the `.ioc` file:

1. Open the `.ioc` file in CubeMX (via CubeIDE).
2. Make peripheral or pin changes.
3. Click **Project → Generate Code**.
4. Rebuild the project to apply changes.

---

## 📌 Recommended Git Workflow

- Always commit your **source code and `.ioc` file**.
- Keep `.gitignore` up-to-date to avoid pushing build artifacts.
- Pull remote changes before pushing to avoid non-fast-forward errors:

```bash
git pull origin main --rebase
git push origin main

```
