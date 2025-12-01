```bash
# Symbolic link to the nix store `ping` bin of the current system.
/run/current-system/sw/bin/ping
```

```bash
# Executable (NixOS wrapper) running the nix store `ping` bin of the current
# system applying special rules (capabilities, setuid…).
/run/wrappers/bin/ping
```

#### NixOS

##### Global
Hiérarchique:
- `/run`
    - `/run/current-system` -> `/nix/store/…nixos-system…`
    - `/run/booted-system` -> `/nix/store/…nixos-system…`
    - `/run/wrappers`
    - `/run/user/<UID>`
    - `/run/systemd`
    - `/run/opengl-driver`
    - `/run/credentials`
    - `/run/tmpfiles.d`
    - `/run/log`
    - `/run/dbus`
    - `/run/keys`
- `/nix`
    - `/nix/path`
        - `/nix/var`
            - `/nix/var/nix`
                - `/nix/var/nix/profiles`
                    - `/nix/var/nix/profiles/default`
                    - `/nix/var/nix/profiles/per-user/<USER>`
                    - `/nix/var/nix/profiles/system`
                    - `/nix/var/nix/profiles/system-<NB>-link`
                - `/nix/var/nix/gcroots/`
                - `/nix/var/nix/db/`
                - `/nix/var/nix/daemon-socket/`
- `/etc`
    - `/etc/nixos`
        - `/etc/nixos/configuration.nix`

Thématique:
- Profils :
    - `~/.nix-profile`
    - `/nix/var/nix/profiles/default`
    - `/nix/var/nix/profiles/per-user/<USER>`
    - `/nix/profile` (not on mine)
    - `/etc/profiles/per-user` (not on mine)

##### System profile
- `./sw`
    - `./sw/bin`
- `./etc`
- `./kernel`
- `./systemd`
- `./bin`
- `./sbin`
- `./lib`
- `./include`
