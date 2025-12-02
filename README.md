# Godot Setup Action

A reusable GitHub Action that installs **Godot Engine** and its **export templates**, making your environment fully ready to **build and export games** in CI pipelines.

---

## Features

- 📦 Automatically downloads the specified Godot version
- 🧰 Installs matching export templates
- ⚡ Uses caching to avoid repeated downloads of templates
- 🔧 Adds `godot` command to `$PATH` so you can run it directly
- 🏗️ Ready to use for building and exporting Godot projects
- 🧩 Works in any repository and workflow

---

## Inputs

| Name            | Required | Description                             |
| --------------- | -------- | --------------------------------------- |
| `godot-version` | ✔        | Godot version to install (e.g. `4.2.2`) |

---

## Example Usage

Add this step to your workflow:

```yaml
- name: Setup Godot
  uses: yourname/godot-setup-action@v1
  with:
    godot-version: "4.2.2"
```

After this action runs, Godot and its export templates are installed and ready for use.
You can immediately call Godot commands anywhere in the workflow:

```yaml
- name: Export Game
  run: godot --headless --export-release "Linux/X11" build/game.x86_64
```
