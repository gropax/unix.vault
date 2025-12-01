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
- [ ] `/`
- [x] `/bin`
- [x] `/boot`
- [x] `/dev`
- [x] `/home`
- [x] `/lib64`
- [x] `/lost+found`
- [x] `/proc`
- [x] `/root`
- [x] `/srv`
- [x] `/sys`
- [x] `/tmp`
- [x] `/usr`
- [x] `/var`
- [ ] `/run`
    - [x] `/run/current-system` -> `/nix/store/…nixos-system…`
    - [x] `/run/booted-system` -> `/nix/store/…nixos-system…`
    - [x] `/run/wrappers`
    - [ ] `/run/user/<UID>`
    - [x] `/run/systemd`
    - [ ] `/run/opengl-driver`
    - [ ] `/run/credentials`
    - [ ] `/run/tmpfiles.d`
    - [ ] `/run/log`
    - [ ] `/run/dbus`
    - [ ] `/run/keys`
- [x] `/nix`
    - [x] `/nix/store`
    - [x] `/nix/var`
        - [x] `/nix/var/nix`
            - [x] `/nix/var/nix/profiles`
                - [x] `/nix/var/nix/profiles/default`
                - [x] `/nix/var/nix/profiles/per-user/<USER>`
                    - [ ] `/nix/var/nix/profiles/per-user/root/channels`
                    - [ ] `/nix/var/nix/profiles/per-user/root/channels-<genid>-link`
                - [x] `/nix/var/nix/profiles/system`
                - [x] `/nix/var/nix/profiles/system-<NB>-link`
            - [x] `/nix/var/nix/gcroots/`
            - [x] `/nix/var/nix/db/`
            - [x] `/nix/var/nix/daemon-socket/`
            - [ ] `/nix/var/nix/temproots`
            - [ ] `/nix/var/nix/userpool`
        - [ ] `/nix/var/log/nix/drvs`
- [x] `/etc`
    - [x] `/etc/nixos`
        - [x] `/etc/nixos/configuration.nix`

Thématique:
- [ ] Profils :
    - [ ] `~/.nix-profile`
    - [x] `/nix/var/nix/profiles/default`
    - [x] `/nix/var/nix/profiles/per-user/<USER>`
    - [ ] `/nix/profile` (not on mine)
    - [ ] `/etc/profiles/per-user` (not on mine)

##### System profile
- [ ] `./sw`
    - [x] `./sw/bin`
- [ ] `./etc`
- [ ] `./kernel`
- [ ] `./systemd`
- [ ] `./bin`
- [ ] `./sbin`
- [ ] `./lib`
- [ ] `./include`
