# roblox-games

Roblox game code, synced into Roblox Studio with [Rojo](https://rojo.space).

## Layout

| Folder        | Shows up in Studio as                                   |
| ------------- | ------------------------------------------------------- |
| `src/shared`  | `ReplicatedStorage.Shared` (ModuleScripts for both sides) |
| `src/server`  | `ServerScriptService.Server` (server Script)            |
| `src/client`  | `StarterPlayer.StarterPlayerScripts.Client` (LocalScript) |

File naming: `*.server.luau` → Script, `*.client.luau` → LocalScript, other `*.luau` → ModuleScript.
An `init.*.luau` file makes its folder become that script.

## Setup (one time)

1. Install [Rokit](https://github.com/rojo-rbx/rokit) (toolchain manager), then in this folder run:
   ```sh
   rokit install
   ```
   This installs the Rojo version pinned in `rokit.toml`.
2. Install the Rojo plugin in Studio:
   ```sh
   rojo plugin install
   ```
   (Or get "Rojo" from the Creator Store.) Restart Studio after installing.

## Syncing into Studio

1. In this folder, run:
   ```sh
   rojo serve
   ```
2. Open your place in Roblox Studio → **Plugins** tab → **Rojo** → **Connect**.
3. Edits to files in `src/` now sync into Studio live. Pull new commits with `git pull` and they sync too.

## Building a place file (optional)

```sh
rojo build -o game.rbxlx
```
